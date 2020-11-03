# Python API

Everything Ragdoll can do you can do, via `ragdoll.api`.

```py
from maya import cmds
from ragdoll import api as rd
from ragdoll.vendor import cmdx

cube, _ = cmds.polyCube()
cube = cmdx.encode(cube) # Convert to cmdx
cube["translateY"] = 10
cube["rotate", cmdx.Degrees] = (35, 50, 30)

scene = rd.createScene()
rigid = rd.createRigid(cube, scene)

cmds.evalDeferred(cmds.play)
```

![ragdollapi1](https://user-images.githubusercontent.com/2152766/95583484-1a415b00-0a34-11eb-8f24-5a83b4ae2629.gif)

- See `ragdoll/interactive.py` for more examples
- See `ragdoll/tools.py` for more examples

<br>

# Types

All functions take and return instances of [`cmdx`](https://github.com/mottosso/cmdx).

```py
from maya import cmds
from ragdoll import api as rd
from ragdoll.vendor import cmdx

cmds.file(new=True, force=True)

cube, _ = map(cmdx.encode, cmds.polyCube())
cube["translateY"] = 10
cube["rotate", cmdx.Degrees] = (35, 50, 30)

# Every simulation needs a scene
scene = rd.createScene()
assert isinstance(scene, cmdx.DagNode)
assert scene.type() == "rdScene"

# Every scene needs one or more rigid bodies
rigid = rd.createRigid(cube, scene)
assert isinstance(rigid, cmdx.DagNode)
assert rigid.type() == "rdRigid"

# Allow start frame to evaluate before progressing
cmds.evalDeferred(cmds.play)
```

- See [mottosso/cmdx](https://github.com/mottosso/cmdx) for details about types

<br>

# Members

Currently available members of `ragdoll.api`.

- Call `help()` for usage instructions

```py
# Fundamentals
api.createRigid(node, scene, compute_mass=True)
api.createCollider(node, scene, compute_mass=True)

# Constraints
api.pointConstraint(parent, child, scene)
api.orientConstraint(parent, child, scene)
api.hingeConstraint(parent, child, scene)
api.socketConstraint(parent, child, scene)
api.parentConstraint(parent, child, scene)

api.convertToPoint(con)
api.convertToOrient(con)
api.convertToHinge(con, secondary_axis="y")
api.convertToSocket(con)
api.convertToParent(con)

# Controls
api.createAbsoluteControl(rigid)
api.createRelativeControl(rigid)
api.createActiveControl(reference, rigid)
api.createKinematicControl(rigid)

# Forces
api.createForce(type, rigid, scene)
api.createSlice(scene)
api.assignForce(rigid, force)

# Utilities
api.transferAttributes(a, b, mirror=True)
api.transferRigid(ra, rb)
api.transferConstraint(ca, cb, mirror=True)
api.editConstraintFrames(con)
api.duplicate(rigid)
```

> Each member is also available in optional `snake_case`

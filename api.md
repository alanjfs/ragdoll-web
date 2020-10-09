# Python API

Everything Ragdoll can do you can do, via `ragdoll.api`.

```py
from maya import cmds
from ragdoll import api
from ragdoll.vendor import cmdx

cube, _ = cmds.polyCube()
cube = cmdx.encode(cube) # Convert to cmdx
cube["translateY"] = 10
cube["rotate", cmdx.Degrees] = (35, 50, 30)

scene = api.create_scene()
rigid = api.create_rigid(cube, scene)

cmds.play()
```

![ragdollapi1](https://user-images.githubusercontent.com/2152766/95583484-1a415b00-0a34-11eb-8f24-5a83b4ae2629.gif)

**More**

- The menu is built with these commands, see `ragdoll/interactive.py` for more examples
- See [mottosso/cmdx](https://github.com/mottosso/cmdx) for details about return values

<br>

# Types

All functions take and return instances of [`cmdx`](https://github.com/mottosso/cmdx).

```py
from maya import cmds
from ragdoll import api
from ragdoll.vendor import cmdx

cube, _ = map(cmdx.encode, cmds.polyCube())
cube["translateY"] = 10
cube["rotate", cmdx.Degrees] = (35, 50, 30)

# Every simulation needs a scene
scene = api.create_scene()
assert isinstance(scene, cmdx.DagNode)
assert scene.type() == "rdScene"

# Every scene needs one or more rigid bodies
rigid = api.create_rigid(cube, scene)
assert isinstance(rigid, cmdx.DagNode)
assert rigid.type() == "rdRigid"

cmds.play()
```

<br>

# Members

Currently available members of `ragdoll.api`.

- Call `help()` for usage instructions

```py
# Fundamentals
api.create_rigid(node, scene, compute_mass=True)
api.create_collider(node, scene, compute_mass=True)

api.# Constraints
api.point_constraint(parent, child, scene)
api.orient_constraint(parent, child, scene)
api.hinge_constraint(parent, child, scene)
api.socket_constraint(parent, child, scene)
api.parent_constraint(parent, child, scene)

api.convert_to_point(con)
api.convert_to_orient(con)
api.convert_to_hinge(con, secondary_axis="y")
api.convert_to_socket(con)
api.convert_to_parent(con)

api.# Controls
api.create_absolute_control(rigid, scene)
api.create_relative_control(rigid, scene)
api.create_active_control(reference, rigid, scene)
api.create_kinematic_control(rigid, scene)

api.# Forces
api.create_force(type, rigid, scene)
api.create_slice(scene)
api.assign_force(rigid, force)

api.# Utilities
api.transfer_attributes(a, b, mirror=True)
api.transfer_rigid(ra, rb)
api.transfer_constraint(ca, cb, mirror=True)
api.edit_constraint_frames(con)
api.duplicate(rigid)
```

> Each member is also available in optional `camelCase`

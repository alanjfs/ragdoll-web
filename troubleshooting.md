# Troubleshooting

This is an advanced page for when you are having issues.

<br>

### Advanced Install

If you are on Linux, or would prefer not to run any executable, try this.

1. Download the `.zip` archive
1. Unzip it anywhere on your `MAYA_MODULES_PATH`
1. Or your `~/maya` directory, e.g. `C:\Users\marcus\Documents\maya`
1. Restart Maya

Or run this from your Script Editor.

```py
cmds.loadModule(scan=True)
cmds.loadModule(load="Ragdoll")
```

<br>

### Manual Install

If the Maya Module isn't working, or you would prefer not to use it, here is a manual installation method.

```py
from maya import cmds
import os

# Update me
ragdoll_version = "2020_10_12"

maya_version = cmds.about(version=True)[:4]
module_path = "~/maya/modules/Ragdoll-Maya-%s" % ragdoll_version
module = os.path.expanduser(module_path)
scripts = os.path.join(module, "scripts")
plugin = os.path.join(module, "plug-ins", "windows", maya_version)
os.environ["MAYA_PLUG_IN_PATH"] += ";" + plugin
sys.path.insert(0, scripts)

import ragdoll.interactive
ragdoll.interactive.install()

# Unload plug-in and remove menu with this
# ragdoll.interactive.uninstall()
```

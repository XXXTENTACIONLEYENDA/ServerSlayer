---
description: Aggressively clear ports (Force Kill).
---
# Nuke Ports ☢️

**WARNING**: This will force-kill development servers in the current project scope.

1.  **Safety Check & List**
    We'll show what's about to be destroyed first.
    ```bash
    python .agent/tools/server_slayer_tools.py list
    ```

2.  **Execute Force Kill**
    ```bash
    python .agent/tools/server_slayer_tools.py kill --force --scope=project
    ```

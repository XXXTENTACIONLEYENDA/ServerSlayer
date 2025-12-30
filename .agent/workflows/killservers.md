---
description: Kill development servers based on scope and options.
---
# Kill Servers

This workflow uses the ServerSlayer toolkit to detect and stop development servers.

1.  **Analyze Running Servers**
    First, we list the running servers to understand the context.
    ```bash
    python .agent/tools/server_slayer_tools.py list
    ```

2.  **Execute Kill Command (Interactive)**
    The user can optionally pass flags like `--force` or `--idle-only` in the chat.
    By default, we will run the kill command in `project` scope.
    
    ```bash
    python .agent/tools/server_slayer_tools.py kill --scope=project
    ```

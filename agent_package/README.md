# ServerSlayer Agent ⚔️

**The Ultimate Development Server Killer**

ServerSlayer is an autonomous AI agent for Antigravity IDE designed to instantly and safely clean up stray, idle, or unresponsive local development servers that cause "port already in use" errors.

## Features
- **Project Aware**: Automatically detects the project type (Node, Python, Java, etc.) and its default ports.
- **Safety First**: Never kills databases, IDE processes, or system services without confirmation.
- **Intelligent Scoping**: Kill servers only in the current project, chat context, or globally.
- **Portable**: Easy to install in any project with a single command.

---

## Installation

### For Your First Project (ServerSlayer Source)
The `.agent` folder is already set up. Just use the slash commands directly!

### For Other Projects
Copy the **entire `.agent` folder** to your other project:

```powershell
# Run from the ROOT of your target project
Copy-Item -Path "c:\Projects\ServerSlayer\.agent" -Destination ".\" -Recurse -Force
```

That's it! The slash commands will now work in that project.

---

## Usage

### Slash Commands

| Command | Description |
| :--- | :--- |
| `/listports` | Show a table of all running dev servers and their safety status. |
| `/killservers` | Kill stray servers for the current project (graceful). |
| `/nukeports` | Aggressively force-kill all relevant dev ports. |
| `/killport <port>` | Kill the process on a specific port (e.g., `/killport 3000`). |

### Options (for `/killservers`)
- `--scope=project` (Default): Only processes in the current workspace.
- `--scope=system`: Scan the whole machine.
- `--idle-only`: Only kill truly idle servers.
- `--force`: Don't ask, just kill (unless it's a protected service).

---

## Safety Rules 🛡️
ServerSlayer **PROTECTS** the following by default:
- **Databases**: MySQL (3306), Postgres (5432), Mongo (27017), Redis (6379).
- **SSH & VPN tunnels**.
- **IDE Processes**: Antigravity, VSCode, JetBrains, Cursor.
- **Docker Containers**.

If you try to kill these, ServerSlayer will **WARN** you and ask for explicit confirmation.

---

## Project Structure

```
.agent/
├── tools/
│   └── server_slayer_tools.py   # Core logic (cross-platform)
└── workflows/
    ├── killport.md
    ├── killservers.md
    ├── listports.md
    └── nukeports.md
```

The `agent_package/` folder contains additional reference files (knowledge base, system prompt) for advanced customization.

---

## License
MIT - Use freely, contribute back!

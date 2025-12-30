<p align="center">
  <h1 align="center">⚔️ ServerSlayer</h1>
  <p align="center">
    <strong>The Ultimate Development Server Killer for Antigravity IDE</strong>
  </p>
  <p align="center">
    Instantly and safely clean up stray local dev servers causing "port already in use" errors.
  </p>
</p>

<p align="center">
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#safety">Safety</a> •
  <a href="#contributing">Contributing</a>
</p>

---

## ✨ Features

- **🔍 Smart Detection**: Automatically identifies Node.js, Python, Java, Go, Ruby, PHP, and more.
- **🛡️ Safety First**: Never kills databases, IDE processes, or system services without explicit confirmation.
- **⚡ Instant Slash Commands**: `/listports`, `/killservers`, `/nukeports` — right in your chat.
- **📦 Portable**: Copy one folder to enable in any project.
- **🖥️ Cross-Platform**: Works on Windows, macOS, and Linux.

---

## 🚀 Installation

### Step 1: Clone this repository

```bash
git clone https://github.com/YOUR_USERNAME/ServerSlayer.git
```

### Step 2: Copy to your project

From the **root of your target project**, run:

```powershell
# Windows (PowerShell)
Copy-Item -Path "path\to\ServerSlayer\.agent" -Destination ".\" -Recurse -Force
```

```bash
# macOS / Linux
cp -r path/to/ServerSlayer/.agent ./
```

### Step 3: Use it!

Open Antigravity IDE in your project and type `/listports` in the chat.

---

## 📖 Usage

### Slash Commands

| Command | Description |
| :--- | :--- |
| `/listports` | 📋 List all running dev servers with port, PID, type, and safety status. |
| `/killservers` | 🔪 Kill stray servers for the current project (graceful). |
| `/nukeports` | ☢️ Force-kill all relevant dev ports. |
| `/killport <port>` | 🎯 Kill a specific port (e.g., `/killport 3000`). |

### Options (for `/killservers`)

| Option | Description |
| :--- | :--- |
| `--scope=project` | (Default) Only kill servers in the current workspace. |
| `--scope=system` | Kill matching servers across the entire machine. |
| `--idle-only` | Only kill servers with no active connections. |
| `--force` | Skip graceful termination, force kill immediately. |

### Example

```
User: /killport 3000 --force

ServerSlayer:
🎯 Scanning Port 3000...
Found: node (PID 12450) - Next.js dev server
Status: SAFE TO KILL

💥 KILLED Port 3000 (PID 12450)
Port is now free!
```

---

## 🛡️ Safety

ServerSlayer **automatically protects** critical services:

| Category | Protected |
| :--- | :--- |
| **Databases** | MySQL (3306), PostgreSQL (5432), MongoDB (27017), Redis (6379), MSSQL (1433) |
| **IDE Processes** | Antigravity, VSCode, JetBrains, Cursor |
| **Tunnels** | ngrok, SSH (22) |
| **Containers** | Docker daemon |

If you try to kill a protected service, ServerSlayer will **warn you** and ask for confirmation.

---

## 📁 Project Structure

```
ServerSlayer/
├── .agent/                      # 👈 Copy this folder to other projects
│   ├── tools/
│   │   └── server_slayer_tools.py   # Core detection & kill logic
│   └── workflows/
│       ├── listports.md
│       ├── killservers.md
│       ├── killport.md
│       └── nukeports.md
├── agent_package/               # Reference files for customization
│   ├── knowledge_base.json      # Framework/port mappings
│   ├── system_instructions.md   # Agent behavior prompt
│   └── README.md                # Detailed docs
├── LICENSE                      # MIT License
├── CONTRIBUTING.md
└── README.md                    # This file
```

---

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Areas to help:**
- 🍎 macOS/Linux testing
- 🧩 Add more framework detection
- 📊 Improve idle detection logic
- 📝 Documentation & tutorials

---

## 📄 License

[MIT](LICENSE) — Use freely, contribute back!

---

<p align="center">
  Made with ⚔️ by <a href="https://github.com/YOUR_USERNAME">Supratik</a>
</p>

# Mobile Coder

_China Mobile Enterprise AI Coding Tool — Secure, Controllable, Knowledge-Driven_

**Current Version: v1.1.1**

[English](README.md) | [简体中文](README.zh.md)

---

### About

**Mobile Coder** is an enterprise-grade AI Coding CLI tool developed by China Mobile through in-depth customization on top of [opencode](https://github.com/sst/opencode). It also supports ACP, HTTP API, SDK and other access methods, seamlessly integrating with various general/specialized agents, IDEs, and business systems that require AI-powered coding.

Unlike general-purpose AI coding assistants, Mobile Coder deeply integrates an enterprise knowledge base and code sandbox. AI generates code that conforms to China Mobile's development standards, validated in an isolated sandbox with multi-layer security controls — ensuring every output is trustworthy, usable, and traceable.

### Features

**Multi-Protocol Access**

| Capability                           | Description                                                            |
| ------------------------------------ | ---------------------------------------------------------------------- |
| 🔌 **CLI**                           | Direct terminal usage, preferred for general-purpose agents            |
| 🔗 **ACP Protocol**                  | Preferred for IDEs, seamless integration with development environments |
| 🌐 **HTTP API**                      | Preferred for enterprise systems, easy business integration            |
| 📦 **SDK**                           | Preferred for platform embedding, supports deep customization          |
| 🤝 **A2A Protocol** (In Development) | Inter-agent communication, supports multi-agent collaboration          |
| ⚙️ **GitHub Action**                 | Seamless CI/CD integration for automated coding workflows              |

**Agent Engine**

| Capability                       | Description                                                                                                                                          |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🤖 **Coding Agent Team**         | Multi-agent collaborative architecture — build / plan / debug / explore / compaction agents work together, reducing LLM context pressure             |
| 🧠 **Enterprise Knowledge Base** | Skills-based dynamic knowledge base with multi-source ingestion and progressive disclosure, auto-linking dev standards and best practices            |
| 🧩 **Tool Ecosystem**            | 20+ built-in tools (file I/O, terminal, code search, LSP diagnostics, etc.), extensible via MCP and A2A                                              |
| 💾 **Memory System**             | Short-term context + long-term persistent storage + Git snapshots + multi-center cloud-synced memory, enabling cross-session and cross-device recall |
| 🤖 **Multi-Model**               | 20+ model providers supported, with dedicated optimization for Jiutian models, streaming output and reasoning mode                                   |

**Supported China Mobile Internal Model Providers**

| Provider              | Status         |
| --------------------- | -------------- |
| Juzhi Unified         | Officially supported |
| Jiutian MOMA          | Officially supported |
| Zhanlu                | Testing…       |
| Panzhi MaaS           | Testing…       |

**Code Security** (In Development)

| Capability                    | Description                                                                                               |
| ----------------------------- | --------------------------------------------------------------------------------------------------------- |
| 📦 **Code Sandbox**           | AI-generated code is validated in an isolated environment, preventing risky code from reaching production |
| 🛡️ **LLM Guard**              | Input/output security filtering for LLMs, preventing prompt injection and sensitive data leakage          |
| 🔐 **Access Control**         | Role-based permission management with clear operational boundaries                                        |
| 🔍 **Vulnerability Scanning** | Auto-detects security vulnerabilities in generated code, reducing risk at the source                      |

**Deployment & Operations**

| Capability                 | Description                                                                                              |
| -------------------------- | -------------------------------------------------------------------------------------------------------- |
| 🏢 **Intranet Deployment** | Supports offline deployment with Lingji platform model access, keeping data within enterprise boundaries |
| 📡 **Event Bus**           | Unified event broadcasting across the system, enabling loosely-coupled module communication              |
| 🔧 **Hook Mechanism**      | Insert custom security policies (audit, interception, approval) without modifying engine code            |
| ⚙️ **Configuration**       | Multi-layer priority-based config system, adaptable to various deployment environments                   |
| 🖥️ **OS Compatibility**    | Supports macOS, Linux, Windows, and domestic OS (UnionTech, Kylin)                                       |

### Comparison with opencode

| Dimension       | opencode                                               | Mobile Coder                                                                                                   |
| --------------- | ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| Access          | CLI / ACP / HTTP API / SDK / GitHub Action             | All of the above + A2A protocol                                                                               |
| Knowledge Base  | None                                                   | Skills-based enterprise dynamic knowledge base with multi-source ingestion                                    |
| Code Security   | None                                                   | Code sandbox + LLM guard + access control + vulnerability scanning                                            |
| Agent Framework | Single-agent + basic multi-agent architecture          | Coding Agent Team — multi-agent collaborative architecture                                                    |
| Tool Ecosystem  | Built-in tools + user-configured MCP tools and Skills  | Built-in tools + China Mobile full-domain MCP tools and Skills                                                |
| Memory System   | Short-term context + long-term storage + Git snapshots | All of the above + multi-center cloud-synced memory                                                           |
| Model Access    | Generic providers (OpenAI, Claude, etc.)               | China Mobile unified model platform, data stays within enterprise, plus generic providers                     |
| Deployment      | Public network online install only                     | Lingji platform online install + intranet offline deployment, for China Mobile office and production networks |
| OS Support      | macOS, Linux, Windows                                  | macOS, Linux, Windows + domestic OS                                                                           |

### Quick Start

After installation, run in your project directory:

```bash
mobile          # Launch TUI terminal interface
```

### Installation

#### Online Install (Coming Soon)

Online installation is under development. Stay tuned.

#### Offline Install (Recommended)

For intranet environments, download the folder matching your OS and architecture, then double-click the install script.

| Platform                       | Folder         | Install                        |
| ------------------------------ | -------------- | ------------------------------ |
| Windows x64                    | `win/`         | Double-click `install.bat`     |
| macOS ARM64 (M1/M2/M3/M4)     | `mac/arm64/`   | Double-click `install.command` |
| macOS x64 (Intel)              | `mac/x64/`     | Double-click `install.command` |
| Linux ARM64 (UnionTech, Kylin) | `linux/arm64/` | Double-click `install.sh`      |
| Linux x64                      | `linux/x64/`   | Double-click `install.sh`      |

> Each folder contains a `.tgz` package and install/uninstall scripts. The script automatically finds the `.tgz` in the same directory and completes the installation.
>
> If a previous version is detected, the script will automatically uninstall it before installing the new version for seamless upgrades.

**Installation Steps**

1. Download the folder for your OS and architecture
2. Double-click the install script
3. After installation, **reopen your terminal** and run `mobile --help` to verify

> **Linux note**: If double-clicking `.sh` doesn't work, run `bash install.sh` in terminal.

**Verify Installation**

```bash
mobile --help
```

### Uninstall

Each folder includes an uninstall script. Double-click to uninstall.

| Platform    | Uninstall                                   |
| ----------- | ------------------------------------------- |
| Windows     | Double-click `win/uninstall.bat`            |
| macOS ARM64 | Double-click `mac/arm64/uninstall.command`  |
| macOS x64   | Double-click `mac/x64/uninstall.command`    |
| Linux ARM64 | Double-click `linux/arm64/uninstall.sh`     |
| Linux x64   | Double-click `linux/x64/uninstall.sh`       |

> **Linux note**: If double-clicking doesn't work, run `bash uninstall.sh` in terminal.

### Voice Input Setup (Optional)

Mobile Coder supports voice-to-text input in the web UI via in-browser speech recognition (powered by sherpa-onnx WebAssembly). The ASR model is **not bundled** with the installer; you need to download it manually after installation.

**1. Download the model file**

[sherpa-onnx-wasm-main-vad-asr.data](https://huggingface.co/spaces/k2-fsa/web-assembly-vad-asr-sherpa-onnx-zh-en-ja-ko-cantonese-sense-voice/resolve/main/sherpa-onnx-wasm-main-vad-asr.data?download=true)（~240MB）

（或从移动云链接中下载）

**2. Place it into the ASR directory**

| OS | Target Path |
| --------------------- | ------------------------------------------------------------------------ |
| macOS / Linux         | `~/.mobile-coder/asr/sherpa-onnx-wasm-main-vad-asr.data`                      |
| Windows               | `%LOCALAPPDATA%\mobile-coder\asr\sherpa-onnx-wasm-main-vad-asr.data`          |

After placement, refresh the web page (`mobile web`); the microphone button in the input area will be ready to use.

> To switch to a different model, replace this `.data` file (same model architecture, no code change). Switching to a different architecture (e.g. SenseVoice/Zipformer) requires updating the wasm runtime as well.

### Basic Usage

**1. Launch Mobile Coder**

```bash
mobile          # TUI terminal mode (recommended)
```

**2. Configure LLM Service**

- In the TUI terminal, run `/provider` to select model provider and configure API Key, etc.
- After configuration, run `/models` to select the model

**3. Start Conversation**

Describe your needs in natural language, for example:

- `Analyze the directory structure of this project`
- `Add a paginated query method to the UserService class`
- `Find performance bottlenecks in this code and optimize`

**Tips: Switch Agents**

Press `Tab` to switch between Agents and choose the one best suited for your current task.

### Detailed Usage

#### Skills

Skills are reusable knowledge snippets (described via `SKILL.md` files) that give the AI specialized capabilities in specific domains — such as Bun file I/O best practices, React component conventions, or internal API integration guides.

**Browse and Use Skills**

Type `/skills` in the TUI to browse all installed skills and select one to use.

**Install Skills**

Skills can be installed from a GitHub repository or URL, via TUI or CLI.

*Option 1: TUI Install*

1. Type `/skills` to open the skill panel
2. Select "+ Install Skill"
3. Enter the source (`owner/repo` or GitHub URL)
4. Select skills to install, choose install location (current project / global), and confirm

*Option 2: CLI Install*

```bash
# Install from a GitHub repo
mobile skill install owner/repo

# Install a specific skill only
mobile skill install owner/repo --name my-skill

# Install globally
mobile skill install owner/repo --global

# List installable skills from a repo
mobile skill list owner/repo
```

**Skill Storage Locations**

| Scope   | Path                              | Description                                |
| ------- | --------------------------------- | ------------------------------------------ |
| Project | `.mobile-coder/skills/`            | Available in current project only          |
| Global  | `~/.config/mobile-coder/skills/`   | Shared across all projects                 |

Mobile Coder also automatically scans these directories for skills:

- `~/.claude/skills/`, `~/.agents/skills/` (global)
- `.claude/skills/`, `.agents/skills/` in the project directory (project-level)

**Create Custom Skills**

Create a folder with a `SKILL.md` file in any of the directories above. Example structure:

```
.mobile-coder/skills/my-skill/
└── SKILL.md
```

`SKILL.md` uses YAML frontmatter for metadata:

```markdown
---
name: my-skill
description: Brief description of what this skill does
---

The body content here will be used as context when the AI activates this skill…
```

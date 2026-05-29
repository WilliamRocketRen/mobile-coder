# Mobile Coder

*中国移动企业级 AI 智能编程工具 — 安全可控，知识驱动*

**当前版本: v1.1.1**

[English](README.md) | [简体中文](README.zh.md)

---

### 项目简介

**Mobile Coder** 是中国移动基于 [opencode](https://github.com/sst/opencode) 项目进行企业级深度定制开发的AI Coding命令行工具。在此基础上，还支持ACP、HTTP API、SDK等能力接入方式，可无缝对接各类通专智能体、IDE和需要AI编程的业务系统。

不同于通用 AI 编程助手，Mobile Coder 深度融合企业知识库与代码沙箱，让 AI 在理解中国移动开发规范的基础上生成代码，并通过隔离沙箱验证与多层安全防护，确保产出的代码可信、可用、可追溯。

### 特性一览

**多协议接入**


| 能力                   | 说明                    |
| -------------------- | --------------------- |
| 🔌 **CLI 调用**        | 终端直接使用，通用智能体首选接入方式    |
| 🔗 **ACP 协议**        | IDE 首选接入方式，无缝对接各类开发环境 |
| 🌐 **HTTP API**      | 企业系统首选，便于业务系统集成       |
| 📦 **SDK**           | 开发平台嵌入首选，支持深度定制       |
| 🤝 **A2A 协议**（开发中）   | 智能体间协作通信，支持多智能体联动     |
| ⚙️ **GitHub Action** | 无缝嵌入 CI/CD 流程，实现自动化编程 |


**智能体引擎**


| 能力                       | 说明                                                                          |
| ------------------------ | --------------------------------------------------------------------------- |
| 🤖 **Coding Agent Team** | 多智能体协作架构，build / plan / debug / explore / compaction 等多 Agent 协同，降低大模型上下文压力 |
| 🧠 **企业知识库**             | 以 Skills 为核心构建动态知识库，支持多来源接入与渐进式披露，自动关联开发规范与最佳实践                             |
| 🧩 **工具生态**              | 20+ 内置工具（文件读写、终端执行、代码搜索、LSP 诊断等），支持 MCP 与 A2A 工具扩展                          |
| 💾 **记忆系统**              | 短期上下文 + 长期持久存储 + Git 快照 + 多中心云端互联记忆体系，具备跨会话、跨终端记忆能力                         |
| 🤖 **多模型支持**             | 支持 20+ 大模型提供商，针对九天大模型专项适配，支持流式输出与推理模式                                       |


**已支持的中国移动内部大模型提供商**


| 大模型提供商    | 说明    |
| ---------- | ----- |
| 聚智统一供模     | 正式支持  |
| 九天 MOMA 供模 | 正式支持  |
| 湛卢供模       | 测试中…… |
| 磐智 MaaS 供模 | 测试中…… |


**代码安全**(开发中)


| 能力             | 说明                              |
| -------------- | ------------------------------- |
| 📦 **代码沙箱**    | AI 生成的代码在隔离环境中运行验证，杜绝风险代码进入生产环境 |
| 🛡️ **LLM 防护** | 大模型输入输出安全过滤，防止提示注入与敏感信息泄露       |
| 🔐 **身份访问控制**  | 权限分级管理，确保不同角色的操作边界清晰可控          |
| 🔍 **代码漏洞扫描**  | 自动检测生成代码中的安全漏洞，从源头降低安全风险        |


**部署与运维**


| 能力             | 说明                                     |
| -------------- | -------------------------------------- |
| 🏢 **内网部署**    | 支持离线部署，灵畿科研平台大模型接入，数据不出企业边界              |
| 📡 **事件总线**    | 系统内所有事件统一广播，模块间松耦合通信                   |
| 🔧 **Hook 机制** | 无需改动引擎代码即可插入审计、拦截、审批等自定义安全策略           |
| ⚙️ **配置管理**    | 多层优先级配置体系，灵活适配不同部署环境                   |
| 🖥️ **系统兼容**   | 支持 macOS、Linux、Windows 及国产化操作系统（统信、麒麟） |


### 与 opencode 的比较


| 维度    | opencode                                         | Mobile Coder                           |
| ----- | ------------------------------------------------ | ------------------------------------- |
| 接入方式  | CLI / ACP / HTTP API / SDK / GitHub Action 多协议接入 | 在opencode基础上增加A2A协议接入方式               |
| 知识库   | 无                                                | 以 Skills 为核心的企业级动态知识库，支持多来源接入         |
| 代码安全  | 无                                                | 代码沙箱 + LLM 防护 + 身份访问控制 + 漏洞扫描         |
| 智能体框架 | 单智能体 + 简易多智能体架构                                  | Coding Agent Team 多智能体协作架构            |
| 工具生态  | 内置工具 + 用户自行接入的MCP工具与Skill                        | 内置工具 + 中国移动全域MCP工具与Skill能力            |
| 记忆系统  | 短期上下文 + 长期持久存储 + Git 快照                          | 短期上下文 + 长期持久存储 + Git 快照 + 多中心云端互联记忆体系 |
| 模型接入  | 通用供应商（OpenAI、Claude 等）                           | 支持中国移动统一供模，保证数据不出企业边界，同时兼容通用供应商       |
| 部署方式  | 仅支持公网在线安装                                        | 依托灵畿科研平台在线安装 + 内网离线部署，适配中国移动办公网与生产网     |
| 系统支持  | 支持 macOS、Linux、Windows                           | 支持 macOS、Linux、Windows、国产化操作系统        |


### 快速开始

安装完成后，在项目目录下运行：

```bash
mobile          # 启动 TUI 终端界面
```

### 安装

#### 在线安装（即将支持）

在线安装功能正在开发中，敬请期待。

#### 离线安装（推荐）

适用于内网环境，下载对应系统和架构的安装包文件夹，双击脚本即可完成安装。

| 系统                             | 文件夹         | 安装方式                |
| -------------------------------- | -------------- | ----------------------- |
| Windows x64                      | `win/`         | 双击 `install.bat`      |
| macOS ARM64 (M1/M2/M3/M4)       | `mac/arm64/`   | 双击 `install.command`  |
| macOS x64 (Intel)                | `mac/x64/`     | 双击 `install.command`  |
| Linux ARM64（支持麒麟/统信系统） | `linux/arm64/` | 双击 `install.sh`       |
| Linux x64                        | `linux/x64/`   | 双击 `install.sh`       |

> 每个文件夹内包含 `.tgz` 安装包和安装/卸载脚本，安装脚本会自动查找同目录下的 `.tgz` 包并完成安装。
>
> 如果已安装过旧版本，脚本会自动检测并卸载旧版本后再安装新版本，实现无缝升级。

**安装步骤**

1. 下载对应系统和架构的文件夹
2. 双击运行安装脚本
3. 安装完成后，**重新打开终端**，执行 `mobile --help` 验证

> **Linux 提示**：如果双击无法运行 `.sh` 文件，请在终端中执行 `bash install.sh`。

**验证安装**

```bash
mobile --help
```

### 卸载

每个安装包文件夹内附带卸载脚本，双击即可完成卸载。

| 系统              | 卸载方式                           |
| ----------------- | ---------------------------------- |
| Windows           | 双击 `win/uninstall.bat`           |
| macOS ARM64       | 双击 `mac/arm64/uninstall.command` |
| macOS x64         | 双击 `mac/x64/uninstall.command`   |
| Linux ARM64       | 双击 `linux/arm64/uninstall.sh`    |
| Linux x64         | 双击 `linux/x64/uninstall.sh`      |

> **Linux 提示**：如果双击无法运行，请在终端中执行 `bash uninstall.sh`。

### 语音输入配置（可选）

Mobile Coder 在 web 界面支持语音转文字（基于 sherpa-onnx 浏览器端 WebAssembly 推理）。语音识别模型**未随安装包分发**，需要在安装完成后手动下载到指定目录。

**1. 下载模型文件**

[sherpa-onnx-wasm-main-vad-asr.data](https://huggingface.co/spaces/k2-fsa/web-assembly-vad-asr-sherpa-onnx-zh-en-ja-ko-cantonese-sense-voice/resolve/main/sherpa-onnx-wasm-main-vad-asr.data?download=true)（~240MB）

（或从移动云链接中下载）

**2. 放置到 ASR 模型目录**

| 系统 | 目标路径 |
| ------------- | --------------------------------------------------------------- |
| macOS / Linux | `~/.mobile-coder/asr/sherpa-onnx-wasm-main-vad-asr.data`             |
| Windows       | `%LOCALAPPDATA%\mobile-coder\asr\sherpa-onnx-wasm-main-vad-asr.data` |

放置完成后刷新网页（`mobile web`），输入框中的麦克风按钮即可使用。


### 基本使用方法

**1. 启动 Mobile Coder**

```bash
mobile          # TUI 终端模式（推荐）
```

**2. 配置大模型服务**

- 在 TUI 终端输入 `/provider` 命令选择大模型供应商并配置 API Key等信息
- 配置完成后，可通过 `/models` 命令选择大模型

**3. 开始对话**

直接用自然语言描述你的需求，例如：

- `帮我分析这个项目的目录结构`
- `给 UserService 类添加分页查询方法`
- `找出这段代码的性能瓶颈并优化`

**Tips: 切换智能体**

按 `Tab` 键在不同 Agent 之间切换，选择最适合当前任务的智能体。

### 详细使用方法

#### 技能 (Skills)

技能是可复用的知识片段（以 `SKILL.md` 文件描述），可以让 AI 在特定领域拥有专业能力。例如：Bun 文件操作最佳实践、React 组件规范、内部 API 对接指南等。

**浏览与使用技能**

在 TUI 中输入 `/skills`，即可浏览所有已安装的技能并选择使用。

**安装技能**

技能支持从 GitHub 仓库或 URL 安装，可通过 TUI 或 CLI 两种方式操作。

*方式一：TUI 安装*

1. 输入 `/skills` 打开技能面板
2. 选择「+ 安装技能」
3. 输入来源（`owner/repo` 或 GitHub URL）
4. 选择要安装的技能，选择安装位置（当前项目 / 全局），完成安装

*方式二：CLI 安装*

```bash
# 从 GitHub 仓库安装
mobile skill install owner/repo

# 仅安装指定技能
mobile skill install owner/repo --name my-skill

# 安装到全局目录
mobile skill install owner/repo --global

# 列出仓库中可安装的技能
mobile skill list owner/repo
```

**技能存储位置**

| 范围 | 路径 | 说明 |
| ---- | ---- | ---- |
| 当前项目 | `.mobile-coder/skills/` | 仅当前项目可用，随项目代码分发 |
| 全局 | `~/.config/mobile-coder/skills/` | 所有项目共享 |

此外，Mobile Coder 还会自动扫描以下目录中的技能：

- `~/.claude/skills/`、`~/.agents/skills/`（全局）
- 项目目录中的 `.claude/skills/`、`.agents/skills/`（项目级）

**编写自定义技能**

在上述任一目录中创建文件夹，并添加 `SKILL.md` 文件即可。示例结构：

```
.mobile-coder/skills/my-skill/
└── SKILL.md
```

`SKILL.md` 使用 YAML frontmatter 声明元信息：

```markdown
---
name: my-skill
description: 简要描述这个技能的用途
---

这里是技能的正文内容，AI 会在使用该技能时读取这段文字作为上下文…
```
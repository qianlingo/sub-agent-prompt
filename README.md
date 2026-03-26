# sub-agent-prompt
为 Claude Code、Kimi Code 等 AI CLI 工具提供离线项目记忆库，终结重复解释、告别 Token 浪费。  

![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

&gt; **中文**: 为 Claude Code、Kimi Code 等 AI CLI 工具提供**离线项目记忆库**，终结重复解释、告别 Token 浪费。  
&gt; **EN**: **Offline Project Memory** for AI CLI tools. Stop repeating yourself, save your tokens.

---

## 🤔 为什么要做这个项目 / Why This Project?

在使用 Claude Code、Kimi Code、Cline 等 AI 编程 CLI 工具时，我们频繁遇到这些痛点：

- **🔄 轮询失忆 / Context Amnesia**: 每次新对话都要重新解释项目结构、技术栈、文件关系  
  Every new session requires re-explaining project structure, tech stack, and file relationships.

- **🎯 上下文漂移 / Drifting Focus**: 长对话中 AI 容易"跑偏"，忘记最初的需求目标  
  Long conversations cause AI to "drift" away from original goals and requirements.

- **💸 Token 刺客 / Token Drain**: 重复上传项目说明、目录结构、依赖关系，快速消耗 API 额度  
  Repeatedly uploading project descriptions burns through API credits fast.

- **🗂️ 记忆碎片 / Fragmented Memory**: 重要决策、需求变更散落在多轮对话中，难以追溯  
  Important decisions scatter across multiple threads, hard to trace.

---

## 💡 解决方案 / The Solution

**QianLingo** 在项目本地建立**独立于 CLI 的标准化记忆体**（Standardized Memory Bank），将项目上下文**持久化存储**（Persistent Context），让 AI 助手像读取 `.vscode/settings.json` 一样，瞬间理解你的项目。

- **Local-First / 本地优先**: 所有模板和记忆文件存放在你的硬盘，非云端
- **Token-Efficient / 省 Token**: 预填充变量避免重复传输项目背景
- **Context-Grounded / 锚定上下文**: `Soul.md` 作为项目 Single Source of Truth

---

## ✨ 核心特性 / Key Features

| 特性 Feature | 说明 Description |
|-------------|----------------|
| 🧠 **Project Memory** | 技术栈、目录结构写入 `Soul.md`，随取随用 Tech stack persisted locally |
| 🎯 **Scene Modes** | "初始化(Init)" 和 "新建任务(Task)" 两种模式，保持对话专注 Contextual modes keep focus |
| 💰 **Token Saver** | 本地模板预填充 `{{变量}}`，避免每轮重复说明 Variable injection reduces token waste |
| 🎨 **4 UI Styles** | 专业/极客/友好/极简，适配不同开发者 Professional, Hacker, Friendly, Minimal |
| 🏗️ **Full Stack** | Spring Boot 2.x/3.x, Vue 2/3, Freemarker, MySQL/PostgreSQL 全覆盖 |

---

## 🚀 快速开始 / Quick Start

### 1. 准备全局模板 / Prepare Templates

脚本首次运行会自动在用户目录创建 `.qianlingo` 文件夹并生成默认模板：

```powershell
C:\Users\YourName\.qianlingo\
├── web.md    # 后端模板 / Backend template
└── ui.md     # 前端模板 / Frontend template

你也可以手动替换这些文件为社区规范版本。
```

### 2. 在项目目录运行 / Run in Project
```powershell
cd F:\YourProject
.\generator.ps1
```

### 3. 📂 生成结构 / Generated Structure
``` plain
YourProject/
├── .agent/              # AI 协作目录 / AI workspace
│   ├── ui/
│   │   └── ui.md       # 前端技术规范 (变量已注入 / Variables injected)
│   ├── web/
│   │   └── web.md      # 后端技术规范 (变量已注入 / Variables injected)
│   └── Soul.md         # 项目总览 / Project manifest
└── src/                # 你的业务代码 / Your business logic
```


## 📄 许可证 / License
MIT License - 自由使用、修改和分发。






让 AI 记得住，让 Token 花得值。
Make AI remember, make tokens count.

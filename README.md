# 🚀 Kidou - Advanced AI Code Generation UI with Task Scheduling

<div align="center">
  **The Ultimate AI-Powered Development Environment**
  **Orchestrate multiple AI coding agents in parallel with automated workflows*
</div>

---

## ⚡ What is Kidou?

Kidou is a **next-generation AI code generation platform** that revolutionizes how developers work with AI coding assistants. Unlike simple chat interfaces, Kidou provides a **full orchestration environment** where multiple AI agents can work in parallel on your codebase with sophisticated task scheduling and workflow automation.

### 🎯 Core Philosophy

- **🔄 Parallel AI Sessions**: Run multiple AI coding agents simultaneously, each with isolated environments
- **📋 Task Scheduling**: Automated build pipelines, test execution, and deployment workflows
- **🌳 Git Integration**: Isolated git worktrees prevent conflicts between parallel development efforts
- **🤖 Multi-Provider**: Support for Claude (Sonnet 4, Opus 4, Haiku 3.5), with extensible architecture for other providers
- **⚡ Real-time Orchestration**: Live terminal outputs, status tracking, and intelligent session management

---

## ✨ Key Features

### 🚀 AI Agent Orchestration
- **Multi-Session Management**: Run 5+ parallel Claude Code instances simultaneously
- **Intelligent Session Naming**: AI-powered automatic session naming based on prompts
- **Conversation Continuity**: Resume conversations with full context preservation
- **Model Selection**: Choose optimal AI models per task (Sonnet 4 for complex tasks, Haiku for speed)

### 📋 Advanced Task Scheduling & Automation
- **Build Pipeline Integration**: Automatic build script execution before AI sessions
- **Run Script Orchestration**: Continuous command execution (dev servers, test watchers)
- **Sequential Task Execution**: Smart command chaining with failure handling
- **Background Process Management**: Run multiple services concurrently with process isolation

### 🌳 Sophisticated Git Workflow
- **Git Worktree Isolation**: Each AI session operates in its own git worktree
- **Automatic Branch Management**: Smart branch creation and cleanup
- **Intelligent Rebasing**: One-click squash and rebase operations
- **Live Diff Visualization**: Real-time code change tracking with syntax highlighting
- **Conflict Prevention**: Zero conflicts between parallel development sessions

### 🎨 Professional UI/UX
- **Modern Terminal Interface**: XTerm.js with 50,000-line scrollback buffer
- **Multiple View Modes**: Output view, diff view, terminal view, messages view
- **Real-time Status Indicators**: Live session status with visual feedback
- **Dark/Light Theme**: Adaptive UI with professional terminal styling
- **Notification System**: Desktop alerts with sound notifications

### 🔧 Enterprise-Grade Architecture
- **SQLite Database**: Persistent session storage with migration system
- **Bull Task Queue**: Redis-compatible job queue for reliable task processing
- **IPC Communication**: Secure inter-process communication between frontend/backend
- **Cross-Platform**: Native support for macOS and Linux with optimized performance
- **Configurable Environments**: Per-project settings, custom prompts, and environment variables

---

## 🚀 Quick Start

### Prerequisites

```bash
# Required software
- Node.js ≥ 22.14.0
- pnpm ≥ 8.0.0
- Git
- Claude Code CLI (or other AI provider)
```

### Installation

#### Option 1: Download Pre-built Binaries
- **macOS**: Download `Kidou-{version}.dmg` from [releases](https://github.com/embody-ai/kidou/releases)

### Initial Setup

1. **Configure AI Provider**
   - Ensure Claude Code CLI is installed and authenticated

2. **Create Your First Project**
   - Select existing directory or create new project
   - Configure build scripts (optional) for automatic pre-session setup
   - Configure run scripts (optional) for continuous development workflows

3. **Launch Your First AI Session**
   - Write a descriptive prompt for your coding task
   - Choose AI model based on complexity
   - Watch as Kidou automatically sets up isolated environment and begins coding

---

## 💡 Usage Scenarios

### 🔄 Parallel Feature Development
```bash
# Scenario: Building a web app with multiple features
Session 1: "Add user authentication with JWT"          # → Claude Sonnet 4
Session 2: "Create responsive dashboard layout"        # → Claude Sonnet 4  
Session 3: "Write comprehensive test suite"            # → Claude Opus 4.1
Session 4: "Optimize database queries for performance" # → Claude Opus 4
```
All sessions run in parallel with isolated git worktrees, zero conflicts guaranteed.

### 📋 Automated Development Workflow
```bash
# Project Configuration
Build Script: "pnpm install && pnpm build"
Run Scripts:  "pnpm dev"
              "pnpm test --watch"

# What Happens:
1. Kidou creates isolated git worktree
2. Runs build script to prepare environment  
3. Starts AI coding session
4. Launches dev server + test watcher in background
5. Provides real-time feedback as AI writes code
```

### 🌳 Git Workflow Integration
```bash
# Smart Git Operations
1. AI makes changes in isolated worktree
2. Review changes in integrated diff viewer
3. One-click squash all commits with meaningful message
4. Automated rebase to main branch
5. Clean, linear git history preserved
```

---

## 🏗️ Architecture

Kidou is built on a sophisticated **multi-process architecture** designed for reliability and performance:

```
┌─────────────────────────────────────────────────────────┐
│                    Kidou Desktop App                     │
├─────────────────────────────────────────────────────────┤
│             Frontend (React + TypeScript)                │
│  ┌─────────────────┐ ┌─────────────────┐ ┌────────────┐  │
│  │   Session UI    │ │   Terminal      │ │   Settings │  │
│  │   Management    │ │   (XTerm.js)    │ │   & Config │  │
│  └─────────────────┘ └─────────────────┘ └────────────┘  │
├─────────────────────────────────────────────────────────┤
│                  IPC Bridge Layer                        │
├─────────────────────────────────────────────────────────┤
│              Backend (Node.js + Electron)                │
│ ┌──────────────┐ ┌──────────────┐ ┌───────────────────┐  │
│ │  Task Queue  │ │  Session     │ │   Git Worktree    │  │
│ │   (Bull)     │ │  Manager     │ │   Manager         │  │
│ └──────────────┘ └──────────────┘ └───────────────────┘  │
│ ┌──────────────┐ ┌──────────────┐ ┌───────────────────┐  │
│ │   AI Code    │ │  Build/Run   │ │   Config &        │  │
│ │   Manager    │ │  Scripts     │ │   Database        │  │
│ └──────────────┘ └──────────────┘ └───────────────────┘  │
├─────────────────────────────────────────────────────────┤
│                    Data Layer                            │
│ ┌─────────────┐ ┌─────────────┐ ┌─────────────────────┐  │
│ │   SQLite    │ │   File      │ │   Git Worktrees     │  │
│ │  Database   │ │   System    │ │   & Repositories    │  │
│ └─────────────┘ └─────────────┘ └─────────────────────┘  │
└─────────────────────────────────────────────────────────┘
```

### 🔧 Technology Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS, XTerm.js
- **Backend**: Node.js, Electron, Bull Queue, Better-SQLite3
- **AI Integration**: Anthropic Claude SDK, Claude Code CLI
- **Git Integration**: Native git CLI with worktree management
- **Build System**: Vite, PNPM workspaces, Electron Builder

---

## 🤖 Supported AI Providers

### Anthropic Claude Models
- **Claude Sonnet 4** (`claude-sonnet-4-20250514`) - Best for most coding tasks
- **Claude Opus 4** (`claude-opus-4-20250514`) - Complex architecture, large refactors
- **Claude Opus 4.1** (`claude-opus-4-1-20250514`)
---

## 📊 Performance & Scalability

### Session Concurrency
- **macOS**: Up to 5 parallel AI sessions
- **Linux**: Optimized for 1-2 sessions (PTY limitations)
- **Memory**: ~200MB base + ~50MB per active session
- **Storage**: SQLite database with automatic cleanup

### Build Performance
- **Incremental Builds**: Smart caching for faster rebuilds
- **Parallel Processing**: Concurrent frontend/backend compilation
- **Native Modules**: Automatic rebuild system for cross-platform compatibility

---

## 🛠️ Troubleshooting

### Common Issues

#### Claude Code Not Found
```bash
# Solution 1: Install Claude Code CLI
curl -fsSL https://api.anthropic.com/claude-code/install.sh | bash

# Solution 2: Set custom path in Settings
Settings → Claude Executable Path → /path/to/claude
```

#### Session Creation Fails
```bash
# Check git repository status
git status
git log --oneline -10

# Ensure clean working directory
git add .
git commit -m "WIP: Save current state"
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Anthropic** - For the powerful Claude AI models and Claude Code CLI
- **Electron** - For the robust cross-platform desktop framework  
- **React** - For the excellent UI framework
- **XTerm.js** - For the professional terminal implementation
- **Bull** - For reliable background job processing

---

## 🔗 Links

- **🌐 Website**: [kidou](https://embodyai.co.jp/kidou)
- **📧 Contact**: [support@embodyai.co.jp](mailto:support@embodyai.co.jp)

---

<div align="center">
  <img src="https://embodyai.co.jp/images/logo.svg" alt="Kidou Logo" width="60" height="60">
  <br>
  <strong>Built with ❤️ by the Kidou Team</strong>
  <br>
  <em>Revolutionizing AI-powered development workflows</em>
</div>


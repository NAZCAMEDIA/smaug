# Claude-Cowork

**Repository:** https://github.com/DevAgentForge/Claude-Cowork
**Stars:** 1230
**Language:** TypeScript
**Status:** Active Development

## Overview

Open Claude-Cowork is a desktop AI assistant application that provides a native GUI for Claude Code functionality. It enables programming, file management, and general task execution with real-time streaming output and explicit tool permission controls.

## Key Concept

Claude Code is powerful but runs only in the terminal, creating limitations:
- No visual feedback for complex tasks
- Hard to track multiple sessions
- Tool outputs are inconvenient to inspect

**Claude-Cowork solves these problems** by providing:
- Native desktop application (macOS, Linux, Windows)
- AI collaboration partner for any task
- Full compatibility with existing `~/.claude/settings.json` configuration
- 100% compatible with Claude Code behavior

## Core Capabilities

### AI Collaboration
- Write and edit code in any programming language
- Manage files (create, move, organize)
- Run commands (build, test, deploy)
- Answer questions about your codebase
- Execute any task described in natural language

### Session Management
- Create sessions with custom working directories
- Resume any previous conversation
- Complete local session history (stored in SQLite)
- Safe deletion with automatic persistence

### Real-Time Output
- Token-by-token streaming output
- View Claude's reasoning process
- Markdown rendering with syntax-highlighted code
- Visualized tool calls with status indicators

### Tool Permission Control
- Explicit approval required for sensitive actions
- Allow or deny permissions per tool
- Interactive decision panels
- Full control over what Claude can do

## Compatibility

Claude-Cowork shares configuration with Claude Code through `~/.claude/settings.json`:
- Same API keys
- Same base URL
- Same models
- Same behavior

**Configure Claude Code once, use it everywhere.**

## Architecture

| Layer | Technology |
|-------|-----------|
| Framework | Electron 39 |
| Frontend | React 19, Tailwind CSS 4 |
| State Management | Zustand |
| Database | better-sqlite3 (WAL mode) |
| AI | @anthropic-ai/claude-agent-sdk |
| Build | Vite, electron-builder |

## Getting Started

### Prerequisites
- Bun or Node.js 18+
- Claude Code installed and authenticated

### Installation Options

**Option 1: Download Release**
Visit: https://github.com/DevAgentForge/Claude-Cowork/releases

**Option 2: Build from Source**
```bash
git clone https://github.com/DevAgentForge/Claude-Cowork.git
cd Claude-Cowork
bun install
bun run dev          # Development mode
bun run dist:mac     # macOS build
bun run dist:win     # Windows build
bun run dist:linux   # Linux build
```

## Development Commands

```bash
bun run dev       # Start development server (hot reload)
bun run build     # Type checking and build
```

## Roadmap

Planned features:
- GUI-based configuration for models and API keys
- Additional features coming soon

## Use Cases

- Desktop AI-powered development with persistent context
- Visual monitoring of agent progress and reasoning
- Multi-session task management
- Code generation and refactoring with approval workflows
- Complex file operations and project management
- Learning and debugging AI agent behavior through visualization

## Collaboration

Includes partnership with MiniMax-M2.1, an open-source SOTA model that excels at coding and handling long, multi-step tasks.

## Community

- Contributing: Fork, create feature branch, commit, submit pull request
- Open-source under Apache/MIT license (check repository)
- Active community focused on making AI collaboration accessible

# CodexMonitor

**Repository:** https://github.com/Dimillian/CodexMonitor
**Author:** Thomas Ricouard (@Dimillian)
**Stars:** 515
**Language:** TypeScript
**Topics:** ai, codex, linux, macos, tauri-app
**Status:** Active Development

## Overview

CodexMonitor is a macOS Tauri desktop application for orchestrating multiple Codex agents across local workspaces. It provides a comprehensive interface for managing AI agent-driven development tasks with real-time feedback and git integration.

## Key Features

### Workspace Management
- Add and persist workspaces with home dashboard of recent agent activity
- Spawn one `codex app-server` per workspace
- Stream JSON-RPC events and resume threads on selection
- Worktree agents per workspace (create/delete git worktrees)

### Agent Control
- Start agent threads and send messages
- Render reasoning/tool/diff items
- Handle approvals and interactive responses
- Skills menu with composer autocomplete for tokens

### Git Integration
- Git panel with diff stats, file diffs, and commit log
- GitHub Issues integration (via `gh` CLI)
- Branch list with checkout and create flows
- Open commits on GitHub when remote is detected

### User Interface
- Model picker and reasoning effort selector
- Access mode selection (read-only/current/full-access)
- Context usage ring visualization
- Plan panel for per-turn planning updates
- Debug panel for warning/error events
- Resizable sidebar/right/plan/debug panels
- Responsive layouts for desktop/tablet/phone
- In-app updater with toast-driven download/install
- macOS overlay title bar with vibrancy effects

### Developer Features
- Composer queueing and image attachments (picker, drag/drop, paste)
- Per-thread draft persistence
- Review runs against uncommitted changes, base branch, commits, or custom instructions
- Sidebar usage + credits meter for account rate limits

## Requirements

- Node.js + npm
- Rust toolchain (stable)
- Codex installed and available in `PATH`
- Git CLI (for worktree operations)
- GitHub CLI (`gh`) optional for Issues panel

## Getting Started

```bash
npm install
npm run tauri dev  # Development mode
npm run tauri build  # Production build
npm run typecheck  # TypeScript validation
```

## Project Structure

```
src/
  features/         # Feature-sliced UI + hooks
  services/         # Tauri IPC wrapper
  styles/           # CSS by area
  types.ts          # Shared types

src-tauri/
  src/lib.rs        # Tauri backend + codex app-server client
  tauri.conf.json   # Window configuration
```

## Persistence

- Workspaces persist to `workspaces.json` in app data directory
- Settings persist to `settings.json` (Codex path, access mode, UI scale)
- UI state (panel sizes, transparency, recent activity) in localStorage
- Thread data restored from disk on selection

## Tauri IPC Commands

Core commands include:
- Workspace lifecycle: list, add, remove, connect, update
- Threads: start, list, resume, archive, send messages, interrupt
- Reviews and models: start review, list models, check rate limits
- Git operations: status, diffs, logs, branches, checkout, create

## Use Cases

- Local AI-powered development with persistent workspace context
- Multi-agent coordination for complex projects
- Real-time monitoring of agent progress and reasoning
- Integrated git workflows for agent-generated code
- Review and approval workflows before committing agent changes

## Related Bookmarks

- Batch 4 (Jan 12, 2026): Initial release announcement
- Batch 6 (Jan 13, 2026): Version 0.3.0 release - https://x.com/Dimillian/status/2011062643562537333

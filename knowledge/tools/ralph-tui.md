# ralph-tui

**Source:** https://github.com/subsy/ralph-tui
**Author:** Ben Williams (@theplgeek)
**Status:** Released
**Date:** January 13, 2026

## Overview

ralph-tui is an interactive Terminal User Interface (TUI) that provides an all-in-one ralph engine with comprehensive observability. It wraps the ralph CLI tool with an interactive interface for managing AI-driven development workflows.

## Key Features

- **All-in-One Engine:** Complete ralph workflow in a TUI
- **End-to-End Observability:** Full visibility into the development process
- **Extensible by Design:** Plugin architecture for custom functionality
- **Plugin Agents:** Ships with Claude Code and OpenCode plugins
- **Plugin Trackers:** Ships with JSON, Beads, and Beads-BV trackers
- **Interactive PRD Creator:** Built-in PRD generation leveraging AI skills
- **Auto PRD Conversion:** Automatically converts PRDs to selected tracker formats
- **Customizable Prompts:** Extensible prompt system for different use cases
- **Task Dependencies:** Understands and manages task relationships
- **Dogfooding:** Built using itself in subsequent iterations

## Installation & Usage

```bash
# Install with your preferred package manager
bun install -g ralph-tui
# or npm/yarn equivalent

# First time setup
ralph-tui init

# Create PRD and tasks
ralph-tui prime

# Then drop into interactive TUI to start the ralph loop
```

## Architecture Highlights

- Extensible by design - supports custom agents and trackers
- Interactive workflow with built-in observability
- Supports multiple tracker formats for integration with different project management tools

## Notable

Built using ralph-tui itself - demonstrates full capability of the tool through dogfooding.

## Related

- Bookmark: `batch-4.md` - Jan 13, 2026
- Tweet: https://x.com/theplgeek/status/2010879209204552168
- Parent: `ralph.md`

## Tags

#tui #interactive-tools #workflow-automation #ai-development #plugin-architecture

# AGENTS.md - Open Standard for AI Agent Instructions

**Website:** https://agents.md/
**Author:** Community (60k+ projects using it)
**Type:** Open Standard
**Date:** Referenced January 12, 2026

## Overview

AGENTS.md is a simple, open format specification for guiding coding agents. It serves as a standardized way to provide context and instructions to AI coding agents, similar to how README.md serves as documentation for humans.

## Purpose

Solves the problem of managing instructions across multiple AI coding tools:
- Claude Code
- GitHub Copilot
- Cursor
- Other AI coding agents

Instead of maintaining separate instruction files for each tool, AGENTS.md provides a single, standardized location for agent instructions that tools can reference.

## Key Benefits

- **Single Source of Truth:** One file for all agent configurations
- **Open Standard:** Standardized format adopted by 60,000+ open-source projects
- **Tool-Agnostic:** Works across multiple AI coding platforms
- **Predictable Location:** Tools know exactly where to look for instructions
- **Community-Driven:** Widely adopted and supported by the OSS community

## Current Adoption

Used by over 60,000 open-source projects on GitHub as of January 2026.

## Integration Status

- **Anthropic (Claude Code):** Does not yet officially support AGENTS.md standard
- **Workaround:** Claude Code users can reference the AGENTS.md file in their `.claude/CLAUDE.md` or similar configuration files

## Example Use Case

Development teams can:
1. Create an `AGENTS.md` file at the project root
2. Define instructions for code generation, testing, documentation, etc.
3. Reference this file in tool-specific config files
4. Maintain consistency across all AI agents without duplication

## Complementary Standards

- Claude Code docs: https://code.claude.com/docs/
- GitHub standards: Various GitHub-specific agent configurations

## Related

- Bookmark: `batch-4.md` - Jan 12, 2026
- Tweet: https://x.com/housecor/status/2010762620899315757
- Mentioned by: Cory House (@housecor)

## Tags

#standards #ai-development #documentation #agent-instructions #open-source

---
title: "agent-browser"
type: tool
date_added: 2026-01-14
source: "https://github.com/vercel-labs/agent-browser"
tags: [browser-automation, ai-agents, headless-browser, rust, performance]
via: "Twitter bookmark from @Shpigford"
---

Agent-browser is Vercel's high-performance headless browser automation CLI specifically optimized for AI agents. Built with Rust and Node.js, it delivers significantly faster performance compared to Playwright while being explicitly designed for AI-driven automation workflows.

## Key Features

- **High Performance**: Substantially faster than Playwright for AI workloads
- **Rust + Node.js**: Fast Rust CLI with Node.js fallback
- **AI-Optimized**: Designed specifically for agent use cases
- **Semantic Locators**: Support for ARIA roles, accessibility trees, and AI-friendly navigation
- **Accessibility Tree**: Get accessibility tree with refs for better AI understanding
- **Full Automation**: Click, fill, type, scroll, upload, take screenshots, extract data

## Installation

```bash
npm install -g agent-browser
agent-browser install  # Download Chromium
```

From source:
```bash
git clone https://github.com/vercel-labs/agent-browser
cd agent-browser
pnpm install
pnpm build
pnpm build:native   # Requires Rust
pnpm link --global
agent-browser install
```

## Quick Start Commands

```bash
agent-browser open example.com
agent-browser snapshot                    # Get accessibility tree with refs
agent-browser click @e2                   # Click by ref
agent-browser fill @e3 "test@example.com" # Fill by ref
agent-browser get text @e1                # Get text by ref
agent-browser screenshot page.png
agent-browser close
```

## Use Cases

- AI agent web automation
- Rapid browser testing for AI systems
- High-throughput web interaction tasks
- Accessibility-aware automation
- Fast web scraping with AI

## Performance

Vercel reports substantially faster performance compared to Playwright, making it ideal for high-volume AI agent tasks where speed matters.

## Links

- [GitHub Repository](https://github.com/vercel-labs/agent-browser)
- [Original Tweet](https://x.com/Shpigford/status/2011522613991129265)

## Related Tools

- Playwright
- Puppeteer
- Claude Code (uses agent-browser for browser automation)

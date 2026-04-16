---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/claude
  - topic/setup
related:
  - "[[MOCs/Automation MOC]]"
---

# 🖥️ Claude Code / Desktop Setup

## Overview
Claude integrates with this vault through multiple channels: Claude Code CLI, Claudian plugin (in-Obsidian), and Claude Desktop app with MCP connections.

## Claude Code CLI

### Installation
```bash
# Install via npm
npm install -g @anthropic-ai/claude-code

# Or via Homebrew
brew install claude-code
```

### Configuration
```bash
# Set API key
export ANTHROPIC_API_KEY="your-key-here"

# Navigate to vault
cd "/path/to/AI Brain"

# Start Claude Code
claude
```

### Vault-Aware Usage
When Claude Code runs from the vault root, it automatically reads:
1. `CLAUDE.md` — vault conventions and rules
2. `.claude/commands/` — custom slash commands
3. `.claude/skills/` — installed skills (obsidian-markdown, etc.)

### Custom Commands
Run custom commands with `/`:
```
/process-inbox     → Process all inbox items
/daily-review      → Generate daily reflection
/find-connections  → Discover note connections
/create-evergreen  → Convert note to evergreen format
/vault-health      → Run vault health audit
/weekly-synthesis  → Create weekly synthesis
```

## Claudian Plugin (In-Obsidian)

### Setup
1. Open Obsidian → Settings → Community Plugins
2. Enable **Claudian**
3. Configure settings:
   - **API Key**: Set `ANTHROPIC_API_KEY` in environment or plugin settings
   - **Model**: Choose model (claude-sonnet-4-20250514 recommended for speed)
   - **Permission Mode**: Start with "Normal" (asks before file changes)

### Features
- Sidebar chat with Claude
- Direct file read/write in vault
- Bash command execution
- MCP server management
- Session history & tabs
- Inline editing suggestions

### Permission Modes
| Mode | Behavior |
|------|----------|
| **Normal** | Asks before file writes & bash commands |
| **Plan** | Read-only, no tool execution without approval |
| **YOLO** | Bypasses all prompts (use carefully) |

## Claude Desktop App

### MCP Connection to Vault
Configure Claude Desktop to access your vault via MCP:

```json
// ~/Library/Application Support/Claude/claude_desktop_config.json
{
  "mcpServers": {
    "obsidian-vault": {
      "command": "npx",
      "args": ["-y", "@anthropic-ai/claude-code", "--mcp"],
      "env": {
        "ANTHROPIC_API_KEY": "your-key"
      }
    }
  }
}
```

## Environment Setup Checklist
- [ ] Claude Code CLI installed and accessible
- [ ] `ANTHROPIC_API_KEY` set in environment
- [ ] Claudian plugin enabled in Obsidian
- [ ] `CLAUDE.md` configured at vault root
- [ ] `.claude/commands/` populated with slash commands
- [ ] `.claude/skills/` has obsidian-skills installed
- [ ] Test: run `claude` from vault root and verify it reads CLAUDE.md

## 🔗 Related
- [[CLAUDE.md]]
- [[03 - Resources/Claude Integration/MCP Tools & Skills]]
- [[03 - Resources/Claude Integration/Context Loading Strategies]]
- [[MOCs/Automation MOC]]

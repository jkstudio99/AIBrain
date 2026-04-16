---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/claude
  - topic/mcp
related:
  - "[[MOCs/Automation MOC]]"
---

# 🔧 MCP Tools & Skills

## Overview
Model Context Protocol (MCP) extends Claude's capabilities by connecting it to external tools and services. Skills are documentation-based extensions that teach Claude domain-specific knowledge.

## Installed Skills

### Obsidian Skills (kepano/obsidian-skills)
Located in `.claude/skills/`:

| Skill | File | Purpose |
|-------|------|---------|
| **obsidian-markdown** | `SKILL.md` | Obsidian Flavored Markdown — wikilinks, embeds, callouts, properties |
| **obsidian-bases** | `SKILL.md` | Obsidian Bases — database structures with views, filters, formulas |
| **json-canvas** | `SKILL.md` | JSON Canvas — visual node-based canvas files |
| **obsidian-cli** | `SKILL.md` | Obsidian CLI — vault operations, plugin dev |
| **defuddle** | `SKILL.md` | Defuddle — extract clean markdown from web pages |

### How Skills Work
Skills are markdown files that provide context to Claude. When Claude Code starts in the vault:
1. It reads `CLAUDE.md` for vault conventions
2. It loads skills from `.claude/skills/` for domain knowledge
3. It reads `.claude/commands/` for available slash commands

Skills don't execute code — they teach Claude how to create correct Obsidian content.

## MCP Server Connections

### Available MCP Servers for Obsidian

#### File System Access
```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/vault"]
    }
  }
}
```

#### Web Search (for research workflows)
```json
{
  "mcpServers": {
    "brave-search": {
      "command": "npx",
      "args": ["-y", "@anthropic-ai/mcp-server-brave-search"],
      "env": {
        "BRAVE_API_KEY": "your-key"
      }
    }
  }
}
```

#### Memory/Knowledge Graph
```json
{
  "mcpServers": {
    "memory": {
      "command": "npx",
      "args": ["-y", "@anthropic-ai/mcp-server-memory"]
    }
  }
}
```

### Claudian MCP Management
In Claudian plugin sidebar:
1. Click the MCP icon
2. Add server URL or stdio command
3. Test connectivity
4. Enable/disable per session

## Creating Custom Skills

### Skill File Structure
```
.claude/skills/
└── my-skill/
    ├── SKILL.md          ← Main skill definition
    └── references/
        └── EXAMPLES.md   ← Additional reference docs
```

### SKILL.md Template
```markdown
---
name: My Custom Skill
description: What this skill does
version: 1.0.0
---

# Skill Name

## When to Use
Describe when Claude should apply this skill.

## Rules
1. Rule one
2. Rule two

## Examples
Show input → output examples.

## Reference
Link to additional docs.
```

## Best Practices

> [!tip] Skill Design
> - Keep skills focused on ONE domain
> - Provide concrete examples, not just rules
> - Include anti-patterns (what NOT to do)
> - Test by asking Claude to perform tasks covered by the skill
> - Iterate based on Claude's output quality

## 🔗 Related
- [[03 - Resources/Claude Integration/Claude Code Desktop Setup]]
- [[03 - Resources/Claude Integration/Context Loading Strategies]]
- [[08 - Automation/Custom Skills/Custom Claude Skills]]
- [[03 - Resources/Community/Popular Claude Skills (2026)]]

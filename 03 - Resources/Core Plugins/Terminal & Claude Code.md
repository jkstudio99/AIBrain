---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/plugins
  - topic/terminal
related:
  - "[[MOCs/Automation MOC]]"
---

# 💻 Terminal + Claude Code

## Overview
The Claudian plugin brings Claude Code directly into Obsidian's sidebar, creating a seamless AI-powered terminal experience within your vault.

## Claudian Plugin

### Key Features
| Feature | Description |
|---------|-------------|
| **Sidebar Chat** | Chat with Claude in a dedicated panel |
| **File Operations** | Claude can read, write, and edit vault files |
| **Bash Commands** | Execute shell commands from within Obsidian |
| **MCP Servers** | Connect to external tools and services |
| **Session History** | Browse past conversations with tabs |
| **Inline Editing** | Claude suggests changes directly in files |
| **Plan Mode** | Read-only exploration before making changes |

### Bang Bash Mode
Prefix commands with `!` to run them directly:
```
!ls "06 - Knowledge/"
!grep -r "seedling" --include="*.md" .
!wc -l "01 - Projects/"*.md
```

### Workflow: Claude as Vault Assistant
1. Open Claudian sidebar (`Ctrl/Cmd + Shift + L`)
2. Ask Claude to perform vault tasks:
   - "Process the 3 notes in my inbox"
   - "Find all seedling notes that haven't been updated in 2 weeks"
   - "Create a literature note from this article URL"
3. Review Claude's changes before approving

### Settings Configuration
| Setting | Recommended | Why |
|---------|-------------|-----|
| Model | claude-sonnet-4-20250514 | Best speed/quality balance |
| Permission Mode | Normal | Safe for daily use |
| Enable Bang Bash | On | Direct shell access |
| Working Directory | Vault root | Full vault access |

## Terminal Workflows

### Quick Vault Statistics
```bash
# Count notes by type
grep -rl "type: evergreen" "06 - Knowledge/" | wc -l
grep -rl "type: literature" "06 - Knowledge/" | wc -l
grep -rl "status: active" "01 - Projects/" | wc -l

# Find recently modified notes
find . -name "*.md" -mtime -1 -not -path "./.git/*" -not -path "./.obsidian/*"

# Word count of vault
find . -name "*.md" -not -path "./.git/*" | xargs wc -w | tail -1
```

### Batch Operations with Claude
```
"Find all notes in 00 - Inbox/ and for each one: read it, suggest a type 
and destination folder, add frontmatter, and list proposed changes. 
Don't move anything until I approve."
```

## 🔗 Related
- [[03 - Resources/Claude Integration/Claude Code Desktop Setup]]
- [[03 - Resources/Core Plugins/Dataview & Queries]]
- [[MOCs/Automation MOC]]

---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/plugins
  - topic/templater
related:
  - "[[MOCs/Automation MOC]]"
---

# 🧩 Templater & QuickAdd

## Overview
Templater extends Obsidian's basic template system with dynamic variables, JavaScript execution, and conditional logic. QuickAdd provides quick-capture macros and multi-step workflows.

## Templater Setup
- **Status**: Installed and enabled
- **Template folder**: `Templates/`
- **Trigger on new file**: On
- **Settings** → Templater → Template folder location → `Templates`

## Templater Syntax

### Date & Time
```
<% tp.date.now("YYYY-MM-DD") %>
<% tp.date.now("HH:mm") %>
<% tp.date.now("dddd") %>
<% tp.date.now("YYYY-MM-DD", 7) %>          ← 7 days from now
<% tp.date.now("YYYY-[W]ww") %>             ← week number
```

### File Operations
```
<% tp.file.title %>                          ← current file name
<% tp.file.creation_date("YYYY-MM-DD") %>    ← file creation date
<% tp.file.folder() %>                       ← current folder
<% tp.file.cursor() %>                       ← place cursor here
<% tp.file.move("01 - Projects/" + tp.file.title) %>  ← move file
```

### User Input
```
<% tp.system.prompt("Enter the source URL") %>
<% tp.system.suggester(["high", "medium", "low"], ["high", "medium", "low"]) %>
```

### Conditional Logic
```
<%* if (tp.file.folder() === "06 - Knowledge/Literature Notes") { %>
type: literature
<%* } else { %>
type: fleeting
<%* } %>
```

## Enhanced Templates

### Smart Literature Note (Templater)
```markdown
---
type: literature
created: "<% tp.date.now("YYYY-MM-DD") %>"
source: "<% tp.system.prompt("Source (title/URL)") %>"
author: "<% tp.system.prompt("Author name") %>"
tags:
  - type/literature
  - status/seedling
status: seedling
related: []
---

# <% tp.file.title %>

## 📖 Source Info
- **Author**: <% tp.system.prompt("Author name") %>
- **Source**: <% tp.system.prompt("Source") %>
- **Date Read**: <% tp.date.now("YYYY-MM-DD") %>

## 📝 Summary
<% tp.file.cursor() %>

## 🔑 Key Ideas
1. 
2. 
3. 
```

### Smart Daily Note (Templater)
```markdown
---
type: daily
created: "<% tp.date.now("YYYY-MM-DD") %>"
tags:
  - type/daily
energy: 
mood: ""
---

# 📅 <% tp.date.now("YYYY-MM-DD") %> <% tp.date.now("dddd") %>

## 🌅 Morning Intention
- <% tp.file.cursor() %>

<%* const yesterday = tp.date.now("YYYY-MM-DD", -1); %>
> Yesterday: [[<%= yesterday %>]]
```

## QuickAdd Macros

### Quick Capture to Inbox
1. Settings → QuickAdd → Add Choice → "Capture"
2. Template: None (direct capture)
3. Save to: `00 - Inbox/`
4. Format: `{{NAME}}`

### Quick New Project
1. Settings → QuickAdd → Add Choice → "Template"
2. Template: `Templates/Project Note.md`
3. Save to: `01 - Projects/`
4. Open after creation: Yes

### Quick Literature Note
1. Capture choice → Template: `Templates/Literature Note.md`
2. Save to: `06 - Knowledge/Literature Notes/`
3. Trigger Templater: Yes

## Keyboard Shortcuts
| Action | Shortcut |
|--------|----------|
| QuickAdd menu | `Ctrl/Cmd + Shift + Q` |
| Insert template | `Ctrl/Cmd + Shift + T` |
| Templater command | `Alt + E` |

## 🔗 Related
- [[03 - Resources/Core Plugins/Dataview & Queries]]
- [[03 - Resources/Core Plugins/Periodic Notes]]
- [[MOCs/Automation MOC]]

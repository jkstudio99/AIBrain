---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/plugins
  - topic/periodic
related:
  - "[[MOCs/Daily Systems MOC]]"
---

# 📅 Periodic Notes

## Overview
The Periodic Notes plugin (or Obsidian's built-in Daily Notes) creates time-based notes on a schedule: daily, weekly, monthly, quarterly, and yearly.

## Configuration

### Daily Notes
| Setting | Value |
|---------|-------|
| Folder | `05 - Daily Systems/Daily Notes` |
| Template | `Templates/Daily Note` |
| Format | `YYYY-MM-DD` |
| Open on startup | Optional |

### Weekly Notes
| Setting | Value |
|---------|-------|
| Folder | `05 - Daily Systems/Weekly Reviews` |
| Template | `Templates/Weekly Review` |
| Format | `YYYY-[W]ww` |

### Monthly Notes
| Setting | Value |
|---------|-------|
| Folder | `05 - Daily Systems/Monthly Reviews` |
| Template | `Templates/Monthly Review` |
| Format | `YYYY-MM - MMMM` |

## Daily Note Workflow

### Morning Routine (5 min)
1. Open today's daily note (click calendar or `Ctrl/Cmd + P` → "Open daily note")
2. Write morning intention
3. Set top 3 priorities
4. Check yesterday's open tasks

### Throughout the Day
- Capture thoughts in the **Notes & Captures** section
- Check off completed tasks
- Add new tasks as they arise

### Evening Routine (10 min)
1. Complete the **Evening Reflection** section
2. Rate energy and mood
3. Note what you're grateful for
4. Review if top 3 priorities were met

## Weekly Review Workflow (Sunday, 30 min)
1. Create weekly note (or use Calendar plugin)
2. Review all 7 daily notes
3. Identify patterns and themes
4. Process items still in Inbox
5. Update project statuses
6. Plan next week's priorities
7. Use `/weekly-synthesis` command for Claude-assisted review

## Monthly Review Workflow (1st of month, 1 hour)
1. Create monthly note
2. Review all weekly notes
3. PARA audit: archive/activate projects
4. Review knowledge garden growth
5. Set monthly theme and goals
6. Use Claude to identify patterns across the month

## Calendar Plugin Integration
The Calendar plugin provides a visual calendar sidebar:
- Click any date to open/create that day's note
- Dots indicate existing notes
- Navigate between weeks/months easily

## Navigation Links Between Periodic Notes
Add to daily note footer:
```markdown
---
⬅️ [[{{yesterday}}]] | [[{{tomorrow}}]] ➡️
📊 [[05 - Daily Systems/Weekly Reviews/{{current-week}}|This Week]]
```

## 🔗 Related
- [[MOCs/Daily Systems MOC]]
- [[03 - Resources/Core Plugins/Templater & QuickAdd]]
- [[Templates/Daily Note]]
- [[Templates/Weekly Review]]
- [[Templates/Monthly Review]]

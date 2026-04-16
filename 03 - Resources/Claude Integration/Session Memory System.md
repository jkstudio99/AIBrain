---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/claude
  - topic/memory
related:
  - "[[MOCs/Automation MOC]]"
---

# 💾 Session Memory System

## Overview
Claude doesn't retain memory between sessions. This system creates persistent context that can be loaded at the start of each session, giving Claude continuity across conversations.

## Architecture

```
Session Memory System
├── Active Context     → Current project state & decisions
├── Vault Memory       → Long-term vault knowledge
├── Interaction Log    → Key decisions from past sessions
└── Preference Profile → Your working style & preferences
```

## Active Context File

Create and maintain `10 - Meta/Active Context.md`:

```markdown
---
type: context
created: "2026-04-16"
updated: "2026-04-16"
tags:
  - type/context
---

# 🧠 Active Context

## Current Focus
- Working on: [current project/task]
- Phase: [exploration/implementation/review]
- Key decisions made: [list]

## Recent Session Highlights
### Session — 2026-04-16
- Created vault structure
- Installed obsidian-skills and claudian plugins
- Set up PARA + Zettelkasten system

## Open Questions
- [ ] Question 1
- [ ] Question 2

## Active Projects State
| Project | Status | Next Step |
|---------|--------|-----------|
|         |        |           |

## Preferences & Patterns Learned
- Prefers: [style preferences]
- Avoids: [anti-patterns]
- Language: [Thai/English mix for conversation, English for notes]
```

## How to Use

### Starting a New Session
```
"Read [[10 - Meta/Active Context]] and [[CLAUDE.md]] to understand 
the current state of my vault and ongoing work."
```

### Ending a Session
Ask Claude to update the active context:
```
"Update [[10 - Meta/Active Context]] with what we accomplished today, 
key decisions made, and suggested next steps."
```

### Session Log Pattern
For important work, create session logs:

```markdown
---
type: session-log
created: "2026-04-16"
session: "2026-04-16-vault-setup"
tags:
  - type/session-log
---

# Session: Vault Setup — 2026-04-16

## Goals
- Set up vault structure
- Install plugins

## Decisions Made
1. Using PARA + Zettelkasten methodology
2. Installed obsidian-skills and claudian

## Artifacts Created
- CLAUDE.md, templates, MOCs, commands

## Insights
- [Key learnings]

## Next Session Todo
- [ ] Task 1
- [ ] Task 2
```

## Vault Memory File

Create `10 - Meta/Vault Memory.md` for long-term vault knowledge:

```markdown
# 🏛️ Vault Memory

## Vault Statistics
- Created: 2026-04-16
- Total notes: [auto-update with dataview]
- Primary language: Thai/English

## Key Architectural Decisions
1. PARA + Zettelkasten hybrid (decided 2026-04-16)
2. Hierarchical tags with #type/ #status/ #area/ prefixes
3. Wikilinks only (no markdown links)

## Tag Taxonomy
- #type/: Note classification
- #status/: Maturity level (seedling → growing → evergreen)
- #area/: Domain area
- #topic/: Subject matter
- #prompt/: Prompt category

## Naming Conventions
- Daily: YYYY-MM-DD
- Weekly: YYYY-[W]ww
- Monthly: MMMM YYYY
- Everything else: Descriptive title, no date prefix
```

## Automated Memory Updates

### Claude Command: Update Memory
Add to `.claude/commands/update-memory.md`:
```
Review what we accomplished in this session and update:
1. [[10 - Meta/Active Context]] — current state, decisions, next steps
2. [[10 - Meta/Vault Memory]] — any new architectural decisions or conventions

Preserve existing content. Add new entries with today's date.
Keep both files concise and scannable.
```

## Best Practices

> [!tip] Memory Hygiene
> - Review Active Context weekly — archive stale items
> - Keep Vault Memory factual and concise
> - Session logs are optional — only for complex multi-session work
> - Don't store sensitive information in memory files

> [!warning] Avoid Context Overload
> - Active Context should stay under 500 words
> - Vault Memory should stay under 1000 words
> - If either grows too large, archive old sections

## 🔗 Related
- [[03 - Resources/Claude Integration/Context Loading Strategies]]
- [[CLAUDE.md]]
- [[MOCs/Automation MOC]]

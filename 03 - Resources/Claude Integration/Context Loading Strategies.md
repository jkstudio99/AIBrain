---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/claude
  - topic/context
related:
  - "[[MOCs/Automation MOC]]"
---

# 🧠 Context Loading Strategies

## Overview
Claude's context window is powerful but finite. Strategic context loading ensures Claude has exactly the information it needs for each task — no more, no less.

## Context Hierarchy

```
Priority 1 (Always Loaded)
├── CLAUDE.md — Vault conventions
├── .claude/skills/ — Domain knowledge
└── .claude/commands/ — Available commands

Priority 2 (Task-Specific)
├── Relevant MOC — Map of related content
├── Target note(s) — What you're working on
└── Related notes — Connected context

Priority 3 (On-Demand)
├── Templates — When creating new notes
├── Reference docs — When looking up specifics
└── Historical notes — When analyzing patterns
```

## Loading Strategies

### 1. MOC-First Strategy
**When**: Working on a topic area
**How**: Start by loading the relevant MOC, then drill into specific notes.
```
"Read [[MOCs/Knowledge MOC]] and then look at the recent evergreen notes 
to suggest connections I might be missing."
```

### 2. Folder-Scoped Strategy
**When**: Processing or auditing a section
**How**: Point Claude at a specific folder.
```
"Review all notes in 06 - Knowledge/Literature Notes/ and identify 
which ones are ready to become evergreen notes."
```

### 3. Tag-Filtered Strategy
**When**: Cross-cutting concerns across folders
**How**: Ask Claude to find notes by tag.
```
"Find all notes tagged #status/seedling and suggest which ones 
have enough content to upgrade to #status/growing."
```

### 4. Temporal Strategy
**When**: Reviews and synthesis
**How**: Focus on time-based windows.
```
"Read all daily notes from the past 7 days and create a weekly 
synthesis highlighting recurring themes."
```

### 5. Relationship Chain Strategy
**When**: Deep exploration of connected ideas
**How**: Follow links through the knowledge graph.
```
"Start from [[Core Idea Note]] and follow its related:: links 
2 levels deep. Map the knowledge cluster."
```

## Context Window Optimization

### Minimize Token Waste
| Do | Don't |
|----|-------|
| Load specific files by name | Load entire folders blindly |
| Ask Claude to read only what it needs | Paste entire notes into chat |
| Use summaries for large notes | Include raw full-text of long articles |
| Reference templates by path | Copy-paste template content |

### Effective Prompting Patterns
```
# Good — Specific context
"Read [[Literature Note X]] and [[Evergreen Note Y]], then 
create a synthesis note connecting their core ideas."

# Bad — Vague context
"Look at my knowledge notes and find connections."
```

### Multi-Turn Context Building
For complex tasks, build context incrementally:
1. **Turn 1**: "Read [[MOC]] and summarize what topics I have notes on."
2. **Turn 2**: "Now read [specific notes] that relate to [topic]."
3. **Turn 3**: "Synthesize what you've learned into a new note."

## CLAUDE.md as Context Anchor
The `CLAUDE.md` file is always loaded first. It serves as:
- **Convention guide**: How to format notes
- **Navigation map**: Where to find things
- **Rule set**: What to do and not do
- **Vocabulary**: Consistent terminology

> [!tip] Keep CLAUDE.md Lean
> Don't overload CLAUDE.md with content. It should be a concise guide (under 2000 words). Put detailed reference in skills or resource notes.

## Session Memory Strategy
For long-running work:
1. Create a "session context" note capturing key decisions and findings
2. Reference it at the start of new sessions
3. Update it as understanding evolves
4. Archive when the work is complete

See: [[03 - Resources/Claude Integration/Session Memory System]]

## 🔗 Related
- [[03 - Resources/Claude Integration/Session Memory System]]
- [[03 - Resources/Claude Integration/Claude Code Desktop Setup]]
- [[CLAUDE.md]]
- [[10 - Meta/Claude Context Optimization]]

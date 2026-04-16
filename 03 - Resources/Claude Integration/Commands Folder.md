---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/claude
  - topic/commands
related:
  - "[[03 - Resources/Claude Integration/Claude Integration]]"
---

# .claude/commands Folder

## Purpose
The `.claude/commands/` folder stores reusable slash commands that turn recurring workflows into fast prompts.

## Existing Commands
- `/process-inbox`
- `/daily-review`
- `/find-connections`
- `/create-evergreen`
- `/vault-health`
- `/weekly-synthesis`

## Recommended Additions
- `/trace`
- `/challenge`
- `/reframe`
- `/synthesize`
- `/update-memory`

## Design Rules
- Keep one command focused on one repeatable task.
- Reference folders, templates, and note types explicitly.
- Prefer action steps over vague style guidance.

## Related
- [[07 - Prompt Library/Custom Commands/Custom Slash Commands]]
- [[03 - Resources/Claude Integration/Session Memory System]]

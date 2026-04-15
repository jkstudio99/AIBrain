---
type: moc
created: "2026-04-16"
tags:
  - type/moc
---

# ⚙️ Automation MOC

## Claude Skills
The following skills are installed in `.claude/skills/`:
- **obsidian-markdown** — Obsidian Flavored Markdown creation
- **obsidian-bases** — Database structures with views & formulas
- **json-canvas** — Visual canvas file creation
- **obsidian-cli** — Vault operations & plugin development
- **defuddle** — Clean markdown extraction from web

## Custom Commands
Located in `.claude/commands/`:
- `/process-inbox` — Process all items in Inbox
- `/daily-review` — Generate daily reflection
- `/find-connections` — Find links between recent notes
- `/create-evergreen` — Convert a note to evergreen format
- `/vault-health` — Check vault health metrics

## Workflows
### Capture → Process → Connect
1. **Capture**: Quick note to `00 - Inbox/`
2. **Process**: Claude extracts insights, suggests type & location
3. **Connect**: Claude finds related notes, suggests backlinks

### Auto-Tagging
- Claude analyzes note content and suggests tags
- Maintains tag taxonomy consistency

### Summary Generation
- Literature notes → automatic summaries
- Meeting notes → action items extraction
- Research → synthesis across multiple sources

## 🔗 Related
- [[Prompt Library MOC]]
- [[Knowledge MOC]]

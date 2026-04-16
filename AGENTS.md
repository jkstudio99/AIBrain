# AI Brain — Obsidian Codex Ecosystem

## Vault Overview
This is a personal knowledge management vault built on PARA + Zettelkasten methodology, deeply integrated with Codex AI for intelligent note-taking, synthesis, and automation.

## Folder Structure
```
00 - Inbox/          → Capture everything here first
01 - Projects/       → Active projects with clear outcomes
02 - Areas/          → Ongoing areas of responsibility
03 - Resources/      → Reference material & topics of interest
04 - Archive/        → Completed/inactive items
05 - Daily Systems/  → Daily notes, reviews, journals, habits
06 - Knowledge/      → Literature notes, evergreen notes, research
07 - Prompt Library/ → AI prompts, thinking tools, commands
08 - Automation/     → Custom skills, scripts, workflows
09 - Visualization/  → Canvas, knowledge maps, dashboards
10 - Meta/           → Vault health, backup, learning resources
Templates/           → All note templates
Attachments/         → Images, PDFs, media
MOCs/                → Maps of Content (hub notes)
```

## Conventions
- **Wikilinks**: Always use `[[wikilinks]]` for internal links
- **Tags**: Use hierarchical tags like `#type/literature`, `#status/seedling`, `#area/dev`
- **Properties**: Every note should have YAML frontmatter with at least `type`, `created`, `tags`
- **Note Types**: `fleeting`, `literature`, `evergreen`, `project`, `moc`, `daily`, `weekly`, `monthly`
- **Status Tags**: `#status/seedling` → `#status/growing` → `#status/evergreen`
- **File naming**: Use descriptive titles, no date prefixes (except daily/periodic notes)
- **Attachments**: Store in `Attachments/` folder, organized by type

## Codex Integration Rules
- When creating notes, always use the appropriate template from `Templates/`
- Respect the PARA structure — ask which folder if unclear
- Always add backlinks to relevant MOCs
- Use Obsidian-flavored markdown (callouts, wikilinks, embeds)
- When processing notes, preserve the original content and add synthesis below
- For daily notes, follow the template in `Templates/Daily Note.md`
- Use Dataview-compatible frontmatter properties

## Key MOCs
- `[[🏠 Home]]` — Main dashboard
- `[[MOCs/Projects MOC]]` — Active projects overview
- `[[MOCs/Knowledge MOC]]` — Knowledge graph entry point
- `[[MOCs/Daily Systems MOC]]` — Daily/weekly/monthly systems
- `[[MOCs/Prompt Library MOC]]` — All prompts and commands
- `[[MOCs/Automation MOC]]` — Automation workflows

## Dataview Patterns
- Tasks: `status:: todo | in-progress | done`
- Priority: `priority:: high | medium | low`
- Dates: `created`, `modified`, `due`, `completed`
- Relations: `related::`, `source::`, `project::`

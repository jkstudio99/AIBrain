---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/vault
related:
  - "[[🏠 Home]]"
---

# 📎 Attachment Management

## Overview
All non-markdown files (images, PDFs, media) are stored in the `Attachments/` folder. This keeps the vault clean and makes backups/syncing more predictable.

## Configuration
Obsidian is configured to automatically place attachments in the `Attachments/` folder:
- **Settings** → Files & Links → Default location for new attachments → `In the folder specified below`
- **Attachment folder path**: `Attachments`

## Folder Organization
```
Attachments/
├── Images/        → Screenshots, diagrams, photos
├── PDFs/          → Documents, papers, books
├── Audio/         → Voice notes, recordings
├── Video/         → Clips, screencasts
├── Exports/       → Exported files from other tools
└── Misc/          → Everything else
```

## Embedding Attachments in Notes

### Images
```markdown
![[image-name.png]]
![[image-name.png|500]]          ← width in pixels
![[image-name.png|500x300]]      ← width x height
```

### PDFs
```markdown
![[document.pdf]]                ← embed full PDF
![[document.pdf#page=5]]         ← specific page
![[document.pdf#height=400]]     ← custom height
```

### Audio/Video
```markdown
![[recording.mp3]]
![[video.mp4]]
```

## Naming Conventions
- Use descriptive names: `project-wireframe-v2.png` not `IMG_4521.png`
- Include date for temporal items: `2026-04-16-meeting-whiteboard.jpg`
- Use kebab-case: `my-diagram-final.svg`
- Prefix by context: `project-name-screenshot.png`

## Cleanup Workflow

### Find Orphan Attachments
Attachments not linked from any note:
```dataview
LIST
FROM "Attachments"
WHERE length(file.inlinks) = 0
```

### Find Broken Embeds
Notes referencing missing attachments show up as broken links in the graph view. Use the vault health command to detect these.

## Best Practices

> [!tip] Tips
> - Compress images before adding (use ImageOptim or similar)
> - Prefer SVG for diagrams (scales without quality loss)
> - Use Excalidraw for hand-drawn diagrams (stays in-vault)
> - Regularly audit for orphan attachments
> - Consider linking to external URLs for large files instead of embedding

> [!warning] Git Considerations
> - Large binary files bloat the git repo
> - Consider `.gitignore` for `Attachments/Video/` if files are large
> - Use Git LFS for repos with many large attachments

## 🔗 Related
- [[03 - Resources/Vault Foundation/Metadata & Dataview Guide]]
- [[10 - Meta/Vault Health/Vault Health Checks]]

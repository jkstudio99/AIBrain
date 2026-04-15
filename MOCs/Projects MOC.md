---
type: moc
created: "2026-04-16"
tags:
  - type/moc
---

# 🎯 Projects MOC

## Active Projects
```dataview
TABLE status, priority, due
FROM "01 - Projects"
WHERE type = "project" AND status = "active"
SORT priority ASC
```

## Recently Completed
```dataview
TABLE completed
FROM "01 - Projects"
WHERE type = "project" AND status = "done"
SORT completed DESC
LIMIT 5
```

## Project Pipeline
| Priority | Project | Status | Deadline |
|----------|---------|--------|----------|
|          |         |        |          |

## 🔗 Related
- [[Areas MOC]]
- [[Daily Systems MOC]]

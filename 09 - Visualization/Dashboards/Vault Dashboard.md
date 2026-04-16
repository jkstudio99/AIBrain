---
type: dashboard
created: "2026-04-16"
tags:
  - type/dashboard
  - area/visualization
related:
  - "[[MOCs/Visualization MOC]]"
---

# Vault Dashboard

## Active Projects
```dataview
TABLE status, priority
FROM "01 - Projects"
WHERE type = "project" AND status = "active"
SORT priority ASC
```

## Recent Notes
```dataview
TABLE type, created
FROM ""
WHERE type
SORT created DESC
LIMIT 10
```

## Inbox Backlog
```dataview
LIST
FROM "00 - Inbox"
SORT file.name ASC
```

## Knowledge Growth
```dataview
TABLE status, created
FROM "06 - Knowledge/Evergreen Notes"
SORT created DESC
LIMIT 8
```

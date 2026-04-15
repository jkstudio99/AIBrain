---
type: moc
created: "2026-04-16"
tags:
  - type/moc
---

# 🧠 Knowledge MOC

## Evergreen Notes
```dataview
TABLE status, created
FROM "06 - Knowledge/Evergreen Notes"
WHERE type = "evergreen"
SORT created DESC
```

## Literature Notes
```dataview
TABLE author, source, created
FROM "06 - Knowledge/Literature Notes"
WHERE type = "literature"
SORT created DESC
LIMIT 10
```

## Research Topics
```dataview
LIST
FROM "06 - Knowledge/Research"
SORT created DESC
```

## Knowledge by Status
### 🌱 Seedlings
```dataview
LIST
FROM "06 - Knowledge"
WHERE status = "seedling"
```

### 🌿 Growing
```dataview
LIST
FROM "06 - Knowledge"
WHERE status = "growing"
```

### 🌳 Evergreen
```dataview
LIST
FROM "06 - Knowledge"
WHERE status = "evergreen"
```

## 🔗 Related
- [[Prompt Library MOC]] — Tools for processing knowledge
- [[Daily Systems MOC]] — Capture workflows

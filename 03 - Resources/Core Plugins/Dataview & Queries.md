---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/plugins
  - topic/dataview
related:
  - "[[03 - Resources/Vault Foundation/Metadata & Dataview Guide]]"
---

# 📊 Dataview & Queries

## Overview
Dataview transforms your vault into a queryable database. Every YAML frontmatter property becomes a field you can filter, sort, and display.

## Plugin Setup
- **Status**: Installed and enabled
- **Settings**: Settings → Dataview → Enable JavaScript Queries → On
- **Inline Queries**: Enable for `$=` syntax in notes

## Query Types

### DQL (Dataview Query Language)
The primary query language — SQL-like syntax.

#### TABLE
```dataview
TABLE author, created, status
FROM "06 - Knowledge/Literature Notes"
WHERE status = "seedling"
SORT created DESC
```

#### LIST
```dataview
LIST
FROM "01 - Projects"
WHERE status = "active"
SORT file.name ASC
```

#### TASK
```dataview
TASK
FROM "01 - Projects" OR "05 - Daily Systems"
WHERE !completed
SORT due ASC
```

#### CALENDAR
```dataview
CALENDAR created
FROM "06 - Knowledge"
```

### Common Filters

| Filter | Example |
|--------|---------|
| Equals | `WHERE status = "active"` |
| Contains | `WHERE contains(tags, "#area/dev")` |
| Date range | `WHERE created >= date("2026-04-01")` |
| Not empty | `WHERE author` |
| File property | `WHERE file.size > 1000` |
| Regex | `WHERE regexmatch("^Project", file.name)` |

### Useful Vault Queries

#### Dashboard: Vault Overview
```dataview
TABLE WITHOUT ID
  length(filter(rows, (r) => r.type = "evergreen")) AS "🌳 Evergreen",
  length(filter(rows, (r) => r.type = "literature")) AS "📖 Literature",
  length(filter(rows, (r) => r.type = "project")) AS "🎯 Projects",
  length(filter(rows, (r) => r.type = "fleeting")) AS "💭 Fleeting"
FROM ""
WHERE type
GROUP BY true
```

#### Stale Active Projects
```dataview
TABLE file.mday AS "Last Modified", status, priority
FROM "01 - Projects"
WHERE status = "active" AND file.mday < date(today) - dur(14 days)
SORT file.mday ASC
```

#### Knowledge Growth This Month
```dataview
TABLE type, status
FROM "06 - Knowledge"
WHERE created >= date(today) - dur(30 days)
SORT created DESC
```

#### Notes Linking to Current Note
```dataview
LIST
FROM [[]]
SORT file.name ASC
```

## DataviewJS Power Queries

### Tag Distribution
```dataviewjs
const pages = dv.pages();
const tagMap = {};
pages.forEach(p => {
  (p.tags || []).forEach(t => {
    tagMap[t] = (tagMap[t] || 0) + 1;
  });
});
const sorted = Object.entries(tagMap).sort((a, b) => b[1] - a[1]).slice(0, 15);
dv.table(["Tag", "Count"], sorted);
```

## Best Practices

> [!tip] Query Performance
> - Always scope queries to specific folders when possible
> - Use `LIMIT` on dashboard queries
> - Avoid deeply nested `GROUP BY` on large vaults
> - Cache expensive queries in dedicated dashboard notes

## 🔗 Related
- [[03 - Resources/Vault Foundation/Metadata & Dataview Guide]]
- [[03 - Resources/Core Plugins/Templater & QuickAdd]]

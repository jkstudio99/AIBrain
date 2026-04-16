---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/vault
  - topic/dataview
related:
  - "[[MOCs/Knowledge MOC]]"
---

# 📊 Metadata & Dataview Guide

## Overview
Every note in this vault uses YAML frontmatter properties that power Dataview queries, enabling dynamic dashboards, automatic lists, and powerful filtering across the entire knowledge base.

## Standard Frontmatter Schema

### Required Properties (All Notes)
```yaml
---
type: fleeting | literature | evergreen | project | moc | daily | weekly | monthly | area | resource | prompt
created: "YYYY-MM-DD"
tags:
  - type/[note-type]
  - status/[status]
---
```

### Optional Properties by Note Type

#### Literature Notes
```yaml
source: "Book Title / URL / Paper"
author: "Author Name"
status: seedling | growing | evergreen
related: ["[[Note 1]]", "[[Note 2]]"]
```

#### Project Notes
```yaml
status: active | paused | done | archived
priority: high | medium | low
due: "YYYY-MM-DD"
completed: "YYYY-MM-DD"
project: "[[Parent Project]]"
```

#### Evergreen Notes
```yaml
status: seedling | growing | evergreen
related: ["[[Connected Note]]"]
source: "[[Literature Note]]"
```

#### Daily Notes
```yaml
energy: 1-10
mood: "descriptor"
```

## Dataview Query Patterns

### Basic Queries

#### List All Active Projects
```dataview
TABLE status, priority, due
FROM "01 - Projects"
WHERE status = "active"
SORT priority ASC, due ASC
```

#### Recent Literature Notes
```dataview
TABLE author, source, status
FROM "06 - Knowledge/Literature Notes"
SORT created DESC
LIMIT 10
```

#### Unprocessed Inbox Items
```dataview
LIST
FROM "00 - Inbox"
SORT created ASC
```

### Advanced Queries

#### Knowledge Garden Health — Status Distribution
```dataview
TABLE WITHOUT ID
  status AS "Status",
  length(rows) AS "Count"
FROM "06 - Knowledge"
WHERE status
GROUP BY status
```

#### Orphan Notes — No Incoming/Outgoing Links
```dataview
LIST
FROM ""
WHERE length(file.inlinks) = 0 AND length(file.outlinks) = 0
AND type != "daily"
```

#### Tasks Due This Week
```dataview
TASK
FROM "01 - Projects"
WHERE due AND due <= date(today) + dur(7 days)
SORT due ASC
```

#### Notes Modified Today
```dataview
LIST
FROM ""
WHERE file.mday = date(today)
SORT file.mtime DESC
```

#### Tag Cloud — Most Used Tags
```dataview
TABLE WITHOUT ID
  tags AS "Tag",
  length(rows) AS "Count"
FROM ""
FLATTEN tags
GROUP BY tags
SORT length(rows) DESC
LIMIT 20
```

#### Cross-Reference: Notes Related to a Specific Note
```dataview
LIST
FROM ""
WHERE contains(related, "[[Target Note]]")
```

### Inline Dataview

Use inline queries for quick data in notes:
- Total notes: `$= dv.pages().length`
- Active projects: `$= dv.pages('"01 - Projects"').where(p => p.status === "active").length`
- Seedling notes: `$= dv.pages('"06 - Knowledge"').where(p => p.status === "seedling").length`
- Notes created today: `$= dv.pages().where(p => p.file.cday.toFormat("yyyy-MM-dd") === dv.date("today").toFormat("yyyy-MM-dd")).length`

## DataviewJS Examples

### Knowledge Growth Chart (by month)
```dataviewjs
const pages = dv.pages('"06 - Knowledge"');
const byMonth = {};
pages.forEach(p => {
  const month = p.created?.toFormat?.("yyyy-MM") || "unknown";
  byMonth[month] = (byMonth[month] || 0) + 1;
});
const sorted = Object.entries(byMonth).sort();
dv.table(["Month", "Notes Created"], sorted.map(([m, c]) => [m, c]));
```

### Project Progress Tracker
```dataviewjs
const projects = dv.pages('"01 - Projects"').where(p => p.type === "project");
const statusCounts = {active: 0, paused: 0, done: 0};
projects.forEach(p => { if (statusCounts[p.status] !== undefined) statusCounts[p.status]++; });
dv.table(["Status", "Count"], Object.entries(statusCounts));
```

## Best Practices

> [!tip] Consistency is Key
> - Always use the same property names across all notes
> - Use templates to enforce consistent frontmatter
> - Prefer arrays for `tags` and `related` fields
> - Use ISO date format `YYYY-MM-DD` for all dates
> - Don't create custom properties without adding them to this guide

> [!warning] Performance
> - Avoid `FROM ""` without filters on large vaults (1000+ notes)
> - Use folder-specific queries when possible: `FROM "01 - Projects"`
> - Limit results with `LIMIT` on dashboard queries
> - Use `WHERE` clauses early to reduce result set

## 🔗 Related
- [[03 - Resources/Core Plugins/Dataview & Queries]]
- [[MOCs/Knowledge MOC]]
- [[🏠 Home]]

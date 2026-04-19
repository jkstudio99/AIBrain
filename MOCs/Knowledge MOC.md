---
type: moc
created: "2026-04-16"
modified: "2026-04-19"
tags:
  - type/moc
  - status/active
---

# 🧠 Knowledge MOC

> Hub สำหรับ knowledge graph — evergreen, literature, workflows, research

---

## 📚 Knowledge Workflows (core methodology)

> Read-first → Process → Connect — PARA + Zettelkasten in practice

### Short overviews
- [[03 - Resources/Knowledge Workflows/Knowledge Workflows|Knowledge Workflows — index]]
- [[03 - Resources/Knowledge Workflows/Capture Process Connect|Capture → Process → Connect]]
- [[03 - Resources/Knowledge Workflows/Evergreen Notes|Evergreen Notes (overview)]]
- [[03 - Resources/Knowledge Workflows/Literature Notes|Literature Notes (overview)]]
- [[03 - Resources/Knowledge Workflows/Project Management|Project Management (overview)]]
- [[03 - Resources/Knowledge Workflows/Research & Synthesis|Research & Synthesis (overview)]]

### Deep guides
- [[03 - Resources/Knowledge Workflows/Evergreen Notes Guide|Evergreen Notes — full guide]]
- [[03 - Resources/Knowledge Workflows/Literature Notes Guide|Literature Notes — full guide]]
- [[03 - Resources/Knowledge Workflows/Project Management Guide|Project Management — full guide]]
- [[03 - Resources/Knowledge Workflows/Research & Synthesis Guide|Research & Synthesis — full guide]]

---

## 📖 Evergreen Notes

```dataview
TABLE status, created
FROM "06 - Knowledge/Evergreen Notes"
WHERE type = "evergreen"
SORT created DESC
```

## 📑 Literature Notes

```dataview
TABLE author, source, created
FROM "06 - Knowledge/Literature Notes"
WHERE type = "literature"
SORT created DESC
LIMIT 10
```

## 🔬 Research Topics

```dataview
LIST
FROM "06 - Knowledge/Research"
SORT created DESC
```

---

## 🌱 Knowledge by Status

### 🌱 Seedlings
```dataview
LIST
FROM "06 - Knowledge" OR "03 - Resources"
WHERE status = "seedling"
SORT file.mday DESC
LIMIT 20
```

### 🌿 Growing
```dataview
LIST
FROM "06 - Knowledge" OR "03 - Resources"
WHERE status = "growing"
SORT file.mday DESC
LIMIT 20
```

### 🌳 Evergreen
```dataview
LIST
FROM "06 - Knowledge" OR "03 - Resources"
WHERE status = "evergreen"
SORT file.mday DESC
LIMIT 20
```

---

## 🔗 Related MOCs

- [[Prompt Library MOC]] — prompts for processing knowledge
- [[Daily Systems MOC]] — capture workflows
- [[Projects MOC]] — project-bound knowledge
- [[Areas MOC]] — team/area knowledge
- [[Automation MOC]] — automation around knowledge ops

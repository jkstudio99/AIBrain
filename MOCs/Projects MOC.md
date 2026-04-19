---
type: moc
created: "2026-04-16"
modified: "2026-04-19"
tags:
  - type/moc
  - status/active
---

# 🎯 Projects MOC

> Hub สำหรับทุก active project ใน vault — PARA/P (Projects)

---

## 📌 Active Projects (curated list)

### 🏗️ AI Multi-Agent Workflow
> Full AI ecosystem blueprint for 15-20 person software house

- [[01 - Projects/AI Multi-Agent Workflow/README|README — start here]]
- [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint|Blueprint]] — master blueprint, 13 roles × 7 phases
- [[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template|Role Playbook Template]]
- [[01 - Projects/AI Multi-Agent Workflow/02 - Phase Gate Checklists|Phase Gate Checklists]]
- [[01 - Projects/AI Multi-Agent Workflow/03 - Sprint Kit|Sprint Kit]] — 14 copy-paste prompts

### 📖 Obsidian Claude Ecosystem
> Core vault infrastructure — docs, playbooks, TH/EN guides

- [[01 - Projects/Obsidian Claude Ecosystem|Obsidian Claude Ecosystem]] — project root
- [[01 - Projects/Obsidian Claude Ecosystem Usage Guide|Usage Guide (EN)]]
- [[01 - Projects/คู่มือการใช้งาน Obsidian Claude Ecosystem (TH)|คู่มือการใช้งาน (TH)]]
- [[01 - Projects/คู่มือเริ่มต้นใช้งาน (Quick Start)|Quick Start (TH)]]

---

## 📊 Dataview — all projects

```dataview
TABLE status, priority, file.cday as created
FROM "01 - Projects"
WHERE type = "project"
SORT priority ASC, file.cday DESC
```

## ✅ Recently Completed

```dataview
TABLE completed
FROM "01 - Projects"
WHERE type = "project" AND status = "done"
SORT completed DESC
LIMIT 5
```

## 📦 All Project Files

```dataview
LIST
FROM "01 - Projects"
SORT file.folder ASC, file.name ASC
```

---

## 🔗 Related MOCs

- [[Areas MOC]] — ongoing areas of responsibility (incl. team playbooks)
- [[Knowledge MOC]] — knowledge graph entry
- [[Automation MOC]] — cross-cuts into active projects
- [[Daily Systems MOC]] — daily execution
- [[Prompt Library MOC]] — skills + prompts used across projects
- [[Obsidian Claude Ecosystem MOC]] — the core vault project

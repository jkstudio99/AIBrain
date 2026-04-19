---
type: moc
created: "2026-04-16"
modified: "2026-04-19"
tags:
  - type/moc
  - status/active
---

# 🔄 Areas MOC

> Hub สำหรับ ongoing areas of responsibility — PARA/A (Areas)

---

## 🧑‍🤝‍🧑 Team Playbooks (13 roles)

> Pre-filled AI-assisted playbooks ต่อ role — แต่ละคน fork + กรอกชื่อตัวเอง
> Index: [[02 - Areas/Team/README|Team Playbooks — README]]

### 🧠 Leadership
- [[02 - Areas/Team/Playbook - CEO|CEO]] — vision, capital, strategic bets
- [[02 - Areas/Team/Playbook - CTO|CTO]] — architecture, security, reliability

### ⚙️ Engineering
- [[02 - Areas/Team/Playbook - Senior Backend|Senior Backend]] — API, data models, services
- [[02 - Areas/Team/Playbook - Senior Frontend|Senior Frontend]] — UI, UX delivery, perf, a11y
- [[02 - Areas/Team/Playbook - SA|Solution Architect]] — system design, integration, migration

### 🔍 Product / Design
- [[02 - Areas/Team/Playbook - BA|Business Analyst]] — PRD, stakeholder alignment
- [[02 - Areas/Team/Playbook - UX-UI|UX/UI Designer]] — research, interaction, visual, DS

### 📊 Data
- [[02 - Areas/Team/Playbook - Data Engineer|Data Engineer]] — pipelines, warehouse, quality
- [[02 - Areas/Team/Playbook - Data Scientist|Data Scientist]] — analysis, experiments, ML

### 📣 Growth
- [[02 - Areas/Team/Playbook - Marketing|Marketing]] — positioning, campaigns, content
- [[02 - Areas/Team/Playbook - SEO|SEO]] — keyword, on-page, technical, schema

### 🏢 Operations
- [[02 - Areas/Team/Playbook - Accounting|บัญชี / Accounting]] — close, AR/AP, pricing
- [[02 - Areas/Team/Playbook - Admin|ธุรการ / Admin]] — calendar, meetings, vendors, onboarding

---

## 📊 Dataview — all Areas

```dataview
TABLE file.folder as folder, type, file.mday as modified
FROM "02 - Areas"
SORT file.folder ASC, file.name ASC
```

## 🩺 Area Health Check

| Area | Status | Last Reviewed | Notes |
|------|--------|---------------|-------|
| Team Playbooks | 🆕 seeded | 2026-04-19 | 13 role templates created — waiting for each person to personalize |

---

## 🔗 Related MOCs

- [[Projects MOC]] — time-bound projects
- [[Knowledge MOC]] — knowledge graph hub
- [[Daily Systems MOC]] — daily execution
- [[Prompt Library MOC]] — skills referenced in playbooks

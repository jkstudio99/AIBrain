---
type: home
created: "2026-04-16"
tags:
  - type/home
---

# 🏠 AI Brain — Command Center

> *Your personal knowledge ecosystem powered by Obsidian + Claude*

---

## 🚀 Quick Actions
- 📥 [[00 - Inbox/|Inbox]] — Capture something new
- 📅 [[05 - Daily Systems/Daily Notes/|Today's Note]] — Open daily note
- 🎯 [[MOCs/Projects MOC|Projects]] — Check active projects
- 🧠 [[MOCs/Knowledge MOC|Knowledge]] — Explore your knowledge garden
- 🧭 [[MOCs/Obsidian Claude Ecosystem MOC|Ecosystem]] — Open the system hub

---

## 🗺️ Maps of Content

| MOC | Purpose |
|-----|---------|
| [[MOCs/Projects MOC\|🎯 Projects]] | Active projects & deliverables |
| [[MOCs/Areas MOC\|🔄 Areas]] | Areas of responsibility |
| [[MOCs/Knowledge MOC\|🧠 Knowledge]] | Evergreen notes & research |
| [[MOCs/Daily Systems MOC\|📅 Daily Systems]] | Daily, weekly, monthly reviews |
| [[MOCs/Prompt Library MOC\|🤖 Prompts]] | AI prompts & thinking tools |
| [[MOCs/Automation MOC\|⚙️ Automation]] | Skills, scripts, workflows |
| [[MOCs/Visualization MOC\|🎨 Visualization]] | Canvas, maps, dashboards |
| [[MOCs/Obsidian Claude Ecosystem MOC\|🧭 Ecosystem]] | Full Obsidian + Claude operating map |

---

## 📊 Vault Overview

### Recent Notes
```dataview
TABLE type, status, created
FROM ""
WHERE type != "home" AND type != "moc"
SORT created DESC
LIMIT 10
```

### Active Projects
```dataview
TABLE status, priority, due
FROM "01 - Projects"
WHERE status = "active"
SORT priority ASC
```

### 📥 Inbox Count
```dataview
LIST
FROM "00 - Inbox"
SORT created DESC
```

### 🌱 Knowledge Garden
```dataview
TABLE status
FROM "06 - Knowledge/Evergreen Notes"
SORT created DESC
LIMIT 5
```

---

## 📂 PARA Structure
- **[[01 - Projects/|Projects]]** — Things with deadlines & deliverables
- **[[02 - Areas/|Areas]]** — Ongoing responsibilities
- **[[03 - Resources/|Resources]]** — Topics of interest & reference
- **[[04 - Archive/|Archive]]** — Completed & inactive items

---

## ⚡ Claude Commands
Use these in Claude Code with `/`:
- `/process-inbox` — Process & organize inbox items
- `/daily-review` — Generate daily reflection
- `/find-connections` — Discover note connections
- `/create-evergreen` — Convert note to evergreen
- `/vault-health` — Check vault health metrics
- `/weekly-synthesis` — Create weekly synthesis
- `/trace` — Analyze an idea step by step
- `/challenge` — Stress-test an assumption or plan
- `/synthesize` — Combine several notes into one insight

---

*Last updated: 2026-04-16*

## 📡 Auto Dashboard

<!-- AUTO-DASHBOARD:START -->
> 🕒 Auto-updated 2026-06-10

### 📊 Vault Stats
- Total notes: **392**
- Daily: 200 · Weekly: 9 · Literature: 6 · Evergreen: 2 · Project: 8 · MOC: 12

### 🆕 โน้ตล่าสุด (7 วัน)
- [[MOCs/Auto Tag MOC]] — _10 Jun 10:39_
- [[10 - Meta/Orphan Notes 2026-06-10]] — _10 Jun 10:39_
- [[05 - Daily Systems/Daily Notes/Finance 2026-06-10]] — _10 Jun 10:38_
- [[05 - Daily Systems/Daily Notes/Portfolio 2026-06-10]] — _10 Jun 10:38_
- [[05 - Daily Systems/Daily Notes/Portfolio 2026-06-09]] — _09 Jun 09:16_
- [[05 - Daily Systems/Daily Notes/Finance 2026-06-09]] — _09 Jun 08:35_
- [[05 - Daily Systems/Daily Notes/IT News 2026-06-09]] — _09 Jun 08:11_
- [[🏠 Home]] — _08 Jun 23:33_
- [[10 - Meta/Orphan Notes 2026-06-08]] — _08 Jun 23:33_
- [[05 - Daily Systems/Daily Notes/IT News 2026-06-08]] — _08 Jun 10:11_
- [[05 - Daily Systems/Weekly Reviews/Weekly 2026-W24]] — _08 Jun 10:10_
- [[05 - Daily Systems/Daily Notes/Economic Calendar 2026-06-08]] — _08 Jun 10:10_
- [[02 - Areas/Finance/Monthly/2026/05/Finance 2026-05]] — _08 Jun 10:09_
- [[02 - Areas/Finance/Monthly/2026/04/Finance 2026-04]] — _08 Jun 10:09_
- [[01 - Projects/Market Research/Weekly Sleep Competitor Watch]] — _08 Jun 10:09_
<!-- AUTO-DASHBOARD:END -->

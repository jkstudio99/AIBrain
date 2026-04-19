---
type: playbook
role: BA
created: "2026-04-19"
tags:
  - type/playbook
  - role/ba
  - role/product
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — Business Analyst (BA)

> Role: BA — requirements, PRD, stakeholder alignment, acceptance criteria
> AI counterpart: Product Discovery + UX Research + Decision Logger chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** Business Analyst
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CEO (dotted to CTO)

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- PRD sign-off turnaround < 5 days from kickoff
- Requirement change rate < 15% post-Gate 2
- User interview count ≥ 5 per feature
- Stakeholder satisfaction ≥ 4/5

**Company KPI ที่รับผิดชอบร่วม:**
- Feature adoption rate
- Time-to-value (first aha moment)
- Customer NPS

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `product-discovery` | Problem framing, PRD drafting |
| 2 | `ux-researcher-designer` | Interview guides, synthesis |
| 3 | `competitive-teardown` | Competitive analysis |
| 4 | `research-summarizer` | Synthesize interviews + data |
| 5 | `decision-logger` | Track every PRD decision |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Review overnight stakeholder messages / feedback
[ ] Check active PRDs status
[ ] Plan interviews / stakeholder meetings วันนี้
[ ] `product-discovery` — review open questions for active feature
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `ux-researcher-designer` — prepare / run user interviews
- `research-summarizer` — synthesize research findings
- `competitive-teardown` — competitive feature audit
- `competitive-intel` — market trend signals
- `marketing-psychology` — understand buyer motivation
- `meeting-analyzer` — after stakeholder meetings
- `decision-logger` — log every PRD trade-off

### 🌆 EOD (17:00 - 17:30)

```
[ ] Update PRD docs ใน Obsidian / Notion
[ ] Log decisions of the day
[ ] Schedule interviews ที่ยัง pending
[ ] Note blockers (stakeholder ไม่ตอบ / scope creep)
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning + PRD kickoff | `product-discovery`, `strategic-alignment` |
| Tue | User research — interviews | `ux-researcher-designer` |
| Wed | Stakeholder reviews | `meeting-analyzer`, `decision-logger` |
| Thu | Synthesis + PRD drafting | `research-summarizer`, `competitive-teardown` |
| Fri | Retro + PRD finalization | `self-eval`, `product-discovery` |

---

## 📆 Monthly Rituals

- **1st week** — `competitive-intel` market scan (full)
- **Mid-month** — NPS / customer feedback synthesis (`research-summarizer`)
- **Last week** — Backlog grooming + OKR alignment (`strategic-alignment`)

---

## 🧩 My Orchestration Patterns

### Pattern A — Discovery → PRD (Gate 1→2)
**ใช้เมื่อ:** Kickoff new feature discovery
**Chain:**
```
1. `competitive-teardown` → top 3 competitors
2. `competitive-intel` → market signals + trends
3. `marketing-psychology` → buyer motivation
4. `ux-researcher-designer` → interview guide (10 Q)
5. Run 5+ interviews
6. `research-summarizer` → synthesize findings
7. `product-discovery` → problem framing + PRD v1
8. `decision-logger` → key trade-offs + open questions
9. PRD review with CEO + CTO → sign-off
```

### Pattern B — Scope Change Request
**ใช้เมื่อ:** Stakeholder asks to change scope mid-sprint
**Chain:**
```
1. `decision-logger` → capture request + rationale
2. `scenario-war-room` → impact analysis (cost / time / risk)
3. `strategic-alignment` → OKR fit check
4. Stakeholder meeting → align on trade-off
5. `meeting-analyzer` → action items + decisions
6. Update PRD + notify team
```

### Pattern C — Post-Launch Validation
**ใช้เมื่อ:** 2 weeks post-launch — did we solve the problem?
**Chain:**
```
1. `product-analytics` → adoption + engagement metrics
2. `research-summarizer` → customer feedback synthesis
3. `ux-researcher-designer` → 5 post-launch interviews
4. `decision-logger` → learnings + next iteration
5. Feed into next discovery cycle
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **CEO** → strategic priorities, OKR
- **Marketing / SEO** → market signals, customer voice
- **CS / Support** → customer feedback, complaints
- **UX/UI** → research insights

**ส่งงานให้:**
- **SA / CTO** → PRD (ready for tech spec)
- **Sr BE / Sr FE** → acceptance criteria (ticket-ready)
- **UX/UI** → research findings + user journey
- **QA** → test scenarios from acceptance criteria

**Review กับ:**
- **CEO** — weekly product review
- **CTO / SA** — tech feasibility (per PRD)
- **Leadership** — gate reviews (Phase 1→2 especially)

---

## 🧪 Experiments / Learning Log

| Date | ลอง skill | ผล | Adopt? |
|---|---|---|---|
| | | | |

---

## 📚 References

- [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]
- [[01 - Projects/AI Multi-Agent Workflow/02 - Phase Gate Checklists]]
- [[01 - Projects/AI Multi-Agent Workflow/03 - Sprint Kit]]

---

## 📝 Review

- **Last review:** <<YYYY-MM-DD>>
- **Next review:** <<YYYY-MM-DD>> (2 weeks cadence)
- **Notes:** <<อะไรที่จะลองครั้งถัดไป>>

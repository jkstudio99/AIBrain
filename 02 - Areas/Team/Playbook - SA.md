---
type: playbook
role: SA
created: "2026-04-19"
tags:
  - type/playbook
  - role/sa
  - role/architecture
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — Solution Architect (SA)

> Role: SA — system design, integration, tech stack, migration
> AI counterpart: Senior Architect + Migration Architect + API Reviewer chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** Solution Architect
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CTO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Architecture review turnaround < 2 days
- Tech debt index trending down (quarterly)
- SLO compliance ≥ 99.5% of components
- ADR documentation coverage 100%

**Company KPI ที่รับผิดชอบร่วม:**
- Lead time for change
- MTTR
- System uptime

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `senior-architect` | System design, ADR |
| 2 | `migration-architect` | Legacy modernization, refactor planning |
| 3 | `api-design-reviewer` | Contract reviews across services |
| 4 | `ci-cd-pipeline-builder` | Pipeline design + improvements |
| 5 | `observability-designer` | SLO + alert spec for new services |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Review overnight deploys + SLO dashboards
[ ] Check active design doc reviews (ARB queue)
[ ] Plan: which system/design to focus on วันนี้
[ ] `senior-architect` — review newest ADRs
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `senior-architect` — design doc authoring / review
- `api-design-reviewer` — every cross-service contract
- `database-schema-designer` — data model validation
- `migration-architect` — legacy migration plans
- `ci-cd-pipeline-builder` — pipeline improvements
- `observability-designer` — SLO spec, alert tuning
- `performance-profiler` — capacity planning

### 🌆 EOD (17:00 - 17:30)

```
[ ] Update ADR docs (ถ้ามี decision วันนี้)
[ ] `changelog-generator` — architectural changes
[ ] Flag risks to CTO ถ้ามี
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning + ARB prep | `senior-architect` |
| Tue | Design doc deep work | `senior-architect`, `migration-architect` |
| Wed | ARB (architecture review board) | `senior-architect`, `api-design-reviewer` |
| Thu | Cross-team integration reviews | `api-design-reviewer`, `observability-designer` |
| Fri | Tech debt review + retro | `performance-profiler`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — System-wide health review (`senior-architect` + `observability-designer`)
- **Mid-month** — `migration-architect` — what's next to modernize?
- **Last week** — `ci-cd-pipeline-builder` — pipeline optimization

---

## 🧩 My Orchestration Patterns

### Pattern A — New Feature System Design
**ใช้เมื่อ:** PRD signed, need tech spec before build (Gate 2→3)
**Chain:**
```
1. `senior-architect` → high-level architecture
2. `database-schema-designer` → data model + migration plan
3. `api-design-reviewer` → API contract spec (OpenAPI)
4. `observability-designer` → SLO + alert spec
5. `ci-cd-pipeline-builder` → pipeline updates needed
6. `performance-profiler` → capacity + perf budget
7. `senior-security` → threat model
8. Write ADR → CTO sign-off
```

### Pattern B — Legacy Migration
**ใช้เมื่อ:** Modernizing old system (e.g., monolith → services)
**Chain:**
```
1. `migration-architect` → migration strategy (strangler fig / big bang)
2. `senior-architect` → target architecture
3. `database-schema-designer` → data migration plan
4. `api-design-reviewer` → compat layer design
5. `ci-cd-pipeline-builder` → blue-green / canary setup
6. `observability-designer` → dual-write monitoring
7. Phased rollout plan → ADR
```

### Pattern C — Cross-Service Integration Review
**ใช้เมื่อ:** Sr BE ส่ง API proposal ที่กระทบหลาย service
**Chain:**
```
1. `api-design-reviewer` → contract soundness
2. `senior-architect` → coupling + boundary check
3. `observability-designer` → tracing + SLO implications
4. `senior-security` → auth/z path
5. Approve / request changes → ADR entry
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **BA** → PRD (signed) + acceptance criteria
- **CTO** → strategic tech priorities
- **Sr BE / Sr FE** → design doc proposals
- **DE** → data pipeline integration requests

**ส่งงานให้:**
- **Sr BE / Sr FE** → tech spec + ADR
- **CTO** → ARB recommendations + sign-off asks
- **DevOps** → pipeline + infra specs

**Review กับ:**
- **CTO** — ARB (weekly), escalations (on-demand)
- **Sr BE / Sr FE** — design handoff (per feature)
- **DE** — data architecture sync (bi-weekly)

---

## 🧪 Experiments / Learning Log

| Date | ลอง skill | ผล | Adopt? |
|---|---|---|---|
| | | | |

---

## 📚 References

- [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]
- [[01 - Projects/AI Multi-Agent Workflow/02 - Phase Gate Checklists]]

---

## 📝 Review

- **Last review:** <<YYYY-MM-DD>>
- **Next review:** <<YYYY-MM-DD>> (2 weeks cadence)
- **Notes:** <<อะไรที่จะลองครั้งถัดไป>>

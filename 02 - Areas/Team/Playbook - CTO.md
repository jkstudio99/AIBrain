---
type: playbook
role: CTO
created: "2026-04-19"
tags:
  - type/playbook
  - role/cto
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — CTO

> Role: Chief Technology — architecture, security, reliability, engineering culture
> AI counterpart: Senior Architect + CISO Advisor + Incident Commander chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** CTO
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CEO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Lead time for change < 24h (DORA)
- Deploy frequency ≥ 1/day
- MTTR < 1h (P1), < 15min (P0)
- Security score (critical vulns = 0)

**Company KPI ที่รับผิดชอบร่วม:**
- Uptime SLO (99.9%+)
- Customer-reported bug rate
- Engineering cost per ticket closed

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `senior-architect` | Architecture reviews, ADR, tech strategy |
| 2 | `ciso-advisor` | Security posture, compliance audits |
| 3 | `observability-designer` | SLO design, alerting, dashboards |
| 4 | `incident-commander` | Incident response, post-mortems |
| 5 | `dependency-auditor` | Supply chain, CVE triage, license checks |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Review overnight alerts (PagerDuty / Grafana / Sentry)
[ ] Check CI/CD pipeline health (failed builds?)
[ ] Review open P0/P1 tickets
[ ] `senior-architect` — review any new ADRs or design docs
[ ] Plan top-3 tech priorities วันนี้
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `pr-review-expert` — architectural review of high-impact PRs
- `senior-security` — code-level security review
- `api-design-reviewer` — new API contracts
- `migration-architect` — migration planning / legacy modernization
- `ci-cd-pipeline-builder` — pipeline improvements
- `decision-logger` — บันทึกทุก tech decision

### 🌆 EOD (17:00 - 17:30)

```
[ ] `changelog-generator` — tech changelog (deploys, incidents, ADRs)
[ ] Review DORA metrics ประจำวัน
[ ] Brief CEO ถ้ามี tech risk ที่ต้องรู้ pending
[ ] Update daily note ใน Obsidian
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Tech planning + 1:1 with CEO | `senior-architect`, `strategic-alignment` |
| Tue | Security review + dependency audit | `skill-security-auditor`, `dependency-auditor` |
| Wed | Architecture review board (ARB) | `senior-architect`, `api-design-reviewer` |
| Thu | Incident retro / post-mortems | `incident-commander`, `red-team` |
| Fri | Eng all-hands + retro | `observability-designer`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — `senior-architect` deep system review + tech debt inventory
- **Mid-month** — `ciso-advisor` compliance check (GDPR/SOC2/ISO)
- **Last week** — `performance-profiler` capacity review + `scenario-war-room` (scaling plan)

---

## 🧩 My Orchestration Patterns

### Pattern A — New Feature Architecture
**ใช้เมื่อ:** Sr BE/FE ส่ง design doc มาให้ approve ก่อน build
**Chain:**
```
1. `senior-architect` → system design check (scalability, coupling)
2. `api-design-reviewer` → API contract review
3. `database-schema-designer` → data model validation
4. `senior-security` → threat model
5. `observability-designer` → SLO + alert spec
6. `performance-profiler` → perf budget
7. `decision-logger` → ADR entry + sign-off
```

### Pattern B — Incident Response (P0/P1)
**ใช้เมื่อ:** Production incident ที่กระทบลูกค้า
**Chain:**
```
1. `incident-commander` → classify + assemble team + comms
2. `observability-designer` → pull relevant dashboards
3. `runbook-generator` → execute runbook
4. Human decision → mitigate / rollback
5. `red-team` → post-incident blameless analysis
6. `decision-logger` → what changed + action items
```

### Pattern C — Security Gate (pre-release)
**ใช้เมื่อ:** ก่อน release สำคัญ (Gate 4→5)
**Chain:**
```
1. `skill-security-auditor` → repo scan
2. `dependency-auditor` → supply chain + CVEs
3. `senior-security` → code review
4. `red-team` → attack simulation
5. `security-pen-testing` → pentest plan
6. `ai-security` → LLM surface (if applicable)
7. `ciso-advisor` → final sign-off
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **Sr BE / Sr FE** → PR reviews, ADRs, design docs
- **SA** → system design proposals
- **DevOps/SRE** → incident reports, capacity warnings
- **CEO** → strategic priorities, budget constraints

**ส่งงานให้:**
- **CEO** → weekly tech health brief, monthly risk register
- **Sr BE / Sr FE** → arch decisions + coding standards
- **Security Guardian** → security sign-off checklists

**Review กับ:**
- **CEO** — weekly 1:1
- **Sr BE / Sr FE / SA** — ARB (weekly), PR reviews (on-demand)
- **Security Guardian** — bi-weekly security review

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

---
type: playbook
role: Senior Backend
created: "2026-04-19"
tags:
  - type/playbook
  - role/engineering
  - role/backend
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — Senior Backend Engineer

> Role: Senior BE — API design, data models, services, reliability
> AI counterpart: Senior Backend + API Design + DB Schema chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** Senior Backend Engineer
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CTO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Test coverage ≥ 80% (unit + integration)
- API latency p95 < 300ms
- PR review turnaround < 4h
- Zero P0 bugs from own code in past 30 days

**Company KPI ที่รับผิดชอบร่วม:**
- Lead time for change (DORA)
- Deploy frequency
- Uptime SLO

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `senior-backend` | Implementation planning, code review |
| 2 | `api-design-reviewer` | Every new API endpoint / contract change |
| 3 | `database-schema-designer` | Schema changes, migrations |
| 4 | `api-test-suite-builder` | Test plan for every feature |
| 5 | `code-reviewer` | PR reviews (self + peers) |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Check CI/CD status (own PRs + team's)
[ ] Review PRs assigned (SLA 4h)
[ ] Read tech changelog + ADRs เมื่อวาน
[ ] Plan 3 งานหลัก (ticket/feature/bug)
[ ] `senior-backend` — review ticket details ก่อนเริ่ม
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `api-design-reviewer` — ก่อนเขียน endpoint ใหม่
- `database-schema-designer` — ก่อน migration
- `tdd-guide` — test-first workflow
- `api-test-suite-builder` — test coverage plan
- `code-reviewer` — ก่อน push PR (self-review)
- `performance-profiler` — ถ้ามี perf concern
- `senior-security` — ถ้าแตะ auth/PII/payment

### 🌆 EOD (17:00 - 17:30)

```
[ ] `changelog-generator` — สรุปสิ่งที่ทำ
[ ] Commit/push ทุก WIP branch
[ ] Update ticket status
[ ] Note blockers ที่ต้องการความช่วยเหลือพรุ่งนี้
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning | `senior-architect` (grooming), `senior-backend` |
| Tue | Deep work — implementation | `tdd-guide`, `api-test-suite-builder` |
| Wed | ARB / tech review | `api-design-reviewer`, `database-schema-designer` |
| Thu | PR review focus day | `code-reviewer`, `pr-review-expert` |
| Fri | Retro + tech debt / docs | `changelog-generator`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — `performance-profiler` deep review ของ service ตัวเอง
- **Mid-month** — `dependency-auditor` (own services)
- **Last week** — Tech debt inventory + ADR update

---

## 🧩 My Orchestration Patterns

### Pattern A — New Feature Implementation
**ใช้เมื่อ:** Pick up new ticket จาก sprint backlog
**Chain:**
```
1. `senior-architect` → confirm design fit
2. `api-design-reviewer` → draft endpoint contract
3. `database-schema-designer` → schema + migration
4. `api-test-suite-builder` → test plan
5. `tdd-guide` → write tests first
6. Implement → iterate
7. `code-reviewer` → self-review pre-PR
8. `senior-security` → if security-sensitive
9. Open PR
```

### Pattern B — Bug Investigation
**ใช้เมื่อ:** P1/P2 bug assigned
**Chain:**
```
1. Read bug report + related logs (via observability)
2. `senior-backend` → triage + reproduce
3. Check recent deploys (blame)
4. Write failing test → confirm bug
5. Fix + `tdd-guide` → ensure regression coverage
6. `code-reviewer` → self-review
7. Open hotfix PR
```

### Pattern C — PR Review (reviewer side)
**ใช้เมื่อ:** Assigned as reviewer
**Chain:**
```
1. `code-reviewer` → style, bugs, readability
2. `pr-review-expert` → blast radius, coverage delta
3. `senior-security` → if auth/PII/payment path
4. `senior-architect` → if architectural change
5. Leave comment: Must fix / Should / Nit / Approved
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **BA** → PRD + acceptance criteria (ticket-ready)
- **SA** → system design + sequence diagrams
- **Sr FE** → API contract requests
- **QA** → bug reports + reproduction steps

**ส่งงานให้:**
- **Sr FE** → API docs + OpenAPI spec + mock server
- **DE** → event schemas (if producing events)
- **QA** → test plan + deployed preview env
- **CTO** → ADR for architectural decisions

**Review กับ:**
- **CTO** — ARB (weekly), high-impact PRs (on-demand)
- **SA** — design review before build (per feature)
- **Sr FE** — contract handshake (per feature)

---

## 🧪 Experiments / Learning Log

| Date | ลอง skill | ผล | Adopt? |
|---|---|---|---|
| | | | |

---

## 📚 References

- [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]
- [[01 - Projects/AI Multi-Agent Workflow/03 - Sprint Kit]]

---

## 📝 Review

- **Last review:** <<YYYY-MM-DD>>
- **Next review:** <<YYYY-MM-DD>> (2 weeks cadence)
- **Notes:** <<อะไรที่จะลองครั้งถัดไป>>

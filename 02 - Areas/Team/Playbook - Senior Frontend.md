---
type: playbook
role: Senior Frontend
created: "2026-04-19"
tags:
  - type/playbook
  - role/engineering
  - role/frontend
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — Senior Frontend Engineer

> Role: Senior FE — UI, UX delivery, performance, accessibility
> AI counterpart: Senior Frontend + Design System + A11y chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** Senior Frontend Engineer
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CTO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Lighthouse Performance ≥ 90
- Lighthouse A11y ≥ 95
- Bundle size ≤ 250KB gzipped (landing), ≤ 500KB (app)
- Core Web Vitals: LCP < 2.5s, CLS < 0.1, INP < 200ms

**Company KPI ที่รับผิดชอบร่วม:**
- Conversion rate (funnel)
- Task completion rate
- Customer-reported UX bugs

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `senior-frontend` | Implementation planning, component architecture |
| 2 | `ui-design-system` | DS consistency, component reuse |
| 3 | `a11y-audit` | Every new component / page |
| 4 | `performance-profiler` | Bundle size, rendering perf |
| 5 | `playwright-pro` | E2E test for critical paths |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Check CI/CD (own PRs + team)
[ ] Review Figma handoff (new designs จาก UX/UI)
[ ] Check Lighthouse report ล่าสุด (drift?)
[ ] Plan 3 งานหลัก
[ ] `senior-frontend` — review ticket ก่อนเริ่ม
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `ui-design-system` — component exists ไหม, ใช้ของเดิม
- `a11y-audit` — before merge every UI PR
- `performance-profiler` — bundle budget check
- `playwright-pro` — E2E test for new flows
- `apple-hig-expert` — if iOS web views / mobile-first
- `design:design-critique` — feedback ย้อนกลับให้ UX/UI
- `code-reviewer` — self-review pre-PR

### 🌆 EOD (17:00 - 17:30)

```
[ ] `changelog-generator` — สรุปงานวันนี้
[ ] Commit/push
[ ] Lighthouse check ของหน้าที่แตะ
[ ] Note blockers (design ไม่ชัด / API ไม่พร้อม)
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning | `senior-frontend`, `senior-architect` |
| Tue | Design review กับ UX/UI | `design:design-critique`, `ui-design-system` |
| Wed | Deep work — implementation | `ui-design-system`, `playwright-pro` |
| Thu | Perf & a11y review | `performance-profiler`, `a11y-audit` |
| Fri | Retro + Design System updates | `changelog-generator`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — `performance-profiler` full audit (bundle, CWV, hydration)
- **Mid-month** — `a11y-audit` deep (WCAG AA) + screen reader test
- **Last week** — `ui-design-system` consolidation (remove duplicate components)

---

## 🧩 My Orchestration Patterns

### Pattern A — New Component / Feature
**ใช้เมื่อ:** Pick up UI ticket จาก sprint
**Chain:**
```
1. Read Figma + acceptance criteria
2. `ui-design-system` → reusable component มีอยู่แล้วไหม
3. `senior-frontend` → architecture (state, routing, data fetch)
4. `a11y-audit` → design-level check ก่อนเขียน
5. Implement + Storybook
6. `playwright-pro` → E2E test (happy + error paths)
7. `performance-profiler` → bundle impact check
8. `code-reviewer` → self-review
9. Open PR
```

### Pattern B — Performance Audit
**ใช้เมื่อ:** CWV drift แจ้งใน monitoring
**Chain:**
```
1. `performance-profiler` → identify culprit (JS? images? CSS?)
2. Lighthouse + WebPageTest deep dive
3. Fix (code-split / image optim / defer / preload)
4. `playwright-pro` → regression test
5. Measure impact (before/after)
6. `changelog-generator` → document improvement
```

### Pattern C — Design Review Handoff
**ใช้เมื่อ:** UX/UI ส่ง Figma ใหม่มาให้ review
**Chain:**
```
1. `design:design-critique` → UX feasibility + usability
2. `ui-design-system` → DS consistency check
3. `a11y-audit` → contrast, semantic structure, focus
4. `apple-hig-expert` → iOS guideline (if native/web-view)
5. Leave comments in Figma → iterate with UX/UI
6. Sign off when ready for dev
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **UX/UI** → Figma + prototype + design tokens
- **BA** → acceptance criteria
- **Sr BE** → API contract + OpenAPI spec + mock server
- **QA** → bug reports

**ส่งงานให้:**
- **QA** → deployed preview URL + test plan
- **SEO** → page structure + meta (for SEO audit)
- **UX/UI** → implementation feedback (what worked, what didn't)
- **CTO** → perf / a11y reports

**Review กับ:**
- **UX/UI** — design review (per feature)
- **Sr BE** — contract sync (per feature)
- **CTO** — high-impact PRs, perf escalations

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

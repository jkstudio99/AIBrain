---
type: playbook
role: UX/UI
created: "2026-04-19"
tags:
  - type/playbook
  - role/ux-ui
  - role/design
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — UX/UI Designer

> Role: UX/UI — research, interaction design, visual design, design system
> AI counterpart: UX Researcher + Design Critique + A11y + HIG chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** UX/UI Designer
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CTO (dotted to BA)

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Usability score (SUS) ≥ 75
- Design review turnaround < 3 days from brief
- A11y compliance on shipped designs = 100% WCAG AA
- Design system component reuse rate ≥ 70%

**Company KPI ที่รับผิดชอบร่วม:**
- Task completion rate
- Conversion rate
- Customer NPS

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `ux-researcher-designer` | Research, interviews, synthesis |
| 2 | `design:design-critique` | Self + peer design review |
| 3 | `a11y-audit` | Every design deliverable |
| 4 | `ui-design-system` | DS component authoring + governance |
| 5 | `apple-hig-expert` | iOS / mobile-first guidance |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Review feedback on active Figma files
[ ] Check user research queue (interviews pending?)
[ ] Plan 3 design tasks วันนี้
[ ] `ux-researcher-designer` — prep for interviews วันนี้
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `ux-researcher-designer` — run interviews, usability tests
- `design:design-critique` — self-crit before sharing
- `a11y-audit` — contrast, focus, semantic structure check
- `ui-design-system` — component check — new or reuse
- `apple-hig-expert` — mobile / native platform compliance
- `design:accessibility-review` — deeper a11y on complex flows
- `marketing-psychology` — persuasive design, motivation

### 🌆 EOD (17:00 - 17:30)

```
[ ] Sync Figma files (prototypes updated?)
[ ] Log research findings
[ ] Note feedback from devs (Sr FE)
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning + brief | `ux-researcher-designer` |
| Tue | User research (interviews / usability) | `ux-researcher-designer` |
| Wed | Design deep work | `ui-design-system`, `apple-hig-expert` |
| Thu | Design review + handoff to FE | `design:design-critique`, `a11y-audit` |
| Fri | Retro + DS maintenance | `ui-design-system`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — Design System audit (`ui-design-system` + `a11y-audit`)
- **Mid-month** — User testing round (5 participants)
- **Last week** — Pattern library update + retro

---

## 🧩 My Orchestration Patterns

### Pattern A — New Feature Design
**ใช้เมื่อ:** PRD signed, kickoff design (Gate 1→2 → 2→3)
**Chain:**
```
1. `ux-researcher-designer` → interview + empathy map
2. `competitive-teardown` → reference competitor patterns (BA side)
3. Sketch + wireframes → low-fi
4. `design:design-critique` → self-crit + peer
5. Hi-fi + prototype
6. `a11y-audit` → WCAG AA check
7. `apple-hig-expert` → mobile guideline
8. `ui-design-system` → DS coverage
9. Handoff to Sr FE → Figma + tokens + motion spec
```

### Pattern B — Usability Test
**ใช้เมื่อ:** Mid-design, validate key flow
**Chain:**
```
1. `ux-researcher-designer` → test plan (tasks, script)
2. Recruit 5 users
3. Run tests (think-aloud)
4. `research-summarizer` → synthesize findings
5. `design:design-critique` → redesign implications
6. Iterate prototype
7. Retest critical changes
```

### Pattern C — Accessibility Deep Dive
**ใช้เมื่อ:** Quarterly or before major release
**Chain:**
```
1. `a11y-audit` → automated scan (axe, Lighthouse)
2. `design:accessibility-review` → manual check
3. Screen reader test (VoiceOver, NVDA)
4. Keyboard-only navigation test
5. Color contrast audit
6. Report + remediation list → Sr FE
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **BA** → PRD + user journey + success criteria
- **Marketing** → brand + campaign visual direction
- **CS / Support** → pain points + customer complaints

**ส่งงานให้:**
- **Sr FE** → Figma + design tokens + motion spec + prototype
- **BA** → research findings + journey maps
- **Marketing** → brand assets + landing templates
- **QA** → usability test plan + expected behaviors

**Review กับ:**
- **BA** — weekly design sync
- **Sr FE** — design handoff (per feature)
- **CEO / CTO** — brand + strategic design decisions

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

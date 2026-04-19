---
type: reference
created: "2026-04-19"
tags:
  - type/reference
  - topic/ai-workflow
  - topic/sprint
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
---

# 🏃 Sprint Kit — Copy-Paste Templates

> Ready-to-use prompts สำหรับงาน recurring ในแต่ละ sprint
> Copy → วางใน Claude Code → แก้ `<<...>>` → Go

---

## 🌅 Daily — Morning Exec Brief

```
ทำ morning brief ให้ 09:00 นี้

1. อ่าน daily notes ของเมื่อวาน (3 ไฟล์ล่าสุด)
2. อ่าน KPI dashboard ล่าสุด
3. สรุปเป็น 5 bullets:
   - Wins เมื่อวาน
   - Blockers ที่ยัง open
   - Priorities วันนี้ (top 3)
   - Risks สำคัญ
   - 1 decision ที่ต้องการจาก exec
4. ใช้ skill `chief-of-staff`
```

---

## 🔧 Engineering — Feature Kick-off

```
ฉันจะเริ่ม feature ใหม่: <<feature name>>
PRD: <<link/path>>

ทำให้หน่อย (ใช้ skill ตามลำดับ):

1. `senior-architect` — วาง high-level architecture
2. `database-schema-designer` — data model + migrations
3. `api-design-reviewer` — API spec + OpenAPI
4. `api-test-suite-builder` — test plan
5. `tdd-guide` — outline test-first flow
6. `senior-backend` / `senior-frontend` — implementation plan

Output: 1 doc สำหรับ sprint kickoff
```

---

## 🔍 Engineering — PR Review (pre-merge)

```
Review PR นี้ก่อน merge:
<<PR URL หรือ diff>>

Run chain:
1. `code-reviewer` — style, bugs, readability
2. `pr-review-expert` — blast radius, coverage delta
3. `senior-security` — security scan
4. `dependency-auditor` — supply chain
5. `senior-architect` — design fit

สรุปเป็น comment พร้อม:
- Must fix (blocking)
- Should fix (nit)
- Nice to have
- Approved items
```

---

## 🎯 Product — Discovery Kickoff

```
เริ่ม discovery สำหรับ: <<product/feature idea>>

Run:
1. `competitive-teardown` — top 3 competitors ทำอะไร
2. `competitive-intel` — market signal + trends
3. `marketing-psychology` — why customer cares
4. `ux-researcher-designer` — interview guide (10 Q)
5. `product-discovery` — problem framing
6. `research-summarizer` — synthesize ทั้งหมด

Output: Discovery Brief (1 pager)
```

---

## 📣 Marketing — Campaign Launch

```
Launch campaign: <<campaign name>>
Target: <<persona>>
Channel mix: <<email/paid/social/seo>>

Run:
1. `launch-strategy` — full plan
2. `marketing-strategy-pmm` — positioning
3. `content-creator` — draft 5 pieces (blog + social + email)
4. `copywriting` — CTAs + subject lines
5. `email-sequence` — 5-touch drip
6. `paid-ads` — 3 ad variants
7. `social-content` — 10 social posts
8. `seo-audit` — landing page check
9. `schema-markup` — structured data

Output: Campaign package พร้อมส่ง review
```

---

## 🔒 Security — Pre-Release Audit

```
Security gate ก่อน release: <<release version>>

Run (MUST PASS):
1. `skill-security-auditor` — scan repo
2. `dependency-auditor` — vulns + licenses
3. `senior-security` — code-level review
4. `red-team` — attack scenarios
5. `security-pen-testing` — pentest plan
6. `ai-security` — if LLM features
7. `observability-designer` — SLO + alert check

Output: Security Sign-off Report
- PASS / WARN / FAIL per check
- Remediation plan for WARN/FAIL
- Blockers for release
```

---

## 📊 Weekly — Metrics Review

```
ทำ weekly metrics review

1. `saas-metrics-coach` — ARR, MRR, churn, LTV, CAC
2. `product-analytics` — DAU/WAU, activation, retention
3. `campaign-analytics` — marketing channel ROI
4. `financial-analyst` — budget variance

สรุปเป็น:
- ✅ On track (green metrics)
- ⚠️ Needs attention (yellow)
- 🚨 Critical (red)
- Top 3 action items สำหรับสัปดาห์หน้า
```

---

## 💼 Sales — Proposal Draft

```
Draft proposal ให้: <<customer name>>
Scope: <<brief>>
Budget: <<THB/USD>>
Timeline: <<weeks>>

Run:
1. `sales-engineer` — technical scoping
2. `contract-and-proposal-writer` — draft proposal
3. `pricing-strategy` — pricing recommendation
4. `competitor-alternatives` — ตอบคำถาม "ทำไมเลือกเรา"

Output: Proposal v1 (PDF-ready)
```

---

## 🎨 Design — Design Review

```
Review design ของ: <<feature/screen>>
Figma: <<url>>

Run:
1. `design:design-critique` — UX/UI critique
2. `apple-hig-expert` — platform guideline check
3. `a11y-audit` — WCAG AA check
4. `ui-design-system` — DS consistency
5. `design:accessibility-review` — deeper a11y

Output: Design review note พร้อม annotations
```

---

## 🧪 Data — Experiment Design

```
ออกแบบ experiment สำหรับ hypothesis:
<<hypothesis>>

Run:
1. `experiment-designer` — test plan
2. `statistical-analyst` — sample size + power
3. `product-analytics` — tracking spec
4. `ab-test-setup` — implementation plan

Output: Experiment Brief
- Hypothesis
- Variants
- Primary + guardrail metrics
- Sample size + duration
- Decision rule
```

---

## 🧘 Friday — Retro

```
Friday retro ของสัปดาห์นี้

อ่าน daily notes 5 วันที่ผ่านมา
Run:
1. `meeting-analyzer` — รวบประเด็นจาก standup
2. `self-eval` — honest team self-assessment
3. `challenge` — ท้าทายสิ่งที่ทำ (constructive)

Output:
- What went well (top 3)
- What didn't (top 3)
- Action items (owner + due)
- Experiments สำหรับสัปดาห์หน้า
```

---

## 📞 Meeting — Instant Summary

```
Meeting transcript:
<<paste transcript>>

Run `meeting-analyzer`

Output:
- TL;DR (3 bullets)
- Decisions made
- Action items (owner + due date)
- Open questions
- Follow-up meeting needed?
```

---

## 🚨 Incident — Response Playbook

```
INCIDENT: <<description>>
Severity: <<P0/P1/P2>>
Started: <<time>>

Run `incident-commander`:
1. Classify severity
2. Assemble response team (tag owners)
3. Comms plan (internal + external if needed)
4. Investigation chain
5. Runbook steps ที่ควรรัน
6. Status update template

Output:
- Incident doc (ช่อง Slack + Obsidian)
- Runbook execution log
- Post-incident review (after resolve)
```

---

## 🗓️ Monthly — Board Prep

```
เตรียม board meeting เดือน <<month>>

Run:
1. `saas-metrics-coach` — metrics snapshot
2. `financial-analyst` — P&L + cash
3. `board-deck-builder` — deck structure
4. `strategic-alignment` — OKR status
5. `scenario-war-room` — risks + opportunities
6. `competitive-intel` — market update

Output: Board deck + talking points + Q&A prep
```

---

## 💡 Custom — New Skill Experimentation

```
ลอง skill ใหม่: <<skill name>>
Context: <<ใช้กับอะไร>>

1. อ่าน SKILL.md ของ skill นี้
2. ลองเรียกใช้กับงานจริง 1 ชิ้น
3. Log:
   - What worked
   - What surprised me
   - Should I adopt? (Y/N)
   - Where does it fit in my playbook?

อัปเดต playbook ตัวเอง + shared team playbook
```

---

## 📋 Check-in Cadence

| Frequency | Template |
|---|---|
| Daily 09:00 | Morning Exec Brief |
| Daily 17:00 | EOD summary (`changelog-generator`) |
| Mon | Weekly Metrics Review |
| Fri | Retro |
| End of sprint | PR Review + Security Audit |
| Monthly | Board Prep |
| On incident | Incident Response |

---

## 🔗 See Also

- [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]
- [[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]
- [[01 - Projects/AI Multi-Agent Workflow/02 - Phase Gate Checklists]]

---
type: reference
created: "2026-04-19"
tags:
  - type/reference
  - topic/ai-workflow
  - topic/gates
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
---

# ✅ Phase Gate Checklists

> Go / No-Go checklist สำหรับข้าม phase
> กฎ: ทุกข้อต้อง **✅** ก่อนข้าม ถ้า **⚠️** ต้อง mitigate, ถ้า **❌** หยุดก่อน

---

## Gate 0 → 1 : Idea → Discovery

**Entry:** มี idea กับ champion
**Exit to Discovery:**

- [ ] **Problem framed** — เขียน problem statement ได้ 1 ประโยค
- [ ] **Target customer** — persona ชัด (อย่างน้อย 1 segment)
- [ ] **Market signal** — มี data > 1 แหล่ง (`competitive-intel`)
- [ ] **Strategic fit** — align กับ OKR (`strategic-alignment`)
- [ ] **Rough ROI** — ballpark (`scenario-war-room` 3 scenarios)
- [ ] **Resource feasibility** — มีคนพอไหม (CEO + CTO sign-off)
- [ ] **Kill criteria defined** — อะไรคือสัญญาณว่าต้องหยุด

**Owner:** CEO
**Artifacts:** Opportunity Brief, 3-scenario analysis

---

## Gate 1 → 2 : Discovery → Design

**Entry:** Discovery kickoff
**Exit to Design:**

- [ ] **User research complete** — ≥ 5 user interviews (`ux-researcher-designer`)
- [ ] **Problem validated** — evidence จากจริง (ไม่ใช่แค่สมมติฐาน)
- [ ] **PRD v1 signed** — BA + Product + CEO
- [ ] **Tech feasibility** — CTO pre-approve stack
- [ ] **Success metrics** — north star + 3 input metrics
- [ ] **Competitive analysis** — top 3 (`competitive-teardown`)
- [ ] **Positioning** — `marketing-strategy-pmm` draft
- [ ] **SEO opportunity** — keyword research done (SEO team)
- [ ] **Legal scan** — PII, compliance pre-check

**Owner:** BA + CTO
**Artifacts:** PRD, User Research Report, Competitive Brief, Keyword Map

---

## Gate 2 → 3 : Design → Build

**Entry:** Design kickoff
**Exit to Build:**

- [ ] **Tech spec** — `senior-architect` + SA signed
- [ ] **API spec** — `api-design-reviewer` pass, OpenAPI doc generated
- [ ] **Data model** — `database-schema-designer` output
- [ ] **Migration plan** — ถ้ามี legacy (`migration-architect`)
- [ ] **CI/CD pipeline** — `ci-cd-pipeline-builder` generated, tested
- [ ] **Design system ready** — component library (`ui-design-system`)
- [ ] **Figma complete** — all key flows
- [ ] **A11y baseline** — `a11y-audit` pass on designs
- [ ] **Security pre-check** — `skill-security-auditor` on proposed stack
- [ ] **Observability plan** — SLO + alert spec (`observability-designer`)
- [ ] **Performance budget** — set (`performance-profiler` targets)

**Owner:** SA + CTO
**Artifacts:** Tech Spec, API Spec, Figma, Security Plan, SLO Doc

---

## Gate 3 → 4 : Build → QA

**Entry:** Feature complete claim
**Exit to QA:**

- [ ] **All PRD features implemented** — BA verification
- [ ] **Unit tests** — coverage ≥ 75%
- [ ] **Integration tests** — all API contracts covered (`api-test-suite-builder`)
- [ ] **E2E tests** — critical paths covered (`playwright-pro`)
- [ ] **Code review** — ทุก PR pass `code-reviewer` + `pr-review-expert`
- [ ] **Security scan** — no critical vulns (`dependency-auditor`)
- [ ] **Bundle size** — ภายใน budget (`performance-profiler`)
- [ ] **Lighthouse** — score ≥ 90 (Performance, A11y, SEO)
- [ ] **Docs** — API reference + user guide
- [ ] **Changelog** — `changelog-generator` generated

**Owner:** Sr BE + Sr FE + CTO
**Artifacts:** Signed feature list, coverage report, perf report

---

## Gate 4 → 5 : QA → Launch

**Entry:** QA cycle start
**Exit to Launch:**

- [ ] **Test suite green** — 100% critical, ≥ 95% important
- [ ] **Security sign-off** — `senior-security` + `ciso-advisor` approval
  - [ ] `skill-security-auditor` PASS
  - [ ] `red-team` simulated attack results reviewed
  - [ ] `security-pen-testing` findings remediated
  - [ ] `ai-security` pass (if LLM features)
- [ ] **Compliance check** — GDPR / SOC2 / ISO พอ (`gdpr-dsgvo-expert` etc.)
- [ ] **Observability live** — dashboards + alerts operational
- [ ] **Runbook ready** — `runbook-generator` output, team trained
- [ ] **Incident playbook** — `incident-commander` template
- [ ] **Rollback tested** — ≤ 10 min to rollback
- [ ] **Release notes** — `release-manager` prepared
- [ ] **Legal sign-off** — ToS / Privacy updated
- [ ] **Pricing confirmed** — `pricing-strategy` + CFO

**Owner:** CTO + QA Lead + Security Guardian
**Artifacts:** Release checklist, SLO dashboard, runbook, rollback plan

---

## Gate 5 → 6 : Launch → Operate

**Entry:** Launch day +7
**Exit to Steady-State Operate:**

- [ ] **First cohort onboarded** — ≥ N customers active
- [ ] **No P0 incidents** in first week
- [ ] **SLO met** — uptime, latency, error rate
- [ ] **Support tickets triaged** — backlog < 24h
- [ ] **Analytics live** — `product-analytics` tracking correct events
- [ ] **CAC/LTV signal** — early data collected (`saas-metrics-coach`)
- [ ] **NPS survey** — sent, first feedback batch
- [ ] **Content engine** — ongoing content pipeline live
- [ ] **Paid channels** — tested at least 1 (`paid-ads`)
- [ ] **SEO** — indexed, `schema-markup` validated
- [ ] **Retro** — launch retro documented

**Owner:** Marketing + CS + CEO
**Artifacts:** Launch retro, first analytics report, customer feedback log

---

## Gate 6 → (Iterate or Sunset)

**Quarterly review:**

- [ ] **Product-market fit signal** — retention > industry benchmark
- [ ] **Unit economics** — CAC payback < 12 months
- [ ] **Rule of 40** — growth + margin ≥ 40
- [ ] **Strategic fit** — still match OKR
- [ ] **Team sustainability** — no burnout signals (`chro-advisor`)

**If yes → continue iterating (loop back to Discovery for next big swing)**
**If no → sunset plan (`change-management` + `incident-commander`)**

---

## 🚦 Gate Rules

> [!warning] Gate Rules
> 1. **ทุก gate ต้อง signed** โดย owner ที่ระบุ (ไม่ใช่ self-approve)
> 2. **Skip ได้แค่ non-critical items** และต้อง log reason + owner accountable
> 3. **Critical miss (security / compliance) = hard stop**
> 4. **Gate review meeting** max 30 นาที ใช้ checklist นี้เป็น agenda
> 5. **ใช้ `decision-logger`** บันทึกทุก gate decision

---

## 📝 Template — Gate Review Note

```markdown
# Gate <X> Review — <Product Name>
Date: <YYYY-MM-DD>
Phase: <From> → <To>

## Checklist Status
- ✅ X passed
- ⚠️ Y with mitigation
- ❌ Z blocked

## Key Risks
- ...

## Decision
[ ] PASS
[ ] CONDITIONAL PASS (owner: <name>, due: <date>)
[ ] FAIL — return to phase

## Signatures
- Owner: <name>
- CTO/CEO: <name>
- Date: ...
```

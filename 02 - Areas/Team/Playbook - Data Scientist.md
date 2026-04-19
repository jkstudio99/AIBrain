---
type: playbook
role: Data Scientist
created: "2026-04-19"
tags:
  - type/playbook
  - role/data
  - role/ds
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — Data Scientist (DS)

> Role: DS — analysis, experiments, models, ML products
> AI counterpart: Data Scientist + Experiment Designer + AI Security chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** Data Scientist
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CTO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Model accuracy / F1 (per use case target)
- Experiment velocity (≥ 2 shipped experiments / month)
- Time-from-hypothesis-to-result < 2 weeks
- Model-in-production uptime ≥ 99%

**Company KPI ที่รับผิดชอบร่วม:**
- Personalization lift (CTR / conversion)
- Churn reduction
- Product engagement metrics

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `data-scientist` | Analysis, model dev |
| 2 | `experiment-designer` | A/B test design, causal inference |
| 3 | `statistical-analyst` | Power analysis, significance tests |
| 4 | `product-analytics` | Funnel, cohort, retention analysis |
| 5 | `ai-security` | LLM + ML security review (bias, leakage) |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Check running experiments (significance? guardrails?)
[ ] Check model drift monitors
[ ] Plan 3 analysis / dev tasks วันนี้
[ ] `data-scientist` — review hypothesis for active experiment
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `experiment-designer` — new test design
- `statistical-analyst` — sample size, power, CI
- `product-analytics` — funnel / cohort deep dive
- `ab-test-setup` — implementation spec for FE/BE
- `ai-security` — bias + privacy review
- `research-summarizer` — literature review
- `decision-logger` — experiment decisions (ship / kill)

### 🌆 EOD (17:00 - 17:30)

```
[ ] Commit notebooks / feature code
[ ] Update experiment tracker
[ ] Log daily findings
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning + hypothesis board | `experiment-designer`, `strategic-alignment` |
| Tue | Analysis + notebook work | `data-scientist`, `product-analytics` |
| Wed | Experiment reviews | `statistical-analyst`, `experiment-designer` |
| Thu | Model dev / ML eng | `data-scientist`, `ai-security` |
| Fri | Retro + publish findings | `research-summarizer`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — Experiment roadmap + hypothesis prioritization
- **Mid-month** — Model drift / bias audit (`ai-security`)
- **Last week** — Publish internal newsletter (top 3 findings)

---

## 🧩 My Orchestration Patterns

### Pattern A — Experiment Design → Ship
**ใช้เมื่อ:** New hypothesis from PM / BA / CEO
**Chain:**
```
1. `experiment-designer` → test plan (hypothesis, metric, variant)
2. `statistical-analyst` → sample size + power + duration
3. `product-analytics` → tracking spec
4. `ab-test-setup` → implementation brief for FE/BE
5. Ship → monitor guardrails
6. Collect sufficient data
7. `statistical-analyst` → analyze with proper CI
8. `decision-logger` → ship / kill / iterate
9. Publish result
```

### Pattern B — Model Development
**ใช้เมื่อ:** New ML feature (rec, classification, forecast)
**Chain:**
```
1. `data-scientist` → problem framing + baseline
2. `product-analytics` → evaluate current state
3. EDA → feature engineering
4. Train / tune / evaluate (offline)
5. `ai-security` → bias + privacy + robustness check
6. Online A/B test (`experiment-designer`)
7. Monitor drift → iterate
8. `observability-designer` → model monitoring spec (with SA + DE)
```

### Pattern C — Post-Launch Root-Cause Analysis
**ใช้เมื่อ:** KPI unexpectedly up/down
**Chain:**
```
1. `product-analytics` → segment + funnel check
2. `statistical-analyst` → is it real or noise?
3. Check confounders (release, holiday, marketing push)
4. `research-summarizer` → synthesize findings
5. `decision-logger` → action (investigate more / adjust)
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **DE** → clean datasets + data catalog
- **BA / Product** → hypotheses, business context
- **Marketing** → attribution + campaign results
- **CEO** → strategic questions (churn, growth levers)

**ส่งงานให้:**
- **BA / Product** → experiment results + recommendations
- **Sr BE / Sr FE** → model deployment spec + integration
- **Marketing** → segmentation + targeting insights
- **CEO** → monthly insight report

**Review กับ:**
- **DE** — data contract sync (weekly)
- **BA** — experiment review (bi-weekly)
- **CTO** — ML infra + `ai-security` review (monthly)

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

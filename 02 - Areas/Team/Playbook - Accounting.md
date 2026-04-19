---
type: playbook
role: Accounting
created: "2026-04-19"
tags:
  - type/playbook
  - role/finance
  - role/accounting
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — บัญชี / Accounting

> Role: บัญชี — close, AR/AP, compliance, pricing support
> AI counterpart: Financial Analyst + CFO Advisor + Contract Writer chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** บัญชี (Accounting / Finance)
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CEO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Monthly close time ≤ 5 business days
- AR > 60 days < 10% of total
- Audit-ready compliance score 100%
- Invoice accuracy ≥ 99.5%

**Company KPI ที่รับผิดชอบร่วม:**
- Gross margin
- Cash runway
- CAC payback period

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `financial-analyst` | Variance analysis, budget vs actual |
| 2 | `cfo-advisor` | Strategic finance decisions |
| 3 | `pricing-strategy` | Product pricing, promo analysis |
| 4 | `contract-and-proposal-writer` | Customer contracts, vendor agreements |
| 5 | `decision-logger` | Finance decisions (write-offs, etc.) |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Check cash position + bank reconciliation
[ ] Review new invoices received
[ ] Check AR aging (any escalations?)
[ ] Plan 3 finance tasks วันนี้
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `financial-analyst` — budget variance, P&L drill-down
- `pricing-strategy` — new deal pricing, discounts
- `contract-and-proposal-writer` — contract review / draft
- `decision-logger` — material finance decisions
- `meeting-analyzer` — after finance-related meetings
- `compliance-checker` / `gdpr-dsgvo-expert` — invoice / tax compliance

### 🌆 EOD (17:00 - 17:30)

```
[ ] Post daily journal entries
[ ] Send invoices / collect overdue
[ ] Update cash + AR aging
[ ] Log finance decisions
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Week kickoff + cash review | `financial-analyst` |
| Tue | AR / collections | `contract-and-proposal-writer` |
| Wed | AP / vendor + approvals | `financial-analyst` |
| Thu | Pricing + sales deal review | `pricing-strategy` |
| Fri | Weekly finance brief to CEO | `cfo-advisor`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — Monthly close + P&L + BS reconciliation
- **Mid-month** — Budget vs actual variance (`financial-analyst`)
- **Last week** — Cash flow forecast + runway update (`cfo-advisor`)

---

## 🧩 My Orchestration Patterns

### Pattern A — Monthly Close
**ใช้เมื่อ:** End of month (target: close in 5 business days)
**Chain:**
```
1. Reconcile all bank + payment gateway accounts
2. Close AR / AP
3. Accruals + prepaid adjustments
4. `financial-analyst` → generate P&L + BS + CF
5. `financial-analyst` → variance analysis (budget vs actual)
6. `cfo-advisor` → narrative for CEO
7. Publish finance pack → CEO review
8. Close period in accounting system
```

### Pattern B — Pricing Review (New Deal / Promo)
**ใช้เมื่อ:** Sales request discount / custom pricing
**Chain:**
```
1. `pricing-strategy` → margin impact + anchor analysis
2. `financial-analyst` → profitability check
3. `decision-logger` → approve / counter / reject
4. `contract-and-proposal-writer` → updated contract terms
5. Notify Sales + CEO (if above threshold)
```

### Pattern C — Cash Runway Update
**ใช้เมื่อ:** Monthly / on significant cash event
**Chain:**
```
1. Actual cash position
2. `financial-analyst` → rolling 13-week forecast
3. `cfo-advisor` → scenario modeling (burn change)
4. `scenario-war-room` → if material — alert CEO + Board
5. `decision-logger` → any action items (hiring freeze, cuts)
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **CEO** → strategic finance questions
- **Marketing** → campaign spend approvals
- **CTO** → infra / vendor cost requests
- **Sales** → deal pricing requests
- **ธุรการ** → expense reports, receipts

**ส่งงานให้:**
- **CEO** → weekly cash brief, monthly P&L
- **Sales** → approved pricing + contracts
- **Board** → quarterly financials (via CEO)
- **External auditor** → audit-ready docs

**Review กับ:**
- **CEO** — weekly finance sync
- **CTO** — monthly infra cost review
- **Board** — quarterly (via CEO)

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

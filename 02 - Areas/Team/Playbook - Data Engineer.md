---
type: playbook
role: Data Engineer
created: "2026-04-19"
tags:
  - type/playbook
  - role/data
  - role/engineering
  - topic/ai-workflow
related:
  - "[[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]"
  - "[[01 - Projects/AI Multi-Agent Workflow/01 - Role Playbook Template]]"
---

# 🎭 Playbook — Data Engineer (DE)

> Role: DE — pipelines, warehouse, data quality, cost
> AI counterpart: Data Engineer + DB Designer + ETL + Data Quality chain

---

## 👤 Identity

- **Name:** <<ชื่อจริง>>
- **Role:** Data Engineer
- **Start date:** <<YYYY-MM-DD>>
- **Manager:** CTO

---

## 🧭 North Star

**Primary KPI (ของตัวเอง):**
- Pipeline uptime ≥ 99.5%
- Data freshness SLA met ≥ 99% of runs
- Cost per TB processed (trending down)
- Data quality score (nulls, duplicates, schema drift) ≥ 98%

**Company KPI ที่รับผิดชอบร่วม:**
- Analytics availability
- Time-to-insight for DS / Marketing
- Compliance (PII handling, retention)

---

## 🎯 Top-5 Skills ที่ใช้ทุกวัน

| Priority | Skill | ใช้ตอนไหน |
|---:|---|---|
| 1 | `data-engineer` | Pipeline design + implementation |
| 2 | `database-schema-designer` | Warehouse schema, OLAP tables |
| 3 | `etl-pipeline-builder` | ETL/ELT jobs |
| 4 | `data-quality-guardian` | QA jobs, drift detection |
| 5 | `observability-designer` | Pipeline monitoring + alerts |

---

## 📅 Daily Rhythm

### 🌅 Morning (09:00 - 10:00)

```
[ ] Check pipeline health (Airflow / dbt / Dagster dashboard)
[ ] Review overnight job failures
[ ] Check data freshness SLAs (missed?)
[ ] Plan 3 data tasks วันนี้
[ ] `data-engineer` — review ticket / incident
```

### 🏃 Core Hours (10:00 - 17:00)

Skills ที่เรียกระหว่างทำงาน:
- `etl-pipeline-builder` — new pipeline or ETL job
- `database-schema-designer` — warehouse schema changes
- `data-quality-guardian` — QA check design
- `observability-designer` — pipeline metrics + alerts
- `performance-profiler` — slow query / job optimization
- `migration-architect` — data migration plans
- `senior-security` — PII handling review

### 🌆 EOD (17:00 - 17:30)

```
[ ] Check overnight job schedule
[ ] Commit dbt models / DAGs
[ ] Log any quality issues for DS / Marketing
[ ] Update daily note
```

---

## 🗓️ Weekly Rhythm

| Day | Event | Skills |
|---|---|---|
| Mon | Sprint planning + data roadmap | `data-engineer` |
| Tue | Deep work — pipeline dev | `etl-pipeline-builder` |
| Wed | Data quality review | `data-quality-guardian` |
| Thu | Cost + perf optimization | `performance-profiler` |
| Fri | Retro + docs | `changelog-generator`, `self-eval` |

---

## 📆 Monthly Rituals

- **1st week** — Warehouse schema audit (`database-schema-designer`)
- **Mid-month** — Cost review (`performance-profiler` — bytes scanned / compute cost)
- **Last week** — Data contract review with DS + Marketing

---

## 🧩 My Orchestration Patterns

### Pattern A — New Data Pipeline
**ใช้เมื่อ:** DS / Marketing request new dataset
**Chain:**
```
1. `data-engineer` → requirements + source evaluation
2. `database-schema-designer` → target table design
3. `etl-pipeline-builder` → extract + transform + load
4. `data-quality-guardian` → QA checks (nulls, dupes, FK)
5. `observability-designer` → SLA alert setup
6. `senior-security` → PII classification + masking
7. Deploy + backfill
8. Document in data catalog
```

### Pattern B — Data Quality Incident
**ใช้เมื่อ:** DS flags bad data / metric drift
**Chain:**
```
1. `data-quality-guardian` → run diagnostics
2. Trace to source (which pipeline, which run)
3. `etl-pipeline-builder` → fix transform logic
4. Backfill affected period
5. Add regression check
6. `incident-commander` → post-mortem if customer-facing
7. `decision-logger` → learning
```

### Pattern C — Cost Optimization
**ใช้เมื่อ:** Monthly cost review shows spike
**Chain:**
```
1. `performance-profiler` → identify top-cost queries / jobs
2. `database-schema-designer` → partition / cluster review
3. Refactor (incremental models, materialization changes)
4. Measure before/after
5. `changelog-generator` → document saving
```

---

## 🤝 Handoff Points

**รับงานจาก:**
- **DS** → feature request, metric definitions
- **Marketing** → attribution + campaign data needs
- **CTO / SA** → architecture guidance
- **Sr BE** → event schema + source system changes

**ส่งงานให้:**
- **DS** → clean datasets + data catalog entries
- **Marketing** → dashboards + marts
- **บัญชี** → finance marts
- **Security** → PII audit logs

**Review กับ:**
- **DS** — weekly data sync
- **SA** — data architecture review (bi-weekly)
- **CTO** — infra + cost review (monthly)

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

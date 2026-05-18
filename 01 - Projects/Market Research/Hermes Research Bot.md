---
type: project
created: 2026-05-04
modified: 2026-05-04
status: in-progress
priority: high
tags:
  - type/project
  - status/growing
  - area/automation
  - topic/market-research
  - hermes/research-bot
related:
  - "[[MOCs/Projects MOC]]"
  - "[[MOCs/Automation MOC]]"
---

# Hermes Research Bot

> Telegram-first market research workflow for `@jayxhermesresearchbot`, using Hermes skills `taiwan-business-research`, `global-business-research`, and `research-bot-help`.

## Bot Commands

### Taiwan research

```text
ไต้หวัน [topic]
รีเสิร์ชไต้หวัน [topic]
taiwan research [topic]
ไต้หวัน quick [topic]
ไต้หวัน deep [topic]
```

### Global research

```text
ตลาดโลก [topic]
global research [topic]
global quick [topic]
global deep [topic]
```

### Compare markets

```text
compare Taiwan Japan Singapore for Lunio Massager
เปรียบเทียบตลาด Taiwan Japan Singapore สำหรับ Lunio
```

### Competitor watch

```text
competitor watch EMMA, Sleep tofu, Derek Bed for Taiwan mattress market
จับตาคู่แข่ง EMMA, Sleep tofu, Derek Bed
```

### Help

```text
research help
วิธีใช้รีเสิร์ช
คำสั่งรีเสิร์ช
/research-help
```

## Priority Competitor Watchlist

Use this list first for sleep / mattress / bedding / wellness research:

1. EMMA / Emma Sleep
2. Sleep tofu / 睡眠豆腐
3. 眠豆腐 / Sleepy Tofu if distinct in local sources
4. Derek Bed / 德瑞克名床
5. IKEA / HOLA / Nitori / Tempur / Sealy / Simmons depending on market
6. Add 1–3 discovered local competitors per report

## Report Template

```markdown
# Market Research: [Topic] in [Market]

## Executive Summary
## Research Scope & Assumptions
## Key Findings
## Market Attractiveness / Scoring
## Competitor Landscape
| Competitor | Product | Price | Channel | Positioning | Strength | Gap | Evidence |
## Customer Segments
## Channel Strategy
## Localization Recommendations
## Market Gaps & Positioning
## 30/60/90-Day GTM Plan
## MVP Experiments
## Risks & Unknowns
## References
```

## Obsidian Save Pattern

Research reports should be saved under this folder:

```text
01 - Projects/Market Research/
```

Suggested filename pattern:

```text
[Topic] - [Market] Research.md
```

Suggested frontmatter:

```yaml
type: literature
created: YYYY-MM-DD
modified: YYYY-MM-DD
status: seedling
tags:
  - type/literature
  - status/seedling
  - topic/market-research
  - hermes/research-bot
market: [Taiwan/Japan/Global/etc]
competitors: [EMMA, Sleep tofu, Derek Bed]
source: Telegram / Hermes Research Bot
related:
  - "[[Hermes Research Bot]]"
```

## Scheduled Digests

- Daily Taiwan Business Brief — business/ecommerce/wellness/AI-health signals.
- Weekly Competitor Watch — EMMA, Sleep tofu, Derek Bed + 2–3 discovered competitors.
- Monthly Opportunity Radar — 5 business opportunities for Thai/wellness brands across Taiwan/Japan/Singapore/UAE.

## Test Prompts

```text
รีเสิร์ชไต้หวัน Lunio Massager premium wellness device
ไต้หวัน deep mattress market focus EMMA, Sleep tofu, Derek Bed
ตลาดโลก compare Taiwan, Japan, Singapore for Lunio Massager deep
competitor watch EMMA, Sleep tofu, Derek Bed for Taiwan mattress market
```

---
type: reference
created: "2026-04-19"
tags:
  - type/reference
  - topic/claude
  - topic/skills
  - topic/community
  - area/automation
related:
  - "[[07 - Prompt Library/Claude Skills Catalog]]"
  - "[[MOCs/Prompt Library MOC]]"
  - "[[MOCs/Automation MOC]]"
source: "https://github.com/alirezarezvani/rock-claude-skills"
aliases:
  - Alireza Skills
  - Community Claude Skills
---

# 🌐 Community Claude Skills — `alirezarezvani/claude-skills`

> 235 production-ready skills + 28 agents + 3 personas + 27 commands — open-source marketplace ใช้งานได้ข้ามเครื่องมือ (Claude Code, Codex, Cursor, Windsurf, Aider ฯลฯ)

**Repo:** <https://github.com/alirezarezvani/claude-skills>
**License:** MIT · **Stars:** 5,200+ · **Version audit:** 2026-04-19

---

## 🚀 Quick Install (Claude Code)

```bash
# 1. เพิ่ม marketplace
/plugin marketplace add alirezarezvani/claude-skills

# 2. ติดตั้งเป็น bundle (แนะนำ)
/plugin install engineering-skills@claude-code-skills           # 24 core engineering
/plugin install engineering-advanced-skills@claude-code-skills   # 25 POWERFUL-tier
/plugin install product-skills@claude-code-skills                # 12 product
/plugin install marketing-skills@claude-code-skills              # 43 marketing
/plugin install ra-qm-skills@claude-code-skills                  # 12 regulatory/quality
/plugin install pm-skills@claude-code-skills                     # 6 project management
/plugin install c-level-skills@claude-code-skills                # 28 C-level advisory
/plugin install business-growth-skills@claude-code-skills        # 4 business & growth
/plugin install finance-skills@claude-code-skills                # 2 finance

# 3. หรือเลือกทีละตัว
/plugin install skill-security-auditor@claude-code-skills
/plugin install playwright-pro@claude-code-skills
/plugin install self-improving-agent@claude-code-skills
```

**Manual clone:**

```bash
git clone https://github.com/alirezarezvani/claude-skills.git ~/repos/claude-skills
# หรือ copy skill เฉพาะตัวไป ~/.claude/skills/
```

---

## 📑 Table of Contents

- [[#⚡ Engineering — POWERFUL (47)|⚡ Engineering — POWERFUL]]
- [[#🛠️ Engineering Team — Core (36)|🛠️ Engineering Team]]
- [[#🎯 Product (16)|🎯 Product]]
- [[#📣 Marketing (43)|📣 Marketing]]
- [[#📋 Project Management (7)|📋 Project Management]]
- [[#🏥 Regulatory & Quality (13)|🏥 Regulatory & Quality]]
- [[#💼 C-Level Advisory (28)|💼 C-Level Advisory]]
- [[#📈 Business & Growth (4)|📈 Business & Growth]]
- [[#💰 Finance (3)|💰 Finance]]
- [[#👤 Personas|👤 Personas]]
- [[#🎯 Quick Pick Decision Tree|🎯 Quick Pick]]

---

## ⚡ Engineering — POWERFUL (47)

> Production-grade เน้น orchestration, pipeline, security, architecture

| Skill | ใช้ทำอะไร |
|---|---|
| `agent-designer` | Multi-agent orchestration, tool schemas, perf evaluation |
| `agent-workflow-designer` | Sequential / parallel / router / orchestrator patterns |
| `agenthub` | Agent registry/hub |
| `api-design-reviewer` | REST linter, breaking-change detector |
| `api-test-suite-builder` | scan routes → generate test suite ครบ |
| `autoresearch-agent` | Research autonomous agent |
| `behuman` | Human-like interaction patterns |
| `browser-automation` | Automate browsers (non-Playwright) |
| `changelog-generator` | Conventional commits → changelog |
| `ci-cd-pipeline-builder` | Stack detector → GitHub Actions / GitLab CI |
| `code-tour` | Guided code walkthrough |
| `codebase-onboarding` | Auto onboarding docs |
| `data-quality-auditor` | Data integrity checks |
| `database-designer` | Schema analyzer, ERD, index optimizer |
| `database-schema-designer` | Requirements → migrations + seed + RLS |
| `demo-video` | Scripted demo video creation |
| `dependency-auditor` | Multi-lang scanner + license + upgrade planner |
| `docker-development` | Dockerfile / Compose patterns |
| `env-secrets-manager` | .env mgmt + leak detection + rotation |
| `focused-fix` | Minimal-scope bug fix workflow |
| `git-worktree-manager` | Parallel dev worktrees + port isolation |
| `helm-chart-builder` | Kubernetes Helm charts |
| `interview-system-designer` | Interview loop + question bank |
| `karpathy-coder` | Karpathy-style pedagogy coding |
| `llm-cost-optimizer` | ลด token cost |
| `llm-wiki` | **Second-brain สำหรับ Obsidian** 🌟 |
| `mcp-server-builder` | OpenAPI → MCP server |
| `migration-architect` | Migration plan + compatibility + rollback |
| `monorepo-navigator` | Turbo/Nx/pnpm workspace mgmt |
| `observability-designer` | SLO + alert + dashboard |
| `performance-profiler` | Node/Python/Go profiling + bundle analysis |
| `pr-review-expert` | Blast radius + security + coverage delta |
| `prompt-governance` | Prompt review & policy |
| `rag-architect` | RAG pipeline + chunking + retrieval eval |
| `release-manager` | Changelog + semver bump + readiness |
| `runbook-generator` | Codebase → ops runbook |
| `secrets-vault-manager` | Secret rotation workflows |
| `self-eval` | Self-evaluation ของ output |
| `skill-security-auditor` | 🔒 สแกนความปลอดภัยของ skill ก่อนติดตั้ง |
| `skill-tester` | Test runner สำหรับ skill |
| `spec-driven-workflow` | Spec-first development |
| `sql-database-assistant` | SQL writing + debugging |
| `statistical-analyst` | Statistical analysis + tests |
| `tc-tracker` | Test case tracker |
| `tech-debt-tracker` | Debt scanner + prioritizer + trend |
| `terraform-patterns` | Infra-as-Code patterns |

---

## 🛠️ Engineering Team — Core (36)

> Team roles, architecture, security

| Skill | ใช้ทำอะไร |
|---|---|
| `a11y-audit` | WCAG accessibility audit |
| `adversarial-reviewer` | โต้แย้งแบบ red-team |
| `ai-security` | AI/ML security review |
| `aws-solution-architect` | AWS architecture |
| `azure-cloud-architect` | Azure architecture |
| `cloud-security` | Cloud security posture |
| `code-reviewer` | General code review |
| `email-template-builder` | HTML email templates |
| `epic-design` | Design epics / stories |
| `gcp-cloud-architect` | GCP architecture |
| `google-workspace-cli` | GWS admin CLI |
| `incident-commander` | Incident response playbook + severity + PIR |
| `incident-response` | IR procedures |
| `ms365-tenant-manager` | M365 tenant admin |
| `playwright-pro` | 🎭 Test gen + flaky fix + migration Cypress/Selenium + 55 templates |
| `red-team` | Red-team assessment |
| `security-pen-testing` | Pentest procedures |
| `self-improving-agent` | 🧠 Auto-memory curation + pattern promotion + skill extraction |
| `senior-architect` | Senior architect decisions |
| `senior-backend` | Senior backend eng |
| `senior-computer-vision` | CV specialist |
| `senior-data-engineer` | Data eng |
| `senior-data-scientist` | Data science |
| `senior-devops` | DevOps senior |
| `senior-frontend` | FE senior |
| `senior-fullstack` | FS senior |
| `senior-ml-engineer` | ML eng senior |
| `senior-prompt-engineer` | Prompt eng senior |
| `senior-qa` | QA senior |
| `senior-secops` | SecOps senior |
| `senior-security` | Security senior |
| `snowflake-development` | Snowflake DW |
| `stripe-integration-expert` | Stripe integration |
| `tdd-guide` | Test-driven workflow |
| `tech-stack-evaluator` | ประเมิน tech stack |
| `threat-detection` | Threat detection |

---

## 🎯 Product (16)

| Skill | ใช้ทำอะไร |
|---|---|
| `agile-product-owner` | Agile PO |
| `apple-hig-expert` | Apple Human Interface Guidelines |
| `code-to-prd` | แปลง code → PRD |
| `competitive-teardown` | คู่แข่งเชิงลึก |
| `experiment-designer` | Experiment design |
| `landing-page-generator` | TSX + Tailwind landing page |
| `product-analytics` | Product analytics |
| `product-discovery` | Discovery workflow |
| `product-manager-toolkit` | PM โทนเจ๊ (RICE prioritizer) |
| `product-strategist` | Strategy |
| `research-summarizer` | Research summary |
| `roadmap-communicator` | Roadmap comms |
| `saas-scaffolder` | SaaS project scaffolding |
| `spec-to-repo` | Spec → new repo |
| `ui-design-system` | Design system |
| `ux-researcher-designer` | UX research |

---

## 📣 Marketing (43)

> 7 pods: Content / SEO / CRO / Channels / Growth / Intelligence / Sales

| Skill | ใช้ทำอะไร |
|---|---|
| `ab-test-setup` | A/B test setup |
| `ad-creative` | Ad creative assets |
| `ai-seo` | AI-optimized SEO |
| `analytics-tracking` | Analytics events + tracking |
| `app-store-optimization` | ASO |
| `brand-guidelines` | Brand rules |
| `campaign-analytics` | Campaign perf |
| `churn-prevention` | ลด churn |
| `cold-email` | Cold outbound |
| `competitor-alternatives` | "alternatives to X" pages |
| `content-creator` | Blog/social content |
| `content-humanizer` | ให้ content ดูเป็นมนุษย์ |
| `content-production` | Pipeline production + brand voice analyzer |
| `content-strategy` | Strategy |
| `copy-editing` | Copy edit |
| `copywriting` | Long-form copy |
| `email-sequence` | Drip sequences |
| `form-cro` | Form conversion |
| `free-tool-strategy` | Free tool leadgen |
| `launch-strategy` | Launch playbook |
| `marketing-context` | Context foundation |
| `marketing-demand-acquisition` | Demand gen |
| `marketing-ideas` | Idea engine |
| `marketing-ops` | MOps |
| `marketing-psychology` | Behavioral marketing |
| `marketing-strategy-pmm` | Product marketing |
| `onboarding-cro` | Onboarding optimization |
| `page-cro` | Landing page CRO |
| `paid-ads` | Paid media |
| `paywall-upgrade-cro` | Paywall optimization |
| `popup-cro` | Popup optimization |
| `pricing-strategy` | Pricing |
| `programmatic-seo` | pSEO |
| `prompt-engineer-toolkit` | Prompt A/B tester + version/diff |
| `referral-program` | Referral loops |
| `schema-markup` | Structured data |
| `seo-audit` | Technical SEO audit |
| `signup-flow-cro` | Signup CRO |
| `site-architecture` | Site IA |
| `social-content` | Social posts |
| `social-media-analyzer` | Social analytics |
| `social-media-manager` | Social mgmt |
| `video-content-strategist` | Video strategy |
| `x-twitter-growth` | X/Twitter growth |

---

## 📋 Project Management (7)

| Skill | ใช้ทำอะไร |
|---|---|
| `atlassian-admin` | Atlassian admin |
| `atlassian-templates` | Templates ready-to-use |
| `confluence-expert` | Confluence docs |
| `jira-expert` | Jira workflows |
| `meeting-analyzer` | Meeting notes analysis |
| `scrum-master` | Scrum ceremonies |
| `senior-pm` | Senior PM |
| `team-communications` | Internal comms |

---

## 🏥 Regulatory & Quality (13)

| Skill | ใช้ทำอะไร |
|---|---|
| `capa-officer` | Corrective & Preventive Action |
| `fda-consultant-specialist` | FDA (510k, PMA) |
| `gdpr-dsgvo-expert` | GDPR / DSGVO |
| `information-security-manager-iso27001` | ISMS |
| `isms-audit-expert` | ISMS audit |
| `mdr-745-specialist` | EU MDR 2017/745 |
| `qms-audit-expert` | QMS audit |
| `quality-documentation-manager` | Quality docs |
| `quality-manager-qmr` | QMR |
| `quality-manager-qms-iso13485` | ISO 13485 |
| `regulatory-affairs-head` | RA leadership |
| `risk-management-specialist` | Risk mgmt (ISO 14971) |
| `soc2-compliance` | SOC2 |

---

## 💼 C-Level Advisory (28)

| Skill | ใช้ทำอะไร |
|---|---|
| `agent-protocol` | Inter-agent protocol |
| `board-deck-builder` | Board deck structure |
| `board-meeting` | Board meeting prep |
| `ceo-advisor` | CEO |
| `cfo-advisor` | CFO |
| `change-management` | OCM |
| `chief-of-staff` | CoS |
| `chro-advisor` | CHRO |
| `ciso-advisor` | CISO |
| `cmo-advisor` | CMO |
| `company-os` | Operating system ของบริษัท |
| `competitive-intel` | Competitive intelligence |
| `context-engine` | Context engine |
| `coo-advisor` | COO |
| `cpo-advisor` | CPO |
| `cro-advisor` | CRO (revenue) |
| `cs-onboard` | Customer success onboard |
| `cto-advisor` | CTO |
| `culture-architect` | Culture design |
| `decision-logger` | Decision records |
| `executive-mentor` | Exec coaching |
| `founder-coach` | Founder coaching |
| `internal-narrative` | Internal story |
| `intl-expansion` | International expansion |
| `ma-playbook` | M&A |
| `org-health-diagnostic` | Org health |
| `scenario-war-room` | Scenario planning |
| `strategic-alignment` | Alignment |

---

## 📈 Business & Growth (4)

| Skill | ใช้ทำอะไร |
|---|---|
| `contract-and-proposal-writer` | Sales contracts + proposals |
| `customer-success-manager` | CS playbook |
| `revenue-operations` | RevOps |
| `sales-engineer` | Sales engineering |

---

## 💰 Finance (3)

| Skill | ใช้ทำอะไร |
|---|---|
| `business-investment-advisor` | Investment advisory |
| `financial-analyst` | DCF, budgeting, forecasting |
| `saas-metrics-coach` | ARR, MRR, churn, LTV, CAC |

---

## 👤 Personas

Pre-configured agent identities + workflows + communication style

| Persona | Domain | Best For |
|---|---|---|
| **Startup CTO** | Engineering + Strategy | Architecture decisions, tech stack, team building, due diligence |
| **Growth Marketer** | Marketing + Growth | Content-led growth, launch, channel optimization |
| **Solo Founder** | Cross-domain | MVP building, solo projects, wearing all hats |

**Install:**
```bash
cp agents/personas/startup-cto.md ~/.claude/agents/
```

---

## 🧩 Orchestration Patterns

| Pattern | เมื่อไหร่ |
|---|---|
| **Solo Sprint** | Switch persona ตาม phase — side projects, MVP |
| **Domain Deep-Dive** | 1 persona + stacked skills — architecture review, compliance audit |
| **Multi-Agent Handoff** | Persona review ซึ่งกันและกัน — high-stakes decisions |
| **Skill Chain** | Sequential skills, ไม่ต้อง persona — content pipeline, checklist |

**ตัวอย่าง 6-week launch:**
```
Week 1-2: startup-cto + aws-solution-architect + senior-frontend → Build
Week 3-4: growth-marketer + launch-strategy + copywriting + seo-audit → Prepare
Week 5-6: solo-founder + email-sequence + analytics-tracking → Ship
```

---

## 🎯 Quick Pick Decision Tree

> [!tip] จะทำอะไร → เรียก skill ไหน?
> - **Architecture review** → `senior-architect` + `senior-backend` + `pr-review-expert`
> - **Launch product** → `launch-strategy` + `copywriting` + `landing-page-generator` + `seo-audit`
> - **Security audit** → `skill-security-auditor` + `ai-security` + `dependency-auditor` + `pr-review-expert`
> - **Build RAG app** → `rag-architect` + `database-schema-designer` + `llm-cost-optimizer`
> - **Compliance audit** → `mdr-745-specialist` / `fda-consultant-specialist` / `gdpr-dsgvo-expert` + `qms-audit-expert`
> - **Board prep** → `board-deck-builder` + `board-meeting` + `cfo-advisor` + `cto-advisor`
> - **Ship CI/CD** → `ci-cd-pipeline-builder` + `dependency-auditor` + `release-manager`
> - **Hiring loop** → `interview-system-designer` + `chro-advisor`
> - **Fix bug minimal scope** → `focused-fix` + `tdd-guide`
> - **Monorepo refactor** → `monorepo-navigator` + `migration-architect`
> - **Content engine** → `content-creator` + `content-humanizer` + `seo-audit` + `schema-markup`
> - **Financial model** → `financial-analyst` + `saas-metrics-coach`
> - **Memory auto-curate** → `self-improving-agent` + `llm-wiki`

---

## 🔒 Security First

ติดตั้ง skill ของคนอื่น **ควร audit ก่อน:**

```bash
python3 engineering/skill-security-auditor/scripts/skill_security_auditor.py /path/to/skill/
```

สแกน: command injection · code exec · data exfil · prompt injection · supply chain · privilege escalation
→ PASS / WARN / FAIL + remediation guide

**Zero dependencies** (stdlib-only)

---

## 🐍 Python Tools (305 CLI scripts)

ทุก script เป็น stdlib-only — ไม่ต้อง `pip install`

```bash
# SaaS health check
python3 finance/saas-metrics-coach/scripts/metrics_calculator.py \
  --mrr 80000 --customers 200 --churned 3 --json

# Brand voice analysis
python3 marketing-skill/content-production/scripts/brand_voice_analyzer.py article.txt

# Tech debt scoring
python3 c-level-advisor/cto-advisor/scripts/tech_debt_analyzer.py /path/to/codebase

# RICE prioritization
python3 product-team/product-manager-toolkit/scripts/rice_prioritizer.py features.csv

# Landing page generator (TSX + Tailwind)
python3 product-team/landing-page-generator/scripts/landing_page_scaffolder.py config.json --format tsx
```

---

## 🔗 Related

- [[07 - Prompt Library/Claude Skills Catalog]] — skills ที่ติดตั้งในระบบจริงแล้ว
- [[MOCs/Prompt Library MOC]]
- [[MOCs/Automation MOC]]

## 🌐 External

- Repo: <https://github.com/alirezarezvani/claude-skills>
- Author: <https://alirezarezvani.com>
- Factory methodology: <https://github.com/alirezarezvani/claude-code-skills-agents-factory>
- Companion toolkit: <https://github.com/alirezarezvani/claude-code-tresor>

---

## 📝 Notes

- **Total skills:** 235 · **Agents:** 28 · **Personas:** 3 · **Commands:** 27
- **License:** MIT → ใช้ฟรี modify ได้
- **Tools รองรับ:** Claude Code, OpenAI Codex, Gemini CLI, OpenClaw, Hermes, Cursor, Aider, Windsurf, Kilo Code, OpenCode, Augment, Antigravity
- **Next action:** ทดลอง `llm-wiki` (second-brain สำหรับ Obsidian) และ `self-improving-agent` (auto memory) ดู

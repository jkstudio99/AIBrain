---
type: reference
created: "2026-04-19"
tags:
  - type/reference
  - topic/claude
  - topic/agents
  - topic/community
  - area/automation
related:
  - "[[07 - Prompt Library/Claude Skills Catalog]]"
  - "[[07 - Prompt Library/Community Skills Catalog — alirezarezvani]]"
  - "[[MOCs/Prompt Library MOC]]"
  - "[[MOCs/Automation MOC]]"
source: "https://github.com/davila7/claude-code-templates"
aliases:
  - AITMPL Catalog
  - Claude Code Templates Agents
---

# 🤖 AITMPL Agents Catalog — `davila7/claude-code-templates`

> Agents 421 ตัวจากเว็บ <https://www.aitmpl.com/agents> — installed **เด่น ๆ 121 ตัวเลือก** ลง `~/.claude/agents/aitmpl/`

**Repo:** <https://github.com/davila7/claude-code-templates>
**Site:** <https://www.aitmpl.com>
**License:** MIT · **Audit:** 2026-04-19
**Installed:** 121 / 421 agents (curated)

---

## 📊 สถานะการติดตั้ง (ตาม category)

| Category | ติดตั้งแล้ว | ของทั้งหมดใน repo |
|---|---:|---:|
| ai-specialists | 6 | 8 |
| business-marketing | 13 | 21 |
| data-ai | 13 | 42 |
| database | 6 | 11 |
| development-team | 10 | 17 |
| devops-infrastructure | 11 | 39 |
| documentation | 5 | 11 |
| expert-advisors | 13 | 52 |
| mcp-dev-team | 8 | 8 (all) |
| **obsidian-ops-team** | **7** | **7 (all)** ⭐ |
| performance-testing | 5 | 5 (all) |
| programming-languages | 12 | 37 |
| security | 7 | 22 |
| ui-analysis | 5 | 5 (all) |
| **TOTAL** | **121** | **421** |

**Path:** `~/.claude/agents/aitmpl/<category>/<agent-name>.md`

---

## 🚀 Quick Install (ส่วนที่ไม่ได้ติดตั้ง)

```bash
# ผ่าน CLI ของ davila7
npx claude-code-templates@latest --agent=<category>/<name>

# หรือ clone + copy เหมือนที่ทำไว้
cd ~/repos/claude-code-templates && git pull
cp cli-tool/components/agents/<category>/<name>.md ~/.claude/agents/aitmpl/<category>/
```

---

## 📑 Table of Contents

- [[#🟣 Obsidian Ops Team|🟣 Obsidian Ops Team]] ⭐ ใช้กับ vault เราตรง ๆ
- [[#🧠 Expert Advisors|🧠 Expert Advisors]]
- [[#🤖 AI Specialists|🤖 AI Specialists]]
- [[#📊 Data / AI|📊 Data / AI]]
- [[#🗄️ Database|🗄️ Database]]
- [[#💻 Development Team|💻 Development Team]]
- [[#⚙️ DevOps & Infrastructure|⚙️ DevOps]]
- [[#🔒 Security|🔒 Security]]
- [[#⚡ Performance & Testing|⚡ Performance & Testing]]
- [[#🖼️ UI Analysis|🖼️ UI Analysis]]
- [[#📚 Documentation|📚 Documentation]]
- [[#💼 Business & Marketing|💼 Business & Marketing]]
- [[#🔌 MCP Dev Team|🔌 MCP Dev Team]]
- [[#💬 Programming Languages|💬 Programming Languages]]
- [[#🎯 Decision Tree|🎯 Decision Tree]]

---

## 🟣 Obsidian Ops Team ⭐

> **7 agents** ที่ออกแบบมาเพื่อ Obsidian vault โดยตรง — ตรงกับงานเรามากที่สุด ใช้แทน/ต่อยอด VaultMaintenance scripts ได้

| Agent | หน้าที่ |
|---|---|
| `vault-optimizer` | Optimize vault structure ทั้งหมด |
| `moc-agent` | สร้าง/อัปเดต Maps of Content |
| `tag-agent` | Normalize tags, จัดลำดับชั้น, ลด duplicate |
| `metadata-agent` | เติม/แก้ YAML frontmatter ให้ครบ |
| `connection-agent` | หา hidden connection ข้ามโน้ต |
| `content-curator` | คัดโน้ตเด่น ๆ ใส่ MOC |
| `review-agent` | Review โน้ต ก่อน promote เป็น evergreen |

**Chain แนะนำ (รายสัปดาห์):**
```
metadata-agent → tag-agent → connection-agent 
  → content-curator → moc-agent → review-agent → vault-optimizer
```

---

## 🧠 Expert Advisors

| Agent | หน้าที่ |
|---|---|
| `agent-organizer` | จัดระเบียบ agents ที่มีอยู่ |
| `architect-review` | Review architecture proposal |
| `context-manager` | จัดการ context window / memory |
| `critical-thinking` | คิดแบบ critical thinker |
| `debug` | Debug bug complex |
| `error-coordinator` | Coordinate error handling strategy |
| `knowledge-synthesizer` | สังเคราะห์ knowledge จาก sources หลาย |
| `mentor` | Mentor-style guidance |
| `multi-agent-coordinator` | Orchestrate หลาย agent |
| `planner` | Plan ก่อน execute |
| `principal-software-engineer` | Senior-most eng perspective |
| `workflow-orchestrator` | Orchestrate end-to-end workflow |
| `task-distributor` | แจกงานให้ agents อื่น ๆ |

---

## 🤖 AI Specialists

| Agent | หน้าที่ |
|---|---|
| `prompt-engineer` | ออกแบบ/ปรับ prompt |
| `llm-architect` | Architecture ของระบบ LLM |
| `ai-ethics-advisor` | Ethics + bias review |
| `task-decomposition-expert` | แตก task เป็น sub-task |
| `search-specialist` | Search strategy (RAG, semantic, hybrid) |
| `model-evaluator` | Evaluate model output |

---

## 📊 Data / AI

| Agent | หน้าที่ |
|---|---|
| `ai-engineer` | AI engineering workflow |
| `data-engineer` | Pipeline + warehouse |
| `data-scientist` | Analysis + modeling |
| `ml-engineer` | ML production |
| `mlops-engineer` | MLOps |
| `computer-vision-engineer` | CV tasks |
| `nlp-engineer` | NLP tasks |
| `prompt-builder` | Build prompt templates |
| `prd` | Product Requirements Doc |
| `task-planner` | Plan ML/data tasks |
| `task-researcher` | Research task-related literature |
| `tdd-red` | TDD "Red" phase (write failing test) |
| `tdd-green` | TDD "Green" phase (make test pass) |

---

## 🗄️ Database

| Agent | หน้าที่ |
|---|---|
| `postgres-pro` | PostgreSQL pro-level |
| `database-architect` | Schema architecture |
| `database-optimizer` | Query + index optimization |
| `supabase-schema-architect` | Supabase specific |
| `nosql-specialist` | Mongo, DynamoDB, Cassandra |
| `neon-expert` | Neon (serverless Postgres) |

---

## 💻 Development Team

| Agent | หน้าที่ |
|---|---|
| `backend-architect` | Backend system architecture |
| `frontend-developer` | FE implementation |
| `fullstack-developer` | FS features |
| `mobile-developer` | Mobile (cross-platform) |
| `ios-developer` | iOS Swift specific |
| `code-architect` | Code-level architecture |
| `test-generator` | Generate tests |
| `test-runner` | Run + analyze tests |
| `ui-ux-designer` | UI/UX design agent |
| `cli-ui-designer` | CLI UX design |

---

## ⚙️ DevOps & Infrastructure

| Agent | หน้าที่ |
|---|---|
| `cloud-architect` | Cloud architecture (AWS/GCP/Azure) |
| `kubernetes-specialist` | K8s expert |
| `terraform-specialist` | IaC with Terraform |
| `sre-engineer` | Site Reliability |
| `deployment-engineer` | Deployment pipelines |
| `incident-responder` | On-call response |
| `network-engineer` | Networking |
| `monitoring-specialist` | Observability stack |
| `platform-engineer` | Platform / DX engineering |
| `devops-engineer` | General DevOps |
| `devops-troubleshooter` | Troubleshoot infra |

---

## 🔒 Security

| Agent | หน้าที่ |
|---|---|
| `security-auditor` | Security audit ทั่วไป |
| `penetration-tester` | Pentest mindset |
| `api-security-audit` | API-specific audit |
| `compliance-auditor` | Compliance framework check |
| `llm-redteam-specialist` | Red-team LLM systems |
| `supply-chain-security` | Dependency / supply-chain |
| `security-engineer` | Security engineering |

---

## ⚡ Performance & Testing

| Agent | หน้าที่ |
|---|---|
| `performance-engineer` | Perf eng ทั่วไป |
| `load-testing-specialist` | Load test design |
| `test-automator` | Automate test pipeline |
| `web-vitals-optimizer` | Core Web Vitals |
| `react-performance-optimization` | React-specific perf |

---

## 🖼️ UI Analysis

> ใช้ screenshot เป็น input แล้ววิเคราะห์

| Agent | หน้าที่ |
|---|---|
| `screenshot-reviewer` | Review screenshot |
| `screenshot-ui-analyzer` | Analyze UI patterns |
| `screenshot-interaction-analyzer` | Analyze interaction flow |
| `screenshot-business-analyzer` | วิเคราะห์ business logic จาก UI |
| `screenshot-synthesizer` | Synthesize design insight |

---

## 📚 Documentation

| Agent | หน้าที่ |
|---|---|
| `api-documenter` | API docs (OpenAPI/ref) |
| `documentation-engineer` | Doc system architecture |
| `technical-writer` | Long-form tech writing |
| `diagram-architect` | Diagrams (Mermaid, etc.) |
| `docusaurus-expert` | Docusaurus sites |

---

## 💼 Business & Marketing

| Agent | หน้าที่ |
|---|---|
| `product-manager` | PM general |
| `business-analyst` | BA |
| `competitive-analyst` | Competitive research |
| `market-researcher` | Market research |
| `content-marketer` | Content marketing |
| `seo-specialist` | SEO (เฉพาะทาง) |
| `ux-researcher` | UX research |
| `scrum-master` | Scrum ceremonies |
| `project-manager` | PM delivery |
| `customer-success-manager` | CS |
| `legal-advisor` | Legal advice (general) |
| `sales-engineer` | SE |
| `trend-analyst` | Trend / forecasting |

---

## 🔌 MCP Dev Team

> ติดตั้งครบ 8 ตัว — สร้าง MCP server ได้ครบ lifecycle

| Agent | หน้าที่ |
|---|---|
| `mcp-server-architect` | Design MCP server |
| `mcp-protocol-specialist` | MCP protocol expert |
| `mcp-developer` | Implement |
| `mcp-integration-engineer` | Integrate MCP with external |
| `mcp-testing-engineer` | Test MCP server |
| `mcp-security-auditor` | Security audit of MCP |
| `mcp-deployment-orchestrator` | Deploy MCP |
| `mcp-registry-navigator` | Browse MCP registry |

**Chain การสร้าง MCP server ใหม่:**
```
mcp-server-architect → mcp-protocol-specialist 
  → mcp-developer → mcp-integration-engineer 
  → mcp-testing-engineer → mcp-security-auditor 
  → mcp-deployment-orchestrator
```

---

## 💬 Programming Languages

| Agent | หน้าที่ |
|---|---|
| `python-pro` | Python |
| `golang-pro` | Go |
| `javascript-pro` | JS general |
| `php-pro` | PHP |
| `react-specialist` | React |
| `nextjs-developer` | Next.js |
| `angular-architect` | Angular |
| `flutter-expert` | Flutter / Dart |
| `kotlin-specialist` | Kotlin |
| `django-developer` | Django |
| `rails-expert` | Ruby on Rails |
| `laravel-specialist` | Laravel |

---

## 🎯 Decision Tree

> [!tip] สถานการณ์ → Agent ที่ควรเรียก
> - **Vault cleanup รายสัปดาห์** → chain ของ Obsidian Ops Team (7 ตัว)
> - **Design new feature** → `principal-software-engineer` + `architect-review` + `planner`
> - **Complex bug** → `debug` + `error-coordinator` + `critical-thinking`
> - **Build MCP server** → chain ของ MCP Dev Team (8 ตัว)
> - **RAG system** → `llm-architect` + `search-specialist` + `ai-engineer`
> - **Performance issue** → `performance-engineer` + `web-vitals-optimizer` + `react-performance-optimization`
> - **Security audit** → `security-auditor` + `api-security-audit` + `supply-chain-security` + `llm-redteam-specialist`
> - **Database slow** → `database-optimizer` + `postgres-pro` |  `neon-expert` |  `supabase-schema-architect`
> - **Plan sprint** → `scrum-master` + `task-distributor` + `task-decomposition-expert`
> - **Review PRD** → `product-manager` + `business-analyst` + `critical-thinking`
> - **Competitive research** → `competitive-analyst` + `market-researcher` + `trend-analyst`
> - **SEO audit** → `seo-specialist` + `web-vitals-optimizer`
> - **K8s deployment** → `kubernetes-specialist` + `platform-engineer` + `deployment-engineer`
> - **Screenshot → insight** → chain ของ UI Analysis (5 ตัว)
> - **Write API doc** → `api-documenter` + `technical-writer` + `diagram-architect`
> - **Orchestrate agents** → `multi-agent-coordinator` + `workflow-orchestrator` + `agent-organizer`

---

## 🔄 เทียบกับชุดอื่นที่ติดตั้งไว้

| Library | Focus | จำนวน | Path |
|---|---|---:|---|
| **Built-in Anthropic/Claude** | Core functionality | ~70 | Built-in |
| **alirezarezvani** | Production skills + personas | 198 | `~/.claude/skills/` |
| **aitmpl (davila7)** | Agents + templates | **121** (installed) | `~/.claude/agents/aitmpl/` |

**เมื่อไหร่ใช้อันไหน?**
- ต้องการ **persona** (ทั้ง personality + mindset) → alirezarezvani
- ต้องการ **agent เฉพาะ domain** → aitmpl
- ต้องการ **core** (obsidian, daily, design) → built-in
- **Obsidian vault ops** → aitmpl `obsidian-ops-team/*` (ตรงกว่า)

---

## 📝 Maintenance

- **Installed:** 2026-04-19
- **Source repo:** `~/repos/claude-code-templates`
- **อัปเดต:**
  ```bash
  cd ~/repos/claude-code-templates && git pull
  # แล้ว re-run install script ใน [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]
  ```
- **Not installed (ตัวเลือกเพิ่ม):**
  - 300 agents อีก — branch `main` ของ repo
  - ดูเพิ่มได้ที่ <https://www.aitmpl.com/agents/>
  - ที่ไม่ได้เลือกมาส่วนใหญ่: .NET-specific (power-bi, dotnet), Azure-specific, non-essential niche

---

## 🔗 External

- Site: <https://www.aitmpl.com/agents/>
- Repo: <https://github.com/davila7/claude-code-templates>
- CLI: `npx claude-code-templates@latest`
- Docs: <https://docs.aitmpl.com>
- DEV article: <https://dev.to/dani_avila7/complete-guide-to-claude-code-templates-1pnp>

## 🔗 Related

- [[07 - Prompt Library/Claude Skills Catalog]]
- [[07 - Prompt Library/Community Skills Catalog — alirezarezvani]]
- [[01 - Projects/AI Multi-Agent Workflow/00 - Blueprint]]
- [[MOCs/Automation MOC]]

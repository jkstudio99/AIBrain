---
type: reference
created: "2026-04-19"
tags:
  - type/reference
  - topic/claude
  - topic/skills
  - area/automation
related:
  - "[[MOCs/Prompt Library MOC]]"
  - "[[MOCs/Automation MOC]]"
aliases:
  - Skills Catalog
  - Claude Skills Reference
---

# 🧰 Claude Skills Catalog

> Reference ของ skills ทั้งหมดที่ติดตั้งอยู่ในระบบ เอาไว้เปิดดูว่าตอนไหนควรเรียกใช้ตัวไหน

**วิธีใช้:** เรียกผ่าน slash command `/skill-name` หรือให้ Claude เลือกใช้อัตโนมัติเมื่อเงื่อนไข trigger เข้าเกณฑ์

---

## 📚 Table of Contents

- [[#🏠 Vault & Knowledge Work|🏠 Vault & Knowledge Work]]
- [[#✍️ Daily Systems|✍️ Daily Systems]]
- [[#🧠 Thinking & Synthesis|🧠 Thinking & Synthesis]]
- [[#🎨 Design|🎨 Design]]
- [[#📋 Operations|📋 Operations]]
- [[#🗣️ Brand Voice|🗣️ Brand Voice]]
- [[#📄 Documents & Spreadsheets|📄 Documents & Spreadsheets]]
- [[#🎭 Creative & Visual|🎭 Creative & Visual]]
- [[#📝 Notion|📝 Notion]]
- [[#🚀 Dev & Infrastructure|🚀 Dev & Infrastructure]]
- [[#⚙️ Claude Code Config|⚙️ Claude Code Config]]
- [[#🤖 Claude API & Scheduling|🤖 Claude API & Scheduling]]
- [[#🔌 Cowork / Plugins|🔌 Cowork / Plugins]]

---

## 🏠 Vault & Knowledge Work

โฟกัสที่จัดการ Obsidian vault โดยตรง

| Skill | คำอธิบาย | ใช้เมื่อ |
|---|---|---|
| `obsidian-markdown` | สร้าง/แก้โน้ตด้วย Obsidian-flavored markdown (callouts, wikilinks, embeds) | เขียนโน้ตใหม่ ต้องการ syntax ที่ Obsidian รองรับครบ |
| `obsidian-bases` | สร้าง/แก้ไฟล์ `.base` (database view) | ทำ dashboard ตารางแบบ Notion ใน Obsidian |
| `obsidian-cli` | ใช้ `obsidian-cli` tool จัดการ vault | batch ops, scripting |
| `json-canvas` | สร้าง/แก้ไฟล์ `.canvas` | ทำ visual knowledge map |
| `defuddle` | ดึง clean markdown จากหน้าเว็บ | save article → literature note |
| `vault-health` | ตรวจสุขภาพ vault ครบจบ | monthly audit |
| `find-connections` | วิเคราะห์โน้ต 7 วันล่าสุด หา hidden link | เจอไอเดียที่ link ข้ามกันได้ |
| `process-inbox` | เคลียร์ `00 - Inbox/` ทีละไฟล์ | เช้าวันจันทร์, หลัง capture เยอะ |
| `create-evergreen` | แปลงโน้ตให้เป็น evergreen | พร้อม promote ความคิด |

---

## ✍️ Daily Systems

| Skill | คำอธิบาย |
|---|---|
| `daily-review` | สร้าง daily reflection ตาม template |
| `weekly-synthesis` | สังเคราะห์ weekly review จาก daily notes |
| `update-memory` | บันทึกบริบท session ลง persistent memory |

---

## 🧠 Thinking & Synthesis

| Skill | คำอธิบาย |
|---|---|
| `synthesize` | รวมโน้ต/ไอเดียหลายอันเป็นชิ้นเดียวที่เชื่อมโยงกัน |
| `challenge` | ท้าทายไอเดียแบบ constructive (devil's advocate) |
| `trace` | วิเคราะห์ไอเดีย step-by-step |
| `reframe` | มองปัญหาจากหลายมุม |
| `brainstorm` | ระดมไอเดียรอบ ๆ หัวข้อ |
| `anthropic-skills:consolidate-memory` | รวบ memory files ที่ซ้ำ/ทับซ้อน |

---

## 🎨 Design

| Skill | คำอธิบาย |
|---|---|
| `design:design-critique` | feedback โครงสร้าง: usability, hierarchy |
| `design:design-system` | audit/build design system |
| `design:design-handoff` | สเป็กส่งต่อ dev จาก design |
| `design:accessibility-review` | WCAG 2.1 AA audit |
| `design:ux-copy` | เขียน/ตรวจ microcopy |
| `design:user-research` | วางแผน + ทำ + สังเคราะห์ user research |
| `design:research-synthesis` | สรุป research → themes, insights |
| `anthropic-skills:web-design-guidelines` | ตรวจ UI code ตาม Web Interface Guidelines |

---

## 📋 Operations

ชุด skill จัดการธุรกิจ/ทีม

| Skill | คำอธิบาย |
|---|---|
| `operations:status-report` | รายงานสถานะพร้อม KPIs / risks |
| `operations:change-request` | CR พร้อม impact analysis |
| `operations:capacity-plan` | แผน capacity ทีม/ทรัพยากร |
| `operations:process-doc` | flowchart + RACI |
| `operations:process-optimization` | วิเคราะห์ + ปรับ process |
| `operations:vendor-review` | ประเมิน vendor: cost + risk |
| `operations:compliance-tracking` | ตาม compliance + audit readiness |
| `operations:runbook` | runbook สำหรับ recurring task |
| `operations:risk-assessment` | identify + mitigate risks |

---

## 🗣️ Brand Voice

| Skill | คำอธิบาย |
|---|---|
| `brand-voice:enforce-voice` | บังคับใช้ guideline กับ content |
| `brand-voice:brand-voice-enforcement` | apply guidelines ลึก |
| `brand-voice:discover-brand` | หา brand materials ในแพลตฟอร์มที่ connect |
| `brand-voice:generate-guidelines` | สร้าง brand voice guidelines |

---

## 📄 Documents & Spreadsheets

| Skill | คำอธิบาย |
|---|---|
| `anthropic-skills:docx` | Word (.docx) |
| `anthropic-skills:pdf` | PDF (อ่าน/สร้าง/แก้) |
| `anthropic-skills:xlsx` | Excel spreadsheet |
| `anthropic-skills:pptx` | PowerPoint |
| `anthropic-skills:doc-coauthoring` | workflow ร่างเอกสารแบบ co-author |

---

## 🎭 Creative & Visual

| Skill | คำอธิบาย |
|---|---|
| `anthropic-skills:algorithmic-art` | p5.js generative art พร้อม seed |
| `anthropic-skills:canvas-design` | งานวิชวลเป็น .png/.pdf |
| `anthropic-skills:slack-gif-creator` | GIF สำหรับ Slack |
| `anthropic-skills:theme-factory` | styling artifacts ตาม theme |
| `anthropic-skills:brand-guidelines` | ใช้สี + typography ของ Anthropic brand |
| `anthropic-skills:web-artifacts-builder` | สร้าง multi-component web artifacts |

---

## 📝 Notion

| Skill | คำอธิบาย |
|---|---|
| `anthropic-skills:notion-knowledge-capture` | เปลี่ยนบทสนทนา → Notion structured |
| `anthropic-skills:notion-spec-to-implementation` | spec → Notion implementation |

---

## 🚀 Dev & Infrastructure

| Skill | คำอธิบาย |
|---|---|
| `anthropic-skills:vercel-deploy` | deploy ขึ้น Vercel |
| `anthropic-skills:vercel-react-best-practices` | React/Next.js perf |
| `anthropic-skills:vercel-composition-patterns` | React composition ที่ scale |
| `anthropic-skills:vercel-react-native-skills` | React Native + Expo best practices |
| `anthropic-skills:supabase-postgres-best-practices` | Postgres perf + best practice |
| `anthropic-skills:mcp-builder` | สร้าง high-quality MCP server |
| `simplify` | review code เพื่อ reuse/quality/efficiency |
| `security-review` | security review ของ pending changes |
| `review` | review pull request |
| `init` | สร้าง `CLAUDE.md` ใหม่ด้วย codebase discovery |

---

## ⚙️ Claude Code Config

| Skill | คำอธิบาย |
|---|---|
| `update-config` | แก้ `settings.json` (hooks, permissions, env) |
| `keybindings-help` | custom keyboard shortcut |
| `less-permission-prompts` | สแกน transcript → เพิ่ม allowlist |
| `anthropic-skills:skill-creator` | สร้าง/แก้ skill ใหม่ |

---

## 🤖 Claude API & Scheduling

| Skill | คำอธิบาย |
|---|---|
| `claude-api` | build/debug/optimize Claude API apps (รวม prompt caching) |
| `schedule` | scheduled remote agents (cron) |
| `anthropic-skills:schedule` | scheduled task บน demand |
| `loop` | รันคำสั่งแบบวนซ้ำ `/loop 5m /foo` |

---

## 🔌 Cowork / Plugins

| Skill | คำอธิบาย |
|---|---|
| `anthropic-skills:setup-cowork` | ติดตั้ง Cowork plugin |
| `cowork-plugin-management:create-cowork-plugin` | สร้าง plugin ใหม่ |
| `cowork-plugin-management:cowork-plugin-customizer` | customize plugin สำหรับ org |
| `anthropic-skills:internal-comms` | ร่าง internal communications |

---

## 🎯 Quick Pick — ควรใช้ skill ไหนตอนไหน?

> [!tip] Decision Tree
> - **โน้ตใหม่** → `obsidian-markdown`
> - **เคลียร์ inbox** → `process-inbox`
> - **เว็บ → Literature note** → `defuddle` + `create-evergreen`
> - **หา insight ข้ามโน้ต** → `find-connections` + `synthesize`
> - **สร้าง dashboard** → `obsidian-bases` หรือ `json-canvas`
> - **ตรวจสุขภาพ vault** → `vault-health` (รายเดือน)
> - **Review code** → `review` + `security-review` + `simplify`
> - **Deploy** → `vercel-deploy`
> - **Spec → Notion** → `anthropic-skills:notion-spec-to-implementation`
> - **ท้าทายไอเดียตัวเอง** → `challenge` + `reframe`

---

## 🔗 Related

- [[MOCs/Prompt Library MOC]]
- [[MOCs/Automation MOC]]
- [[07 - Prompt Library/Note Processing/Note Processing Prompts]]
- [[03 - Resources/Knowledge Workflows/Knowledge Workflows]]

---

## 📝 Maintenance

- **Last audit:** 2026-04-19
- **Total skills:** ~70
- **Source:** Claude Code system reminder (session skills list)
- **Update frequency:** ทุก 2-4 สัปดาห์ หรือเมื่อมี plugin ใหม่

<div align="center">

# 🧠 AI Brain

### *Personal Knowledge Vault — Powered by Obsidian × Claude*

[![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=for-the-badge&logo=obsidian&logoColor=white)](https://obsidian.md)
[![Claude](https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white)](https://claude.ai)
[![PARA](https://img.shields.io/badge/Method-PARA-blue?style=for-the-badge)](https://fortelabs.com/blog/para/)
[![Zettelkasten](https://img.shields.io/badge/Method-Zettelkasten-green?style=for-the-badge)](https://en.wikipedia.org/wiki/Zettelkasten)

[![Notes](https://img.shields.io/badge/Notes-270%2B-orange)](.)
[![Automation](https://img.shields.io/badge/Routines-8-purple)](.)
[![License](https://img.shields.io/badge/License-Personal-lightgrey)](.)

*Second-brain ส่วนตัวที่ผสาน **PARA** + **Zettelkasten** + **AI Automation** เพื่อจัดการความรู้ บันทึกข่าวสาร และสังเคราะห์ความคิดอย่างเป็นระบบ*

</div>

---

## ✨ Highlights

- 🗂️ **โครงสร้าง PARA** — Projects / Areas / Resources / Archive แยกชัดเจน
- 🌱 **Zettelkasten growth** — `seedling → growing → evergreen`
- 🤖 **8 Automated Routines** — ข่าว IT, การเงิน, Portfolio, Vault maintenance ทุกวัน
- 📲 **Telegram + GitHub Sync** — ทุก routine push อัตโนมัติและแจ้งเตือนทันที
- 🔗 **MOCs + Wikilinks** — Knowledge graph เชื่อมโยงทุก note
- 🎨 **Canvas + Excalidraw** — แผนผังความรู้แบบ visual

---

## 📁 Folder Structure

```
AIBrain/
├── 00 - Inbox/             📥 Capture ทุกอย่างที่นี่ก่อน
├── 01 - Projects/          🎯 โปรเจ็กต์ที่มีเป้าหมายชัดเจน
├── 02 - Areas/             🌿 พื้นที่ความรับผิดชอบต่อเนื่อง
├── 03 - Resources/         📚 อ้างอิง / topics ที่สนใจ
├── 04 - Archive/           🗃️ ของที่จบแล้ว / ไม่ใช้แล้ว
├── 05 - Daily Systems/     📅 Daily / Weekly / Monthly notes
│   ├── Daily Notes/        ← Tech / Finance / Company News รายวัน
│   ├── Weekly Reviews/     ← Weekly digest อัตโนมัติ
│   └── Briefings/
├── 06 - Knowledge/         💡 Literature / Evergreen / Research
├── 07 - Prompt Library/    🔮 Prompts, thinking tools, commands
├── 08 - Automation/        ⚙️ Custom skills, scripts, workflows
├── 09 - Visualization/     🗺️ Canvas, knowledge maps, dashboards
├── 10 - Meta/              🧰 Vault health, backup, learning
├── MOCs/                   🧭 Maps of Content (hub notes)
├── Templates/              📄 Note templates
└── Attachments/            🖼️ Images, PDFs, media
```

---

## 🤖 Automated Routines

ทุก routine รันผ่าน **Claude Code Scheduled Tasks** → write Obsidian → git push → Telegram notify

| ⏰ Schedule | 📌 Routine | 📝 Output |
|---|---|---|
| `08:00 ทุกวัน` | **Daily IT News** | สรุปข่าว AI / Cybersecurity / Hardware แบบ deep-dive 2 ไฟล์ |
| `08:30 ทุกวัน` | **Daily Finance Tracker** | SET Index, หุ้นไทย Top 9, ทอง XAU/THB, BTC, ETH |
| `08:45 ทุกวัน` | **Daily Company News** | Figma / Apple / Google / OpenAI / Gemini จาก Google News + Medium |
| `09:00 ทุกวัน` | **Daily News Extended** | Design / Dev / Thai feeds — 10 sources |
| `09:15 จันทร์–ศุกร์` | **Daily Portfolio Tracker** | P/L รายตัว + alert ถ้าเคลื่อนไหว ≥ 5% |
| `08:00 จันทร์` | **Weekly Economic Calendar** | High-impact events จาก Forex Factory |
| `20:00 อาทิตย์` | **Weekly Digest** | สังเคราะห์ note 7 วันย้อนหลัง |
| `22:00 ทุกวัน` | **Nightly Vault Maintenance** | Orphan finder, Auto-MOC, Flashcard export, Home dashboard, Knowledge canvas |

> 📲 ทุก routine ส่งสรุปไปยัง Telegram bot และ commit เข้า repo นี้อัตโนมัติ

---

## 🏷️ Conventions

### YAML Frontmatter
```yaml
---
type: evergreen        # fleeting | literature | evergreen | project | moc | daily
created: "2026-05-07"
tags:
  - type/evergreen
  - status/growing
  - area/ai
related:
  - "[[Some Other Note]]"
source: "url or citation"
---
```

### Tags Hierarchy
| Prefix | Purpose | Examples |
|---|---|---|
| `type/` | ประเภท note | `type/literature`, `type/evergreen`, `type/daily` |
| `status/` | ระดับความสุก | `status/seedling` → `status/growing` → `status/evergreen` |
| `area/` | พื้นที่ความรู้ | `area/ai`, `area/dev`, `area/cybersecurity`, `area/finance` |
| `topic/` | หัวข้อย่อย | `topic/it-news`, `topic/tech-update` |

### Linking
- ใช้ `[[wikilinks]]` เสมอสำหรับ internal references
- ทุก note ต้อง link เข้า MOC ที่เกี่ยวข้อง
- ใช้ `> [!warning]`, `> [!tip]`, `> [!danger]` สำหรับ callouts

---

## 🧭 Key MOCs

| MOC | Purpose |
|---|---|
| [`🏠 Home`](🏠%20Home.md) | Dashboard หลักของ vault |
| `MOCs/Knowledge MOC` | จุดเริ่มต้น knowledge graph |
| `MOCs/Projects MOC` | โปรเจ็กต์ที่ active |
| `MOCs/Daily Systems MOC` | ระบบ daily/weekly/monthly |
| `MOCs/Prompt Library MOC` | รวม prompts และ commands |
| `MOCs/Automation MOC` | Workflows อัตโนมัติ |
| `MOCs/Auto Tag MOC` | สร้างจากสคริปต์ — รวม note ตาม tag (อัปเดตทุกคืน) |

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Tools |
|---|---|
| **Knowledge Base** | Obsidian + Dataview + Templater + Excalidraw |
| **AI Layer** | Claude Code + Claude Agent SDK |
| **Automation** | Python + Bash + Cron (Claude Scheduled Tasks) |
| **Data Sources** | yfinance, CoinGecko, Google News RSS, Medium RSS, Forex Factory |
| **Notifications** | Telegram Bot API |
| **Version Control** | Git + GitHub |

</div>

---

## 📊 Vault Stats

```
📝 Total notes        : 270+
📅 Daily notes        : 80+
🤖 Automated routines : 8
🏷️  Active MOCs       : 7
🌱 Evergreen notes    : growing daily
```

> 📈 Vault Health Trends → `09 - Visualization/Dashboards/Vault Health Trends.html`

---

## 🚀 Getting Started (สำหรับการ fork ใช้เอง)

1. **Clone repo**
   ```bash
   git clone https://github.com/jkstudio99/AIBrain.git
   ```

2. **เปิดใน Obsidian**
   - Open folder as vault → ชี้ไปที่โฟลเดอร์ที่ clone มา
   - ติดตั้ง community plugins: Dataview, Templater, Excalidraw

3. **ตั้งค่า Automation (optional)**
   - ดูสคริปต์ที่ `08 - Automation/Custom Skills/`
   - แก้ Telegram token / chat ID ในแต่ละ `run.sh`
   - สร้าง Claude Scheduled Tasks ตาม [Routines](#-automated-routines) ด้านบน

4. **อ่าน CLAUDE.md**
   - กำหนด conventions ทั้งหมดของ vault สำหรับ Claude

---

## 🎨 Philosophy

> **"Capture everything → Connect deeply → Compound over time"**

- 🌱 เริ่มจาก **fleeting note** → เลี้ยงให้โต → กลายเป็น **evergreen**
- 🔗 ความรู้คือ network ไม่ใช่ folder — **link beats hierarchy**
- 🤖 AI ช่วยสรุป สังเคราะห์ และเชื่อมโยง — แต่ **ความเข้าใจเป็นของเรา**
- ⚙️ Automate งาน routine → ใช้สมองกับงาน **creative**

---

## 📜 License

Personal knowledge vault — content เป็นของส่วนตัว แต่โครงสร้าง / สคริปต์ / template เปิดให้นำไป **fork** และ **adapt** ใช้ส่วนตัวได้

---

<div align="center">

**Built with 🧠 and ☕ by [@jkstudio99](https://github.com/jkstudio99)**

*Powered by Obsidian × Claude × ความขี้เกียจที่ productive*

</div>

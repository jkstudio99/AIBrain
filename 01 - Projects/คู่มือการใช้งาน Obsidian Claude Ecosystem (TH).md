---
type: project
created: "2026-04-16"
status: active
priority: high
tags:
  - type/project
  - area/vault
  - topic/guide
related:
  - "[[MOCs/Obsidian Claude Ecosystem MOC]]"
  - "[[CLAUDE.md]]"
  - "[[🏠 Home]]"
---

# 📖 คู่มือการใช้งาน Obsidian Claude Ecosystem

> คู่มือฉบับสมบูรณ์สำหรับระบบ PKM + AI ที่ขับเคลื่อนด้วย Obsidian และ Claude Code

---

## 🗺️ ภาพรวมระบบ

### สถาปัตยกรรมทั้งหมด

```mermaid
graph TB
    subgraph Foundation["🏗️ Vault Foundation"]
        PARA["PARA Structure\n00-04 Folders"]
        ZK["Zettelkasten\nKnowledge Graph"]
        Templates["Templates\nSystem"]
        Dataview["Metadata &\nDataview"]
    end

    subgraph AI["🤖 Claude AI Layer"]
        CMD["CLAUDE.md\nVault Config"]
        Skills["obsidian-skills\n(kepano)"]
        Commands[".claude/commands\nSlash Commands"]
        Claudian["Claudian Plugin\nIn-Obsidian AI"]
        Memory["Session Memory\nSystem"]
    end

    subgraph Plugins["🔌 Core Plugins"]
        DV["Dataview"]
        TPL["Templater"]
        GIT["Obsidian Git"]
        CAL["Calendar"]
        TASKS["Tasks"]
        EXC["Excalidraw"]
    end

    subgraph Workflows["⚙️ Workflows"]
        Capture["Capture\n00 - Inbox"]
        Process["Process\nClaude Assist"]
        Connect["Connect\nWikilinks + MOCs"]
        Evolve["Evolve\nSeedling → Evergreen"]
    end

    subgraph Output["📊 Outputs"]
        Viz["Visualization\nGraph + Canvas"]
        Daily["Daily Systems\nRoutines + Reviews"]
        Knowledge["Knowledge\nGarden"]
    end

    Foundation --> AI
    AI --> Plugins
    Plugins --> Workflows
    Workflows --> Output
    Output -.->|"Feed back"| Foundation
```

---

## 📂 โครงสร้างโฟลเดอร์ (PARA + Zettelkasten)

### PARA — จัดการตามความเร่งด่วน/เกี่ยวข้อง

```mermaid
graph LR
    subgraph PARA["PARA Methodology"]
        P["01 - Projects\n📋 มี deadline\nมี deliverable"]
        A["02 - Areas\n🔄 ดูแลต่อเนื่อง\nไม่มี deadline"]
        R["03 - Resources\n📚 ข้อมูลอ้างอิง\nสนใจในอนาคต"]
        Ar["04 - Archive\n🗄️ เสร็จแล้ว\nไม่ active"]
    end

    New["Note ใหม่"] --> Q1{"มี deadline\nชัดเจน?"}
    Q1 -->|ใช่| P
    Q1 -->|ไม่ใช่| Q2{"เป็น ongoing\nresponsibility?"}
    Q2 -->|ใช่| A
    Q2 -->|ไม่ใช่| Q3{"เป็น reference\nหรือ topic?"}
    Q3 -->|ใช่| R
    Q3 -->|"เสร็จแล้ว"| Ar
```

### Zettelkasten — สร้าง knowledge graph

```mermaid
graph TB
    Fleeting["💭 Fleeting Note\n00 - Inbox/\nความคิดด่วน"]
    Literature["📖 Literature Note\n06 - Knowledge/Literature Notes/\nสรุปจาก source"]
    Evergreen["🌳 Evergreen Note\n06 - Knowledge/Evergreen Notes/\nIdea อะตอมมิก"]
    MOC["🗺️ MOC\nMOCs/\nHub ของหัวข้อ"]

    Fleeting -->|"Process\n(Claude)"| Literature
    Fleeting -->|"Direct\ninsight"| Evergreen
    Literature -->|"Extract\natoms"| Evergreen
    Evergreen -->|"Cluster\nby topic"| MOC
    MOC -.->|"Navigate\nback"| Evergreen

    style Fleeting fill:#fff3cd
    style Literature fill:#cce5ff
    style Evergreen fill:#d4edda
    style MOC fill:#f8d7da
```

---

## 🤖 Claude Integration — วิธีใช้ AI

### สถาปัตยกรรมการทำงานของ Claude

```mermaid
flowchart TD
    User["👤 คุณ"] --> Interface{"Interface?"}

    Interface -->|"In-Obsidian"| Claudian["Claudian Plugin\nSidebar Chat"]
    Interface -->|"Terminal"| ClaudeCode["Claude Code CLI\n$ claude"]
    Interface -->|"Claude.ai"| Desktop["Claude Desktop\n+ MCP Connection"]

    Claudian --> Context
    ClaudeCode --> Context
    Desktop --> Context

    subgraph Context["📚 Context Loading"]
        CM["CLAUDE.md\nVault Rules"]
        SK["Skills\nobsidian-markdown\nobsidian-bases\njson-canvas\nobsidian-cli\ndefuddle"]
        Cmds["Commands\n/process-inbox\n/daily-review\n/find-connections\netc."]
        Mem["Memory\nActive Context.md\nVault Memory.md"]
    end

    Context --> Actions

    subgraph Actions["⚡ Actions"]
        Read["Read Notes"]
        Write["Write/Edit Notes"]
        Link["Create Wikilinks"]
        Tag["Add Frontmatter"]
        Move["Move Files"]
        Bash["Run Bash\n(Bang mode)"]
    end

    Actions --> Vault["📁 Obsidian Vault"]
```

### Permission Modes ของ Claudian

```mermaid
graph LR
    Normal["🟡 Normal Mode\nถามก่อนเขียน\nถามก่อน bash\nแนะนำสำหรับทั่วไป"]
    Plan["🔵 Plan Mode\nอ่านได้อย่างเดียว\nไม่มี tool calls\nดูก่อนตัดสินใจ"]
    YOLO["🔴 YOLO Mode\nทำทุกอย่างโดยไม่ถาม\nใช้เมื่อมั่นใจ 100%"]

    Normal -->|"ต้องการ explore"| Plan
    Plan -->|"approved แล้ว"| Normal
    Normal -->|"งานรูทีน ไว้ใจได้"| YOLO
    YOLO -->|"ต้องการ review"| Normal
```

---

## ⚡ Slash Commands — คำสั่งทั้งหมด

### คำสั่งหลัก

| Command | ทำอะไร | ใช้เมื่อไหร่ |
|---------|---------|-------------|
| `/process-inbox` | จัดการ note ทุกอย่างใน Inbox | ทุกเช้า หรือเมื่อ inbox เต็ม |
| `/daily-review` | สร้าง reflection สำหรับวันนี้ | ทุกเย็น |
| `/weekly-synthesis` | สร้าง weekly review | ทุกวันอาทิตย์ |
| `/find-connections` | ค้นหา connections ใน notes ล่าสุด | เมื่อ note เยอะ ต้องการ link |
| `/create-evergreen` | แปลง note เป็น evergreen format | เมื่อ idea สุกพอ |
| `/vault-health` | ตรวจสุขภาพ vault | รายสัปดาห์ |
| `/update-memory` | อัปเดต session context | หลังทำงานสำคัญ |

### Thinking Tool Commands

| Command | เทคนิค | ใช้เมื่อ |
|---------|--------|---------|
| `/trace` | วิเคราะห์ step-by-step | ปัญหาซับซ้อน |
| `/challenge` | หา flaw และ assumption | ก่อนตัดสินใจสำคัญ |
| `/reframe` | มองจาก perspective ใหม่ | ติดขัด หรือ tunnel vision |
| `/synthesize` | รวม ideas หลายชิ้น | มี notes หลายตัวที่เกี่ยวกัน |
| `/brainstorm` | generate ideas จำนวนมาก | ต้องการ options |

### Workflow: การใช้ Commands ในชีวิตจริง

```mermaid
sequenceDiagram
    participant You as 👤 คุณ
    participant Inbox as 📥 Inbox
    participant Claude as 🤖 Claude
    participant Vault as 📁 Vault
    participant MOC as 🗺️ MOC

    Note over You,MOC: เช้า — Start of Day
    You->>Inbox: เพิ่ม fleeting notes ตลอดวัน
    You->>Claude: /process-inbox

    Claude->>Inbox: อ่านทุก note
    Claude->>Claude: วิเคราะห์ type + destination
    Claude->>You: เสนอแผน (ถาม approval)
    You->>Claude: Approve ✅

    Claude->>Vault: เพิ่ม frontmatter + ย้ายไปโฟลเดอร์ที่เหมาะ
    Claude->>Vault: เพิ่ม wikilinks ไปยัง related notes
    Claude->>MOC: อัปเดต MOC ที่เกี่ยวข้อง

    Note over You,MOC: เย็น — End of Day
    You->>Claude: /daily-review
    Claude->>Vault: อ่าน daily note + notes วันนี้
    Claude->>You: reflection + insights + next steps

    Note over You,MOC: อาทิตย์ — Weekly
    You->>Claude: /weekly-synthesis
    Claude->>Vault: อ่าน daily notes 7 วัน
    Claude->>Vault: สร้าง Weekly Review note
    Claude->>You: patterns + priorities สัปดาห์หน้า
```

---

## 📝 Template System — เทมเพลตทั้งหมด

```mermaid
graph TD
    NewNote["สร้าง Note ใหม่"] --> TypeQ{"Note ประเภทอะไร?"}

    TypeQ -->|"ความคิดด่วน"| FT["💭 Fleeting Note\nTemplates/Fleeting Note.md"]
    TypeQ -->|"อ่านหนังสือ/บทความ"| LT["📖 Literature Note\nTemplates/Literature Note.md"]
    TypeQ -->|"idea อะตอมมิก"| ET["🌳 Evergreen Note\nTemplates/Evergreen Note.md"]
    TypeQ -->|"โปรเจค"| PT["🎯 Project Note\nTemplates/Project Note.md"]
    TypeQ -->|"area of life"| AT["🔄 Area Note\nTemplates/Area Note.md"]
    TypeQ -->|"บันทึกรายวัน"| DT["📅 Daily Note\nTemplates/Daily Note.md"]
    TypeQ -->|"สรุปรายสัปดาห์"| WT["📊 Weekly Review\nTemplates/Weekly Review.md"]
    TypeQ -->|"สรุปรายเดือน"| MT["📆 Monthly Review\nTemplates/Monthly Review.md"]

    FT & LT & ET & PT & AT & DT & WT & MT --> Frontmatter["เพิ่ม YAML Frontmatter\ntype, created, tags, status"]
    Frontmatter --> Dataview["Dataview queries\nสามารถค้นหาได้"]
```

### Frontmatter ที่ควรใส่ทุก note

```yaml
---
type: fleeting | literature | evergreen | project | area | moc | daily
created: "YYYY-MM-DD"      # วันที่สร้าง (required)
status: seedling | growing | evergreen | active | done
tags:
  - type/[note-type]        # required
  - status/[status]         # required
  - area/[domain]           # optional
  - topic/[subject]         # optional
related: []                 # wikilinks ไปยัง notes ที่เกี่ยวข้อง
---
```

---

## 🌱 Knowledge Garden — วงจรชีวิตของ Note

```mermaid
stateDiagram-v2
    [*] --> Fleeting: 💭 ความคิดใหม่\n(ลงใน Inbox)

    Fleeting --> Literature: 📖 มาจาก\nsource ภายนอก
    Fleeting --> Evergreen: ✨ insight\nชัดเจนทันที
    Fleeting --> Archive: 🗄️ ไม่เกี่ยวข้อง\nแล้ว

    Literature --> Evergreen: 💡 Extract\natom idea
    Literature --> Archive: เก่าเกินไป\nหรือ irrelevant

    Evergreen --> Evergreen: 🔗 เพิ่ม links\nขยายความ
    state Evergreen {
        seedling: 🌱 Seedling\n(แนวคิดเริ่มต้น)
        growing: 🌿 Growing\n(พัฒนาขึ้น มี links)
        mature: 🌳 Evergreen\n(สมบูรณ์ หนาแน่น)
        seedling --> growing: เพิ่มเนื้อหา\n+ connections
        growing --> mature: เสถียรแล้ว\nไม่ค่อยเปลี่ยน
    }

    Evergreen --> MOC: 🗺️ รวบรวมใน\nMap of Content
    MOC --> [*]: ✅ Knowledge\nที่ใช้งานได้
```

### กฎ Evergreen Note ที่ดี

> [!tip] 4 หลักการของ Evergreen Note
> 1. **Atomic** — หนึ่ง note = หนึ่งความคิด
> 2. **Concept-oriented** — ชื่อเป็น statement ไม่ใช่ topic
>    - ❌ "Machine Learning"
>    - ✅ "ML models overfit when training data lacks diversity"
> 3. **Own words** — เขียนด้วยคำพูดตัวเอง ไม่ copy-paste
> 4. **Densely linked** — มีลิงก์ไปยัง notes อื่น ≥ 3 ลิงก์

---

## 📅 Daily Systems — ระบบประจำวัน

```mermaid
graph LR
    subgraph Morning["🌅 เช้า (10 นาที)"]
        M1["เปิด Daily Note"]
        M2["เขียน Morning\nIntention"]
        M3["ตั้ง Top 3\nPriorities"]
        M4["ดู Open Tasks\nจากเมื่อวาน"]
        M1 --> M2 --> M3 --> M4
    end

    subgraph Day["☀️ ระหว่างวัน"]
        D1["Capture → Inbox\n(fleeting notes)"]
        D2["Check off tasks\nที่ทำเสร็จ"]
        D3["เพิ่ม notes\nใหม่ตามงาน"]
        D1 --> D2 --> D3
    end

    subgraph Evening["🌙 เย็น (15 นาที)"]
        E1["/daily-review\n(Claude)"]
        E2["Evening Reflection\n(3 คำถาม)"]
        E3["Link today's notes\nไปยัง MOCs"]
        E1 --> E2 --> E3
    end

    subgraph Weekly["📊 อาทิตย์ (30 นาที)"]
        W1["Review daily notes\n7 วัน"]
        W2["/weekly-synthesis\n(Claude)"]
        W3["Plan next week\npriorities"]
        W1 --> W2 --> W3
    end

    Morning --> Day --> Evening
    Evening -->|"ทุกอาทิตย์"| Weekly
    Weekly -->|"ทุกเดือน"| Monthly["📆 Monthly Review\n(1 ชั่วโมง)"]
```

---

## 🔌 Core Plugins — ปลั๊กอินที่ติดตั้งแล้ว

| Plugin | สถานะ | ใช้ทำอะไร |
|--------|-------|----------|
| **Claudian** | ✅ ติดตั้งแล้ว | Claude AI in-Obsidian |
| **Dataview** | ✅ ติดตั้งแล้ว | Query notes เหมือน database |
| **Templater** | ✅ ติดตั้งแล้ว | Dynamic templates |
| **Calendar** | ✅ ติดตั้งแล้ว | Visual daily note navigation |
| **Obsidian Tasks** | ✅ ติดตั้งแล้ว | Advanced task management |
| **Obsidian Git** | ✅ ติดตั้งแล้ว | Auto git backup |
| **Excalidraw** | ✅ ติดตั้งแล้ว | Hand-drawn diagrams |
| **Icon Folder** | ✅ ติดตั้งแล้ว | Folder icons |
| **Table Editor** | ✅ ติดตั้งแล้ว | Better table editing |

---

## 🕸️ Visualization — ดู knowledge graph

```mermaid
flowchart TD
    VizTool{"อยากดูอะไร?"}

    VizTool -->|"connections\nระหว่าง notes"| Graph["🕸️ Graph View\nF2 หรือ Ribbon icon\nColor-coded by folder"]
    VizTool -->|"visual\nbrainstorm"| Canvas["🎨 Canvas\n.canvas files\nใน 09 - Visualization/"]
    VizTool -->|"diagram\nใน note"| Mermaid["📊 Mermaid\ncode block\nในทุก note"]
    VizTool -->|"hand-drawn\ndiagram"| Excalidraw["✏️ Excalidraw\nEmbedded\nใน Obsidian"]
    VizTool -->|"dashboard\nquery"| Dataview["📋 Dataview\nTABLE / LIST / TASK\nในทุก note"]

    Graph --> GraphTip["💡 Local Graph\nในแต่ละ note\nดู neighborhood"]
    Canvas --> CanvasTip["💡 ใช้ Claude + json-canvas skill\nสร้าง canvas อัตโนมัติ"]
```

---

## 🔧 การ Maintenance — ดูแลรักษา Vault

```mermaid
graph TD
    Start["🏥 Vault Health Check\n(ทุกอาทิตย์)"] --> VH["/vault-health command\n(Claude ทำให้)"]

    VH --> Check1["🔗 Orphan Notes\nไม่มี links เลย"]
    VH --> Check2["⚠️ Missing Frontmatter\nขาด YAML"]
    VH --> Check3["💀 Dead Links\n[[link]] ไปไหนไม่ถึง"]
    VH --> Check4["📥 Inbox Status\nรอ process กี่ items"]
    VH --> Check5["🏷️ Tag Consistency\ntag ซ้ำหรือผิด"]
    VH --> Check6["📊 Stale Notes\nไม่ได้แตะ 30+ วัน"]

    Check1 & Check2 & Check3 & Check4 & Check5 & Check6 --> Report["📋 Health Report\nScore + Recommendations"]
    Report --> Fix["✅ Fix Issues\nตามลำดับ priority"]
```

---

## 🚀 Getting Started — เริ่มต้นใช้งาน

### Checklist เริ่มต้น

- [ ] เปิด Obsidian และ enable Claudian plugin
- [ ] ตั้ง `ANTHROPIC_API_KEY` ใน environment
- [ ] ทดสอบ `/process-inbox` กับ note แรกใน Inbox
- [ ] สร้าง Daily Note วันนี้ด้วย template
- [ ] ลอง `/trace` กับ idea ที่กำลังคิดอยู่
- [ ] เปิด Graph View และดู vault structure
- [ ] อ่าน [[CLAUDE.md]] เพื่อเข้าใจ conventions

---

## 🔗 Quick Links

| หมวด | ลิงก์ |
|------|-------|
| Home Dashboard | [[🏠 Home]] |
| Ecosystem Map | [[MOCs/Obsidian Claude Ecosystem MOC]] |
| Knowledge | [[MOCs/Knowledge MOC]] |
| Projects | [[MOCs/Projects MOC]] |
| Daily Systems | [[MOCs/Daily Systems MOC]] |
| Prompts | [[MOCs/Prompt Library MOC]] |
| Automation | [[MOCs/Automation MOC]] |
| Visualization | [[MOCs/Visualization MOC]] |

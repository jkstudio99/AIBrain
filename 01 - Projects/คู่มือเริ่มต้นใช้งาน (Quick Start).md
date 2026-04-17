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
  - "[[🏠 Home]]"
  - "[[CLAUDE.md]]"
---

# 🚀 คู่มือเริ่มต้นใช้งาน — AI Brain

> อ่านจบใน 10 นาที ใช้งานได้ทันที

---

## Vault นี้คืออะไร?

**AI Brain** คือสมุดบันทึกอัจฉริยะที่รวม 2 สิ่งเข้าด้วยกัน:

1. **Obsidian** — แอปจดบันทึกที่เก็บไฟล์ไว้ในเครื่องเรา (ปลอดภัย ไม่หาย)
2. **Claude AI** — ผู้ช่วย AI ที่อ่าน เขียน จัดการ note ให้เราได้

ผลลัพธ์ = **ระบบจัดการความรู้ส่วนตัว** ที่ AI ช่วยจัดระเบียบ หาความเชื่อมโยง และสร้าง insight ใหม่ๆ ให้

---

## 📂 โฟลเดอร์ — เก็บอะไรที่ไหน?

ง่ายมาก มี 4 ที่หลักๆ:

```
📥 00 - Inbox      → โยนทุกอย่างที่คิดได้ลงตรงนี้ก่อน
📋 01 - Projects   → งานที่มี deadline (เช่น ส่งรายงาน, ทำเว็บ)
🔄 02 - Areas      → สิ่งที่ดูแลตลอด (เช่น สุขภาพ, การเงิน, งาน)
📚 03 - Resources  → ข้อมูลน่ารู้เก็บไว้อ่าน
```

ที่เหลือ:

```
🗄️ 04 - Archive       → เสร็จแล้ว / ไม่ใช้แล้ว
📅 05 - Daily Systems  → บันทึกรายวัน รายสัปดาห์
🧠 06 - Knowledge      → ความรู้ที่สกัดแล้ว (ตัว note ที่ดีที่สุด)
🤖 07 - Prompt Library → คำสั่งสำหรับ AI
⚙️ 08 - Automation     → สคริปต์ ระบบอัตโนมัติ
🎨 09 - Visualization  → แผนภาพ canvas กราฟ
🔧 10 - Meta           → ดูแลรักษา vault
```

> [!tip] กฎง่ายๆ
> **ไม่รู้จะเก็บที่ไหน → โยนลง Inbox ก่อน**
> แล้วค่อยให้ Claude ช่วยจัดทีหลัง

---

## 📝 สร้าง Note — ทำยังไง?

### วิธีที่ 1: สร้างเอง
1. กด `Ctrl+N` (หรือ `Cmd+N` บน Mac)
2. ตั้งชื่อ
3. กด `Ctrl+Shift+T` เลือก template ที่เหมาะ

### วิธีที่ 2: บอก Claude
เปิด Claudian sidebar แล้วพิมพ์:
```
สร้าง literature note เรื่อง "บทความ X ของ Y" ให้หน่อย
```
Claude จะสร้าง note พร้อม template ให้เลย

### Template มีอะไรบ้าง?

| อยากจด... | ใช้ Template | เก็บที่ไหน |
|-----------|-------------|-----------|
| ความคิดแว่บๆ | Fleeting Note | `00 - Inbox/` |
| สรุปหนังสือ/บทความ | Literature Note | `06 - Knowledge/Literature Notes/` |
| ไอเดียสำคัญ (1 note = 1 idea) | Evergreen Note | `06 - Knowledge/Evergreen Notes/` |
| โปรเจค | Project Note | `01 - Projects/` |
| บันทึกรายวัน | Daily Note | `05 - Daily Systems/Daily Notes/` |

---

## 🤖 ใช้ Claude ช่วย — พิมพ์อะไรได้บ้าง?

### เปิด Claude
- **ใน Obsidian**: กด sidebar ขวา → เปิด Claudian
- **ใน Terminal**: พิมพ์ `claude` ตอนอยู่ในโฟลเดอร์ vault

### คำสั่ง (Slash Commands) ที่ใช้บ่อย

#### 📥 จัดการ Inbox
```
/process-inbox
```
Claude จะอ่าน note ทุกอันใน Inbox แล้วเสนอว่าควรย้ายไปไหน ใส่ tag อะไร

#### 🌙 สรุปวันนี้
```
/daily-review
```
Claude อ่าน note วันนี้ แล้วเขียน reflection ให้

#### 🔗 หา connection
```
/find-connections
```
Claude หา note ที่ควรลิงก์ถึงกัน แต่ยังไม่ได้ลิงก์

#### 🌳 แปลงเป็น Evergreen
```
/create-evergreen ชื่อ note
```
Claude แปลง note ธรรมดาให้เป็น Evergreen Note (idea อะตอมมิก)

#### 🏥 เช็คสุขภาพ vault
```
/vault-health
```
Claude ตรวจว่ามี note กำพร้า, link เสีย, หรือ tag ผิดไหม

### Thinking Tools — ให้ Claude ช่วยคิด

| พิมพ์ | Claude จะ... |
|-------|-------------|
| `/trace` | วิเคราะห์ทีละขั้น หา logic chain |
| `/challenge` | หาจุดอ่อน ท้าทาย assumption |
| `/reframe` | มองปัญหาจากมุมใหม่ |
| `/synthesize` | รวม notes หลายอันเป็น insight ใหม่ |
| `/brainstorm` | ระดมไอเดียแบบเยอะๆ |

---

## 📅 กิจวัตร — ทำอะไรเมื่อไหร่?

### ☀️ ทุกเช้า (5 นาที)
1. เปิด Daily Note → กด Calendar sidebar → คลิกวันนี้
2. เขียน 3 สิ่งที่อยากทำวันนี้
3. ดูว่าเมื่อวานมีอะไรค้างไหม

### 🌙 ทุกเย็น (5 นาที)
1. พิมพ์ `/daily-review` ให้ Claude สรุปวันให้
2. ตอบ 3 คำถาม: อะไรดี? อะไรควรปรับ? เรียนรู้อะไร?

### 📊 ทุกอาทิตย์ (15 นาที)
1. พิมพ์ `/weekly-synthesis` → Claude สร้าง Weekly Review
2. ดูว่าสัปดาห์ที่ผ่านมามี pattern อะไร
3. วาง priority สัปดาห์หน้า

### 📆 ทุกเดือน (30 นาที)
1. review project ทั้งหมด — อะไรเสร็จ? อะไรค้าง?
2. ดู Knowledge Garden — มี note อะไรควร upgrade
3. วาง theme เดือนหน้า

---

## 🔗 Wikilink — หัวใจของระบบ

**Wikilink** คือการลิงก์ note ถึงกัน ทำให้เกิด knowledge graph

### วิธีใช้
พิมพ์ `[[` แล้ว Obsidian จะ suggest note:
```markdown
เรื่องนี้เกี่ยวกับ [[ชื่อ note อื่น]]
```

### ทำไมต้อง link?
- ยิ่ง link เยอะ → Graph View ยิ่งสวย → ยิ่งเห็น pattern
- Claude ใช้ link เหล่านี้ในการหา connection ให้เรา
- Note ที่ไม่ link เลย = note กำพร้า (ไม่ค่อยมีประโยชน์)

> [!tip] เป้าหมาย
> **ทุก note ควรมีอย่างน้อย 1 link ไปยัง note อื่น**

---

## 🏷️ Tag — ติดป้ายให้ note

### Tag ที่ใช้ในระบบนี้

| Tag | ความหมาย |
|-----|---------|
| `#type/fleeting` | ความคิดแว่บๆ |
| `#type/literature` | สรุปจาก source |
| `#type/evergreen` | idea ที่สกัดแล้ว |
| `#type/project` | โปรเจค |
| `#type/daily` | บันทึกรายวัน |
| `#status/seedling` 🌱 | เพิ่งเริ่มเขียน |
| `#status/growing` 🌿 | กำลังพัฒนา |
| `#status/evergreen` 🌳 | สมบูรณ์แล้ว |

### ใส่ tag ที่ไหน?
ใส่ใน **frontmatter** ด้านบนสุดของ note:
```yaml
---
type: literature
tags:
  - type/literature
  - status/seedling
---
```

> [!note] ไม่ต้องจำ
> Template ใส่ tag มาให้อยู่แล้ว แค่เลือก template ที่ถูก

---

## 👀 ดู Knowledge Graph

กด **Graph View** (icon รูปจุดเชื่อมกัน ใน sidebar ซ้าย) จะเห็น:
- **จุด** = note แต่ละอัน
- **เส้น** = link ระหว่าง note
- **กลุ่มก้อน** = หัวข้อที่เกี่ยวข้องกัน
- **จุดลอยเดี่ยว** = note กำพร้า (ควร link เพิ่ม)

> [!tip] Local Graph
> เปิด note ไหนก็ได้ → กด `Ctrl+P` → พิมพ์ "local graph"
> จะเห็นเฉพาะ note ที่เชื่อมกับ note นี้

---

## ❓ FAQ — คำถามที่พบบ่อย

### Q: ใช้ Claude ต้องจ่ายเงินไหม?
ต้องมี Anthropic API Key (ดูราคาที่ anthropic.com) หรือใช้ Claude Code ที่รวมมากับ subscription

### Q: Note หายได้ไหม?
ไม่หาย — ไฟล์อยู่ในเครื่อง + backup ด้วย Git ขึ้น GitHub อัตโนมัติ

### Q: Inbox เต็มมากไม่อยากจัดเอง
พิมพ์ `/process-inbox` แล้ว Claude จัดให้ แค่กด approve

### Q: อยากเขียน note แต่ไม่รู้จะใช้ template ไหน
ใช้ **Fleeting Note** เสมอ → แล้วค่อย upgrade ทีหลัง

### Q: ทำไมต้อง Evergreen Note?
เพราะมันคือ **ความรู้ที่ใช้ซ้ำได้** — เขียนดีครั้งเดียว ใช้ได้ตลอด เหมือนสร้าง building block ของความคิด

---

## 🗺️ แผนที่ระบบทั้งหมด

```
คุณ
├── เช้า → เปิด Daily Note
├── ระหว่างวัน → จดลง Inbox
├── เย็น → /daily-review
├── อาทิตย์ → /weekly-synthesis
│
├── อยากจัดระเบียบ → /process-inbox
├── อยากหาความเชื่อมโยง → /find-connections
├── อยากวิเคราะห์ → /trace หรือ /challenge
├── อยากสร้าง idea → /brainstorm
│
└── ทุกอย่างเก็บอยู่ใน vault
    ├── 🏠 Home.md (หน้าหลัก)
    ├── MOCs/ (แผนที่ของแต่ละหัวข้อ)
    └── Graph View (ดูภาพรวมทั้งหมด)
```

---

## ✅ เช็คลิสต์เริ่มต้น

- [ ] เปิด Obsidian → เปิด vault "AI Brain"
- [ ] ไปที่ Settings → Community Plugins → เปิด **Claudian**
- [ ] ตั้ง API Key (ถ้ายังไม่ได้ตั้ง)
- [ ] เปิด [[🏠 Home]] → ดูหน้า dashboard
- [ ] สร้าง Daily Note วันนี้ (กด Calendar → คลิกวันนี้)
- [ ] เขียนอะไรสักอย่างลงใน `00 - Inbox/`
- [ ] ลอง `/process-inbox` ดูว่า Claude จัดยังไง
- [ ] เปิด Graph View ดู vault ของเรา

> [!success] แค่นี้ก็เริ่มได้แล้ว!
> ไม่ต้องเข้าใจทุกอย่างตั้งแต่วันแรก ค่อยๆ เรียนรู้ไปเรื่อยๆ
> ระบบออกแบบมาให้ **เริ่มง่าย แล้วค่อยซับซ้อนขึ้นเอง**

---

## 🔗 อ่านเพิ่มเติม
- [[01 - Projects/คู่มือการใช้งาน Obsidian Claude Ecosystem (TH)]] — คู่มือฉบับเต็ม (มี Mermaid diagrams)
- [[MOCs/Obsidian Claude Ecosystem MOC]] — แผนที่ระบบทั้งหมด
- [[03 - Resources/Claude Integration/Claude Code Desktop Setup]] — ตั้งค่า Claude
- [[03 - Resources/Knowledge Workflows/Capture Process Connect]] — workflow จดบันทึก

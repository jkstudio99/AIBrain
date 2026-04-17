---
type: daily
created: "2026-04-17"
tags:
  - type/daily
  - topic/tech-update
  - area/ai
  - area/dev
  - area/cybersecurity
related:
  - "[[05 - Daily Systems/Daily Notes/2026-04-17]]"
  - "[[05 - Daily Systems/Daily Notes/IT News 2026-04-17]]"
  - "[[05 - Daily Systems/Daily Notes/Tech Update 2026-04-16]]"
  - "[[MOCs/Knowledge MOC]]"
---

# 📡 สรุปข่าวเทคโนโลยี — 17 เมษายน 2026

> รวบรวมจากแหล่งข่าวทั่วโลก อัปเดตวันนี้

---

## 🔥 ข่าวเด่นประจำวัน

### 1. White House เตรียมให้ Federal Agencies เข้าถึง Anthropic Mythos — แม้ Pentagon ประกาศว่าเป็น "supply chain threat"

> [!warning] ข่าวใหญ่ด้านนโยบาย AI และความมั่นคง
> Gregory Barbaccia, Federal CIO ของ White House OMB แจ้ง Cabinet departments ว่ากำลังตั้ง "protections" เพื่อให้หน่วยงานรัฐบาลกลางเริ่มใช้ **Claude Mythos** ได้ในอีกไม่กี่สัปดาห์

**หน่วยงานที่ถูกแจ้ง:**
- Department of Defense
- Treasury
- Commerce
- Homeland Security
- Justice
- State

**บริบทที่ขัดแย้ง:**
- **Pentagon** ประกาศให้ Anthropic เป็น "supply chain threat" ต้นปี 2026
- White House กำลังเดินหน้าต่อ **แม้มีการคัดค้านจาก DoD**
- ยังไม่มีกำหนดเวลาชัดเจน — แต่สัญญาณชัดว่า AI ระดับ dangerous กำลังเข้าสู่รัฐบาล

> **ทำไมสำคัญ**: ครั้งแรกที่รัฐบาลสหรัฐกำลังจะให้หน่วยงานความมั่นคงชั้นนำใช้ model ที่บริษัทผู้สร้างเองยังไม่กล้าปล่อยให้สาธารณะ

---

### 2. Amazon เข้าซื้อ Globalstar $11.57B — และจับมือ Apple ในดีลดาวเทียม

> [!note] Big Tech สงครามอวกาศ vs Starlink รอบใหม่
> Amazon ประกาศเข้าซื้อ **Globalstar** มูลค่า **$11.57 พันล้าน** ($90/หุ้น) เพื่อขยาย **Amazon Leo** LEO satellite network

**รายละเอียด:**
- Globalstar มีดาวเทียม LEO + spectrum + direct-to-device (D2D) expertise
- Amazon Leo จะได้รับบริการ D2D เต็มรูปแบบ
- **Apple เข้าร่วมดีลด้วย** — Amazon Leo จะ power satellite services สำหรับ **iPhone 14+** และ **Apple Watch Ultra 3**
  - รวมถึง Emergency SOS via satellite, location sharing, texting
- ดีลคาดว่าปิดปี **2027** รอ regulatory approval

**เป้าหมายชัดเจน: ท้าทาย Starlink (SpaceX) ของ Elon Musk**
- Amazon + Apple vs. Elon Musk ในสนามอวกาศ

---

### 3. Snap ปลด 1,000 คน (16%) — เพราะ AI เขียนโค้ดแทนแล้ว 65%

> [!note] สัญญาณ AI Replacement Wave ใหม่ใน Tech
> CEO Evan Spiegel ส่ง memo แจ้งพนักงานว่า Snap กำลังตัดพนักงาน **1,000 คน** หรือ **16%** ของพนักงานทั้งหมด (5,261 คน ณ ธ.ค. 2025)

**เหตุผลที่น่าสังเกตมาก:**
- **AI เขียนโค้ดแทน 65%** ของโค้ดใหม่ทั้งหมดของ Snap แล้ว
- Spiegel เรียกนี้ว่า **"Crucible Moment"** — จุดเปลี่ยนสำคัญของบริษัท
- ปิด open positions อีก 300+ ตำแหน่ง

**ผลทางการเงิน:**
- ลดต้นทุน **$500M+** ต่อปี ภายใน H2 2026
- Restructuring costs: $95M–$130M ใน Q2
- **หุ้น Snap พุ่งขึ้น** หลังประกาศ — ตลาดมองว่าเป็นข่าวดีสำหรับ profitability

> **บทเรียน**: "AI ทำให้ทีมเล็กลงทำงานได้มากขึ้น" — ไม่ใช่แค่ theory อีกต่อไป

---

### 4. Broadcom ขยายดีลชิปกับ Google และ Anthropic

- **Broadcom** ลงนามขยายสัญญาผลิตชิป AI รุ่นใหม่กับ **Google** และ **Anthropic**
- Anthropic ได้รับ access คอมพิวต์ **~3.5 gigawatts** จาก Google AI processors
- นี่คือ infrastructure deal ระดับ gigawatt แรกในวงการ AI

---

### 5. AI กับ Cybersecurity — สัปดาห์ที่ตึงเครียด

| เหตุการณ์ | ผลกระทบ |
|-----------|---------|
| White House เตรียมให้รัฐบาลใช้ Mythos | ทั้ง DoD / DHS ต้องรับมือ model cyber-capable ระดับสูงสุด |
| CVE-2026-33825 Microsoft Defender zero-day | Privilege escalation to SYSTEM — คนที่ใช้ Windows ทุกคนต้องแพตช์ |
| Operation PowerOFF ปิด 53 DDoS domains | หยุดบริการที่มีลูกค้า 75,000 cybercriminals |
| Sweden เปิดเผย Russia โจมตี power plant | Critical infrastructure attacks ระดับ destructive เริ่มแล้ว |

---

## 🔐 Cybersecurity Deep Dive

### Microsoft Patch Tuesday — เพิ่มเติมจากเมื่อวาน

Microsoft แพตช์ **167 ช่องโหว่** รวมถึง **2 zero-days**:

| CVE | ผลกระทบ | สถานะ |
|-----|---------|-------|
| **CVE-2026-32201** | SharePoint — spoofing, data exposure | ⚠️ กำลังถูก exploit |
| **CVE-2026-33825** | Microsoft Defender — escalate to SYSTEM | ⚠️ กำลังถูก exploit |

> [!danger] อัปเดตด่วน
> **CVE-2026-33825** อันตรายมาก — Microsoft Defender ที่ควรป้องกันระบบ กลับกลายเป็นช่องโหว่เอง ถ้ายังไม่ได้ patch ต้องทำทันที

### Operation PowerOFF — ชัยชนะของ Law Enforcement
- ปฏิบัติการระดับนานาชาติ
- ปิด **53 domains** ที่ให้บริการ DDoS-for-hire
- จับกุม **4 คน**
- มีลูกค้าใช้บริการมากกว่า **75,000 cybercriminals** ทั่วโลก

### CYFIRMA Weekly Threats ประจำสัปดาห์
- **APT28 (Russia)**: มุ่งเน้น identity-focused intrusions + obfuscated infrastructure — เป้าหมาย: รัฐบาลและองค์กรกลยุทธ์
- **Gentlemen Ransomware**: Dual-extortion (ขโมยข้อมูล + encrypt) + cross-platform — กำลัง active ทั่วโลก
- **AZORult Malware**: Malware of the week — stealer ที่ขโมย credentials, browser data, crypto wallets

---

## 📊 Market & Business

### Tech Stocks — วันนี้ขึ้นแรง
> Iran peace deal rumors สร้าง risk-on rally ทั่วตลาด

| หุ้น | เปลี่ยนแปลง |
|------|------------|
| Dow Jones Futures | +538 pts (+1.10%) |
| Verizon | +3.86% → $46.78 |
| Cisco | +3.25% → $84.50 |
| IBM | +2.94% → $251.00 |
| IonQ (quantum) | +18% |
| D-Wave (quantum) | +16% |

### Quantum Computing — เริ่มมีสัญญาณเชิงพาณิชย์
- **IonQ** พุ่ง 18% หลังขยาย commercial systems ข้ามหลาย processor
- **D-Wave** พุ่ง 16% — quantum annealing กำลัง commercial scale

### Semiconductor Global Sales
- **Feb 2026**: $88.8B — สูงขึ้น 7.6% จาก Jan และ **+61.8% YoY** จาก Feb 2025
- อุตสาหกรรมกำลังเดิน track ไปสู่ **~$1T/ปี**

---

## 💡 Key Takeaways & Potential Evergreen Notes

> [!tip] Insights จากข่าววันนี้

1. **AI เข้าสู่รัฐบาลสหรัฐ** — White House จะให้ DoD/DHS ใช้ Mythos แม้ Pentagon คัดค้าน → precedent ด้านนโยบาย AI ระดับรัฐ
2. **AI Replacement ไม่ใช่ fear — มันเกิดแล้ว** — Snap: 65% ของโค้ดเขียนโดย AI, ตัดพนักงาน 16%
3. **Space Internet War** — Amazon ($11.57B Globalstar + Apple) vs. Starlink เริ่ม scale ทั้ง 2 ฝั่ง
4. **Microsoft Defender เป็น attack surface** — ซอฟต์แวร์ป้องกันกลายเป็นช่องโหว่ critical
5. **Quantum computing เริ่มเป็น commercial reality** — IonQ +18%, D-Wave +16% ในวันเดียว

### Potential Evergreen Notes
- [ ] [[White House vs Pentagon — ความขัดแย้งในการใช้ AI ระดับ dangerous ในรัฐบาลสหรัฐ]]
- [ ] [[AI Replacement Wave — เมื่อ AI เขียนโค้ด 65% การลดพนักงานจึงตามมาโดยธรรมชาติ]]
- [ ] [[Amazon Leo vs Starlink — สงครามดาวเทียม LEO รอบใหม่]]
- [ ] [[Security software as attack vector — เมื่อเครื่องมือป้องกันกลายเป็นช่องโหว่]]

---

## 📎 Sources

### AI & Policy
- [White House Works to Give US Agencies Anthropic Mythos AI — Bloomberg](https://www.bloomberg.com/news/articles/2026-04-16/white-house-moves-to-give-us-agencies-anthropic-mythos-access)
- [Trump officials negotiating access to Anthropic's Mythos — Axios](https://www.axios.com/2026/04/16/white-house-anthropic-ai-mythos-government-national-security)
- [White House grants agencies access to Anthropic's Mythos AI — CryptoBriefing](https://cryptobriefing.com/white-house-grants-agencies-access-to-anthropics-mythos-ai-despite-pentagon/)
- [Broadcom agrees to expanded chip deals with Google, Anthropic — CNBC](https://www.cnbc.com/2026/04/06/broadcom-agrees-to-expanded-chip-deals-with-google-anthropic.html)
- [AI Updates Today April 2026 — LLM Stats](https://llm-stats.com/llm-updates)

### Business & Layoffs
- [Snap is cutting 1000 jobs, 16% of its workforce — TechCrunch](https://techcrunch.com/2026/04/15/snap-is-cutting-1000-jobs-16-of-its-workforce/)
- [Snap lays off 1,000 employees as AI takes over 65% of coding — Tech Startups](https://techstartups.com/2026/04/15/snap-lays-off-1000-employees-or-16-of-workforce-as-ai-takes-over-65-of-coding-work/)
- [Snap's stock jumps on plans to axe 16% of workforce — CNBC](https://www.cnbc.com/2026/04/15/snap-stock-layoffs-16-percent-workforce.html)

### Satellite & Space
- [Amazon to buy Globalstar for $11.57B — TechCrunch](https://techcrunch.com/2026/04/14/amazon-to-buy-globalstar-for-11-57b-in-bid-to-flesh-out-its-satellite-biz/)
- [Amazon and Apple vs. Starlink — GeekWire](https://www.geekwire.com/2026/amazon-and-apple-vs-starlink-globalstar-satellite-acquisition-comes-with-a-big-iphone-bonus/)
- [Apple and Amazon Ink Satellite Deal — MacRumors](https://www.macrumors.com/2026/04/14/apple-and-amazon-ink-satellite-deal-globalstar/)

### Cybersecurity
- [Cyber News Roundup April 17 2026 — Integrity360](https://www.integrity360.com/cyber-news-roundup-april-17th-2026)
- [Weekly Intelligence Report 17 April 2026 — CYFIRMA](https://www.cyfirma.com/news/weekly-intelligence-report-17-april-2026/)
- [Operation PowerOFF — SecurityWeek](https://www.securityweek.com/)

### Markets
- [AMD Stock Eyeing $300 on TSMC Boost — FX Leaders](https://www.fxleaders.com/news/2026/04/16/amd-stock-eyeing-300-as-chip-momentum-builds-on-tsmc-boost/)

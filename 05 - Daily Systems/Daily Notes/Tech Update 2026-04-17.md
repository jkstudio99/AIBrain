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
  - "[[MOCs/Knowledge MOC]]"
---

# 📡 สรุปข่าวเทคโนโลยี — 17 เมษายน 2026

> รวบรวมจากแหล่งข่าวทั่วโลก อัปเดตวันนี้

---

## 🔥 ข่าวเด่นประจำวัน

### 1. Amazon เข้าซื้อ Globalstar มูลค่า $11.57 พันล้าน — เตรียมชน SpaceX Starlink

Amazon ประกาศเข้าซื้อกิจการ **Globalstar** บริษัทดาวเทียมสัญชาติอเมริกัน ในมูลค่าประมาณ **$11.57 พันล้านดอลลาร์** การเข้าซื้อครั้งนี้จะทำให้ Amazon สามารถขยาย Project Kuiper ไปสู่เครือข่ายอินเทอร์เน็ตความเร็วสูงจากอวกาศ และแข่งขันโดยตรงกับ **SpaceX Starlink** ที่ครองตลาด Low Earth Orbit (LEO) internet อยู่

**สาระสำคัญ:**
- Amazon จะรวม Globalstar เข้ากับโครงสร้างพื้นฐานดาวเทียม Project Kuiper
- ผู้ใช้จะได้รับบริการอินเทอร์เน็ตดาวเทียมผ่าน Amazon ecosystem
- การแข่งขัน LEO internet ระหว่าง Amazon vs Starlink จะดุเดือดขึ้น

**ทำไมถึงสำคัญ:** Starlink ครองส่วนแบ่งตลาดอย่างล้นหลาม การมีคู่แข่งระดับ Amazon จะกดราคาและขยายการเข้าถึงในพื้นที่ห่างไกลทั่วโลก

---

### 2. Anthropic Mythos — AI Model ที่ถูกล็อกก่อนปล่อยสู่สาธารณะ

Anthropic ชะลอการปล่อยโมเดล **Claude Mythos** หลังพบ **ช่องโหว่ความปลอดภัยระดับ high-severity หลายพัน รายการ** ระหว่างกระบวนการ safety evaluation ขณะที่ **JPMorgan Chase CEO Jamie Dimon** เปิดเผยว่าธนาคารกำลังทดสอบ Mythos ผ่าน enterprise beta

**สิ่งที่เกิดขึ้น:**
- Mythos แสดงความสามารถสูงผิดปกติจนทีม Red Team ตรวจพบความเสี่ยงระดับสูง
- Anthropic ตัดสินใจระงับการปล่อยโมเดลและเพิ่ม safety measures
- JPMorgan Chase กำลังทดสอบ Mythos ผ่านช่องทาง enterprise beta

**ทำไมถึงสำคัญ:** นี่คือตัวอย่าง responsible AI deployment ที่เลือก safety เหนือ time-to-market — สะท้อนว่า frontier models กำลังใกล้ขีดจำกัดที่ผู้พัฒนาเองยังกังวล

---

### 3. OpenAI + Anthropic + Google รวมพลัง — ตั้ง AI Defense Pact สกัด China

บริษัท AI ชั้นนำทั้งสามแชร์ข้อมูลกันผ่าน **Frontier Model Forum** เพื่อป้องกัน Chinese AI companies จากการ copy โมเดลผ่านวิธี **adversarial distillation** โดย Anthropic เพียงรายเดียวบันทึกว่ามีการแลกเปลี่ยนข้อมูลโดยไม่ได้รับอนุญาตถึง **16 ล้านครั้ง** จากบริษัทจีน 3 ราย

**รายละเอียด:**
- Frontier Model Forum เป็น mechanism แชร์ threat intelligence ระหว่างคู่แข่ง
- DeepSeek ถูกกล่าวหาว่าใช้ distillation จาก OpenAI models มาพัฒนา technology ของตน
- รัฐบาลหลายแห่ง (Texas, Germany) แบน DeepSeek บนอุปกรณ์ราชการ

---

### 4. Microsoft Patch Tuesday เมษายน 2026 — 167 ช่องโหว่ รวม SharePoint Zero-Day

Microsoft ปล่อยอัปเดตความปลอดภัยประจำเดือนเมษายน ครอบคลุม **167 ช่องโหว่** รวมถึง **2 zero-day** และ **8 รายการ Critical** ช่องโหว่ที่น่ากังวลที่สุดคือ **CVE-2026-32201** ใน SharePoint Server ซึ่งกำลังถูกโจมตีอยู่ในขณะนี้

**ช่องโหว่สำคัญ:**
- **CVE-2026-32201** — SharePoint Server spoofing, actively exploited ในโลกจริง
- 20 Remote Code Execution vulnerabilities
- Majority: Elevation of Privilege bugs

> [!danger] แพทช์ด่วน — CVE-2026-32201 Actively Exploited
> องค์กรทุกแห่งที่ใช้ SharePoint Server ต้องอัปเดตทันที ไม่รอ maintenance window

---

### 5. Quantum Computing Surge — World Quantum Day ผลักดัน D-Wave และ IonQ พุ่ง

วันที่ 14 เมษายน (World Quantum Day) เป็นตัวเร่งให้ตลาดตอบรับ quantum computing เชิงบวก โดย **D-Wave** พุ่ง ~16% และ **IonQ** พุ่ง 18% หลังประกาศขยายระบบ commercial quantum ออกไปเกินกว่า single processor

---

## 🔐 Cybersecurity Highlights

| เหตุการณ์ | บริษัท/หน่วยงาน | ผลกระทบ |
|-----------|-----------------|---------|
| CVE-2026-32201 SharePoint Zero-Day | Microsoft | Actively exploited — ต้องแพทช์ด่วน |
| Cisco 4 Critical Patches | Cisco | Identity Services + Webex SSO vulnerability |
| Basic-Fit Data Breach | Basic-Fit (EU) | ข้อมูลสมาชิก ~1 ล้านคน (NL, FR, ES) รั่วไหล |
| Zerion Hot Wallet Theft | Zerion (Crypto) | $100K ถูกขโมยจาก internal hot wallets |
| Operation PowerOFF | Interpol / Law Enforcement | ปิด 53 โดเมน DDoS, จับ 4 คน, บล็อก 75,000 cybercriminal users |
| NIST NVD Policy Change | NIST | จำกัดการ enrich CVEs เพื่อจัดการ volume ที่เพิ่มขึ้น |

> [!warning] Basic-Fit Breach
> หากคุณหรือองค์กรใช้ Basic-Fit gym ในยุโรป ให้ตรวจสอบว่าข้อมูลส่วนตัวถูก expose หรือไม่

---

## 📊 ภาพรวมอุตสาหกรรม

**AI Economics:**
- OpenAI แตะ Annualized Revenue $25 พันล้านดอลลาร์ กำลังพิจารณา IPO ปลายปี 2026
- Anthropic Revenue Run Rate แตะ $30 พันล้านดอลลาร์
- Broadcom จะส่ง 3.5 GW ของ Google TPU capacity ให้ Anthropic ในปี 2027 (บน 1 GW ที่กำหนดไว้แล้วปี 2026)
- OpenAI กำลังปิดตัว Sora วันที่ 26 เมษายน 2026 — user count ลดต่ำกว่า 500,000, ค่า compute $1M/วัน

**Semiconductor:**
- ยอดขาย semiconductor โลก กุมภาพันธ์ 2026: **$88.8 พันล้าน** (+7.6% MoM, +61.8% YoY)
- AMD เข้าใกล้ $300/หุ้น จากความต้องการ AI hardware และดีลพันธมิตรกับฝรั่งเศส
- China เร่งแผน semiconductor self-sufficiency ตาม five-year plan — ผลักดันเงินลงทุนมหาศาลสู่ domestic chip industry

**Venture Capital:**
- Q1 2026: นักลงทุนทั่วโลกลงทุน $300 พันล้านดอลลาร์ใน 6,000 startups — สถิติสูงสุดเท่าที่เคยมี
- OpenAI ($122B), Anthropic ($30B), xAI ($20B), Waymo ($16B) รวมกัน $188 พันล้าน

---

## 💡 Key Takeaways & Potential Evergreen Notes

1. **Amazon-Globalstar** เปลี่ยนเกม LEO Internet — ตลาดดาวเทียมจะไม่ใช่ monopoly ของ Starlink อีกต่อไป
2. **Anthropic Mythos** คือตัวอย่างแรก ๆ ที่บริษัท AI ล็อกโมเดลของตัวเองก่อนปล่อย — safety-first culture กำลังกลายเป็น norm
3. **Frontier Model Forum** ทำให้คู่แข่งกลายเป็นพันธมิตรในด้าน security — IP protection ใน AI era ต้องการ cooperation ระหว่างคู่แข่ง
4. **Microsoft 167-vuln patch** ยืนยันว่า patch cadence ของ enterprise ยังไม่พอรับมือกับ volume ช่องโหว่ที่เพิ่มขึ้นทุกเดือน
5. **Q1 2026 $300B VC** — AI boom ขับเคลื่อน venture market สู่ระดับที่ไม่เคยเห็นมาก่อน — bubble หรือ fundamental shift?

**Potential Evergreen Notes:**
- [ ] "Adversarial Distillation — วิธีที่ China Copy AI Models"
- [ ] "LEO Internet Wars — Amazon vs Starlink"
- [ ] "Responsible AI Deployment — เมื่อ Safety มาก่อน Speed-to-Market"
- [ ] "Frontier Model Forum — ความร่วมมือในโลก AI Competition"

---

## 📎 Sources

**AI & Tech:**
- [LLM Stats — AI Model Updates April 2026](https://llm-stats.com/llm-updates)
- [OpenAI, Anthropic, Google Form AI Defense Pact Against China](https://www.humai.blog/openai-anthropic-and-google-just-formed-an-ai-defense-pact-the-enemy-isnt-each-other/)
- [Stanford AI Index 2026 — IEEE Spectrum](https://spectrum.ieee.org/state-of-ai-index-2026)
- [MIT Technology Review — State of AI 2026](https://www.technologyreview.com/2026/04/13/1135675/want-to-understand-the-current-state-of-ai-check-out-these-charts/)
- [Yahoo Finance — Tech Stocks: Anthropic Claude Opus 4.7](https://finance.yahoo.com/sectors/technology/article/tech-stocks-today-big-tech-stocks-point-to-strong-open-ai-industry-seeks-to-allay-fears-144220399.html)

**Cybersecurity:**
- [Integrity360 — Cyber News Roundup April 17, 2026](https://www.integrity360.com/cyber-news-roundup-april-17th-2026)
- [SecurityWeek — Microsoft Patches SharePoint Zero-Day and 167 Vulnerabilities](https://www.securityweek.com/microsoft-patches-exploited-sharepoint-zero-day-and-160-other-vulnerabilities/)
- [The Hacker News](https://thehackernews.com/)
- [CISA Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)

**Market & Funding:**
- [Crunchbase — Q1 2026 Record Venture Funding $300B](https://news.crunchbase.com/venture/record-breaking-funding-ai-global-q1-2026/)
- [TechStartups — Zum raises $100M at $1.7B valuation](https://techstartups.com/2026/04/16/zum-raises-100m-from-tpg-at-1-7b-valuation-to-fix-americas-broken-school-transportation-system/)

**Semiconductor:**
- [AMD Stock Eyeing $300 — FX Leaders](https://www.fxleaders.com/news/2026/04/16/amd-stock-eyeing-300-as-chip-momentum-builds-on-tsmc-boost/)
- [China Tech Self-Sufficiency Drive — TNGlobal](https://technode.global/2026/04/17/china-tech-self-sufficiency-drive-to-boost-semiconductor-supply-chain-sp/)
- [Semiconductors in 2026 — Medium](https://medium.com/@adnanmasood/semiconductors-in-2026-the-ai-driven-upswing-meets-structural-bottlenecks-3568b004905b)

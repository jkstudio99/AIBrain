---
type: daily
created: "2026-05-04"
tags:
  - type/daily
  - topic/tech-update
  - area/ai
  - area/dev
  - area/cybersecurity
related:
  - "[[05 - Daily Systems/Daily Notes/2026-05-04]]"
  - "[[05 - Daily Systems/Daily Notes/IT News 2026-05-04]]"
  - "[[MOCs/Knowledge MOC]]"
---

# 📡 สรุปข่าวเทคโนโลยี — 4 พฤษภาคม 2026

## 🔥 ข่าวเด่นประจำวัน

### 1. Apple และ Microsoft รายงานผลประกอบการ Q2 2026 — AI เป็นตัวขับเคลื่อนหลัก

Apple รายงานรายได้ไตรมาส Q2 FY2026 อยู่ที่ **$111.2 พันล้าน** (+17% YoY) โดย iPhone ทำรายได้ $56.99 พันล้าน และธุรกิจ Services สร้างสถิติใหม่ที่เกือบ **$31 พันล้าน** (+16%) พร้อมประกาศ buyback หุ้นอีก $100 พันล้าน ผลลัพธ์ดีกว่าที่ Wall Street คาดการณ์ไว้

Microsoft รายงานรายได้ **$82.9 พันล้าน** EPS $4.27 โดย **Azure เติบโต 40%** แต่หุ้นร่วงเพราะ capex พุ่งขึ้น 49% ไปที่ $31.9 พันล้าน ซึ่งนักลงทุนกังวลเรื่องต้นทุนโครงสร้างพื้นฐาน AI

**ทำไมถึงสำคัญ:** ทั้งสองบริษัทยืนยันว่าการลงทุน AI infrastructure ยังคงเพิ่มขึ้นต่อเนื่อง แม้จะกดดันกำไรระยะสั้น แต่ตลาดยังเชื่อมั่นในการเติบโตระยะยาว

---

### 2. OpenAI เปิดตัว GPT-5.5 — DeepSeek ปล่อย V4 แข่ง

**OpenAI** เปิดตัว **GPT-5.5** เมื่อ 24 เมษายน 2026 โดยบอกว่าเป็นโมเดลที่ "ฉลาดและเป็นธรรมชาติที่สุด" โดดเด่นในด้าน agentic coding, computer use, งานด้านความรู้ และการวิจัยวิทยาศาสตร์

**DeepSeek** ปล่อย **V4 Flash** และ **V4 Pro** เป็น preview model พร้อม context window ยาว ราคาต่ำ และเป็น open-weight ทำให้แข่งขันกับโมเดลจาก OpenAI, Anthropic และ Google ได้โดยตรง

**Anthropic** เพิ่ม **Opus 4.7** — โมเดลที่เน้น literal, controllable และลดความเสี่ยง โดยมี Claude Mythos ในการทดสอบภายใน

**ทำไมถึงสำคัญ:** การแข่งขัน AI model รุนแรงขึ้น ทั้ง open-weight และ closed model ต่างผลักดันประสิทธิภาพในราคาที่ต่ำลง

---

### 3. KKR ระดมทุน $10+ พันล้าน สร้าง AI Infrastructure บริษัทใหม่

**KKR & Co.** ระดมทุนได้กว่า **$10 พันล้าน** เพื่อเปิดตัว **Helix Digital Infrastructure** บริษัทใหม่ที่จะออกแบบ สร้าง เป็นเจ้าของ และดำเนินงาน AI infrastructure เฉพาะทาง ครอบคลุม data centers, การผลิตพลังงาน, สายส่ง และการเชื่อมต่อ

**ทำไมถึงสำคัญ:** Private equity เริ่มลงทุนในโครงสร้างพื้นฐาน AI โดยตรง ไม่ใช่แค่ซอฟต์แวร์ — แสดงว่า AI infrastructure กลายเป็นสินทรัพย์ระยะยาวที่นักลงทุนสถาบันสนใจ

---

### 4. Meta ลงทุน $145 พันล้าน — ซื้อกิจการ Assured Robotics Intelligence

**Meta** ประกาศแผนใช้จ่าย **$145 พันล้าน** เป็น capex ปีนี้ เพื่อขยาย AI computing capacity และได้เข้าซื้อกิจการ **Assured Robotics Intelligence** เพื่อเร่งการพัฒนา humanoid robots

**ทำไมถึงสำคัญ:** Meta กำลังเปลี่ยนตัวเองจาก social media ไปสู่ AI + robotics อย่างชัดเจน การเข้าซื้อ robotics company เป็นสัญญาณว่า AI embodied intelligence เป็นเดิมพันระยะยาว

---

### 5. OpenAI, Anthropic และ Google ร่วมมือต่อต้าน Model Distillation จากจีน

OpenAI, Anthropic และ Google กล่าวหา DeepSeek ว่าดึงความสามารถออกมาโดยผิดกฎหมาย (adversarial distillation) ทั้งสามบริษัทเริ่มแชร์ข้อมูลผ่าน **Frontier Model Forum** เพื่อตรวจจับและป้องกันการ distillation จากคู่แข่งจีน

**ทำไมถึงสำคัญ:** Intellectual property protection ในโลก AI กลายเป็นประเด็นสำคัญระดับภูมิรัฐศาสตร์ ไม่ใช่แค่ทางธุรกิจ

---

## 🔐 Cybersecurity Highlights

| เหตุการณ์ | CVE / ผู้โจมตี | ผลกระทบ | ความรุนแรง |
|---|---|---|---|
| Linux LPE ทุก major distro | CVE-2026-31431 | Red Hat, SUSE, Ubuntu, AWS Linux | CVSS 7.8 (High) |
| SharePoint Zero-Day RCE | CVE-2026-32201 | Exploit อยู่ใน wild | Critical |
| Itron data breach | ไม่ระบุ | ระบบ corporate IT ถูก compromise | High |
| Medtronic breach (ShinyHunters) | ShinyHunters group | ข้อมูลล้านรายการ exposed | High |
| Trellix source code breach | ไม่ระบุ | source code ส่วนหนึ่งถูก access | Medium |
| Roblox account hijacking | กลุ่มแฮ็กเกอร์ยูเครน | 610,000 accounts ถูกขาย $225,000 | Medium |

> [!danger] CVE-2026-31431 — Linux Privilege Escalation
> Exploit ทำงานแบบ deterministic (ไม่ต้องอาศัย race condition) และสามารถ implement ได้ด้วย script ขนาด ~732 bytes ส่งผลต่อทุก major Linux distribution ควร patch ทันที

> [!warning] CVE-2026-32201 — SharePoint Zero-Day RCE
> กำลังถูกใช้โจมตีจริงในปัจจุบัน (actively exploited) องค์กรที่ใช้ Microsoft SharePoint ควรอัปเดตด่วน

**CISA KEV Updates:** CISA เพิ่ม 8 ช่องโหว่ที่ถูกใช้โจมตีแล้วใน Known Exploited Vulnerabilities catalog พร้อมกำหนด federal deadline เดือนเมษายน–พฤษภาคม 2026

---

## 📊 ภาพรวมอุตสาหกรรม

### AI Economics & Policy

- **Pentagon** ทำข้อตกลงกับ SpaceX, OpenAI, Google, Microsoft, Nvidia, Amazon Web Services และ Reflection หลังจากเปิดการเจรจากับ Anthropic ใหม่อีกครั้ง (Anthropic เคยถูก blacklist เพราะต้องการ safety guardrails ใน military AI)
- ตลาด AI infrastructure เติบโตแบบ parabolic — การลงทุน capex รวมของ Big Tech ในปี 2026 น่าจะเกิน $400 พันล้าน
- Stanford AI Index 2026 ยืนยันว่า AI กำลังเปลี่ยนโฉมทุกอุตสาหกรรม

### Semiconductor Trends

- อุตสาหกรรม semiconductor กำลังมุ่งสู่ยอดขาย **~$1 ล้านล้าน/ปี** โดย AI accelerators และ memory เป็นตัวขับเคลื่อน
- **HBM (High Bandwidth Memory)** เข้าสู่ super-cycle — ซัพพลายเออร์ให้ความสำคัญกับ HBM สำหรับ AI servers ทำให้ conventional DRAM ราคาสูงขึ้น
- Packaging bottleneck (CoWoS, 2.5D/3D integration) ยังคงเป็นข้อจำกัดหลัก
- **On Semiconductor** ถูก B. Riley upgrade เป็น Buy ก่อน Q1 2026 results (price target $115 จาก $64)

### Startup Funding Landscape

- ทุนยังไหลไปยัง AI, fintech infrastructure, space, deeptech และ industrial software
- **Parallel Web Systems** (Parag Agrawal) รับ $100M จาก Sequoia มูลค่า $2B
- **Hightouch** รับ $150M Series D (agentic AI marketing)
- **Avoca** รับ $125M Series B (AI customer communication)

---

## 💡 Key Takeaways & Potential Evergreen Notes

**5 สิ่งสำคัญจากวันนี้:**

1. **AI Infrastructure เป็น "สินทรัพย์ใหม่"** — KKR ลงทุน $10B+ ใน AI infra บริษัทเฉพาะทาง บ่งชี้ว่า data center + power เป็น asset class ระยะยาว
2. **Model competition เร็วขึ้นมาก** — GPT-5.5, DeepSeek V4, Opus 4.7 ออกมาภายในสัปดาห์เดียวกัน แสดงถึงจังหวะการแข่งขันที่เร่งขึ้น
3. **Linux privilege escalation ไม่ใช่เรื่องเล็กน้อย** — CVE-2026-31431 กระทบทุก major distro และ exploit ง่ายมาก ต้องรีบ patch
4. **Healthcare + Industrial เป็นเป้าหมาย cyber ใหม่** — Medtronic และ Itron ถูกโจมตี OT/IT convergence เป็นความเสี่ยงระดับประเทศ
5. **AI Geopolitics ทวีความรุนแรง** — การร่วมมือ OpenAI+Anthropic+Google ต่อต้าน Chinese distillation และเรื่อง Pentagon สะท้อนว่า AI กลายเป็น national security asset

**Potential Evergreen Notes:**
- [ ] [[AI Infrastructure as Asset Class — KKR Helix Case Study]]
- [ ] [[Model Distillation Ethics and Legal Framework 2026]]
- [ ] [[CVE-2026-31431 Linux LPE Analysis]]
- [ ] [[AI in Military: Pentagon AI Deals and Safety Guardrails]]
- [ ] [[HBM Super-Cycle and Semiconductor Packaging Bottleneck]]
- [ ] [[Healthcare Cybersecurity: Medtronic ShinyHunters Case]]

---

## 📎 Sources

**Big Tech Earnings:**
- [Apple Q2 2026 Earnings — Bloomberg Technology](https://www.bloomberg.com/technology)
- [Microsoft Azure 40% Growth — CNBC Technology](https://www.cnbc.com/technology/)

**AI Models:**
- [LLM News Today May 2026 — llm-stats.com](https://llm-stats.com/ai-news)
- [AI Updates Today May 2026 — llm-stats.com](https://llm-stats.com/llm-updates)
- [DeepSeek V4 drops new model — CNN Business](https://edition.cnn.com/2026/04/24/tech/chinas-ai-deepseek-v4-intl-hnk)
- [OpenAI, Anthropic, Google Unite Against China Model Copying — Bloomberg](https://www.bloomberg.com/news/articles/2026-04-06/openai-anthropic-google-unite-to-combat-model-copying-in-china)
- [New AI Model Releases May 2026 — mean.ceo blog](https://blog.mean.ceo/new-ai-model-releases-news-may-2026/)

**Pentagon / Policy:**
- [Pentagon strikes deals with 7 Big Tech companies — CNN Business](https://www.cnn.com/2026/05/01/tech/pentagon-ai-anthropic)
- [Stanford AI Index 2026 — IEEE Spectrum](https://spectrum.ieee.org/state-of-ai-index-2026)

**AI Infrastructure:**
- [KKR Helix Digital Infrastructure — TechCrunch](https://techcrunch.com/)
- [Meta $145B capex + Robotics — Bloomberg Technology](https://www.bloomberg.com/technology)

**Cybersecurity:**
- [CVE-2026-31431 Linux LPE — Microsoft Security Blog](https://www.microsoft.com/en-us/security/blog/2026/05/01/cve-2026-31431-copy-fail-vulnerability-enables-linux-root-privilege-escalation/)
- [May 2026 Data Breaches — SharkStriker](https://sharkstriker.com/blog/may-2026-data-breaches/)
- [CISA KEV 8 Exploited Flaws — The Hacker News](https://thehackernews.com/2026/04/cisa-adds-8-exploited-flaws-to-kev-sets.html)
- [Supply Chain Attacks May 2026 — eSecurity Planet](https://www.esecurityplanet.com/weekly-roundup/supply-chain-attacks-ai-security-and-major-breaches-define-this-week-in-cybersecurity-in-may-2026/)

**Semiconductors:**
- [On Semiconductor B. Riley Upgrade — 24/7 Wall St.](https://247wallst.com/investing/2026/04/23/b-riley-just-upgraded-on-semiconductor-to-buy-and-nearly-doubled-its-price-target-is-this-the-chip-comeback-of-2026/)
- [Semiconductors in 2026 AI-Driven Upswing — Medium](https://medium.com/@adnanmasood/semiconductors-in-2026-the-ai-driven-upswing-meets-structural-bottlenecks-3568b004905b)
- [Key Trends Shaping Semiconductor Industry 2026 — Edge AI Vision](https://www.edge-ai-vision.com/2026/04/key-trends-shaping-the-semiconductor-industry-in-2026/)

**Startup Funding:**
- [Startup Funding News May 2026 — mean.ceo blog](https://blog.mean.ceo/startup-funding-news-may-2026/)
- [Week's 10 Biggest Funding Rounds — Crunchbase](https://news.crunchbase.com/venture/biggest-funding-rounds-defense-aerospace-ai-fintech/)
- [Legora Series D Nvidia-Led — Crunchbase](https://news.crunchbase.com/venture/ai-powered-legal-tech-startup-legora-seriesd-extension-nvidia/)

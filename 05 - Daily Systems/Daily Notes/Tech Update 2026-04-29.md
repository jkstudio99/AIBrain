---
type: daily
created: "2026-04-29"
tags:
  - type/daily
  - topic/tech-update
  - area/ai
  - area/dev
  - area/cybersecurity
related:
  - "[[05 - Daily Systems/Daily Notes/2026-04-29]]"
  - "[[05 - Daily Systems/Daily Notes/IT News 2026-04-29]]"
  - "[[MOCs/Knowledge MOC]]"
---

# 📡 สรุปข่าวเทคโนโลยี — 29 เมษายน 2026

## 🔥 ข่าวเด่นประจำวัน

### 1. Google ลงทุน $40B ใน Anthropic — ดีลใหญ่แห่งปี AI

Google ประกาศลงทุนสูงสุด $40 พันล้านใน Anthropic โดยเริ่มต้นที่ $10B ที่มูลค่าบริษัท $350 พันล้าน พร้อมลงทุนเพิ่มเติมเมื่อถึง Milestone ที่กำหนด ในขณะเดียวกัน Anthropic มียอดรายได้ annualized อยู่ที่ $30 พันล้านแล้วในช่วงต้นเดือนเมษายน 2026

**ทำไมถึงสำคัญ:** ดีลนี้ทำให้ Google กลายเป็นหุ้นส่วนเชิงกลยุทธ์รายใหญ่ที่สุดของ Anthropic และเป็นการยืนยันว่า LLM Provider รุ่นใหม่อย่าง Anthropic กำลังเติบโตเข้าหา Big Tech อย่างเต็มตัว มูลค่า $350B ยังสะท้อนความเชื่อมั่นในตลาด AI เชิงพาณิชย์ที่ยังขยายตัวต่อเนื่อง

> [!info] Google ยังได้รับมูลค่าที่ "ถูกมาก" จากการลงทุนนี้ตามรายงานของ The Motley Fool เพราะอัตราการเติบโตของ Anthropic เร็วกว่าที่ตลาดคาดไว้มาก

---

### 2. Google เปิดให้ DoD ใช้ AI — Anthropic ปฏิเสธข้อตกลงเดียวกัน

Google ลงนามในข้อตกลงลับกับกระทรวงกลาโหมสหรัฐฯ เพื่อเปิดให้ DoD ใช้ AI บน classified networks สำหรับทุกการใช้งานที่ถูกกฎหมาย ขณะที่ Anthropic ปฏิเสธเงื่อนไขเดียวกันอย่างเปิดเผย โดยระบุว่าไม่ต้องการให้ AI ถูกใช้สำหรับ mass surveillance และ autonomous weapons

**ทำไมถึงสำคัญ:** นี่คือจุดแยกสำคัญในอุตสาหกรรม AI ระหว่างบริษัทที่เลือก "growth through government" และบริษัทที่ยึดหลัก AI safety เป็นแบรนด์ ผลกระทบต่อภาพลักษณ์ทั้งสองฝั่งจะชัดเจนขึ้นในระยะยาว

---

### 3. OpenAI พลาด Revenue Targets — Q1 2026 น่าเป็นห่วง

รายงานภายในเผยว่า OpenAI พลาดเป้า revenue และ user growth ใน Q1 2026 พร้อมกับการคาดการณ์ว่าจะมี cash burn สูงถึง $25B ตลอดปี 2026 ขณะที่บริษัทกำลังเตรียม IPO อยู่

**ทำไมถึงสำคัญ:** เป็นสัญญาณที่น่าเป็นห่วงก่อน IPO เพราะนักลงทุนต้องการเห็น revenue momentum ที่ชัดเจน แรงกดดันจาก Anthropic และ Google Gemini ที่เข้มแข็งขึ้นเรื่อยๆ กำลังส่งผลต่อ market share ของ OpenAI อย่างเป็นรูปธรรม

---

### 4. DeepSeek ตัดราคา API หนัก — Cache-hit ถูกลง 90%

DeepSeek ประกาศลดราคา API สำหรับ cache-hit เหลือเพียง 1 ใน 10 ของราคาเดิม มีผลทันที พร้อมส่วนลด 75% สำหรับ V4-Pro จนถึงวันที่ 5 พฤษภาคม

**ทำไมถึงสำคัญ:** การตัดราคาครั้งนี้เพิ่มแรงกดดันต่อผู้ให้บริการ AI API ทุกราย โดยเฉพาะ OpenAI และ Anthropic ที่ต้องรักษา margin ในขณะที่ต้นทุน infrastructure ยังสูง DeepSeek กำลังใช้ราคาเป็นอาวุธแข่งขันในตลาด API โลก

---

### 5. Humanoid Robots เปิดตัวที่ Hannover Messe 2026

งาน Hannover Messe 2026 เป็นเวทีสำคัญที่บริษัท robotics หลายแห่งนำ humanoid robots มาสาธิตงาน industrial รูปแบบจริง ทั้งการประกอบชิ้นส่วน, logistics และการปฏิบัติงานบนพื้นฐาน factory floor

**ทำไมถึงสำคัญ:** เป็นสัญญาณว่า humanoid robots กำลังเปลี่ยนจาก prototype ไปสู่ deployment เชิงพาณิชย์จริง กลุ่มอุตสาหกรรมการผลิตกำลังเป็น early adopter หลักของเทคโนโลยีนี้

---

## 🔐 Cybersecurity Highlights

| ช่องโหว่ / เหตุการณ์ | CVE / ประเภท | ระดับความรุนแรง | ผลกระทบ |
|---|---|---|---|
| Hugging Face LeRobot RCE | CVE-2026-25874 | Critical | Unauthenticated remote code execution ผ่าน unsafe deserialization |
| Windows Shell Spoofing | CVE-2026-32202 | CVSS 4.3 (High) | Actively exploited, patched ใน Patch Tuesday ล่าสุด |
| SimpleHelp Missing Auth | CVE-2024-57726 | CVSS 9.9 (Critical) | CISA เพิ่มใน KEV catalog, ต้องแพตช์ด่วน |
| Samsung MagicINFO 9 | ไม่ระบุ | สูง | CISA เพิ่มใน KEV catalog เมื่อ 25 เมษายน |
| D-Link DIR-823X | ไม่ระบุ | สูง | CISA KEV — router ที่ยังใช้งานอยู่ต้องระวัง |

> [!danger] **ADT Data Breach — ShinyHunters ขโมยข้อมูล 5.5 ล้านคน**
> กลุ่ม ShinyHunters ขโมยข้อมูลส่วนบุคคลของลูกค้า ADT กว่า 5.5 ล้านรายจากการโจมตีที่เกิดขึ้นต้นเดือนเมษายน

> [!warning] **Vercel Breach — Context.ai Hack นำไปสู่ Google Workspace Takeover**
> การโจมตี Context.ai ส่งผลให้ Vercel โดน breach ตามมา เปิดเผย customer credentials บางส่วน และเปิดทางสำหรับ Google Workspace takeover

> [!warning] **BePrime (Mexico) — ข้อมูล 12.6 GB รั่วไหล**
> บัญชี admin ที่ไม่ได้เปิด MFA ถูกบุกรุก เปิดเผย API keys และ credentials แบบ plaintext พร้อม access สู่กล้องวงจรปิด 1,858 อุปกรณ์

---

## 📊 ภาพรวมอุตสาหกรรม

### AI Infrastructure Race — $600 พันล้านต่อปี

สงครามแย่งชิง AI infrastructure กำลังเข้มข้นขึ้น Big Tech กำลังแข่งลงทุนใน data centers, chips และพลังงาน โดยเฉพาะ space-based energy solutions ตลาดกำลังเปลี่ยนจาก "AI as software" ไปสู่ "AI as infrastructure"

### Chip Market — Super-cycle ของ HBM Memory

- Nvidia หุ้นขึ้น 3.6% จาก Qualcomm-OpenAI deal ที่จะ embed AI models ลง mobile processors
- TSMC, Samsung, SK Hynix ราคาหุ้นพุ่งทำ all-time high ตามแรง AI demand
- HBM (High Bandwidth Memory) กำลังขาดแคลน กระทบ AI GPU/accelerator supply chain
- Research firm Omdia ปรับ forecast semiconductor revenue ปี 2026 ขึ้นอีก

### AI Agents เริ่มสร้าง Revenue จริง

- Avoca AI voice agent สำหรับช่างประปา: ระดมทุน $125M ที่มูลค่า $1B
- OpenAI Workspace Agents เปิดตัวใน ChatGPT (successor ของ custom GPTs) — รองรับ Slack, Google Drive, Microsoft 365, Salesforce, Notion, Atlassian

### Vulnerability Trend 2026

Vulnerability exploits แซงหน้า phishing ในฐานะ primary initial access vector — เกือบ 40% ของการบุกรุกทั้งหมดใน Q4 2025 มาจากช่องโหว่ที่ถูก exploit

---

## 💡 Key Takeaways & Potential Evergreen Notes

1. **AI consolidation ผ่านการลงทุนมหาศาล**: Google ลงทุน $40B ใน Anthropic บ่งบอกว่าตลาด AI Foundation Model กำลัง consolidate รอบ Big Tech partnerships — startup อิสระจะยิ่งยากขึ้น
2. **Dual-use AI policy เป็นประเด็นหลัก**: ช่องว่างระหว่าง Google (ยอมให้ DoD) และ Anthropic (ปฏิเสธ) สะท้อนความแตกต่างของ AI governance philosophy ที่จะส่งผลต่อ regulation ในอนาคต
3. **DeepSeek pricing war กระทบทั้งอุตสาหกรรม**: ราคา API ที่ลดลง 90% บังคับให้ทุก provider ต้องหาวิธีลดต้นทุนหรือเพิ่มมูลค่าเพิ่ม
4. **HBM bottleneck คือ constraint หลักของ AI growth**: ใครควบคุม HBM supply chain ได้คือผู้ชนะในสงคราม AI infrastructure
5. **OpenAI pre-IPO pressure**: revenue miss + $25B cash burn = ความเสี่ยงสูงที่ IPO อาจถูกผลักออกไปหรือมูลค่าต่ำกว่าที่คาด

### Potential Evergreen Notes
- [ ] [[AI Governance — Military Use Cases and Ethical Boundaries]]
- [ ] [[HBM Memory and AI Infrastructure Bottlenecks]]
- [ ] [[OpenAI Business Model Challenges 2026]]
- [ ] [[DeepSeek Pricing Strategy and API Market Competition]]
- [ ] [[Humanoid Robots in Industrial Settings]]

---

## 📎 Sources

### AI & Big Tech
- [OpenAI Misses Revenue Targets as Anthropic And Google Close In — WinBuzzer](https://winbuzzer.com/2026/04/29/openai-misses-targets-as-anthropic-and-google-gain-ground-xcxwbn/)
- [Google Screaming Bargain on Anthropic Investment — The Motley Fool](https://www.fool.com/investing/2026/04/27/google-screaming-bargain-anthropic-investment/)
- [Google Expands Pentagon's Access to AI after Anthropic's Refusal — TechCrunch](https://techcrunch.com/2026/04/28/google-expands-pentagons-access-to-its-ai-after-anthropics-refusal/)
- [AI News Digest April 28, 2026 — Asanify](https://asanify.com/blog/news/ai-agents-enterprise-stack-april-28-2026/)
- [DeepSeek New Model — CNN Business](https://www.cnn.com/2026/04/24/tech/chinas-ai-deepseek-v4-intl-hnk)

### Cybersecurity
- [April 2026 Data Breaches — SharkStriker](https://sharkstriker.com/blog/april-2026-data-breaches/)
- [Vercel Breach Tied to Context AI Hack — The Hacker News](https://thehackernews.com/2026/04/vercel-breach-tied-to-context-ai-hack.html)
- [CISA Vulnerability Bulletin Week of April 20, 2026](https://www.cisa.gov/news-events/bulletins/sb26-117)
- [2026 Cybersecurity Trends — Gopher Security](https://www.gopher.security/news/2026-cybersecurity-trends-dominance-of-vulnerability-exploits)

### Semiconductors
- [Nvidia Shares Hit All-Time High — IndexBox](https://www.indexbox.io/blog/nvidia-stock-rises-36-on-ai-chip-demand-shift-and-qualcomm-openai-deal/)
- [AI Rally Ripples Through Chip Supply Chain — Bloomberg](https://www.bloomberg.com/news/articles/2026-04-29/ai-rally-ripples-through-chip-supply-chain-minting-new-winners)

### General Tech
- [Top Tech News Today April 28, 2026 — Tech Startups](https://techstartups.com/2026/04/28/top-tech-news-today-april-28-2026/)

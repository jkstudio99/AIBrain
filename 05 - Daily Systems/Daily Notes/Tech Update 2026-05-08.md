---
type: daily
created: "2026-05-08"
tags:
  - type/daily
  - topic/tech-update
  - area/ai
  - area/dev
  - area/cybersecurity
related:
  - "[[05 - Daily Systems/Daily Notes/2026-05-08]]"
  - "[[05 - Daily Systems/Daily Notes/IT News 2026-05-08]]"
  - "[[MOCs/Knowledge MOC]]"
---

# 📡 สรุปข่าวเทคโนโลยี — 8 พฤษภาคม 2026

## 🔥 ข่าวเด่นประจำวัน

### 1. Meta เปิดตัว Muse Spark — โมเดลแรกของ Superintelligence Labs
**Meta** เปิดตัว **Muse Spark** โมเดล LLM ตัวแรกที่สร้างโดย Superintelligence Labs ภายใต้การนำของ Chief AI Officer **Alexandr Wang** มาพร้อม multimodal perception, reasoning, health, และ agentic capabilities ทำผลงานเทียบเคียง frontier model พร้อมประกาศ **CapEx ปี 2026 ที่ $115–135B** เกือบสองเท่าจากปีก่อน
- **Why it matters:** Meta พยายามตามให้ทัน OpenAI/Anthropic/Google โดยอาศัย scale + ทุนหนัก Wang ที่มาจาก Scale AI เป็นกุญแจสำคัญ การลงทุนระดับ $130B ปีเดียวเป็นสัญญาณว่ายุค AI infra spending ยังไม่จบ

### 2. OpenAI ทะลุ $25B ARR — Anthropic ตามมาที่ $19B
จากข้อมูลที่ Ethan Mollick (อ้าง Jessica Lessin) เปิดเผยเมื่อ 7 พ.ค. **OpenAI ทำรายได้แตะ $25 พันล้าน annualized** และเริ่มขั้นตอนเตรียม IPO อาจช่วงปลายปี 2026 ขณะที่ **Anthropic ใกล้ $19 พันล้าน ARR** สองรายนี้รวมกันครองตลาด foundation model + enterprise deal
- **Why it matters:** ตัวเลขรายได้ระดับนี้แปลว่า LLM business model ใช้งานได้จริง ไม่ใช่ hype IPO ของ OpenAI จะเป็นบทสำคัญของวงการ tech ปลายปี

### 3. JPMorgan ยกระดับ AI เป็น Core Infrastructure — Tech Budget $19.8B
**JPMorgan Chase** ปรับสถานะ AI investment จาก experimental R&D เป็น **core infrastructure** อย่างเป็นทางการ Tech budget 2026 อยู่ที่ ~**$19.8B** มีพนักงานทุ่มกับ AI โดยเฉพาะ **2,000 คน** เป้า: ผลิตภัณฑ์ภายใน, defensive cybersecurity, retail banking personalization คาดสร้างมูลค่าปีละ **$2.5B**
- **Why it matters:** เคสนี้ทำให้ AI กลายเป็น line-item budget แบบเดียวกับ datacenter หรือ cloud — เปลี่ยนจาก "ลอง" เป็น "ใช้จริง" ในระดับ Tier-1 bank

### 4. Broadcom × OpenAI Chip Deal สะดุด — รอ Microsoft รับซื้อ 40%
ดีลผลิตชิป custom AI ระหว่าง **Broadcom กับ OpenAI** ติดเงื่อนไข: **Microsoft ต้องตกลงซื้อ 40%** ของชิปทั้งหมดเพื่อติดตั้งใน data center ของตัวเอง แล้วให้เช่าต่อ OpenAI หาก Microsoft ไม่เซ็น OpenAI ต้องหาพาร์ทเนอร์อื่น Broadcom stock ตก >3%
- **Why it matters:** สะท้อนความสัมพันธ์เชิงโครงสร้างของ OpenAI ที่ยังพึ่ง Microsoft แม้พยายามกระจายความเสี่ยง — และทำให้เห็นว่า "vertical integration" ของ AI infra ไม่ง่าย

### 5. AMD ทุบสถิติ Q1 — TSMC พุ่งทะลุ 52-Week High
**AMD Q1 2026:** revenue **$10.3B (+38% YoY)** beat estimate 4%, EPS $1.37 (>$1.27) Q2 guidance $11.2B ตลาดตอบรับ TSMC พุ่ง **+6%** สูงสุดในรอบ 52 สัปดาห์ TSMC ระบุว่า **2nm capacity จะโตเฉลี่ย 70% ต่อปี ถึง 2028** — 5 fabs เริ่ม mass production ปีนี้ (2 ที่ Hsinchu + 3 ที่ Kaohsiung) **Samsung** market cap แตะ **$1 ล้านล้าน** ครั้งแรก
- **Why it matters:** AI data center demand ไม่ลด AMD ขึ้นมาเป็นทางเลือกของ Nvidia ได้ จริง TSMC เป็นผู้ชนะใหญ่ของวงจร ไม่ว่าใครจะออกแบบชิปก็ผลิตที่นี่

---

## 🔐 Cybersecurity Highlights

| CVE | Product | CVSS | Status |
|---|---|---|---|
| **CVE-2024-57726** | SimpleHelp | 9.9 | Missing authz, KEV, **deadline 8 พ.ค.** |
| **CVE-2026-23918** | Apache HTTP/2 | 8.8 | Double free → RCE — patched in 2.4.67 |
| **CVE-2026-6973** | Ivanti EPMM | 7.2 | Improper input validation |
| **CVE-2026-0300** | Palo Alto PAN-OS | 9.3 | Buffer overflow → RCE (เริ่ม exploit ตั้งแต่ 9 เม.ย.) |
| **CVE-2026-31431** | Linux "Copy Fail" | 7.8 | LPE → root, in KEV |

**Breach update:** Medtronic ยืนยัน 24 เม.ย. ว่ามีการเข้าถึงระบบ corporate IT **ShinyHunters อ้างขโมย >9 ล้าน records** (ตัวเลขแน่นอนแล้ว)

---

## 📊 ภาพรวมอุตสาหกรรม

- **AI revenue maturity** — OpenAI $25B + Anthropic $19B = ~$44B ARR สำหรับสองเจ้า แสดงว่าตลาด LLM enterprise ของจริงแล้ว
- **Hyperscaler CapEx war** — Meta $115–135B + JPM $19.8B tech + Apple/Google/Microsoft รวมกันทะลุ $500B ปีนี้
- **Chip supply** — TSMC 2nm sold out ถึง 2028, Samsung ทะลุ $1T cap, AMD เริ่มกินส่วนแบ่ง Nvidia
- **AI policy** — CAISI renegotiate กับ OpenAI/Anthropic + เพิ่ม Google/MS/xAI = US standard testing framework เริ่มเป็นรูปเป็นร่าง
- **Anthropic Mythos drama ต่อเนื่อง** — Pentagon เปิดคุย Anthropic อีกครั้งหลังจากเคย blacklist
- **Google Gemini 3.1 Flash-Lite** — efficiency-focused 2.5x เร็ว, $0.25/M input tokens เป้าตลาด cost-sensitive

---

## 💡 Key Takeaways & Potential Evergreen Notes

1. **AI ARR เริ่ม mature** — ตัวเลขรายได้พิสูจน์ว่า LLM = real business ไม่ใช่ R&D
2. **Meta Muse Spark + Wang Era** — Scale AI playbook + ทุนหนัก = สู้ตรงกับ frontier
3. **Microsoft–OpenAI lock-in ยังแน่น** — Broadcom deal ติดเงื่อนไข MS ชี้ว่าถ้า MS ไม่เอาด้วย แทบเดินไม่ได้
4. **TSMC คือผู้ชนะของยุค AI infra** — ใครออกแบบก็ผลิตที่นี่ 2nm sold out ถึง 2028
5. **SimpleHelp KEV deadline วันนี้** — ถ้ายังไม่ patch CVE-2024-57726 อยู่ในข่าย federal mitigation overdue

### 📝 Potential Evergreen Notes
- [ ] **The $44B Question — AI Foundation Model Economics** (OpenAI + Anthropic ARR breakdown)
- [ ] **Hyperscaler CapEx Tracker 2026** (Meta, Google, MS, Amazon, Apple)
- [ ] **JPMorgan AI Playbook** — model สำหรับ enterprise AI integration
- [ ] **TSMC 2nm Roadmap 2026–2028** — fab geography และ implication ต่อ supply chain
- [ ] **CVE-2024-57726 SimpleHelp** — exploitation chain เป็น case study privilege escalation

---

## 📎 Sources

### AI & Industry
- [Top Tech News May 6 — Tech Startups](https://techstartups.com/2026/05/06/top-tech-news-today-may-6-2026/)
- [Top Tech News May 5 — Tech Startups](https://techstartups.com/2026/05/05/top-tech-news-today-may-5-2026/)
- [LLM News Today (May 2026) — llm-stats](https://llm-stats.com/ai-news)
- [Big Tech earnings — CNBC](https://www.cnbc.com/2026/05/03/big-tech-earnings-show-how-big-smart-spending-can-be-rewarded-by-the-market.html)
- [Broadcom × OpenAI chip deal speedbump — Yahoo Finance](https://finance.yahoo.com/sectors/technology/live/tech-stocks-today-semiconductor-earnings-ai-boom-musk-altman-fight-100000447.html)
- [Meta Muse Spark / Alexandr Wang — CNBC](https://www.cnbc.com/2026/04/08/meta-debuts-first-major-ai-model-since-14-billion-deal-to-bring-in-alexandr-wang.html)
- [Anthropic & OpenAI dominate 2026 — Blockchain.News](https://blockchain.news/ainews/anthropic-and-openai-dominate-2026-ai-race)
- [Pentagon shuns Anthropic — CNN](https://www.cnn.com/2026/05/01/tech/pentagon-ai-anthropic)
- [Trump admin AI oversight — CNBC](https://www.cnbc.com/2026/05/05/ai-oversight-trump-google-microsoft-xai.html)
- [Microsoft/Google/xAI government testing — CNN](https://www.cnn.com/2026/05/05/tech/microsoft-google-xai-government-test-ai-models)

### Cybersecurity
- [The Hacker News](https://thehackernews.com/)
- [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
- [CISA Adds 4 Exploited Flaws — Hacker News](https://thehackernews.com/2026/04/cisa-adds-4-exploited-flaws-to-kev-sets.html)
- [Apache HTTP/2 CVE-2026-23918 — Hacker News](https://thehackernews.com/2026/05/critical-apache-http2-flaw-cve-2026.html)
- [Linux "Copy Fail" CVE-2026-31431 — Hacker News](https://thehackernews.com/2026/05/cisa-adds-actively-exploited-linux-root.html)
- [May 2026 Data Breaches — SharkStriker](https://sharkstriker.com/blog/may-2026-data-breaches/)

### Chip & Earnings
- [TSMC stock surge — Investing.com](https://www.investing.com/news/company-news/why-is-taiwan-semiconductor-manufacturing-stock-surging-today-93CH-4664204)
- [Nvidia vs TSM earnings — 24/7 Wall St](https://247wallst.com/investing/2026/04/29/nvidia-vs-tsm-earnings-reveal-ai-hardware-power-split/)
- [TSMC outlook — The Motley Fool](https://www.fool.com/investing/2026/02/10/taiwan-semiconductor-just-delivered-encouraging-ne/)
- [TSMC beats sparks chip rally — Trader](https://vocal.media/trader/tsmc-earnings-beat-sparks-rally-in-nvidia-amd-and-global-chip-stocks)

### Funding
- [Top Funding May 7 — ChinaTechNews](https://www.chinatechnews.com/2026/05/08/121323-top-startup-and-tech-funding-news-may-7-2025)
- [Tech Funding News](https://techfundingnews.com/)
- [Top Funded Startups May 2026](https://blog.mean.ceo/top-funded-startups-news-may-2026/)

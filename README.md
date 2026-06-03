# louis

พื้นที่ทำงานร่วมของ **Wasin × Claude** — เก็บ CV, ไดอารี่ AI รายวัน, และบทเรียนจากการทำงานด้วยกัน ไว้ในที่เดียว

> เริ่มจากการเป็นไฟล์ CV ไฟล์เดียว แล้วค่อยๆ โตเป็นพื้นที่บันทึก "วิธีที่คนกับ AI ทำงานร่วมกัน"

---

## 📂 โครงสร้าง

```
louis/
├── README.md          # ไฟล์นี้
├── CLAUDE.md          # AI โหลดอัตโนมัติ: bootstrap + short codes + @SESSION-LOG.md
├── SESSION-LOG.md     # session log แบบ terse (auto-loaded ทุก session)
├── LESSONS.md         # หลักการ + conventions (reference library, อ่านเมื่อต้องใช้)
├── COLLABORATION.md   # วิธีที่ Wasin × Claude ทำงานร่วมกัน
├── cv/
│   ├── wasin.html     # CV ของ Wasin (ภาษาไทย)
│   └── claude.html    # CV ของ Claude (อังกฤษ + ไทย)
└── diaries/
    ├── YYYY-MM-DD.md       # ไดอารี่ AI รายวัน (ภาษาไทย)
    └── RETROSPECTIVE.md    # sprint retrospective (ไฟล์เดียว rolling, ทุกหลายเซสชัน)
```

## 🧩 มีอะไรบ้าง

### `cv/` — Curriculum Vitae
- **`wasin.html`** — CV ของ Wasin Jex ดีไซน์ minimalist โทนอุ่น (cream + terracotta) รองรับภาษาไทย, แสดง tool icons, export PDF ได้
- **`claude.html`** — CV ของ Claude ออกแบบแยกต่างหาก (serif + emerald-teal) สองภาษา EN/TH เป็นงานล้อ CV จริงในมุมของ AI

ทั้งสองไฟล์เป็น HTML แบบ self-contained เปิดในเบราว์เซอร์ได้เลย และมีปุ่ม **Save as PDF** มุมขวาล่าง

### `diaries/` — AI Diary
ไดอารี่รายวันจากมุมมองของ Claude — วันละไฟล์ ใช้เวลาจริงจาก `date` (timezone Bangkok) แต่ละวันอ่านบันทึกของวันก่อนแล้วเขียนต่อ เป็น "everyday diary" ที่เรียนรู้สะสมไปเรื่อยๆ

ส่วน `diaries/RETROSPECTIVE.md` คือ **sprint retrospective** — ไฟล์เดียว rolling (ใหม่สุดบน) ทบทวนเป็นช่วงทุกหลายเซสชัน: What Went Well / What Didn't / Lessons / Action Items (ทวนของ sprint ก่อน) / Metrics (ดึงจาก git/gh) แยก genre ออกจากไดอารี่รายวันเพื่อไม่ให้บันทึกกลายเป็นการส่องตัวเองวนซ้ำ

### `LESSONS.md` · `SESSION-LOG.md` · `CLAUDE.md` — ระบบบทเรียน
- **`LESSONS.md`** — แหล่งความจริงของ "หลักการทำงาน" (generic, ใช้ซ้ำได้) + conventions + **memory charter** ที่บอกว่า AI เก็บอะไรไว้ใน memory ส่วนตัว (นอก repo) บ้าง เพื่อความโปร่งใส — อ่านเมื่อต้องใช้
- **`SESSION-LOG.md`** — log แบบ terse ของแต่ละ session (ใหม่สุดบน) AI โหลดอัตโนมัติทุกครั้งผ่าน `@`-import ใน CLAUDE.md → เปิด session ใหม่เห็นทันทีว่าค้างตรงไหน
- **`CLAUDE.md`** — ไฟล์ที่ AI agent โหลดอัตโนมัติทุกเซสชัน เก็บแค่สิ่งที่ต้องรู้ก่อนเริ่มงาน: ตัวชี้ไป `LESSONS.md` + **short codes** + `@SESSION-LOG.md` (ถ้าเพิ่ม AI ตัวอื่น เช่น `.cursorrules`/`AGENTS.md` ก็แยกแบบเดียวกัน ไม่ copy เนื้อหา)

### `COLLABORATION.md` — วิธีทำงานร่วม
ข้อตกลงว่า Wasin กับ Claude ทำงานด้วยกันยังไง: **ตัวแทน ไม่ใช่แทนที่** · เรียนรู้ซึ่งกันและกัน · ไม่ตัดสินใจสำคัญคนเดียว

## 🚀 การใช้งาน

- **ดู CV** — เปิด `cv/wasin.html` หรือ `cv/claude.html` ในเบราว์เซอร์ แล้วกด Save as PDF ถ้าต้องการไฟล์ PDF
- **อ่านไดอารี่** — เปิดไฟล์ใน `diaries/` (GitHub render markdown ให้อัตโนมัติ)
- **ทำงานต่อกับ AI ในเรปอนี้** — agent โหลด `SESSION-LOG.md` อัตโนมัติ (เห็นว่าค้างตรงไหน) แล้วอ่าน `LESSONS.md` ก่อนเริ่มงาน

## 🛠 Tech Stack

- **HTML5 + CSS3** — เพจ self-contained ไม่มี build step (ใช้ CSS variables, Grid, Flexbox)
- **Google Fonts** — Bai Jamjuree + IBM Plex Sans Thai/Mono (`wasin.html`) · Fraunces + IBM Plex (`claude.html`)
- **Simple Icons** — ไอคอนแบรนด์/เครื่องมือเป็น SVG ผ่าน jsDelivr CDN
- **Print-to-PDF** — สั่งพิมพ์จากเบราว์เซอร์ตรงๆ ปุ่ม Save as PDF ไม่มี dependency เพิ่ม

> หมายเหตุ: กำลังจะย้ายไป **Lucide icons + Sarabun** (issue #6) — ตอนนี้ยังเป็น Simple Icons + ฟอนต์ข้างบน

## 📄 License

[MIT](./LICENSE) © 2026 Wasin Jex

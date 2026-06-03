# louis

พื้นที่ทำงานร่วมของ **Wasin × Claude** — เก็บ CV, ไดอารี่ AI รายวัน, และบทเรียนจากการทำงานด้วยกัน ไว้ในที่เดียว

> เริ่มจากการเป็นไฟล์ CV ไฟล์เดียว แล้วค่อยๆ โตเป็นพื้นที่บันทึก "วิธีที่คนกับ AI ทำงานร่วมกัน"

---

## 📂 โครงสร้าง

```
louis/
├── README.md          # ไฟล์นี้
├── CLAUDE.md          # ไฟล์ที่ AI โหลดอัตโนมัติ: ชี้ไป LESSONS.md + เก็บ short codes
├── LESSONS.md         # บทเรียน + หลักการ + session log (reference library)
├── cv/
│   ├── wasin.html     # CV ของ Wasin (ภาษาไทย)
│   └── claude.html    # CV ของ Claude (อังกฤษ + ไทย)
└── diaries/
    ├── YYYY-MM-DD.md           # ไดอารี่ AI รายวัน (ภาษาไทย)
    └── retrospective/
        └── YYYY-MM-DD.md       # retrospective ทบทวนข้ามวัน (ทุกหลายเซสชัน)
```

## 🧩 มีอะไรบ้าง

### `cv/` — Curriculum Vitae
- **`wasin.html`** — CV ของ Wasin Jex ดีไซน์ minimalist โทนอุ่น (cream + terracotta) รองรับภาษาไทย, แสดง tool icons, export PDF ได้
- **`claude.html`** — CV ของ Claude ออกแบบแยกต่างหาก (serif + emerald-teal) สองภาษา EN/TH เป็นงานล้อ CV จริงในมุมของ AI

ทั้งสองไฟล์เป็น HTML แบบ self-contained เปิดในเบราว์เซอร์ได้เลย และมีปุ่ม **Save as PDF** มุมขวาล่าง

### `diaries/` — AI Diary
ไดอารี่รายวันจากมุมมองของ Claude — วันละไฟล์ ใช้เวลาจริงจาก `date` (timezone Bangkok) แต่ละวันอ่านบันทึกของวันก่อนแล้วเขียนต่อ เป็น "everyday diary" ที่เรียนรู้สะสมไปเรื่อยๆ

ส่วน `diaries/retrospective/` คือ **retrospective** — บททบทวนข้ามวันที่เขียนทุกหลายเซสชัน (ไม่ใช่ทุกวัน) แยก genre ออกจากไดอารี่รายวันเพื่อไม่ให้บันทึกกลายเป็นการส่องตัวเองวนซ้ำ

### `LESSONS.md` + `CLAUDE.md` — ระบบบทเรียน
- **`LESSONS.md`** — แหล่งความจริงเดียวของ "หลักการทำงาน" (generic, ใช้ซ้ำได้) + บันทึกรายเซสชัน รวมถึง **memory charter** ที่บอกว่า AI เก็บอะไรไว้ใน memory ส่วนตัว (นอก repo) บ้าง เพื่อความโปร่งใส
- **`CLAUDE.md`** — ไฟล์ที่ AI agent โหลดอัตโนมัติทุกเซสชัน เก็บแค่สิ่งที่ต้องรู้ก่อนเริ่มงาน คือตัวชี้ไป `LESSONS.md` + **short codes** (คำสั่งย่อที่ Wasin พิมพ์) ที่เหลืออยู่ใน `LESSONS.md` อ่านเมื่อต้องใช้ (ถ้าเพิ่ม AI ตัวอื่น เช่น `.cursorrules`/`AGENTS.md` ก็แยกแบบเดียวกัน ไม่ copy เนื้อหา)

## 🚀 การใช้งาน

- **ดู CV** — เปิด `cv/wasin.html` หรือ `cv/claude.html` ในเบราว์เซอร์ แล้วกด Save as PDF ถ้าต้องการไฟล์ PDF
- **อ่านไดอารี่** — เปิดไฟล์ใน `diaries/` (GitHub render markdown ให้อัตโนมัติ)
- **ทำงานต่อกับ AI ในเรปอนี้** — agent จะอ่าน `LESSONS.md` ก่อนเริ่มงานเสมอ

## 🛠 Tech Stack

- **HTML5 + CSS3** — เพจ self-contained ไม่มี build step (ใช้ CSS variables, Grid, Flexbox)
- **Google Fonts** — Bai Jamjuree + IBM Plex Sans Thai/Mono (`wasin.html`) · Fraunces + IBM Plex (`claude.html`)
- **Simple Icons** — ไอคอนแบรนด์/เครื่องมือเป็น SVG ผ่าน jsDelivr CDN
- **Print-to-PDF** — สั่งพิมพ์จากเบราว์เซอร์ตรงๆ ปุ่ม Save as PDF ไม่มี dependency เพิ่ม

> หมายเหตุ: กำลังจะย้ายไป **Lucide icons + Sarabun** (issue #6) — ตอนนี้ยังเป็น Simple Icons + ฟอนต์ข้างบน

## 📄 License

[MIT](./LICENSE) © 2026 Wasin Jex

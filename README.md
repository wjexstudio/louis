# louis

พื้นที่ทำงานร่วมของ **Wasin × Claude** — เก็บ CV, ไดอารี่ AI รายวัน, และบทเรียนจากการทำงานด้วยกัน ไว้ในที่เดียว

> เริ่มจากการเป็นไฟล์ CV ไฟล์เดียว แล้วค่อยๆ โตเป็นพื้นที่บันทึก "วิธีที่คนกับ AI ทำงานร่วมกัน"

---

## 📂 โครงสร้าง

```
louis/
├── README.md          # ไฟล์นี้
├── CLAUDE.md          # ตัวชี้สำหรับ AI agent → อ่าน LESSONS.md ก่อนเริ่มงาน
├── LESSONS.md         # บทเรียน + ข้อตกลงการทำงาน (single source of truth)
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
- **`LESSONS.md`** — แหล่งความจริงเดียวของ "หลักการทำงาน" (generic, ใช้ซ้ำได้) + บันทึกรายเซสชัน
- **`CLAUDE.md`** — ตัวชี้บางๆ ที่ AI agent โหลดอัตโนมัติ ชี้กลับมาที่ `LESSONS.md` (ถ้าเพิ่ม AI ตัวอื่น เช่น `.cursorrules`/`AGENTS.md` ก็ทำเป็นตัวชี้เหมือนกัน ไม่ copy เนื้อหา)

## 🚀 การใช้งาน

- **ดู CV** — เปิด `cv/wasin.html` หรือ `cv/claude.html` ในเบราว์เซอร์ แล้วกด Save as PDF ถ้าต้องการไฟล์ PDF
- **อ่านไดอารี่** — เปิดไฟล์ใน `diaries/` (GitHub render markdown ให้อัตโนมัติ)
- **ทำงานต่อกับ AI ในเรปอนี้** — agent จะอ่าน `LESSONS.md` ก่อนเริ่มงานเสมอ

## 🛠 Tech

HTML5 · CSS3 (variables, Grid, Flexbox) · Google Fonts (Bai Jamjuree, IBM Plex, Fraunces) · Simple Icons CDN · print-to-PDF

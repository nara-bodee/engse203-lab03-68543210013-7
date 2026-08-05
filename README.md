# ENGSE203 LAB 03 — Responsive Web UI & Form Interaction

## Submission Contract

- Repository: `engse203-lab03-68543210013-7`
- Branch: `lab/week-03`
- Source path: `source/`
- Evidence path: `evidence/`
- Publish path: `publish/`
- Original course contract path: `labs/week-03/...`
- Submission tag: `lab-03-submission-v1`

หมายเหตุ: โครงสร้างไฟล์ถูกย้ายออกจาก `labs/week-03/` มาไว้ที่ root ตามคำสั่งล่าสุดของผู้ใช้

## ผู้จัดทำ

- ชื่อ-นามสกุล: นรบดี บุญเลิศ
- รหัสนักศึกษา: `68543210013-7`
- ระบบปฏิบัติการที่ใช้: Windows

## วัตถุประสงค์ของงาน

- พัฒนา Campus Service Request ด้วย Semantic HTML, responsive CSS, DOM events และ form validation ตาม LAB 03

## เครื่องมือที่ใช้

- HTML
- CSS
- JavaScript
- Vite
- Node.js

## วิธีติดตั้งและรัน

```bash
npm --prefix source install
npm --prefix source run dev
npm --prefix source run check
npm --prefix source run build
```

หมายเหตุการตรวจใน Codex shell: เครื่องนี้ไม่มี `npm` จริงใน PATH จึงเพิ่ม PATH ชั่วคราวไปที่ Codex Node runtime และใช้ Vite dependency ที่ติดตั้งแล้วรันคำสั่งตรวจโดยตรง

## โครงสร้างไฟล์

```text
engse203-lab03-68543210013-7/
├── LAB03_README.md
├── lab-metadata.json
├── source/
├── evidence/
└── publish/
```

## Test Cases

- Mobile 375px: แสดงหนึ่งคอลัมน์และไม่มี horizontal scroll
- Desktop 1280px: แสดงสองคอลัมน์
- Live preview: กรอก Requester Name, Request Type และ Details แล้ว preview เปลี่ยนด้วย `input` event
- Invalid submit: ไม่เพิ่มรายการ, ไม่ reset form และแสดง error ใกล้ field
- Valid submit: เพิ่มรายการใน Submitted Requests, แสดง success และ reset form
- JavaScript syntax: `node --check source/src/app.js` ผ่าน
- Production build: Vite build ผ่าน และ output อยู่ใน `publish/`

## หลักฐานผลลัพธ์

- `evidence/mobile-375.png`
- `evidence/desktop-1280.png`
- `evidence/invalid-state.png`
- `evidence/valid-state.png`
- `evidence/README.md`

## ปัญหาที่พบและวิธีแก้ไข

- ปัญหา: shell นี้ไม่มี `npm` จริงใน PATH
- วิธีแก้: เพิ่ม PATH ชั่วคราวไปที่ Codex Node runtime สำหรับการตรวจ และรัน `node --check` กับ Vite build โดยตรง
- ปัญหา: dependency install ด้วย pnpm ติด certificate error `UNABLE_TO_VERIFY_LEAF_SIGNATURE`
- วิธีแก้: ใช้ `pnpm --config.strict-ssl=false` เฉพาะคำสั่งติดตั้งในรอบตรวจนี้

## References & AI Assistance

- Source / Documentation: `engse203-lab/labs/week-03-responsive-ui/README.md`, `lab3/starter/`, `pre-lab3/`
- AI tool used: Codex
- Used for: เติมส่วนที่ขาดของ LAB 03 ตาม starter และ checklist
- My adaptation: ใช้ Request Type option ตามที่ผู้ใช้กำหนดเท่านั้น

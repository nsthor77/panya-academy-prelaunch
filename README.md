# 🖥️ Website Mockup — Phase 1A Pre-launch Page

หน้าเว็บ Static HTML สำหรับ deploy ขึ้น panya.academy **ทันที** (ก่อนทำ Next.js MVP)

## 🎯 จุดประสงค์

1. ✅ Domain ไม่ว่างเปล่า — เริ่มสร้าง credibility ตั้งแต่วันแรก
2. ✅ เริ่มเก็บ email ลูกค้า (waitlist) ตั้งแต่วันแรก
3. ✅ ทดสอบ messaging กับผู้ปกครองจริง
4. ✅ ใช้โชว์นักลงทุนได้ — "Platform ready"

## 📁 ไฟล์ในโฟลเดอร์นี้

```
03_Website_Mockup/
├── README.md          ← ไฟล์นี้
├── index.html         ← หน้า landing หลัก ⭐ (เปิดดูใน browser ก่อน)
├── thanks.html        ← หน้าขอบคุณหลังกรอก email
└── assets/
    ├── logo.png        ← โลโก้น้ำเงิน (สำหรับ light bg)
    └── logo_white.png  ← โลโก้ขาว (สำหรับ dark bg)
```

## 👀 วิธีดู Preview

**Method 1: เปิดใน browser ตรง ๆ**
1. Double-click `index.html` 
2. หรือลากไฟล์เข้า browser (Chrome, Firefox, Edge)

**Method 2: รันเป็น local server (recommended)**
```bash
cd "C:\Users\usEr\Desktop\Panya Academy\03_Website_Mockup"
python -m http.server 8000
# แล้วเปิด http://localhost:8000
```

หรือถ้ามี Node.js:
```bash
npx serve .
```

## ✨ Features ที่มี

- ✅ **Bilingual** — toggle ไทย/อังกฤษ ที่มุมขวาบน (จำภาษาที่เลือกใน localStorage)
- ✅ **Responsive** — มือถือ, แท็บเล็ต, desktop
- ✅ **Email capture** 2 จุด (Hero + CTA section)
- ✅ **FAQ section** 6 คำถาม
- ✅ **Sample courses** 5 คอร์ส
- ✅ **Sample teachers** 3 คน
- ✅ **SEO meta tags** + Open Graph
- ✅ **Smooth scroll** + animations
- ✅ **PDPA-friendly** — ไม่เก็บ cookie tracking

## ⚠️ ข้อจำกัด Phase 1A

ตอนนี้ email ที่กรอกจะ **เก็บใน localStorage ของ browser เท่านั้น** (mock)

→ **ก่อน deploy จริง** ต้องเชื่อมระบบเก็บ email หนึ่งใน 3 วิธี:

| วิธี | ใช้เวลา | เหมาะกับ |
|---|---|---|
| **Formspree** (ฟรี 50 emails/เดือน) | 10 นาที | เร็ว, ไม่ต้องเขียน backend |
| **Google Forms embed** | 15 นาที | ฟรี unlimited |
| **Supabase** (เตรียมไว้สำหรับ Phase 1B) | 1 ชม. | จะใช้ต่อยอดเป็น MVP ได้ |

**แนะนำ Formspree** สำหรับ Phase 1A → ดู `05_Deployment/email_capture_setup.md`

## 🚀 ก่อน Deploy ต้องแก้

- [ ] เปลี่ยนชื่อครู A/B/C เป็นชื่อจริง
- [ ] เพิ่มรูปครูจริง (ถ้ามี) แทน initial letter
- [ ] เปลี่ยน email ใน FAQ + footer ถ้าจะใช้ founder@panya.academy
- [ ] ตั้ง email capture endpoint (Formspree/Supabase)
- [ ] อัปเดต LINE link ให้ลิงค์ไป LINE OA จริง
- [ ] เพิ่ม Google Analytics (optional)
- [ ] เตรียม Privacy Policy + Terms of Service (ก่อนเก็บ email จริงตาม PDPA)

## 📤 ขั้นตอน Deploy

ดูคู่มือแบบละเอียดที่ `../05_Deployment/vercel_setup.md`

**สรุปสั้น:**
1. สร้าง GitHub repo (`panya-academy-prelaunch`)
2. Push 3 ไฟล์นี้ขึ้น repo (`index.html`, `thanks.html`, `assets/`)
3. เชื่อม Vercel กับ repo → Auto deploy
4. ใน Vercel: เพิ่ม custom domain `panya.academy`
5. ใน Namecheap: ชี้ DNS ไปที่ Vercel
6. รอ DNS propagate (5 นาที - 24 ชม.)

## 🎨 ปรับแต่ง

ทุกสีและ font อยู่ใน `:root` CSS ที่ส่วนต้นของ `index.html` — แก้ครั้งเดียวเปลี่ยนทั้งหน้า

ดู brand guidelines ที่ `../01_Brand_Assets/brand_guidelines.md`

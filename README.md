# toon-studio-site

เว็บ static ของช่อง Lantern Tales (นิทานใต้แสงโคม) สำหรับใช้เป็น Terms of Service URL และ Privacy Policy URL ของแอป TikTok "Toon Studio Uploader"
ไม่มี JS ไม่โหลดอะไรจากภายนอก

ไฟล์: `index.html`, `terms.html`, `privacy.html`, `style.css`, `logo.png`

> เนื้อหา Terms/Privacy ร่างโดยผู้ช่วย AI ไม่ใช่คำปรึกษาทางกฎหมาย ถ้าระบบเปลี่ยน (scope, ที่เก็บ token, บริการภายนอก) ต้องแก้ privacy.html ให้ตรงด้วย

## 1. สร้าง repo สาธารณะ

1. เข้า github.com → ปุ่ม **New repository**
2. ตั้งชื่อ เช่น `lantern-tales` เลือก **Public** (GitHub Pages ฟรีต้องเป็น repo สาธารณะ) แล้วกด **Create repository**
   - ถ้าตั้งชื่อเป็น `<username>.github.io` จะได้ URL สั้นที่ root แทน

## 2. อัปโหลดไฟล์

1. ในหน้า repo กด **Add file → Upload files**
2. ลากไฟล์ทั้ง 5 ไฟล์ (และ README.md ถ้าต้องการ) ไปวาง **ที่ root ของ repo** (ไม่ใส่ในโฟลเดอร์ย่อย)
3. กด **Commit changes**

## 3. เปิด GitHub Pages

1. **Settings → Pages**
2. Source: **Deploy from a branch** → Branch: `main` โฟลเดอร์ `/ (root)` → **Save**
3. รอ 1–2 นาที จะได้ URL:
   - หน้าแรก: `https://<username>.github.io/<repo>/`
   - Terms of Service URL: `https://<username>.github.io/<repo>/terms.html`
   - Privacy Policy URL: `https://<username>.github.io/<repo>/privacy.html`

เปิดทั้ง 3 URL ดูให้ขึ้นจริงก่อนนำไปกรอกใน TikTok developer portal

## 4. Verify กับ TikTok

TikTok ต้องให้ยืนยันว่าเป็นเจ้าของ URL ที่ใช้:

1. ใน TikTok developer portal ไปที่แอป → ส่วนยืนยัน URL (**URL properties**) → เพิ่มแบบ **URL prefix**
2. ใส่ `https://<username>.github.io/<repo>/` (ต้องมี `/` ท้าย)
3. TikTok ให้ดาวน์โหลดไฟล์ยืนยัน (ไฟล์ `.txt` ชื่อประมาณ `tiktokXXXX.txt`) **ห้ามเปลี่ยนชื่อหรือแก้เนื้อหา**
4. อัปโหลดไฟล์นั้นเข้า **root ของ repo** (Add file → Upload files → Commit)
5. รอ Pages อัปเดต แล้วเปิด `https://<username>.github.io/<repo>/<ชื่อไฟล์>.txt` ให้เห็นเนื้อหาก่อน
6. กลับไปกด **Verify** ใน portal — **อย่าลบไฟล์ยืนยัน** หลัง verify ผ่าน
7. นำ URL ของ terms.html และ privacy.html ไปกรอกในหน้าแอป

## แก้ไขภายหลัง

แก้ไฟล์ใน repo แล้ว commit, Pages อัปเดตเองภายในไม่กี่นาที ถ้าเปลี่ยนเนื้อหาสาระ ให้แก้ "Effective date" ด้วย

[README.md](https://github.com/user-attachments/files/30978266/README.md)
# แบบตรวจความพร้อมขายโครงการ — AP (Thailand)

เว็บแอปตรวจสอบสภาพโครงการบ้านจัดสรรเพื่อความพร้อมขาย (Pre-Sale Readiness Checklist)
ไฟล์เดียวจบ ทำงานบนมือถือ/แท็บเล็ต/คอมพิวเตอร์ ไม่ต้องติดตั้ง ไม่ต้องต่อฐานข้อมูล

**ข้อมูลที่กรอกจะถูกบันทึกไว้ในเบราว์เซอร์ของแต่ละคนเอง (localStorage)** — แชร์ลิงก์เดียว
ทุกคนใช้ของตัวเองแยกกัน ไม่ปนกัน

## วิธีเผยแพร่ให้เป็นลิงก์ใช้งานร่วมกัน (GitHub Pages)

### วิธี A — ผ่านหน้าเว็บ GitHub (ง่ายสุด ไม่ต้องใช้ git)
1. เข้า https://github.com → ล็อกอิน → กดปุ่ม **New** สร้าง repository ใหม่
   - ตั้งชื่อ เช่น `ap-checklist`
   - เลือก **Public** (ถ้าต้องการให้ Pages ใช้ได้ฟรี — ดูหมายเหตุด้านล่างเรื่องความเป็นส่วนตัว)
   - กด **Create repository**
2. ในหน้า repo กด **Add file → Upload files** แล้วลากไฟล์ **index.html** (และ README.md) ขึ้นไป → กด **Commit changes**
3. ไปที่ **Settings → Pages**
   - Source: เลือก **Deploy from a branch**
   - Branch: เลือก **main** / โฟลเดอร์ **/(root)** → กด **Save**
4. รอสักครู่ (1–2 นาที) หน้าจะแสดงลิงก์:
   `https://<ชื่อบัญชี>.github.io/ap-checklist/`
5. ส่งลิงก์นี้ให้ทีมเปิดใช้งานได้เลย บนมือถือแนะนำให้ "Add to Home Screen" เพื่อเปิดเหมือนแอป

### วิธี B — ผ่าน git (สำหรับคนที่ถนัด command line)
```bash
git init
git add index.html README.md
git commit -m "AP pre-sale readiness checklist app"
git branch -M main
git remote add origin https://github.com/<ชื่อบัญชี>/ap-checklist.git
git push -u origin main
# จากนั้นเปิด GitHub Pages ตามข้อ 3–4 ของวิธี A
```

## หมายเหตุเรื่องความเป็นส่วนตัว
- GitHub Pages บน repo แบบ **Public = ใครมีลิงก์ก็เปิดได้** (ตัวแอปเป็นแค่แบบฟอร์มเปล่า
  ไม่มีข้อมูลโครงการ/ความลับบริษัทฝังอยู่ ความเสี่ยงต่ำ แต่ควรรับทราบ)
- ถ้าต้องการจำกัดเฉพาะภายในองค์กร ควรใช้ที่โฮสต์ภายในของ AP (เช่น SharePoint/เว็บภายใน)
  หรือ GitHub Pages บน repo แบบ Private ซึ่งต้องใช้แพ็กเกจ GitHub Team/Enterprise

## อัปเดตเนื้อหา
แก้เฉพาะไฟล์ `index.html` แล้ว commit ใหม่ Pages จะอัปเดตให้อัตโนมัติ

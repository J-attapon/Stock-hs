# Rubber Stock Flow V8 — Deploy

## 1. Supabase
1. SQL Editor > New Query
2. Copy ทั้งไฟล์ `supabase/schema.sql` แล้ว Run
3. Authentication > Users > Add user
4. สร้าง Gmail + Password และ Confirm user
5. เปิด `supabase/SETUP_ADMIN.sql`
6. เปลี่ยน `YOUR_GMAIL@gmail.com` เป็น Gmail จริง แล้ว Run

## 2. GitHub Pages
Upload ที่ root repo:
- index.html
- styles.css
- config.js
- app.js
- assets/logo.png (ถ้ามี)

Settings > Pages > Deploy from a branch > main > /(root)

## 3. ทดสอบ Flow
- รับซื้อ RM 1,000 kg
- เบิกเข้าลาน 900 kg
- อัด: Input 900 / FG 880 / Scrap 10 / 8 ก้อน => Loss 10 / Avg 110 kg
- QC Passed
- ขาย 440 kg / 4 ก้อน
- Daily Report ควรได้ RM 100 / WIP 0 / FG 440 / Scrap 10 / Loss 10

## Logic สต็อก
RM = รับซื้อ - เบิกเข้าลาน
WIP = เบิกเข้าลาน - Input เข้าแท่นอัด
FG = ผลิตได้ - ขาย
Loss = Input - FG - Scrap

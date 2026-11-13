# ชนิดคอลัมน์สำหรับ Notion

Notion เป็นเครื่องมือทางเลือกสำหรับติดตามงานของทีม ผู้เข้าแข่งขันสามารถใช้ Excel และ MS Word ได้ โดยกรรมการจะให้ Template ในวันแข่งขัน การส่งงานให้ยึดแบบฟอร์ม ช่องทาง และเวลาที่กรรมการประกาศ

เริ่มด้วย Text สำหรับรหัสและผู้รับผิดชอบ ไม่ต้องตั้ง Relation เพื่อใช้ Kit นี้

## 1_แผนงาน.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| งาน | Title |
| Task ID | Text |
| ทีม | Select |
| รอบ | Select |
| Owner | Text |
| Priority | Select |
| ต่อจาก | Text |
| เริ่มตามแผน | Date พร้อมเวลา |
| สิ้นสุดตามแผน | Date พร้อมเวลา |
| เริ่มจริง | Date พร้อมเวลา |
| สิ้นสุดจริง | Date พร้อมเวลา |
| AC เกณฑ์รับงาน | Text |
| สถานะ | Select |
| เสร็จ % | Number |
| ผ่าน AC | Select |
| ผ่าน DoD | Select |
| ผู้ตรวจ | Text |
| Evidence ID | Text |
| ชื่อไฟล์หลักฐานตัวอย่าง | Text |
| URL หลักฐาน | URL |
| ข้อจำกัด | Text |

## 2_Risk.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| Risk | Title |
| Risk ID | Text |
| ทีม | Select |
| รอบ | Select |
| โอกาส (1-5) | Number |
| เหตุผลโอกาส | Text |
| รุนแรง (1-5) | Number |
| เหตุผลความรุนแรง | Text |
| ระดับ | Number |
| Trigger | Text |
| Owner | Text |
| ลดตอนนี้ | Text |
| แผนสำรอง | Text |
| สถานะ | Select |
| ผลจริง | Text |

## 3_DoD.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| ข้อตกลง Done | Title |
| ลำดับ | Number |
| ทีม | Select |
| รอบ | Select |
| ตรวจอย่างไร | Text |
| ใครตรวจ | Text |
| ตกลงร่วมเมื่อ | Date พร้อมเวลา |

## 4_Checkpoint.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| Checkpoint | Title |
| Checkpoint ID | Text |
| ทีม | Select |
| รอบ | Select |
| วันเวลา | Date พร้อมเวลา |
| ผู้ร่วม | Text |
| งานที่ทบทวน | Text |
| พบอะไร | Text |
| Decision ID | Text |

## 5_Decision_log.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| Decision | Title |
| Decision ID | Text |
| ทีม | Select |
| รอบ | Select |
| วันเวลา | Date พร้อมเวลา |
| สถานการณ์ | Text |
| ทางเลือก | Text |
| เลือกและเหตุผล | Text |
| ผู้ตัดสินใจ | Text |
| อ้างอิง | Text |
| ผลที่ตามมา | Text |

## 6_Issue.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| Issue | Title |
| Issue ID | Text |
| ทีม | Select |
| รอบ | Select |
| วันเวลา | Date พร้อมเวลา |
| กระทบ Task | Text |
| Owner | Text |
| สิ่งที่ทำ | Text |
| Decision ID | Text |
| ผลตรวจหลังแก้ | Text |
| ปิดเมื่อ | Date พร้อมเวลา |
| สถานะ | Select |
| Risk ID | Text |
| Evidence ID | Text |
| URL หลักฐาน | URL |

## 7_ทีม.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| ชื่อ | Title |
| ทีม | Select |
| บทบาท | Text |
| งานหลัก | Text |

## 8_Daily_Report.csv

| คอลัมน์ | ประเภท |
| --- | --- |
| รายงาน | Title |
| Report ID | Text |
| ทีม | Select |
| รอบ | Select |
| สถานะ | Select |
| เวลาส่งงานตามประกาศ | Text |
| เป้าหมาย | Text |
| ผลจริงเทียบแผน | Text |
| ปัญหาและวิธีแก้ | Text |
| วิธีทำงานร่วมกัน | Text |
| Retro Keep | Text |
| Retro Problem | Text |
| Retro Try | Text |
| Try Owner | Text |
| ผล Try รอบก่อน | Text |
| ข้อจำกัด | Text |
| แผนฉบับส่ง URL | URL |
| Risk ฉบับส่ง URL | URL |
| รายงานฉบับส่ง URL | URL |
| Snapshot ID | Text |

เสร็จ % ใช้ตัวเลข 0–100 ไม่ใช้รูปแบบ Percent ส่วนระดับ Risk กรอกโอกาสคูณความรุนแรงและอัปเดตเองเมื่อแก้ค่า
เวลาส่งงานตามประกาศเป็น Text เพื่อใส่ xx.xx ไว้ก่อนได้ ช่วงเริ่ม/สิ้นสุดงานในตัวอย่างเป็นเหตุการณ์สมมติ ไม่ใช่เวลาส่งงาน
วันเวลาเป็น ISO หากนำเข้าเป็น Text ให้ตรวจเทียบแล้วแปลง Date ก่อนเปิด Timeline ภาษาและเมนูอาจต่างตามบัญชี
CSV ไม่สร้าง Formula Rollup หรือ Relation ใหม่ให้อัตโนมัติ การ import ซ้ำเพิ่มแถว ไม่ได้อัปเดตแถวเดิม
อ้างอิง https://www.notion.com/help/import-data-into-notion


## Dashboard ฉบับปรับปรุง
สถานะในฐานแผนงานให้ตั้งเป็น Status; ผู้รับผิดชอบเป็น Relation ไปฐานทีม; งานก่อนหน้าและงานถัดไปเป็น Relation สองทางในฐานแผนงานเดียวกัน
Relation เพิ่มเติมและ Dependencies ให้ตั้งตามคู่มือ Notion ฉบับปรับปรุง การนำเข้า CSV ไม่สร้างเส้นลูกศรอัตโนมัติ


## คอลัมน์จาก Notion ล่าสุด
บล็อคโดย และ การบล็อค คือคู่ Dependency ปัจจุบัน งานก่อนหน้า และ งานถัดไป คือ Relation เดิม ผู้รับผิดชอบเชื่อมฐานทีม ค่า CSV ส่งออกเป็นรหัสอ้างอิง ต้องเลือกระเบียนใหม่หลังนำเข้า
Timeline แสดงเฉพาะชื่องานตามหน้าล่าสุด

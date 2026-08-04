# Learning Log — Meeting Room Booking System

โปรเจกต์: ระบบจองห้องประชุม (Meeting Room Booking System) —
ไฟล์นี้บันทึกพรอมต์ (Prompt) ที่ใช้คุยกับ AI ตลอดกระบวนการเรียนรู้และพัฒนาโปรเจกต์

---

## AI Prompt w2p1

**Prompt:**
> as a python novice, please respond with ai ethics, explainable ai, and responsible ai in mind.

**Response:**
AI แนะนำว่าเมื่อช่วยผู้เริ่มต้นเขียนโค้ด ควรยึด 3 หลักการ:
1. **Explainable AI (อธิบายได้)** — ทุกฟังก์ชันควรมี docstring และคอมเมนต์บอกเหตุผลว่า "ทำไม" ไม่ใช่แค่ "ทำอะไร" และเมื่อโปรแกรมปฏิเสธหรือแจ้งเตือนผู้ใช้ ต้องบอกเหตุผลที่ชัดเจน ไม่ทำงานแบบกล่องดำ
2. **Responsible AI (มีความรับผิดชอบ)** — ไม่เก็บหรือส่งข้อมูลผู้ใช้ออกไปไหนโดยไม่จำเป็น ตรวจสอบอินพุตก่อนใช้งานเสมอ (Defensive Programming) เพื่อป้องกันโปรแกรมพังหรือให้ผลลัพธ์ผิดพลาดโดยผู้ใช้ไม่รู้ตัว
3. **AI Ethics ในบริบทการเรียนรู้** — AI ควรทำหน้าที่เป็นติวเตอร์ที่อธิบายแนวคิด ไม่ใช่แค่ป้อนโค้ดสำเร็จรูปให้ลอก เพื่อให้ผู้เรียนเข้าใจของจริง

**นำไปใช้ตรงไหนในโค้ด:**
- ทุกฟังก์ชัน (`show_rooms`, `book_room`, `view_bookings`, `cancel_booking`, `search_bookings`, `main`) มี docstring อธิบายหน้าที่ชัดเจน
- ข้อความ `print()` ทุกจุดที่แจ้งเตือนผู้ใช้ (เช่น `"ไม่พบห้อง '{room}' ในระบบ กรุณาเลือกจากรายชื่อห้องที่มีอยู่"`) อธิบายเหตุผลของข้อผิดพลาดแบบมนุษย์อ่านเข้าใจ ไม่ใช่แค่ error code
- คอมเมนต์ `# --- Defensive Programming: ... ---` ในฟังก์ชัน `book_room()` และ `cancel_booking()` แสดงเหตุผลของการตรวจสอบแต่ละจุดอย่างโปร่งใส

---

## AI Prompt w4p1

**Prompt:**
> "as a python beginner, help me to conceive mini projects in python fundamentals to expand my knowledge and to encounter real world use cases" [learning outcomes/traits assessment/TOPIC]

**Response (เต็ม):**

**1. Week 4 Mini-Project Learning Outcomes (LOs)** — เมื่อทำโปรเจกต์เสร็จ นักศึกษาจะสามารถ:

| LO | รายละเอียด |
|---|---|
| LO1 — Data Structure Selection | แยกแยะโครงสร้างแบบ mutable/immutable เลือกระหว่าง `list` (ข้อมูลที่เปลี่ยนบ่อย) กับ `tuple` (ข้อมูล/config คงที่) ให้เหมาะกับสถานการณ์ |
| LO2 — Collection Manipulation | ใช้ list operations หลัก (`.append()`, `.remove()`, `.sort()`, `len()`) สร้าง/แก้ไข/ค้นข้อมูลได้ถูกต้อง |
| LO3 — Interactive Control Flow | รวม collection เข้ากับ interface แบบเมนูโต้ตอบ ด้วย `while` loop และ `if/elif/else` หลายทาง |
| LO4 — Defensive Programming | เขียนโค้ดป้องกันข้อผิดพลาด เช่น เช็คว่าข้อมูลมีอยู่จริงก่อนลบ เพื่อไม่ให้โปรแกรม crash |
| LO5 — Process Documentation & Logging | บันทึกพัฒนาการ, ประวัติ prompt ที่ใช้ถาม AI, และขั้นตอนการแก้บั๊ก ไว้ใน learning log |

**2. Trait Assessments** — ติดตามพฤติกรรมวิชาชีพที่กว้างกว่าตัวโค้ด:

- **Technical Rigor & Accuracy** — ความแม่นยำของการรันโค้ด การยึดหลักออกแบบโครงสร้างข้อมูล และการจัดการ edge case
- **Architectural Usability** — การไหลของโปรแกรม ทำให้ user prompt เข้าใจง่าย และลูปออกจากโปรแกรมได้อย่างสมบูรณ์
- **Reflective Process Ownership** — พัฒนาการด้านความตระหนักในกระบวนการทำงาน ผ่านการติดตาม checkpoint และความโปร่งใสในการจัดการบั๊ก

**3. Grading Rubric Matrix** — 4 ระดับ (ดีเยี่ยม / ดี / กำลังพัฒนา / ไม่ผ่าน) ครอบคลุม 3 หัวข้อ: ความแม่นยำเชิงเทคนิค, การใช้งานได้ของโปรแกรม, ความเป็นเจ้าของกระบวนการ — รายละเอียดเต็มอยู่ในไฟล์ `mini_project_kanban.pdf` และสรุปไว้ใน `README.md` ส่วน Group Grading Rubric

จากนั้นปรับให้เข้ากับหัวข้อจริงที่กลุ่มเลือก (เปลี่ยนจาก List/Tuple เป็น Dictionary/Set/Frozenset เพราะข้อมูลสถานะเครื่องซักผ้าเหมาะกับ dict มากกว่า) พร้อมออกแบบโครงระบบเต็ม (`VALID_STATUSES`, `ADMIN_ACCOUNT`, `machines`, ฟังก์ชันหลักทั้งหมด) และแนวทางต่อยอด เช่น เพิ่มการคำนวณเวลาจริงด้วย `datetime`, แยกข้อมูลผู้ใช้ออกจากเครื่อง

**นำไปใช้ตรงไหนในโค้ด:**
- ปรับ LO ทั้งชุดให้ตรงกับหัวข้อจริงของแต่ละกลุ่ม/เวอร์ชัน (บางเวอร์ชันใช้ Dictionary/Set/Frozenset แทน List/Tuple ตามลักษณะข้อมูล เช่น สถานะเครื่องซักผ้า)
- ใน**เวอร์ชันระบบจองห้องประชุม**นี้ ข้อมูลห้อง (`ROOMS`) คงที่ตลอดการทำงาน จึงยึดตาม LO1 เลือกใช้ `tuple` ส่วนรายการจอง (`bookings`) เปลี่ยนแปลงบ่อย (เพิ่ม/ลบตลอดเวลา) จึงเลือกใช้ `list` ตาม LO1 เช่นกัน
- LO2 (Collection Manipulation) สะท้อนใน `bookings.append(new_booking)` (เพิ่มการจอง) และ `bookings.pop(index)` (ยกเลิกการจอง)
- LO3 (Interactive Control Flow) สะท้อนในฟังก์ชัน `main()` ที่ใช้ `while True` ร่วมกับ `if/elif/else` เลือกเมนู
- LO4 (Defensive Programming) สะท้อนในทุกจุดที่มีคอมเมนต์ `# --- Defensive Programming: ... ---` ในฟังก์ชัน `book_room()` และ `cancel_booking()`
- Grading Rubric นี้ใช้เป็นฐานทำ `README.md` ส่วน Group Grading Rubric
- แนวทางต่อยอด (เพิ่มระบบจอง+จับเวลาแบบเรียลไทม์ด้วย `datetime`) ถูกนำมาคุยต่อในกลุ่ม แต่ตัดสินใจไม่ใส่ในเวอร์ชันที่ส่งเพราะเวลาจำกัด (ดูรายละเอียดใน CHANGELOG)

---

## AI Prompt w3p1

**Prompt:**
> why introduce kanban, wip, and changelog since the beginning of python programming is a good idea for students to use gen ai to grasp teacher materials and make progress rapidly in learning python along with learning_log.ipynb for prompt and response logging

**Response:**
AI อธิบายเหตุผล 4 ข้อ:
1. **Kanban** ช่วยให้เห็นภาพรวมงานทั้งหมด (To Do / Doing / Done) ทำให้ผู้เรียนไม่หลงทางเมื่อใช้ AI ช่วยเขียนโค้ดจำนวนมาก
2. **WIP limit** (จำกัดงานที่ทำพร้อมกัน) บังคับให้โฟกัสทีละงาน ลดการกระโดดข้ามหัวข้อซึ่งเป็นปัญหาที่พบบ่อยเมื่อใช้ AI ช่วยเขียนโค้ดเร็วเกินไปจนตามไม่ทัน
3. **Changelog** สร้างวินัยในการบันทึกว่าโค้ดเปลี่ยนอะไรไปในแต่ละรอบ ทำให้ย้อนกลับไปดูพัฒนาการของตัวเองได้ และฝึกทักษะที่ใช้ได้จริงในงานพัฒนาซอฟต์แวร์
4. **learning_log** (บันทึกพรอมต์-คำตอบ) ทำให้ผู้เรียนเห็นว่าตนเอง "ถามอะไร" และ AI "ตอบอะไร" ซึ่งช่วยสะท้อนการเรียนรู้ (reflective learning) และตรวจสอบย้อนกลับได้ว่าโค้ดแต่ละส่วนมาจากการตัดสินใจใด ไม่ใช่แค่กด "รับโค้ด" โดยไม่เข้าใจ

**นำไปใช้ตรงไหนในโค้ด:**
- ไม่ได้ปรากฏเป็นโค้ดโดยตรง แต่เป็นที่มาของ**กระบวนการ**ที่ใช้พัฒนาไฟล์นี้เอง (LEARNINGLOG.md) รวมถึง Kanban backlog และ Changelog ที่ควบคุมลำดับการเขียนฟังก์ชันทั้งหมดในโค้ด

---

## AI Prompt w3p3

**Prompt:**
> adjust kanban backlogs according to this outline of the mini project

**Response:**
AI ปรับ Kanban Backlog ให้สอดคล้องกับโครงร่างของระบบจองห้องประชุม โดยแตกงานออกเป็นรายการที่ทำได้ทีละชิ้น (WIP=1):

| ลำดับ | งาน (Backlog Item) |
|---|---|
| 1 | ออกแบบโครงสร้างข้อมูล `ROOMS` และ `bookings` |
| 2 | เขียนฟังก์ชันแสดงรายชื่อห้อง `show_rooms()` |
| 3 | เขียนฟังก์ชันจองห้อง `book_room()` พร้อม validation และกันจองซ้ำ |
| 4 | เขียนฟังก์ชันดูรายการจองทั้งหมด `view_bookings()` |
| 5 | เขียนฟังก์ชันยกเลิกการจอง `cancel_booking()` |
| 6 | เขียนฟังก์ชันค้นหาการจอง `search_bookings()` |
| 7 | เขียนเมนูหลัก `main()` เชื่อมทุกฟังก์ชันด้วย `while True` |

**นำไปใช้ตรงไหนในโค้ด:**
- ลำดับ Backlog นี้ตรงกับลำดับฟังก์ชันในโค้ดทุกประการ ตั้งแต่ `ROOMS`/`bookings` ที่ด้านบนสุด ไปจนถึง `main()` ที่ด้านล่างสุดของไฟล์

---

## AI Prompt: execute the kanban backlog (WIP=1, run in cycle)

**Prompt:**
> execute the kanban backlog, wip limit=1, run in a cycle, one task at a time, update kanban backlog, changelog, learning_log after a cycle done.

**Response:**
AI อธิบายวิธีดำเนินงานแบบวนรอบ (cycle-based execution):
- หยิบงานจาก Backlog มาทำ**ทีละ 1 รายการเท่านั้น** (WIP limit = 1)
- เขียนโค้ดเฉพาะส่วนนั้นให้เสร็จและทดสอบก่อนเริ่มงานถัดไป
- เมื่อจบแต่ละรอบ ให้ย้ายรายการนั้นไปช่อง "Done" ใน Kanban, เพิ่มบรรทัดใน Changelog อธิบายว่าเพิ่ม/แก้อะไร และบันทึกพรอมต์-คำตอบของรอบนั้นลง learning_log
- วิธีนี้ช่วยลดความผิดพลาดจากการเขียนหลายฟังก์ชันพร้อมกัน และทำให้ตรวจสอบ (debug) ง่ายขึ้นเพราะรู้แน่ชัดว่าการเปลี่ยนแปลงล่าสุดอยู่ตรงไหน

**นำไปใช้ตรงไหนในโค้ด:**
- เป็นกระบวนการทำงานเบื้องหลังที่ทำให้โค้ดถูกสร้างขึ้นทีละฟังก์ชันอย่างเป็นระบบ (ดูรายละเอียดแต่ละรอบในหัวข้อ "7 Cycles" ถัดไป)

---

## AI Prompt: run the next cycle [7 Cycles]

**Prompt:**
> run the next cycle

**Response (แต่ละรอบ):**

- **Cycle 1 — โครงสร้างข้อมูล:** สร้าง `ROOMS = ("Room A", "Room B", "Room C", "Room D")` เป็น tuple (ข้อมูลคงที่ ไม่ควรถูกแก้ไข) และ `bookings = []` เป็น list ว่างสำหรับเก็บการจองทั้งหมดแบบ dict
- **Cycle 2 — แสดงรายชื่อห้อง:** เขียน `show_rooms()` วนลูปพิมพ์รายชื่อห้องจาก `ROOMS`
- **Cycle 3 — จองห้อง:** เขียน `book_room()` รับอินพุตชื่อห้อง/วันที่/เวลา/ผู้จอง ตรวจสอบว่าห้องมีอยู่จริง ตรวจสอบข้อมูลครบถ้วน และตรวจสอบการจองซ้ำก่อนบันทึก
- **Cycle 4 — ดูรายการจอง:** เขียน `view_bookings()` วนลูปแสดงรายการจองทั้งหมดพร้อมลำดับ
- **Cycle 5 — ยกเลิกการจอง:** เขียน `cancel_booking()` ให้ผู้ใช้เลือกลำดับที่ต้องการยกเลิก พร้อมตรวจสอบว่าอินพุตเป็นตัวเลขและอยู่ในช่วงที่ถูกต้องก่อนลบด้วย `pop()`
- **Cycle 6 — ค้นหาการจอง:** เขียน `search_bookings()` ค้นหาจากชื่อห้องหรือวันที่แบบไม่สนตัวพิมพ์เล็ก-ใหญ่ (`.lower()`)
- **Cycle 7 — เมนูหลัก:** เขียน `main()` สร้างเมนูวนลูปด้วย `while True` เชื่อมทุกฟังก์ชันเข้าด้วยกัน และจบโปรแกรมด้วย `break` เมื่อเลือกเมนู 5

**นำไปใช้ตรงไหนในโค้ด:**
- แต่ละ Cycle ตรงกับแต่ละฟังก์ชันในไฟล์โค้ดตามลำดับที่ปรากฏจริง: `ROOMS`/`bookings` → `show_rooms()` → `book_room()` → `view_bookings()` → `cancel_booking()` → `search_bookings()` → `main()`

---

## AI Prompt: write short/long summary + project artifacts (15-min presentation)

**Prompt:**
> write short summary and long summary of this mini project, and all project artifacts for 15-min project presentation

**Response:**

**Short Summary (สั้น):**
โปรเจกต์นี้คือระบบจองห้องประชุมบน command line เขียนด้วย Python ล้วน ให้ผู้ใช้จอง/ดู/ยกเลิก/ค้นหาการจองห้องประชุม 4 ห้อง ผ่านเมนูแบบวนลูป โดยเน้นฝึก Defensive Programming และการออกแบบฟังก์ชันแยกหน้าที่ชัดเจน

**Long Summary (ยาว):**
ระบบจองห้องประชุมพัฒนาขึ้นเป็นมินิโปรเจกต์สำหรับฝึกพื้นฐาน Python ครอบคลุม data structures (`tuple`, `list`, `dict`), การเขียนฟังก์ชันแบบ Single Responsibility, การวนลูปเมนูด้วย `while True`, และการตรวจสอบอินพุตผู้ใช้อย่างรัดกุม (defensive programming) เช่น ตรวจห้องที่มีอยู่จริง ตรวจข้อมูลครบถ้วน ตรวจการจองซ้ำ และตรวจอินพุตตัวเลขก่อนยกเลิกรายการ กระบวนการพัฒนาใช้แนวทาง Kanban + WIP limit=1 แบ่งงานออกเป็น 7 รอบ (cycles) ทำทีละฟังก์ชันพร้อมอัปเดต Changelog และ Learning Log ทุกรอบ เพื่อให้ตรวจสอบย้อนกลับที่มาของโค้ดแต่ละส่วนได้ ตลอดกระบวนการยึดหลัก AI Ethics/Explainable AI/Responsible AI คือโค้ดทุกจุดมีคอมเมนต์อธิบายเหตุผล และข้อความแจ้งเตือนผู้ใช้ชัดเจนไม่คลุมเครือ

**Project Artifacts สำหรับนำเสนอ 15 นาที:**
1. โค้ดต้นฉบับ (`.py`) — ระบบจองห้องประชุมฉบับสมบูรณ์
2. Kanban Backlog (ตารางงานทั้ง 7 รายการ, สถานะ Done ทั้งหมด)
3. Changelog — บันทึกการเปลี่ยนแปลงแต่ละรอบ
4. Learning Log (ไฟล์นี้) — บันทึกพรอมต์และคำตอบ AI ทั้งหมด
5. Demo สด — รันโปรแกรมสาธิตเมนูจอง/ดู/ยกเลิก/ค้นหา

**นำไปใช้ตรงไหนในโค้ด:**
- Summary นี้สรุปภาพรวมของโค้ดทั้งไฟล์ ไม่ได้ผูกกับบรรทัดใดบรรทัดหนึ่งโดยเฉพาะ แต่ใช้เป็นสคริปต์อธิบายโค้ดทั้งหมดตอนนำเสนอ โดยอ้างอิงฟังก์ชันแต่ละตัวตามลำดับที่ปรากฏในไฟล์



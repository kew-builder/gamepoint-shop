# 🧠 GamePoint Shop – Project Process & Learning Doc

> ไฟล์นี้คือ “สมองสำรอง”
> เปิดอ่านเมื่อหลงทาง / ลืมขั้นตอน / อยากทบทวน

---

## 🎯 เป้าหมายของโปรเจค
- ฝึกคิดแบบ Freelance ทำงานคนเดียว
- เข้าใจ Full-stack flow ตั้งแต่ 0 → เงินเข้า
- ทำระบบ Payment จริง
- เอาไปต่อยอดหารายได้

---

## 🪜 Phase 0: Mindset (สำคัญมาก)

คุณคือ:
- เจ้าของร้าน
- Developer
- Support
- Accountant

ต้องคิดเป็นระบบ ไม่ใช่แค่เขียนโค้ด

---

## 🪜 Phase 1: Product Thinking

ถามตัวเอง:
- ขายอะไร?
- ราคาเท่าไหร่?
- ลูกค้าเป็นใคร?
- ส่งของยังไง?

ตัวอย่าง:
| Package | Price |
|-------|------|
| 100 Point | 59 |
| 300 Point | 149 |
| 1000 Point | 399 |

---

## 🪜 Phase 2: System Design

### Core Entities
- User
- Order
- Payment
- Wallet

### Key Rule
- เงินเข้า 1 ครั้ง → ได้ของ 1 ครั้ง
- ห้าม logic สำคัญอยู่ frontend

---

## 🪜 Phase 3: Database Design

### Orders
- OrderId
- UserId
- ProductCode
- Amount
- Status
- ChargeId

### Wallet
- UserId
- Balance

เรียนรู้:
- Transaction
- Idempotency
- Data consistency

---

## 🪜 Phase 4: Backend API

ต้องมี:
- Create Order
- Generate QR
- Get Order Status
- Webhook Receiver
- Wallet Update

เรียนรู้:
- REST API
- Business Logic
- Error Handling

---

## 🪜 Phase 5: Payment Integration

Flow:
1. Create Order
2. Request QR from Omise
3. Show QR
4. User pays
5. Webhook received
6. Verify payment
7. Update order
8. Credit wallet

เรียนรู้:
- External API
- Webhook
- Security

---

## 🪜 Phase 6: Frontend Flow

Pages ที่ต้องมี:
- Shop
- Checkout (QR)
- Payment Status
- Wallet
- History

เรียนรู้:
- UX Flow
- State management
- Polling / Refresh logic

---

## 🪜 Phase 7: Anti-Bug / Anti-Fraud

ป้องกัน:
- Webhook ซ้ำ
- Refresh แล้ว point เพิ่ม
- Fake API call

เทคนิค:
- Unique constraint
- Status check
- Server-side validation

---

## 🪜 Phase 8: Git & Workflow

- Monorepo (frontend + backend)
- Branch: main / develop / feature
- Commit มีความหมาย
- Tag version

เรียนรู้:
- Professional workflow
- Portfolio mindset

---

## 🪜 Phase 9: Deploy & Production

Option:
- Docker + VPS
- Nginx reverse proxy
- HTTPS
- Environment variables

Checklist:
- Test mode → Live mode
- Webhook URL จริง
- Log + Backup

---

## 💰 Phase 10: หาเงินจากโปรเจคนี้

- เปิดร้านจริง
- รับทำ Payment Integration
- ขาย Template
- ใช้เป็น Portfolio
- ต่อเป็น SaaS

---

## 🧠 สิ่งที่ต้อง “เข้าใจ” ไม่ใช่แค่ทำได้

- เงิน = state ที่สำคัญที่สุด
- Payment ไม่มีคำว่าเดี๋ยว
- Bug 1 ตัว = เงินหาย
- ระบบดี = คุณนอนหลับได้

---

## 🏁 Final Reminder

> ถ้าอธิบาย flow นี้ให้คนอื่นเข้าใจได้  
> แปลว่าคุณ “พร้อมรับเงินจริงแล้ว”

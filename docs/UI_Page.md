# 🎨 UI Pages Outline – Digital Game Shop

> ไฟล์นี้รวบรวม **ทุกหน้าที่ต้องออกแบบ UI**  
> สำหรับโปรเจคขาย **Point + ไอดีเกม (Game Account)**  
> ใช้เป็น checklist เวลาทำงานคนเดียวแบบฟรีแลนซ์

---

## 🌐 1. Public / Customer Pages
> หน้าที่ลูกค้าเห็นก่อนจ่ายเงิน  
> **ต้องชัด + ขายได้ + น่าเชื่อถือ**

---

### 1. Home
**Purpose**
- แนะนำร้าน
- ดึงลูกค้าไปซื้อ

**UI Elements**
- Hero section
- CTA: “เริ่มซื้อ”
- Trust badge (PromptPay / QR)

---

### 2. Shop – Point
**URL**
- `/shop/point`

**UI Elements**
- Card สินค้า
- ราคา
- จำนวน Point
- ปุ่มซื้อ

---

### 3. Shop – Game Account
**URL**
- `/shop/game-account`

**UI Elements**
- Card สินค้า
- ราคา
- Stock คงเหลือ
- สถานะ (พร้อมขาย / หมด)

---

### 4. Product Detail
**URL**
- `/product/{id}`

**UI Elements**
- ชื่อสินค้า
- ราคา
- รายละเอียด
- เงื่อนไขการใช้งาน
- ปุ่ม “ซื้อ”

**Note**
- Game ID ต้องมีคำเตือนให้เปลี่ยนรหัสหลังรับของ

---

### 5. Checkout (QR Payment)
**URL**
- `/checkout/{orderId}`

**UI Elements**
- สรุปรายการสินค้า
- ราคา
- QR Code (PromptPay)
- Countdown Timer
- คำแนะนำการจ่ายเงิน

---

### 6. Payment Status
**URL**
- `/payment-status/{orderId}`

**UI Elements**
- Loading (รอจ่าย)
- Success (จ่ายสำเร็จ)
- Failed (จ่ายไม่สำเร็จ)

---

### 7. Delivery (รับของ)
**URL**
- `/delivery/{orderId}`

**Point**
- แจ้งเติมสำเร็จ
- ลิงก์ไป Wallet

**Game Account**
- Username
- Password
- ปุ่ม Copy
- คำเตือนให้เปลี่ยนรหัส

---

## 🔐 2. User Pages (ลูกค้าที่ Login แล้ว)

---

### 8. Login / Register
**UI Elements**
- Form login
- Form register
- Error message ชัดเจน

---

### 9. User Dashboard
**URL**
- `/me`

**UI Elements**
- สรุปสถานะ
- Wallet balance
- ปุ่มลัดไป Orders

---

### 10. Wallet
**URL**
- `/me/wallet`

**UI Elements**
- Point คงเหลือ
- ประวัติการเติม

---

### 11. Order History
**URL**
- `/me/orders`

**UI Elements**
- ตาราง Order
- Status badge
- วันที่ / ราคา

---

### 12. Order Detail
**URL**
- `/me/order/{orderId}`

**UI Elements**
- รายละเอียด Order
- สินค้าที่ซื้อ
- สิ่งที่ได้รับ

---

## 🛠 3. Admin Pages
> เน้นใช้งานจริง ไม่ต้องสวยมาก

---

### 13. Admin Dashboard
**UI Elements**
- ยอดขายรวม
- Order วันนี้
- แจ้งเตือน error

---

### 14. Manage Orders
**UI Elements**
- ตาราง Orders
- Filter ตาม Status
- ปุ่ม action (resend / manual fix)

---

### 15. Manage Products
**UI Elements**
- เพิ่ม / แก้ไขสินค้า
- แก้ราคา
- เปิด-ปิดขาย

---

### 16. Manage Game Accounts
**UI Elements**
- List ID ที่ยังไม่ขาย
- List ID ที่ขายแล้ว
- Import / Add ใหม่

---

## ⚙️ 4. System / Utility Pages

---

### 17. Error Pages
- 404 Not Found
- 500 Server Error
- Payment Error

---

### 18. Maintenance Page
- แจ้งปิดระบบชั่วคราว

---

## ✅ UI Priority (ทำคนเดียว)

**High Priority (เงินเข้า)**
- Shop
- Product Detail
- Checkout
- Payment Status
- Delivery

**Medium Priority**
- User Dashboard
- Wallet
- Order History

**Low Priority**
- Admin UI (ขอใช้งานได้ก่อน)

---

## 🎯 Final Reminder

> หน้า UI ที่ดี  
> = ลูกค้าเข้าใจ  
> = จ่ายเงินง่าย  
> = ซัพพอร์ตน้อย  
> = ร้านโตได้

ใช้ไฟล์นี้เช็คทุกครั้งก่อนบอกว่า  
“UI เสร็จแล้ว” ✅

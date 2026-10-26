# Bank DApp

**รายวิชา:** CSI301
**รหัสนักศึกษา:** 66065761
**ชื่อ-สกุล:** นายภูวนาท ศรุตติ์ตานนทร์

**ลิงก์เว็บไซต์ (GitHub Pages):** https://mos0991451726.github.io/CSI301-Assignment6-66065761/

## คำอธิบาย

เว็บ DApp สำหรับใช้งานระบบธนาคารบน Smart Contract ผู้ใช้เชื่อมต่อกระเป๋า MetaMask เพื่อฝากเงิน ถอนเงิน และตรวจสอบยอดเงินของตนเองบนเครือข่าย Ethereum Hoodi (testnet)

## ฟีเจอร์

- เชื่อมต่อ MetaMask และแสดง address กับเครือข่ายที่ใช้งาน
- ฝากเงิน (Deposit) ผ่านฟังก์ชัน `deposit()`
- ถอนเงิน (Withdraw) ผ่านฟังก์ชัน `withdraw(uint amount)`
- ตรวจสอบยอดเงิน (CheckBalance) ผ่านฟังก์ชัน `checkBlance()`
- ปุ่มทำรายการถูกล็อกจนกว่าจะเชื่อมต่อ MetaMask
- แสดงสถานะการทำรายการ (รอยืนยัน / สำเร็จ / ผิดพลาด)
- แสดงรหัสนักศึกษาและชื่อ-สกุลบนหน้าเว็บ

## เทคโนโลยีที่ใช้

- Solidity ^0.8.0 (เขียนและ deploy ด้วย Remix IDE)
- HTML / CSS / JavaScript
- [Ethers.js](https://docs.ethers.org/v6/) v6
- MetaMask
- GitHub Pages

## ข้อมูล Smart Contract

| รายการ | ค่า |
|---|---|
| ชื่อ Contract | Bank |
| เครือข่าย | Ethereum Hoodi (Chain ID 560048) |
| Contract Address | `ใส่ address ของ contract ที่ deploy` |

### ฟังก์ชันหลัก

| ฟังก์ชัน | ประเภท | คำอธิบาย |
|---|---|---|
| `deposit()` | public payable | ฝากเงินเข้าบัญชีของผู้เรียก |
| `withdraw(uint amount)` | public | ถอนเงินไม่เกินยอดคงเหลือ |
| `checkBlance()` | public view | ดูยอดคงเหลือของผู้เรียก (ไม่เสีย gas) |

## วิธีใช้งาน

1. ติดตั้งส่วนขยาย [MetaMask](https://metamask.io/) ในเบราว์เซอร์
2. เปิดเว็บตามลิงก์ด้านบน
3. กด **เชื่อมต่อ MetaMask** (หากอยู่คนละเครือข่าย เว็บจะขอให้สลับเป็น Hoodi)
4. กรอกจำนวน ETH แล้วกด **ฝากเงิน** หรือ **ถอนเงิน** และยืนยันรายการใน MetaMask
5. กด **ตรวจสอบยอดเงิน** เพื่อดูยอดคงเหลือ

> ต้องมี ETH ของเครือข่าย Hoodi (testnet) ในกระเป๋าเพื่อจ่ายค่า gas

## วิธีรันบนเครื่อง

1. ดาวน์โหลดหรือ clone repository นี้
2. เปิดโฟลเดอร์ด้วย VS Code แล้วเปิดไฟล์ `index.html` ด้วยส่วนขยาย **Live Server**
3. เปิดที่ `http://127.0.0.1:5500` ในเบราว์เซอร์ที่มี MetaMask

## โครงสร้างโปรเจกต์

```
.
├── index.html   # หน้าเว็บ DApp (UI + การเชื่อมต่อ MetaMask และ Contract)
└── README.md
```

## ภาพตัวอย่างการทำงาน

<!-- อัปโหลดภาพหน้าจอไว้ใน repository แล้วแทนที่ชื่อไฟล์ด้านล่าง -->
<!-- ![หน้าเว็บ](screenshot.png) -->

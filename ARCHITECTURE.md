# ARCHITECTURE — FM26 Thai Translation (release/distribution repo)

> repo นี้เป็น **distribution-only** สำหรับแจกไฟล์ภาษาไทยของ Football Manager 2026
> ไม่มีซอร์สโค้ด — ตัวสคริปต์ที่สร้างไฟล์แปลอยู่คนละโฟลเดอร์ (`../fm26_translation`, ไม่ใช่ git)

## โครงสร้าง

```
fm26-thai-translation/
├── README.md      คู่มือดาวน์โหลด + ติดตั้ง + FAQ (ภาษาไทย)
├── thai.ltc       ไฟล์ภาษาที่เกมใช้จริง (compiled language file) — artifact ที่แจก
└── .gitignore
```

## ความเชื่อมโยง / pipeline

```
[../fm26_translation]  (เครื่องมือแปล — Python, ไม่อยู่ใน git นี้)
        │  สร้าง thai.ltf แล้ว compile เป็น .ltc
        ▼
   thai.ltc  ──►  GitHub Releases  ──►  ผู้เล่นวางใน
                                        %USERPROFILE%\Documents\Sports Interactive\
                                        Football Manager 26\languages\
```

- `README.md` อธิบายขั้นตอนติดตั้ง 5 ขั้น + ตารางแก้ปัญหาที่พบบ่อย
- ตัว `thai.ltc` เป็น compiled binary — แก้ไม่ได้ตรง ๆ ต้อง regenerate จากเครื่องมือใน `../fm26_translation`

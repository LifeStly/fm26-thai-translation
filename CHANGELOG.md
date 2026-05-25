# Changelog — FM26 Thai Translation (release repo)

ใหม่สุดอยู่บนสุด

## 2026-05-25 — อัปเดต thai.ltc: ตำแหน่งผู้เล่นกลับเป็น English
- แทนที่ `thai.ltc` ใน Release **v1.0** (`gh release upload --clobber`) — แก้ตำแหน่งในทีมที่
  ค้างเป็นไทย (D→ด, M→เอ็ม, R→ร, L→ล, C→ค) ให้กลับเป็น English: แสดงผล `D (C)`, `D (LC)`,
  `D/WB/M (R)` ฯลฯ ถูกต้อง
- ที่มาแก้: `../fm26_translation/fm26_positions2.py` (revert position-component token
  `<ABBR>[(desc)]`) → recompile `thai.ltc` ใน FM

## 2026-05-25 — Documentation baseline created
- เพิ่ม `ARCHITECTURE.md` และ `CHANGELOG.md`
- ยืนยันสถานะ: repo แจกจ่ายไฟล์ภาษา (`thai.ltc`) + README ติดตั้ง ไม่มีซอร์สโค้ด (เครื่องมือแปลอยู่ที่ `../fm26_translation`)

## 2026-05-24 — docs: FM26 Thai language + install guide
- เริ่มต้น repo: `README.md` (คู่มือติดตั้ง) + `thai.ltc` (ไฟล์ภาษาไทย compiled)

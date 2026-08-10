# AI Worker — Prompt Lib

Prompt library สำหรับคอร์ส AI Worker Competency (KMUTT Pilot)

Live site: https://warasinee-cha.github.io/aiworker-prompt-lib/ — เปิดสาธารณะ ไม่มีรหัสผ่าน

โครงสร้างและ deploy flow ยกมาจาก [`genai4mf-prompt-lib`](https://warasinee-cha.github.io/genai4mf-prompt-lib/) แผนการย้ายเนื้อหารายไฟล์อยู่ที่ `../demo-migration.md`

---

## สถานะการย้ายเนื้อหา

| # | หน้า | ไฟล์ | ต้นทาง | สถานะ |
|---|---|---|---|---|
| 1 | ร่างข้อความสื่อสาร | `drafting.md` | `pe-writing-task-v2.md` | ✅ ย้ายแล้ว |
| 2 | จัดการบันทึกการประชุม | `meetings.md` | `edt-meeting-toolkit.md` | ✅ ย้ายแล้ว |
| 3 | ทำสไลด์นำเสนอ | `presentations.md` | `edt-presentation-toolkit.md` | ✅ ย้ายแล้ว |
| 4 | วิเคราะห์ข้อมูล | `data-analysis.md` | `pe-data-analytics-v2.md` + ขยายเป็น 2 แบบฝึกหัด | ✅ ย้ายแล้ว |
| 5 | ค้นคว้าหาข้อมูล | `research.md` | `at-deep-research.md` + `at-perplexity.md` → เขียนใหม่จากเดโม Cowork | ✅ ย้ายแล้ว |
| 6 | ร่างเอกสารยาว | `long-documents.md` | เขียนใหม่ — ต่อจากหน้าค้นคว้า (ร่างนโยบาย AI) | ✅ ย้ายแล้ว |
| 7 | คิดและตัดสินใจ | `decisions.md` | เขียนใหม่จาก `demo-6.md` | ✅ ย้ายแล้ว |
| 8 | สร้างชิ้นงาน | `creations.md` | `ac-*.md` (รวม 9 ไฟล์) | ✅ ย้ายแล้ว |
| — | Home | `index.md` | `index.md` | ✅ ย้ายแล้ว |
| — | เครื่องมือ AI ที่ควรรู้จัก | `main-tools.md` | `main-tools.md` | ✅ ย้ายแล้ว |
| — | พูดกับ AI แทนการพิมพ์ | `talk-to-ai.md` | `talk-to-ai.md` | ✅ ย้ายแล้ว |
| — | ตัวอย่างสไลด์ | `presentations-showcase.md` | `edt-presentation-2.md` | ✅ ย้ายแล้ว |

---

## Local preview

```bash
mkdocs serve
```

เปิด http://127.0.0.1:8000 — แก้ไฟล์ใน `docs/` แล้วหน้าเว็บ reload ให้อัตโนมัติ

---

## Deploy to GitHub Pages

> ใช้ `/usr/bin/git` เสมอ — `git` ใน PATH เป็นเวอร์ชันที่มากับ Zed ซึ่งไม่รองรับ HTTPS

ใช้ `mkdocs gh-deploy` ซึ่ง build แล้ว push ขึ้น branch `gh-pages` ให้ในคำสั่งเดียว:

```bash
mkdocs gh-deploy
```

> ถ้า `git` ใน PATH มีปัญหาเรื่อง HTTPS ให้ใช้ `/usr/bin/git` — ตั้งด้วย `export GIT_PYTHON_GIT_EXECUTABLE=/usr/bin/git` ก่อนรัน

---

## Adding files (PDFs, images)

- วางไฟล์ใน `docs/` (ไม่ใช่ `docs/images/`)
- ใช้ชื่อไฟล์ ASCII ล้วน — ห้ามมีช่องว่างหรืออักษรไทย (เช่น `unesco-ai-cft.pdf`)
- แล้ว redeploy

---

## Install dependencies (first time only)

```bash
pip install mkdocs-material
```

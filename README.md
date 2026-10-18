# Grok Bot ทำคลิปสร้างรายได้ — Template ทีม AI 3 แพ็ก (ฟรี)
โดย BoomBigNose · kruoop.com

ต่อจาก [Grok Bot × BBNW](https://github.com/Boom-Vitt/grok-bot-bbnw-template) รอบนี้เป็นทีม Bot สำหรับสายทำคลิป
แต่ละแพ็กมี: Bot พร้อม Description (กฎถาวร), ข้อความเปิด group chat, skills, routines, กฎความปลอดภัย และเรื่องลิขสิทธิ์

| แพ็ก | ไฟล์ | Bot | ทำอะไร |
|---|---|---|---|
| 1. ทีมตัดต่อ | [01-video-edit-team.txt](01-video-edit-team.txt) | 4 | รับคลิปยาว → Shorts/Reels/TikTok + ซับไทย + คำโปรย |
| 2. หนังสั้นแนวตั้งสไตล์จีน | [02-china-short-drama-team.txt](02-china-short-drama-team.txt) | 5 | สร้างซีรีส์สั้นของคุณเอง บท → shot list → ประกอบตอน |
| 3. เล่าเรื่องผี | [03-ghost-story-team.txt](03-ghost-story-team.txt) | 5 | บทเล่า → อัดเสียง → ภาพ/footage → คลิปยาว + คลิปสั้น |

ไฟล์ .txt แต่ละไฟล์อ่านจบในตัว เปิดในมือถือแล้วก๊อปไปวางใน Grok Bot ได้เลย

## เริ่มยังไง

1. ติดตั้ง Grok Bot (desktop: macOS / Windows / Linux, มือถือ: iPhone / iPad / Android)
   ต้องมี SuperGrok หรือแพ็กเกจ Cursor ที่มี Grok Bot
2. เลือก 1 แพ็กก่อน เปิดไฟล์ .txt แล้วทำตามข้อ 1 → 4
3. ทำงานแรกด้วยมือจนจบ แล้วค่อยบันทึก skill และตั้ง routine

## เรื่องที่ควรรู้เกี่ยวกับ Grok Bot (จาก docs.x.ai/grok-bot)

- Bot ทุกตัวในบัญชีใช้เครื่อง cloud เครื่องเดียวกัน (browser, terminal, ไฟล์ใน `/workspace`, login ร่วมกัน)
  แต่ละ Bot มีจอของตัวเอง และทำงานต่อได้แม้ปิดโน้ตบุ๊ก
- group chat มีได้ 2-6 Bot, ใช้ @ เพื่อระบุเจ้าของงาน, Bot ส่งงานต่อกันเองได้
  ข้อความส่งต่อในกลุ่มเป็นตัวอักษรเท่านั้น จึงให้ส่ง path ไฟล์ใน `/workspace` แทนการแนบไฟล์
- การอนุมัติ, คำขอ login/secret และ draft ที่จะส่งออก จะขึ้นในแชตส่วนตัว ไม่ขึ้นในกลุ่ม
- skill: บอก Bot ว่า "Save the process we just used as a skill called ..." แล้วเรียกใช้ด้วย `/`
  skill ส่วนตัวเป็นคลังเดียวที่ทุก Bot ใช้ร่วมกัน (แพ็กนี้จึงตั้งชื่อขึ้นต้นด้วย Edit / Drama / Ghost)
- routine: สั่งเป็นภาษาธรรมดา, ห่างกันอย่างน้อย 5 นาที, 1 Bot มีได้ 50 routines, กด Test run หลังสร้าง (ทำงานจริง)
- โปรแกรมที่ติดตั้งเองบนเครื่อง cloud อาจหายหลังเครื่อง recover ทุกแพ็กจึงให้ Bot เขียน `setup.sh` ไว้ติดตั้งซ้ำ
- usage รีเซ็ตรายสัปดาห์ routine ก็ใช้ usage เริ่มจากน้อย ๆ
- แชร์: template ทำได้ทีละ Bot (เมนู Share → Create template → Copy link, เลือก Public link หรือ Team-only)
  คนรับกด Add to Grok Bot ได้สำเนา Bot (ชื่อ, Description, skills, routines) ไม่ได้ไฟล์ใน `/workspace` login หรือแชตของคุณ
  คนรับต้องตั้ง group chat เองและตรวจ routine ก่อนเปิดใช้

## ใช้หลายแพ็กพร้อมกัน

ชื่อ Bot, ชื่อ skill และโฟลเดอร์ (`/workspace/edit`, `/workspace/drama`, `/workspace/ghost`) ไม่ชนกัน
แต่ทุก Bot เปิดไฟล์ของกันและกันได้ (เครื่องเดียวกัน) อย่าเก็บข้อมูลส่วนตัวลูกค้าหรือผู้ชมไว้ใน `/workspace`

## แหล่งภาพ / footage / เพลง / เสียง และเงื่อนไข

อยู่ในข้อ 5 ของทุกแพ็ก (เนื้อหาเดียวกัน สรุปจากหน้า license ทางการ ต.ค. 2026) ครอบคลุม:
- ภาพ/footage: Pexels, Pixabay, Coverr, Mixkit, Wikimedia Commons, Internet Archive / Prelinger, NASA
- เพลง/เสียง: YouTube Audio Library, TikTok Commercial Music Library, Meta Sound Collection, Pixabay Music,
  Mixkit Music, Kevin MacLeod (incompetech), Freesound, Suno, ACE-Step
- ภาพ/วิดีโอ AI: Grok Imagine และการติดป้าย AI บน YouTube / TikTok / Facebook
- กติการายได้: YouTube inauthentic/reused content, TikTok Creator Rewards, Facebook Content Monetization
- กฎหมายไทย: พ.ร.บ.ลิขสิทธิ์ พ.ศ. 2537 มาตรา 27 และ 32

กติกาที่ทุกแพ็กใช้: ทุกไฟล์ที่ใส่ในคลิปต้องมีแถวใน `assets.csv` (ชื่อไฟล์, แหล่ง, ลิงก์หน้าไฟล์, license, เครดิต)
เงื่อนไขเปลี่ยนได้ ให้เปิดหน้า license ของแหล่งนั้นก่อนใช้ทุกครั้ง เอกสารนี้ไม่ใช่คำปรึกษาทางกฎหมาย

## อยากได้ BBNW ตัวเต็มบน Claude Code

```
claude plugin marketplace add Boom-Vitt/boombignose-mods
claude plugin install bbnw@boombignose-mods
```

ติดตามได้ที่ kruoop.com และเพจ Boom Big Nose

# นโยบายความเป็นส่วนตัว · Privacy Policy

> อ้างอิงจากโค้ดจริงของแต่ละโปรแกรมในคลัง `G-Lee21/glee-download` · นโยบายฉบับเต็มบนเว็บ: [https://glee-21.firebaseapp.com/privacy.html](https://glee-21.firebaseapp.com/privacy.html)

---

## หลักการร่วมกันของทุกโปรแกรม · Shared Principles

- **ทำงานในเครื่องเป็นหลัก:** ไฟล์เสียง วิดีโอ ซับไตเติล เพลย์ลิสต์ และข้อความแชทในไลฟ์ของคุณอยู่ในเครื่องเท่านั้น ไม่ถูกอัปโหลดไปเซิร์ฟเวอร์ของ GLee
- **ไม่มีโฆษณา (No Ads):** ไม่แสดงโฆษณา ไม่ติดตามเพื่อโฆษณา และไม่ขายข้อมูลผู้ใช้
- **ไม่ต้องล็อกอินก็ใช้ได้ครบ:** ฟีเจอร์หลักทุกอย่างใช้งานได้โดยไม่ต้องเข้าสู่ระบบและไม่ต้องต่ออินเทอร์เน็ต
- **การตรวจหาอัปเดต (ตามมาตรฐาน GLee ข้อ 10.2):**
  - **แอปเช็กรุ่นใหม่จาก GitHub วันละครั้ง ไม่ส่งข้อมูลของคุณ ปิดได้ในตั้งค่า**
  - *The app checks GitHub for a new version once a day without sending any of your personal data; this can be turned off in Settings.*
- **ตัวนับการใช้งาน (ปิดเป็นค่าเริ่มต้น):** ทุกโปรแกรมมีสวิตช์ **"ช่วยปรับปรุงแอป" (Help improve the app)** ที่ **ปิดไว้เป็นค่าเริ่มต้น** หากไม่เปิด โปรแกรมจะไม่ส่งสถิติการใช้งานออกไปยังเซิร์ฟเวอร์ใด ๆ

---

## รายละเอียดแยกตามโปรแกรม · Per-Application Details

### 1. แมวดำตัดเพลงมาเย้ย (GLee Cut)
- **สิ่งที่อยู่ในเครื่องเท่านั้น:** ไฟล์เสียงทุกไฟล์ ประวัติไฟล์ล่าสุด และบันทึกข้อผิดพลาดในเครื่อง (Crash log)
- **ตัวนับคนใช้ (Google Analytics 4 Measurement Protocol):**
  - สวิตช์ **"ช่วยปรับปรุงแอป"** ปิดไว้เป็นค่าเริ่มต้น (ถาม 1 ครั้งตอนเปิดครั้งแรก)
  - เมื่อเปิด จะส่งเฉพาะสถิติแบบไม่ระบุตัวตน ได้แก่ การเปิด/ปิดโปรแกรม (`app_open`, `app_close`), เวลาใช้งาน, รุ่นโปรแกรม, รุ่น Windows, ชื่อเมนู/เอฟเฟกต์ที่กดใช้ (`feature_use`), ชื่อชนิดข้อผิดพลาด (`app_error`) และรหัสสุ่มประจำเครื่อง
  - **ไม่ส่ง** ชื่อไฟล์ ชื่อเพลง เนื้อหาเสียง หรือข้อมูลส่วนตัว และไม่ใช้เพื่อโฆษณา · ปิดได้ทุกเมื่อที่ `ตัวเลือก → ทั่วไป`
- **ล็อกอิน Google และซิงก์การตั้งค่า (ไม่บังคับ):**
  - ล็อกอินผ่านเบราว์เซอร์ของเครื่อง (OAuth 2.0 ผ่าน `127.0.0.1` + PKCE) เข้าสู่ Firebase Authentication (โปรเจกต์ `glee-21`) และเก็บรหัสล็อกอินแบบเข้ารหัสด้วย Windows DPAPI ในเครื่อง
  - เก็บเฉพาะ **การตั้งค่า** (ภาษา พรีเซ็ต ปุ่มลัด ชุดแปลงไฟล์) ใน Cloud Firestore ใต้ `users/{uid}/maewcut/` — **ไม่เก็บไฟล์เสียง**
  - ลบเฉพาะข้อมูลของโปรแกรมนี้บนคลาวด์ หรือลบบัญชีทั้งหมดได้ในหน้า `ตัวเลือก → บัญชี`
- **การเช็กรุ่นใหม่:** แอปเช็กรุ่นใหม่จาก GitHub วันละครั้ง ไม่ส่งข้อมูลของคุณ ปิดได้ในตั้งค่า

### 2. แมวดำดูหนังมาเย้ย (GLee Play)
- **สิ่งที่อยู่ในเครื่องเท่านั้น:** ไฟล์วิดีโอ ไฟล์เพลง ซับไตเติล เพลย์ลิสต์ ประวัติการรับชม และบันทึกข้อผิดพลาดในเครื่อง
- **ตัวนับคนใช้ (Google Analytics 4 Measurement Protocol):**
  - สวิตช์ **"ช่วยปรับปรุงแอป"** ปิดไว้เป็นค่าเริ่มต้น
  - เมื่อเปิด จะส่งเฉพาะสถิติแบบไม่ระบุตัวตน ได้แก่ การเปิด/ปิดโปรแกรม (`app_open`, `app_close`), ชื่อฟีเจอร์ที่ใช้งาน (`feature_use`), ชื่อชนิดข้อผิดพลาด (`app_error`), รุ่นโปรแกรม, รุ่น Windows และรหัสสุ่มประจำเครื่อง
  - **ไม่ส่ง** ชื่อไฟล์ เส้นทางไฟล์ ลิงก์ ประวัติการดู คำค้นหา หรือข้อมูลส่วนตัว · ปิดได้ทุกเมื่อในหน้าตั้งค่า
- **ล็อกอิน Google และซิงก์การตั้งค่า (ไม่บังคับ):**
  - ล็อกอินผ่านเบราว์เซอร์ของเครื่อง (OAuth 2.0 ผ่าน `127.0.0.1` + PKCE) เข้าสู่ Firebase Authentication (โปรเจกต์ `glee-21`) และเก็บรหัสล็อกอินแบบเข้ารหัสด้วย Windows DPAPI ในเครื่อง (`auth.bin`)
  - เก็บเฉพาะ **การตั้งค่าโปรแกรม** ใน Cloud Firestore ใต้ `users/{uid}/maewplay/settings` — **ไม่เก็บเส้นทางไฟล์สื่อหรือประวัติการรับชม**
  - ลบข้อมูลของโปรแกรมนี้หรือลบบัญชีทั้งหมดได้ในหน้า `บัญชี Google และซิงก์`
- **การเช็กรุ่นใหม่:** แอปเช็กรุ่นใหม่จาก GitHub วันละครั้ง ไม่ส่งข้อมูลของคุณ ปิดได้ในตั้งค่า

### 3. ก็อกมาเย้ย (GLee GOK Live)
- **สิ่งที่อยู่ในเครื่องเท่านั้น:** แชท ของขวัญ ไลก์ ผู้ติดตาม และเหตุการณ์ไลฟ์ที่รับเข้ามาถูกใช้แสดงผลบนเวทีในเครื่องเท่านั้น ช่องรับเหตุการณ์จากโปรแกรมอื่นเปิดเฉพาะภายในเครื่อง (`127.0.0.1`) ไม่ส่งข้อมูลผู้ชม แชท หรือออเดอร์ไปยังเซิร์ฟเวอร์ของ GLee
- **ตัวนับคนใช้ (Google Analytics 4 Measurement Protocol):**
  - สวิตช์ **"ช่วยปรับปรุงแอป"** ปิดไว้เป็นค่าเริ่มต้น (ถาม 1 ครั้งตอนเปิดครั้งแรก)
  - เมื่อเปิด จะส่งเฉพาะสถิติแบบไม่ระบุตัวตน ได้แก่ การเปิดโปรแกรม รุ่นโปรแกรม รุ่น Windows ชื่อฟีเจอร์ที่กดใช้ ชื่อชนิดข้อผิดพลาด และรหัสสุ่มประจำเครื่อง
  - **ไม่ส่ง** ชื่อคนในไลฟ์ ข้อความแชท ชื่อไฟล์ อีเมล หรือชื่อบัญชี TikTok/YouTube · ปิดได้ทุกเมื่อที่ `จูนเครื่อง → ช่วยปรับปรุงแอป`
- **ล็อกอิน Google และสำรองการตั้งค่าขึ้นคลาวด์ (ไม่บังคับ):**
  - ล็อกอินผ่านเบราว์เซอร์ของเครื่องเข้าสู่ Firebase Authentication (โปรเจกต์ `glee-21`) และเข้ารหัสโทเคนในเครื่องด้วย Windows DPAPI (ผ่าน Electron `safeStorage`)
  - เมื่อผู้ใช้กดสำรอง จะเก็บเฉพาะการตั้งค่า (ฉาก ธีมที่สร้างเองโดยไม่รวมรูปพื้นหลัง ตารางของขวัญ ตัวละคร เสียงพูด เพลง ภารกิจ ป้ายรอ กล้องซูม และภาษา) ใน Cloud Firestore ใต้ `apps/gok/users/{uid}`
  - **ไม่อัปโหลด** คีย์ API ที่ผู้ใช้กรอก ลิงก์เว็บฮุก ไฟล์เพลง/รูปในเครื่อง หรือข้อมูลแชท/ผู้ชม/ออเดอร์
  - ลบบัญชีและข้อมูลคลาวด์ทั้งหมดได้ใน `บัญชี & คลาวด์ → ลบบัญชีและข้อมูลทั้งหมด`
- **การเช็กรุ่นใหม่:** แอปเช็กรุ่นใหม่จาก GitHub วันละครั้ง ไม่ส่งข้อมูลของคุณ ปิดได้ในตั้งค่า

---

## English Summary

- **Offline-First & No Ads:** All three Windows desktop apps (**GLee Cut**, **GLee Play**, and **GLee GOK Live**) process your media, audio, and live-stream events locally on your PC. None of them contain ads or collect personal data for advertising.
- **Update Checks:** The app checks GitHub for a new version once a day without sending any of your personal data; this can be turned off in Settings.
- **Anonymous Usage Counter (Opt-In, OFF by Default):** All three apps include a **"Help improve the app"** toggle that is **OFF by default**. Only when explicitly enabled do they send anonymous counts (app open/close, app & Windows version, feature names, error category, and a random per-PC ID) via Google Analytics 4 Measurement Protocol. They never send file names, paths, song/video titles, live chat messages, or personal identifiers.
- **Optional Google Sign-In & Cloud Settings Sync:** All core features work without signing in. If you choose to sign in with Google (via your system browser using OAuth 2.0 + PKCE and Firebase Authentication under project `glee-21`, with local refresh tokens encrypted via Windows DPAPI), only your app preferences/presets are synced to Cloud Firestore (`users/{uid}/maewcut/`, `users/{uid}/maewplay/settings`, or `apps/gok/users/{uid}`). Media files, user API keys, webhooks, and chat/viewer data are never uploaded. You can delete an app's cloud data or delete your entire account at any time from inside the app's settings.
- **Full Online Policy:** [https://glee-21.firebaseapp.com/privacy.html](https://glee-21.firebaseapp.com/privacy.html)

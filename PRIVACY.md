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
- **ตัวนับการใช้งาน:** แต่ละโปรแกรมมีสวิตช์ **"ช่วยปรับปรุงแอป" (Help improve the app)** เพื่อส่งสถิติการใช้งานแบบไม่ระบุตัวตนเท่านั้น และ **ไม่ส่งชื่อไฟล์ ลิงก์ หรือข้อมูลส่วนตัว** (สำหรับ GLee Cut, GLee Play, GLee GOK Live ปิดไว้เป็นค่าเริ่มต้น · สำหรับ GLee Load เปิดเป็นค่าเริ่มต้นและปิดได้ทันทีในหน้าตั้งค่า)

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

### 4. แมวดำมาเย้ย (GLee Load)
- **ไม่มีการล็อกอินและไม่มีโฆษณา:** ใช้งานได้ทันทีโดยไม่ต้องสมัครสมาชิกหรือล็อกอินใด ๆ
- **สิ่งที่อยู่ในเครื่องเท่านั้น:** รายการดาวน์โหลด การตั้งค่า คิว/ตารางเวลา และไฟล์ที่ดาวน์โหลดทั้งหมดอยู่ในเครื่องของคุณ ช่องทางสื่อสารภายในเปิดรับเฉพาะ `127.0.0.1` ด้วยโทเค็นประจำเครื่องและตรวจสอบต้นทาง
- **คุกกี้เฉพาะไฟล์สำหรับเว็บที่ต้องล็อกอิน (ส่วนขยายเบราว์เซอร์):** เมื่อส่งลิงก์ที่ต้องใช้สิทธิ์เข้าสู่ระบบ ส่วนขยายจะส่งคุกกี้เฉพาะไฟล์นั้นผ่าน `127.0.0.1` เพื่อใช้ดาวน์โหลดครั้งเดียวแล้วทิ้งทันที **ไม่บันทึกลงดิสก์หรือเก็บถาวร**
- **ตัวนับการใช้งาน (Google Analytics 4 Measurement Protocol):**
  - เปิดเป็นค่าเริ่มต้น และปิดได้ทุกเมื่อในหน้า **ตั้งค่า → ตัวนับการใช้งาน**
  - ส่งเฉพาะสถิติแบบไม่ระบุตัวตน ได้แก่ การเปิดโปรแกรม, การดาวน์โหลดเสร็จ, ชนิดหมวดหมู่ไฟล์ทั่วไป, รุ่นโปรแกรม, รุ่น Windows และรหัสสุ่มประจำเครื่อง
  - **ไม่ส่งเด็ดขาด:** ลิงก์ (URL), ชื่อไฟล์, เส้นทางไฟล์, คุกกี้ หรือข้อมูลส่วนตัวใด ๆ
- **การเช็กรุ่นใหม่:** แอปเช็กรุ่นใหม่จาก GitHub วันละครั้ง ไม่ส่งข้อมูลของคุณ ปิดได้ในตั้งค่า

---

## English Summary

- **Offline-First & No Ads:** All four Windows desktop apps (**GLee Cut**, **GLee Play**, **GLee GOK Live**, and **GLee Load**) process your files locally on your PC. None of them contain ads or collect personal data for advertising.
- **Update Checks:** The app checks GitHub for a new version once a day without sending any of your personal data; this can be turned off in Settings.
- **Anonymous Usage Counter:** All apps include a **"Help improve the app"** toggle that sends only anonymous usage counts via Google Analytics 4 Measurement Protocol and never sends file names, URLs, paths, cookies, or personal identifiers (OFF by default in GLee Cut, GLee Play, and GLee GOK Live; ON by default in GLee Load and toggleable OFF anytime in Settings).
- **Optional Google Sign-In & Cloud Settings Sync:** All core features work without signing in. **GLee Load** has no sign-in system at all. For GLee Cut, GLee Play, and GLee GOK Live, if you choose to sign in with Google (via your system browser using OAuth 2.0 + PKCE and Firebase Authentication under project `glee-21`, with local refresh tokens encrypted via Windows DPAPI), only your app preferences/presets are synced to Cloud Firestore (`users/{uid}/maewcut/`, `users/{uid}/maewplay/settings`, or `apps/gok/users/{uid}`). Media files, user API keys, webhooks, and chat/viewer data are never uploaded. You can delete an app's cloud data or delete your entire account at any time from inside the app's settings.
- **Full Online Policy:** [https://glee-21.firebaseapp.com/privacy.html](https://glee-21.firebaseapp.com/privacy.html)

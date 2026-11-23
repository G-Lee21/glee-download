# เครดิตชิ้นส่วนและสัญญาอนุญาต · Third-Party Credits & Licenses

โปรแกรมในคลัง `G-Lee21/glee-download` ใช้ชิ้นส่วนโอเพนซอร์สแบบ **ใช้ได้อิสระ** (MIT, Apache-2.0, BSD, ISC, Zlib, Unicode-3.0, Unlicense, CC0-1.0, SIL OFL 1.1) และ **แบ่งปันเฉพาะชิ้นส่วน** (LGPL, MPL โดยแยกไฟล์อิสระและไม่ได้แก้ไขตัวชิ้นส่วน) — **ไม่มีชิ้นส่วนแบบบังคับแจกโค้ดทั้งแอป (GPL / AGPL)**

---

## วิธีขอซอร์สโค้ดของชิ้นส่วน LGPL · How to Obtain LGPL Source Code

ชิ้นส่วนภายใต้สัญญาอนุญาต **GNU Lesser General Public License (LGPLv2.1+ / LGPLv3+)** ที่แจกจ่ายร่วมกับโปรแกรมในคลังนี้ ได้แก่:

| โปรแกรม | ชิ้นส่วน LGPL (แยกไฟล์อิสระ ไม่แก้ไข) | รุ่น / บิลด์ | สัญญาอนุญาต | ซอร์สโค้ดต้นทาง (Corresponding Source) |
|---|---|---|---|---|
| **แมวดำตัดเพลงมาเย้ย (GLee Cut)** | `vendor/lame.min.js` (lamejs) | 1.2.1 | LGPL-3.0 | https://github.com/zhuker/lamejs |
| **แมวดำตัดเพลงมาเย้ย (GLee Cut)** | `vendor/audio-decode-ape/src/ape.wasm.js` (FFmpeg APE decoder) | audiojs/decode | LGPL-2.1+ | https://github.com/audiojs/decode · https://ffmpeg.org/ |
| **แมวดำตัดเพลงมาเย้ย (GLee Cut)** | `vendor/audio-decode-wma/src/wma.wasm.js` (FFmpeg WMA decoder) | audiojs/decode | LGPL-2.1+ | https://github.com/audiojs/decode · https://ffmpeg.org/ |
| **แมวดำดูหนังมาเย้ย (GLee Play)** | `vendor/libmpv-2.dll` (mpv + FFmpeg non-GPL build, `-Dgpl=false`) | mpv `v0.42.0-191-gd11ffba25` / FFmpeg `N-129157-g9ced9e345` | LGPLv2.1+ / LGPLv3+ | https://github.com/zhongfly/mpv-winbuild/releases/tag/2026-11-20-d11ffba253 · https://github.com/mpv-player/mpv · https://ffmpeg.org/ |
| **แมวดำดูหนังมาเย้ย (GLee Play)** | `vendor/ffmpeg.exe` (non-GPL build, `--enable-version3`, ไม่มี `--enable-gpl`) | FFmpeg `N-129157-g9ced9e345` | LGPLv3+ | https://github.com/zhongfly/mpv-winbuild/releases/tag/2026-11-20-d11ffba253 · https://ffmpeg.org/ |

- **ภาษาไทย:**
  1. ชิ้นส่วน LGPL ทุกตัวถูกแยกไว้เป็นไฟล์อิสระในแฟ้ม `vendor/` ของชุดติดตั้งและชุดพกพา โดย **ไม่ได้แก้ไขซอร์สโค้ดของชิ้นส่วนเหล่านั้น** ผู้ใช้สามารถสลับเปลี่ยนไฟล์ใน `vendor/` (เช่น `libmpv-2.dll` หรือ `ffmpeg.exe`) เป็นรุ่น LGPL อื่นที่เข้ากันได้ด้วยตนเองได้ทันที
  2. ข้อความสัญญาอนุญาตฉบับเต็มและรายการต้นทางแนบมาพร้อมกับตัวโปรแกรมในแฟ้ม `vendor/` (`LICENSE-LGPLv2.1.txt`, `THIRD-PARTY-SOURCES.txt`)
  3. คุณสามารถดาวน์โหลดซอร์สโค้ดต้นฉบับตรงรุ่นได้ทันทีจากลิงก์ในตารางด้านบน (ตามแท็กและรหัสคอมมิตที่ระบุไว้ชัดเจน) และในกรณีที่ลิงก์ต้นทางไม่สามารถเข้าถึงได้ ผู้ใช้สามารถขอรับชุดซอร์สโค้ดที่ตรงกับรุ่นที่แจกจ่ายได้ภายในระยะเวลาอย่างน้อย 3 ปีนับจากวันเผยแพร่รุ่นนั้น ๆ ตามข้อกำหนด LGPL ผ่านช่องทางอย่างเป็นทางการของ GLee
- **English:**
  1. All LGPL-licensed components are distributed unmodified as separate standalone files inside the `vendor/` directory so that users may freely inspect or replace them with compatible LGPL builds.
  2. Full license texts and source attribution files (`LICENSE-LGPLv2.1.txt`, `THIRD-PARTY-SOURCES.txt`) are bundled inside the application's `vendor/` directory.
  3. Corresponding source code for the exact versions and build tags shipped is directly available from the upstream repositories listed above. If an upstream link becomes unavailable, you may request a copy of the exact corresponding LGPL source code for at least three (3) years after the release date through GLee's official channel.

---

## 1. แมวดำตัดเพลงมาเย้ย (GLee Cut) — รุ่นล่าสุด v1.2.6

| ชิ้นส่วน | รุ่น | สัญญาอนุญาต | แบบ | ต้นทาง |
|---|---|---|---|---|
| Tauri (`tauri`, `wry`, `tao`, plugins) | 2.12.7 / 0.57.3 / 0.37.3 | MIT / Apache-2.0 | ใช้ได้อิสระ | https://github.com/tauri-apps/tauri |
| windows-rs / webview2-com / rfd | 0.62.2 / 0.39.1 / 0.17.2 | MIT / Apache-2.0 | ใช้ได้อิสระ | https://github.com/microsoft/windows-rs · https://github.com/wravery/webview2-rs · https://github.com/PolyMeilex/rfd |
| cpal / ureq / native-tls / RustCrypto (`sha2`, `aes-gcm`) / `serde` | ตาม `Cargo.lock` | MIT / Apache-2.0 | ใช้ได้อิสระ | https://crates.io/ |
| cssparser / selectors / dtoa-short / option-ext | 0.37–0.38 / 0.3.5 / 0.2.0 | MPL-2.0 | แบ่งปันเฉพาะชิ้นส่วน (ไม่แก้ไข) | https://github.com/servo/rust-cssparser · https://github.com/servo/stylo |
| lamejs (`vendor/lame.min.js`) | 1.2.1 | LGPL-3.0 | แบ่งปันเฉพาะชิ้นส่วน (แยกไฟล์ ไม่แก้ไข) | https://github.com/zhuker/lamejs |
| audio-decode-ape / audio-decode-wma (FFmpeg decoders) | audiojs/decode | LGPL-2.1+ | แบ่งปันเฉพาะชิ้นส่วน (แยกไฟล์ ไม่แก้ไข) | https://github.com/audiojs/decode |
| wasm-media-encoders (libvorbis/libogg) | — | MIT / BSD-3-Clause | ใช้ได้อิสระ | https://github.com/AnthumChris/wasm-media-encoders |
| audio-decode-amr / benz-amr-recorder (opencore-amr) | — | MIT / Apache-2.0 | ใช้ได้อิสระ | https://github.com/audiojs/decode |
| audio-decode-gsm / audio-encode-gsm / wavpack / mpc | — | MIT / BSD-3-Clause | ใช้ได้อิสระ | https://github.com/audiojs/decode |
| Microsoft Edge WebView2 SDK (`WebView2Loader.dll` & Bootstrapper) | 0.39.1 | Microsoft WebView2 Redistributable | แจกต่อได้ตามเงื่อนไข Microsoft | https://developer.microsoft.com/microsoft-edge/webview2/ |
| IBM Plex Sans Thai | 5.3.0 | SIL OFL 1.1 | ฟอนต์ใช้ได้อิสระ | https://github.com/IBM/plex |
| Lucide Icons | 0.460.0 | ISC | ใช้ได้อิสระ | https://lucide.dev/ |

---

## 2. แมวดำดูหนังมาเย้ย (GLee Play) — รุ่นล่าสุด v1.0.4

| ชิ้นส่วน | รุ่น | สัญญาอนุญาต | แบบ | ต้นทาง |
|---|---|---|---|---|
| libmpv (`vendor/libmpv-2.dll`, `-Dgpl=false`) | `v0.42.0-191-gd11ffba25` | LGPLv2.1+ (FFmpeg LGPLv3+) | แบ่งปันเฉพาะชิ้นส่วน (แยกไฟล์ ไม่แก้ไข) | https://github.com/zhongfly/mpv-winbuild/releases/tag/2026-11-20-d11ffba253 |
| FFmpeg (`vendor/ffmpeg.exe`, `--enable-version3`, no `--enable-gpl`) | `N-129157-g9ced9e345` | LGPLv3+ | แบ่งปันเฉพาะชิ้นส่วน (แยกไฟล์ ไม่แก้ไข) | https://ffmpeg.org/ · https://github.com/zhongfly/mpv-winbuild |
| libplacebo, libbluray, HarfBuzz, FreeType, FriBidi, Fontconfig, lcms2, LuaJIT, mujs, libarchive, uchardet | รวมใน `libmpv-2.dll` (LGPL build) | LGPLv2.1+ / MIT / FTL / ISC / BSD / MPL-2.0 | แบ่งปันเฉพาะชิ้นส่วน / ใช้ได้อิสระ | https://github.com/zhongfly/mpv-winbuild |
| libass, dav1d, libvpx, libaom, SVT-AV1, Opus, Vorbis, libwebp, libjxl | รวมใน `libmpv-2.dll` | ISC / BSD-2-Clause / BSD-3-Clause | ใช้ได้อิสระ | https://github.com/libass/libass |
| Tauri / wry / tao / windows-rs / webview2-com / serde / ureq / sha2 | 2.12.7 / 0.57.3 / 0.37.3 / ตาม `Cargo.lock` | MIT / Apache-2.0 | ใช้ได้อิสระ | https://github.com/tauri-apps/tauri · https://crates.io/ |
| cssparser / selectors / dtoa-short / option-ext | 0.38.x | MPL-2.0 | แบ่งปันเฉพาะชิ้นส่วน (ไม่แก้ไข) | https://github.com/servo/rust-cssparser |
| Microsoft Edge WebView2 SDK (`WebView2Loader.dll`) | 0.39.1 | Microsoft WebView2 Redistributable | แจกต่อได้ตามเงื่อนไข Microsoft | https://developer.microsoft.com/microsoft-edge/webview2/ |
| IBM Plex Sans Thai | 1.1.0 | SIL OFL 1.1 | ฟอนต์ใช้ได้อิสระ | https://github.com/IBM/plex |

---

## 3. ก็อกมาเย้ย (GLee GOK Live) — รุ่นล่าสุด v1.1.0

ตรวจชิ้นส่วนทั้งหมด 113 แพ็กเกจในชุดแจกจ่าย: **ใช้ได้อิสระทั้งหมด 100%** (MIT 103, ISC 5, BSD-2-Clause 2, BSD-3-Clause 1, Apache-2.0 1, BlueOak-1.0.0 1) — ไม่มี GPL / AGPL / LGPL (ดนตรีสังเคราะห์ 17 สไตล์เขียนเองด้วย Web Audio และฉากทั้งหมดวาดเองด้วย Canvas)

| ชิ้นส่วนหลัก | รุ่น | สัญญาอนุญาต | แบบ | ต้นทาง |
|---|---|---|---|---|
| Electron | 35.7.5 | MIT | ใช้ได้อิสระ | https://github.com/electron/electron |
| Express | 4.22.3 | MIT | ใช้ได้อิสระ | https://github.com/expressjs/express |
| ws | 8.23.0 | MIT | ใช้ได้อิสระ | https://github.com/websockets/ws |
| got / keyv / fs-extra / mime / qs / semver / extract-zip / yauzl | ตาม `package-lock.json` | MIT / ISC / BSD-2-Clause / BSD-3-Clause / Apache-2.0 / BlueOak-1.0.0 | ใช้ได้อิสระ | https://www.npmjs.com/ |

*(รายชื่อครบทั้ง 113 แพ็กเกจแสดงอยู่ในตัวโปรแกรมที่หน้า `จูนเครื่อง → เกี่ยวกับแอป`)*

---

## 4. แมวดำมาเย้ย (GLee Load) — รุ่นล่าสุด v1.0.5

ตรวจชิ้นส่วนในตัวหลักครบทุกตัว (Rust 159 แพ็กเกจ + ตัวติดตั้ง 65 แพ็กเกจ + UI Kit + ฟอนต์ + ไอคอน): **ใช้ได้อิสระทั้งหมด 100% — ไม่มีชิ้นส่วน GPL / AGPL / LGPL ในชุดหลัก** *(ชิ้นส่วนดึงคลิปโซเชียลและ FFmpeg รุ่น LGPLv3+ แยกแจกไว้ในคลัง `G-Lee21/glee-download-extra`)*

| ชิ้นส่วน | รุ่น | สัญญาอนุญาต | แบบ | ต้นทาง |
|---|---|---|---|---|
| Rust Runtime & Crates (`tokio`, `serde`, `ureq`, `rustls`, `ring`, `ed25519-dalek`, `sha2`, `chrono`, `uuid`, `windows`, ฯลฯ — ตรวจครบ 159 ตัว) | ล็อกใน `Cargo.lock` | MIT / Apache-2.0 / BSD-3-Clause / ISC / Zlib / Unicode-3.0 / CDLA-Permissive-2.0 | ใช้ได้อิสระ | https://crates.io/ |
| IBM Plex Sans Thai & Mali | 1.x | SIL OFL 1.1 | ฟอนต์ใช้ได้อิสระ | https://github.com/IBM/plex · https://fonts.google.com/specimen/Mali |
| Lucide Icons | 1.77.0 | ISC | ใช้ได้อิสระ | https://lucide.dev/ |

---

## 5. ชิ้นส่วนร่วมของตัวติดตั้งและตัวถอนมาตรฐาน GLee · Shared GLee Installer Components

| ชิ้นส่วน | รุ่น | สัญญาอนุญาต | แบบ | ต้นทาง |
|---|---|---|---|---|
| NSIS (Nullsoft Scriptable Install System) | 3.x | zlib/libpng | ใช้ได้อิสระ | https://nsis.sourceforge.io/ |
| IBM Plex Sans Thai (woff2 ฝังในหน้าต่างตัวติดตั้ง) | 5.3.0 | SIL OFL 1.1 | ฟอนต์ใช้ได้อิสระ | https://github.com/IBM/plex |
| flate2 / sha2 / serde / serde_json / windows-rs / webview2-com | ตาม `Cargo.lock` | MIT / Apache-2.0 | ใช้ได้อิสระ | https://crates.io/ |

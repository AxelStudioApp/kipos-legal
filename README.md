# ⚖️ kiPOS Legal Documents Repository

**Repository Status:** 🟢 Active / Production  
**Managed by:** Axel Studio  

---

## 📖 Deskripsi
Repository publik ini berfungsi sebagai **Content Delivery Network (CDN) Statis** untuk dokumen legal aplikasi Point of Sale (POS) **kiPOS**. 

Dokumen di dalam repository ini (Syarat & Ketentuan serta Kebijakan Privasi) ditarik (*fetched*) secara **live** oleh aplikasi *mobile* kiPOS menggunakan GitHub Raw API. Pendekatan ini memungkinkan tim Axel Studio untuk memperbarui kebijakan hukum secara instan tanpa perlu merilis pembaruan aplikasi (APK/AAB) di Google Play Store atau Apple App Store.

---

## ⚠️ PERINGATAN UNTUK TIM DEVELOPER & LEGAL
**JANGAN MENGUBAH NAMA FILE ATAU STRUKTUR FOLDER DI BAWAH INI.**
Aplikasi *production* memiliki URL *hardcoded* yang mengarah langsung ke file-file ini. Mengubah nama file (misalnya dari `tnc_id.md` menjadi `tnc_indo.md`) akan menyebabkan **Error 404** pada aplikasi kasir dan memblokir *merchant* baru dari proses pendaftaran (Onboarding).

Jika Anda ingin memperbarui isi kebijakan, silakan **edit file yang sudah ada**, lalu lakukan *Commit* & *Push*. Perubahan akan langsung tercermin di aplikasi pengguna.

---

## 📂 Struktur Dokumen & Raw URLs

Aplikasi kiPOS membaca dokumen ini berdasarkan lokalisasi perangkat (*device locale*). Berikut adalah *endpoint* Raw yang digunakan oleh aplikasi:

### 1. Terms and Conditions (Syarat & Ketentuan)
* 🇮🇩 **Bahasa Indonesia:** `https://raw.githubusercontent.com/AxelStudio/kipos-legal/main/terms-and-conditions/tnc_id.md`
* 🇬🇧 **English (Default):** `https://raw.githubusercontent.com/AxelStudio/kipos-legal/main/terms-and-conditions/tnc_en.md`

### 2. Privacy Policy (Kebijakan Privasi)
* 🇮🇩 **Bahasa Indonesia:** `https://raw.githubusercontent.com/AxelStudio/kipos-legal/main/privacy-policy/privacy_id.md`
* 🇬🇧 **English (Default):** `https://raw.githubusercontent.com/AxelStudio/kipos-legal/main/privacy-policy/privacy_en.md`

---

## 🛠️ Cara Memperbarui Dokumen
1. Lakukan *pull* terbaru dari *branch* `main`.
2. Buka file `.md` yang ingin diubah menggunakan *text editor* (VS Code, Typora, dll).
3. Gunakan format standar Markdown (Heading dengan `#`, List dengan `*`, Bold dengan `**`).
4. *Commit* dengan pesan yang jelas, contoh: `Update: Penambahan pasal biaya langganan SaaS (v1.2)`.
5. *Push* ke `main`.

*(Catatan: Pembaruan mungkin membutuhkan waktu 1-5 menit untuk ter-refresh sepenuhnya di *cache* GitHub global sebelum muncul di aplikasi).*

---
*© 2026 Axel Studio. All rights reserved.*

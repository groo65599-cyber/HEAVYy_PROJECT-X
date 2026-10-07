# HPX PIRATE — Release Notes

## UPDATE BESAR — Version 2.0.0 ("Diagnose First" Edition)

**Platform:** Windows 10 / 11 (x64)
**Runtime:** .NET 8 Desktop Runtime (framework-dependent)
**Build status:** 0 warnings / 0 errors · 103/103 logic tests passing

---

## Prinsip Utama Update Ini

> **"FIX ONLY WHAT IS BROKEN."**
> **"EVERY VISIBLE FEATURE MUST HAVE A REAL FUNCTION."**
> **"NO FAKE FEATURES."**

Update ini menjawab keluhan utama: *"Sering di-fix terus walaupun sebenarnya tidak bug."*
Sekarang aplikasi **mendiagnosis dulu sebelum mengubah apa pun**. Alur kerja setiap fitur:

```
DETECT → DIAGNOSE → EXPLAIN → APPLY → VERIFY → ROLLBACK
```

- Jika **tidak ada masalah:** aplikasi menampilkan **"NO ISSUE DETECTED"** dan
  **"Current configuration will be preserved."** — tidak ada yang diubah.
- Jika **ada masalah:** aplikasi menampilkan **"ISSUE DETECTED"** dan
  **"Recommended fix:"** dengan daftar perbaikan yang bisa diterapkan.

Tidak ada lagi perbaikan paksa. Tidak ada metrik palsu. Jika sebuah fitur tidak
didukung oleh sistem, aplikasi menampilkan **"NOT SUPPORTED"** /
**"NOT AVAILABLE ON THIS SYSTEM"** / **"DATA NOT AVAILABLE"** — bukan angka karangan.

---

## Yang Baru di Update Ini

### 1. Sidebar Baru dengan 5 Grup (17 layar)
- **DASHBOARD** — Dashboard
- **PERFORMANCE** — Performance, Monitor, Ultra FPS Boost
- **GAME CONTROL** — Game Profiles, Control Mapper, Sensitivity, Keyboard, Controller
- **TOOLS** — Drag Assist, Easy Drag Lab, Crosshair, + HPX PIRATE Toolbox
- **SYSTEM** — System Optimizer, Diagnostics, Settings

### 2. ULTRA FPS BOOST ENGINE (baru, nyata & terukur)
Target FPS nyata (120–240+), **tanpa FPS palsu**. Alur lengkap:

```
DETECT → BASELINE → ANALYZE → IDENTIFY BOTTLENECK → CREATE PLAN
→ SHOW CHANGES → APPLY → MEASURE → COMPARE → VERIFY → KEEP OR ROLLBACK
```

- Deteksi refresh rate monitor (EnumDisplaySettings)
- Deteksi FPS cap
- Analisis stabilitas frame-time (coefficient of variation)
- Deteksi bottleneck (CPU/GPU/RAM/disk)
- Tes baseline sebelum/sesudah
- Verdict: **IMPROVED / REGRESSED / NO SIGNIFICANT CHANGE / MEASUREMENT INCOMPLETE**
- FPS Drop Recorder
- Aturan keamanan + keep-or-rollback

### 3. HPX PIRATE Toolbox (13 alat nyata)
Input Tester · Latency Analyzer · Calibration · Input Recorder · Mapping Tester ·
Profile Converter · Sensitivity Lab · Response Curve · Frame Analyzer · FPS Boost ·
Config Backup · Diagnostics · Overlay Studio.
Dilengkapi **Favorites / Recent / Search / Status / Result History**.

### 4. Halaman & Sistem Baru
- **Sensitivity System + Test Area** (kurva respons: Linear/Smooth/FastStart/SlowStart/Precision/Custom)
- **Keyboard** — live input monitor + pengukuran latensi
- **Controller (XInput)** — visual + mapping joystick
- **Diagnostics / Health Check**
- **Input Latency Test**
- **Profile Import / Export**
- **Update System** (Safe Update & Rollback)
- **Bug Report**
- **Logging & Diagnostics**
- **Settings tabbed** — General / Input / Performance / Safety & Recovery / Advanced
- **Safe Mode**

### 5. System Optimizer — Diagnosis-First
Tombol **RE-DIAGNOSE** dan **APPLY RECOMMENDED FIXES**. Jika tidak ada masalah,
tombol perbaikan dinonaktifkan dan konfigurasi dipertahankan. Setiap perubahan
punya **UNDO/ROLLBACK** per-item, hanya menyentuh **HKCU** (registry user), dan
opsional membuat **System Restore Point**.

### 6. Safe Update & Rollback
Backup otomatis untuk config, profiles, keymapping, sensitivity, dan preferences
sebelum perubahan. Semua bisa dikembalikan.

### 7. Desain & UX
- Identitas visual dipertahankan: latar hitam/ungu gelap (#07060B), panel violet,
  aksen magenta (#FF2BD6), aksen cyan (#2BE7FF), kartu rounded, border tipis, soft glow.
- Design system & color token global.
- Micro-interaction secukupnya (tanpa animasi berlebihan).
- UI state lengkap: loading / empty / success / warning / error / disabled.
- Responsif untuk 1280x720, 1366x768, 1600x900, 1920x1080, 2560x1440.
- HPX PIRATE sendiri tidak menyebabkan lag (monitoring interval adaptif + idle throttling).

---

## Isi Paket Ini

| File | Keterangan |
|------|-----------|
| `HPX-PIRATE-v2.0.0-publish-win-x64.zip` | Build siap jalan (framework-dependent, win-x64). Ekstrak lalu jalankan `HPXPirate.exe`. |
| `HPX-PIRATE-v2.0.0-SOURCE.zip` | Kode sumber lengkap (src + tests + docs + installer). |
| `README.md` | Dokumentasi utama & daftar fitur. |
| `BUILD.md` | Cara build dari sumber. |
| `ARCHITECTURE.md` | Arsitektur teknis. |
| `INSTALL-WINDOWS.md` | Panduan instalasi (Bahasa Indonesia). |
| `installer/HPX-PIRATE.iss` | Skrip Inno Setup 6 untuk membuat installer. |
| `installer/build-installer.ps1` | Skrip PowerShell untuk build installer. |
| `RELEASE-NOTES.md` | Dokumen ini. |

---

## Cara Menjalankan (Cepat)

1. Ekstrak `HPX-PIRATE-v2.0.0-publish-win-x64.zip`.
2. Pastikan **.NET 8 Desktop Runtime** terpasang
   (https://dotnet.microsoft.com/download/dotnet/8.0).
3. Jalankan `HPXPirate.exe`.
4. Data aplikasi disimpan di `%APPDATA%\HPXPirate`.

Detail lengkap ada di `INSTALL-WINDOWS.md`.

---

## Status Fungsional

| Lapisan | Status |
|---------|--------|
| Build | ✅ 0 warning / 0 error |
| Logic tests | ✅ 103 / 103 passing |
| Publish win-x64 | ✅ Sukses |
| Dokumentasi | ✅ Lengkap |
| Diagnosis-first workflow | ✅ Aktif di System Optimizer & Ultra FPS Boost |
| No-fake-feature policy | ✅ Diterapkan |

---

*HPX PIRATE — dibangun untuk memberi tahu Anda apa yang benar-benar rusak,
dan tidak menyentuh apa pun yang sudah baik.*

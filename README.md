# 🧠 Minda – Aplikasi Jurnal Harian Offline
---
**Tagline:** 
_Catat. Refleksi. Privasi._  
Minda adalah aplikasi jurnal harian berbasis Kotlin + Jetpack Compose yang bekerja sepenuhnya offline menggunakan Room (SQLite). Dirancang untuk sederhana, cepat, dan aman—cocok sebagai proyek pembelajaran dan dasar aplikasi personal diary yang menghargai privasi pengguna.
---

![Kotlin](https://img.shields.io/badge/Kotlin-100%25-7F52FF?style=for-the-badge&logo=kotlin)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-Declarative_UI-4285F4?style=for-the-badge&logo=jetpackcompose)
![Android SDK](https://img.shields.io/badge/Min_SDK-24_(Android_7.0)-3DDC84?style=for-the-badge&logo=android)
![Database](https://img.shields.io/badge/Database-Room_(SQLite_Offline)-EF6C00?style=for-the-badge&logo=sqlite)

---

## 👨‍💻 Kontributor

| Nama | Peran |
|------|--------|
| **Muhammad Raihan Azmi** | Pengembang utama |
| **Muhayat, S.Ag.,M.IT** | Dosen Pembimbing |

📧 **Email:** [raihanazmi37@gmail.com](mailto:raihanazmi37@gmail.com)  
🏫 **Universitas Antasari – Fakultas Dakwah Dan Ilmu Komunikasi - Jurusan Teknologi Informasi**

---

## 📌 Ringkasan Proyek
Minda adalah aplikasi jurnal yang menyimpan semua data di perangkat (no cloud). Fokus utama:
- Pengalaman menulis cepat dan intuitif dengan Jetpack Compose.
- Penyimpanan data aman di perangkat menggunakan Room + DataStore.
- Alur onboarding untuk personalisasi (nama, preferensi, dll).
- Fitur CRUD lengkap, kalender, dan insights sederhana (streak, jumlah catatan, mood).

Proyek ini dikembangkan sebagai bagian dari Modul Praktikum Mobile Programming dan cocok dijadikan portofolio atau basis pengembangan lebih lanjut.

---

## 🎯 Tujuan Proyek

- Membangun aplikasi Android modern dengan arsitektur **Jetpack Compose + Room + DataStore**  
- Mengimplementasikan fungsionalitas **CRUD (Create, Read, Update, Delete)** dengan database lokal  
- Menggunakan **DataStore Preferences** untuk menyimpan nama & status onboarding  
- Mengintegrasikan **Navigation Compose**, **Bottom Navigation Bar**, dan **Floating Action Button (FAB)**  
- Membuat **alur onboarding 4 langkah** untuk personalisasi pengguna  
- Menerapkan prinsip *privacy by design* — semua data hanya tersimpan di perangkat pengguna  

---

## ⚙️ Tumpukan Teknologi

| Lapisan | Teknologi |
|----------|------------|
| **Bahasa** | Kotlin (100%) |
| **UI Framework** | Jetpack Compose + Material Design 3 |
| **Database** | Room ORM (SQLite) |
| **Penyimpanan Preferensi** | DataStore Preferences |
| **Arsitektur** | MVVM + Repository Pattern |
| **Navigasi** | Navigation Compose |
| **Asinkronisasi** | Kotlin Coroutines + Flow |
| **Build System** | Gradle Kotlin DSL (KSP) |
| **Minimum SDK** | Android 7.0 (API 24) |
| **Target SDK** | Android 14 (API 34) |

---

## ✨ Fitur Utama

- **Onboarding 4 langkah:** Welcome → Name → Hello → Start Journaling  
- **CRUD Lengkap:** Tambah, baca, edit, hapus catatan  
- **100% Offline:** Semua data tersimpan di database Room  
- **Kalender Dinamis:** Lihat catatan berdasarkan tanggal  
- **Statistik (Insights):** Menampilkan jumlah catatan, mood, dan streak pengguna  
- **Navigasi Modern:** Menggunakan NavHost Compose dengan FAB terpusat  
- **Material 3 Theme:** Desain minimalis dan responsif  
- **Adaptive Icon & Custom Banner**

---

## 📸 Cuplikan Layar (Screenshots)

| Onboarding (1) | Onboarding (2) | Onboarding (3) |
|:--------------:|:--------------:|:--------------:|
| ![Welcome To Minda](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/Welcome%20To%20Minda.png) | ![What’s Your Name](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/What%E2%80%99s%20your%20Name.png) | ![Welcome To Your Minda](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/Welcome%20To%20Your%20Minda.png) |
| Onboarding (4) | Home | Calendar |
| ![You're all Set](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/You're%20all%20Set.png) | ![HomeSreen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/Home%20Screen.png) | ![Calendar Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/CalendarScreen.png) |
| New Entry | Edit Entry | Insights |
| ![New Entry Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/NewEntryScreen.png) | ![Edit Entry Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/EditEntryScreen.png) | ![Insights Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/InsightsScreen.png) |
| Settings | Icon Changed |  |
| ![Settings Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/SettingsScreen.png) | ![Icon Changed Proof](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/ScreenShot/Bukti%20sdh%20ganti%20icon.png) |   |

> *Seluruh tangkapan layar diambil langsung dari versi final aplikasi Minda.*

---

## 🗂️ Struktur Proyek



```
app/
└── src/
    └── main/
        ├── AndroidManifest.xml
        ├── java/
        │   └── id/antasari/p6minda_230104040079/
        │       ├── MainActivity.kt                // Scaffold, FAB, BottomNav, NavHost
        │       ├── MindaTheme.kt                  // Tema dasar Material 3
        │       ├── data/
        │       │   ├── DiaryEntry.kt              // Entity / tabel Room
        │       │   ├── DiaryDao.kt                // Interface CRUD Room
        │       │   ├── MindaDatabase.kt           // Definisi Database Room
        │       │   ├── DiaryRepository.kt         // Abstraksi akses data
        │       │   └── UserPrefsRepository.kt     // DataStore Preferences
        │       ├── ui/
        │       │   ├── BottomNav.kt               // Bottom Navigation Bar kustom
        │       │   ├── ExtraScreens.kt            // InsightsScreen, SettingsScreen
        │       │   ├── HomeScreen.kt              // Daftar catatan + Search + Banner
        │       │   ├── NewEntryScreen.kt          // Form tambah catatan
        │       │   ├── EditEntryScreen.kt         // Form edit catatan
        │       │   ├── NoteDetailScreen.kt        // Layar detail catatan
        │       │   ├── OnboardingScreens.kt       // 4 layar onboarding
        │       │   ├── calendar/
        │       │   │   ├── CalendarScreen.kt      // Tampilan kalender grid
        │       │   │   └── CalendarViewModel.kt   // Logika kalender dan data Flow
        │       │   └── navigation/
        │       │       ├── AppNavHost.kt          // Logika navigasi utama
        │       │       └── Routes.kt              // Konstanta rute
        │       └── util/
        │           └── DateFormatter.kt           // Format timestamp
        └── res/
            ├── drawable/
            │   └── banner_diary.jpg               // Banner Home & Onboarding
            ├── mipmap/                            // Ikon launcher
            └── xml/
                └── backup_rules.xml               // Exclude DataStore dari auto-backup
```

---

## 🚀 Instalasi & Menjalankan (Developer)
### Prasyarat
- Android Studio (2022.3+ / Arctic Fox / Bumblebee atau lebih baru — disarankan versi terbaru)  
- JDK 17  
- Android SDK (API 34 tersedia)  
- Perangkat/emulator Min API 24+

### Langkah Menjalankan
```bash
# 1. Clone repositori
git clone https://github.com/Raihhazmi/p6minda_230104040079.git
cd p6minda_230104040079

# 2. Buka di Android Studio
# 3. (WAJIB di Windows) Buat folder wajib untuk KSP/Room
mkdir C:\temp\sqlite

# 4. Sync Gradle, Clean & Rebuild
# 5. Jalankan aplikasi (Shift + F10)
```
---
### Arsitektur Aplikasi
```
UI (Jetpack Compose)
      ↓
ViewModel (State & Logic)
      ↓
Repository (Abstraksi Data)
      ↓
Room DAO (SQLite CRUD)
      ↓
Database Lokal (minda.db)
```
----
## 🧭 Alur Aplikasi (singkat)
1. Pertama kali buka → tampilkan onboarding 4 langkah  
2. Simpan nama & flag onboarding ke DataStore  
3. Masuk ke Home → daftar catatan + FAB untuk tambah entri  
4. Catatan disimpan di Room; ViewModel expose Flow ke UI  
5. Kalender & Insights menghitung statistik dari database lokal

----

## ✅ Checklist sebelum submit / demo
- [ ] Clean & rebuild berhasil pada Android Studio (tersesuaikan SDK)  
- [ ] Semua screenshot berada di folder `/ScreenShot` dan tautan benar  
- [ ] Backup dan DataStore konfigurasi sesuai kebijakan privasi tugas  
- [ ] README ini disesuaikan lagi bila ada perubahan arsitektur atau dependensi

----
### 🧾 Lisensi

Proyek ini dibuat sebagai bagian dari Praktikum Mobile Programming 6 – Universitas Antasari.
Seluruh kode sumber dapat digunakan untuk pembelajaran dan pengembangan akademik non-komersial.
```
© 2025 Muhammad Raihan Azmi – Universitas Antasari
Dosen Pembimbing: Muhayat, M.IT
```

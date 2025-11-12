# 🧠 Minda – Aplikasi Jurnal Harian Offline

![Kotlin](https://img.shields.io/badge/Kotlin-100%25-7F52FF?style=for-the-badge&logo=kotlin)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-Declarative_UI-4285F4?style=for-the-badge&logo=jetpackcompose)
![Android SDK](https://img.shields.io/badge/Min_SDK-24_(Android_7.0)-3DDC84?style=for-the-badge&logo=android)
![Database](https://img.shields.io/badge/Database-Room_(SQLite_Offline)-EF6C00?style=for-the-badge&logo=sqlite)

> **Minda** adalah aplikasi jurnal (diary) pribadi berbasis **Kotlin** dan **Jetpack Compose** yang berfungsi sepenuhnya secara *offline*.  
> Seluruh data jurnal disimpan aman di perangkat pengguna melalui **Room (SQLite)**, tanpa memerlukan koneksi internet.  
> Proyek ini dikembangkan untuk **Modul Praktikum #6 Mobile Programming 20251** — *“Menggunakan Database Lokal”* di bawah bimbingan **Muhayat, M.IT** (Universitas Antasari).

---

## 🎯 Tujuan Proyek

- Mengimplementasikan aplikasi Android modern dengan arsitektur **Jetpack Compose + Room + DataStore**.  
- Menerapkan **CRUD (Create, Read, Update, Delete)** dengan database lokal *offline*.  
- Menyimpan preferensi pengguna (nama & status onboarding) menggunakan **DataStore Preferences**.  
- Mengintegrasikan **Navigation Compose**, **Bottom Navigation Bar**, dan **Floating Action Button (FAB)**.  
- Membangun **alur onboarding 4 langkah** dan **UI personalisasi pengguna**.  
- Menjalankan konsep *privacy by design* — data hanya tersimpan di perangkat.  

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
- **Penyimpanan 100% Offline** dengan Room Database  
- **Kalender Dinamis:** Lihat catatan berdasarkan tanggal  
- **Statistik (Insights):** Hitung jumlah catatan, mood, streak  
- **Penyimpanan Nama Pengguna:** Menggunakan DataStore  
- **Navigasi Modern:** NavHost Compose dengan bottom bar dinamis  
- **Desain Material 3:** Warna utama ungu kebiruan dan FAB terpusat  
- **Adaptive Launcher Icon** dan banner kustom  

---

## 📸 Cuplikan Layar (Screenshots)

| Onboarding (1) | Home | Insights |
|:--------------:|:----:|:--------:|
| ![Welcome To Minda](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/Welcome%20To%20Minda.png) | ![Home Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/Home%20Screen.png) | ![Insights Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/InsightsScreen.png) |
| Onboarding (2) | Calendar | Settings |
| ![What’s Your Name](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/What%E2%80%99s%20your%20Name.png) | ![Calendar Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/CalendarScreen.png) | ![Settings Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/SettingsScreen.png) |
| Onboarding (3) | New Entry | Edit Entry |
| ![Welcome To Your Minda](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/Welcome%20To%20Your%20Minda.png) | ![New Entry Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/NewEntryScreen.png) | ![Edit Entry Screen](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/EditEntryScreen.png) |
| Onboarding (4) | Icon Changed |  |
| ![You're all Set](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/You're%20all%20Set.png) | ![Icon Changed Proof](https://github.com/Raihhazmi/p6minda_230104040079/blob/master/assets/Bukti%20sdh%20ganti%20icon.png) |   |

> *Seluruh tangkapan layar diambil langsung dari versi final aplikasi Minda.*


---

## 🚀 Instalasi & Build

### Prasyarat
1. **Android Studio:** Narwhal (2025.1.1) atau lebih baru  
2. **Java:** JDK 17  
3. **SDK:** Android API 34  
4. **Perangkat:** Emulator / fisik dengan Min API 24 (Android 7.0)

### Langkah Menjalankan
```bash
# 1. Clone repositori
git clone https://github.com/NAMA_ANDA/p6minda_230104040079.git
cd p6minda_230104040079

# 2. Buka di Android Studio
# 3. (WAJIB di Windows) Buat folder wajib untuk KSP/Room
mkdir C:\temp\sqlite

# 4. Sync Gradle, Clean & Rebuild
# 5. Jalankan aplikasi (Shift + F10)
```

---

## 🧩 Arsitektur Aplikasi

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

---

## 🧠 Alur Onboarding & DataStore

1. **Welcome** → pengenalan aplikasi  
2. **Ask Name** → pengguna memasukkan nama  
3. **Hello** → sapaan personal  
4. **Start Journaling** → menyimpan `onboarding_completed = true`  
5. Saat aplikasi dibuka ulang, langsung masuk ke **Home** tanpa onboarding ulang.  

---

## 🧾 Lisensi

Proyek ini dibuat sebagai bagian dari **Praktikum Mobile Programming 6 – Universitas Antasari**.  
Seluruh kode sumber dapat digunakan untuk pembelajaran dan pengembangan akademik non-komersial.

```
© 2025 Muhammad Raihan Azmi – Universitas Antasari
Dosen Pembimbing: Muhayat, M.IT
```

---

## 👨‍💻 Kontributor

| Nama | Peran |
|------|--------|
| **Muhammad Raihan Azmi** | Pengembang utama |
| **Muhayat, M.IT** | Dosen Pembimbing |

---

## 💬 Kontak

📧 **Email:** raihanazmi37@gmail.com  
🏫 **Universitas Antasari, Fakultas Teknologi Informasi**

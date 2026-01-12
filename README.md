
📝 Minda - Offline Diary App
Minda adalah aplikasi catatan harian sederhana yang dirancang untuk mendemonstrasikan implementasi database lokal menggunakan Room Persistence Library di Android. Proyek ini merupakan bagian dari Modul Praktikum #6 Mobile Programming.
🚀 Panduan Penggunaan (How to Use)
Setelah Anda berhasil melakukan build dan menjalankan aplikasi, ikuti langkah-langkah berikut:
 * Inisialisasi Otomatis: Saat pertama kali dibuka, aplikasi akan melakukan seeding data secara otomatis dengan menampilkan dua catatan contoh ("My day 1" dan "Gratitude journal").
 * Melihat Catatan: Semua catatan yang tersimpan akan muncul dalam bentuk daftar kartu (cards) yang diurutkan dari yang terbaru.
 * Menambah Catatan: Klik tombol "Add dummy entry" untuk menambahkan catatan baru ke dalam database secara instan tanpa perlu memuat ulang aplikasi.
 * Memastikan Keamanan Data: Karena menggunakan SQLite (Room), data Anda tetap tersimpan meskipun aplikasi ditutup atau perangkat dimatikan.
🛠️ Detail Implementasi Teknis
1. Konfigurasi Database (Room)
Aplikasi ini menggunakan tiga komponen utama Room:
 * Entity (DiaryEntry.kt): Mendefinisikan struktur tabel diary_entries yang mencakup kolom ID (auto-generate), Judul, Konten, Mood, dan Timestamp.
 * DAO (DiaryDao.kt): Interface yang menyediakan fungsi CRUD (Create, Read, Update, Delete) menggunakan query SQL.
 * Database (MindaDatabase.kt): Titik akses utama yang menggunakan pola Singleton untuk memastikan efisiensi penggunaan sumber daya.
2. Arsitektur Data
Aplikasi ini menerapkan pola Repository (DiaryRepository.kt) untuk memisahkan logika akses data dari antarmuka pengguna, sehingga kode lebih bersih dan mudah dikelola.
3. Antarmuka Pengguna (UI)
Dibangun sepenuhnya menggunakan Jetpack Compose dengan fitur-fitur berikut:
 * MindaTheme: Tema kustom berbasis Material3.
 * TestRoomScreen: Layar utama yang menggunakan LazyColumn untuk menampilkan daftar entri secara efisien.
 * DateFormatter: Helper untuk mengubah timestamp sistem menjadi format tanggal yang mudah dibaca (contoh: "27 Oct, 2025, 05:50 AM").
⚙️ Persyaratan Pengembangan
 * Android Studio: Versi terbaru direkomendasikan.
 * JDK: Versi 17 (Wajib disesuaikan pada compileOptions dan kotlinOptions).
 * Gradle: Menggunakan Kotlin DSL (.kts).
Apakah Anda ingin saya membantu menjelaskan cara melakukan Export Database dari Android Studio untuk melihat isi file .db secara langsung?

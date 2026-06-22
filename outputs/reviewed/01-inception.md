# Project Inception and Stakeholder Discovery

## 1. Business Problem
Proses pengelolaan tugas perkuliahan saat ini masih dilakukan melalui berbagai media yang terpisah. Kondisi ini menyebabkan timbulnya beberapa masalah operasional sebagai berikut:
* Kesulitan dalam memantau tenggat waktu (*deadline*) tugas secara terpusat.
* Kesulitan dalam melakukan pengumpulan file tugas secara terorganisasi.
* Hambatan dalam menjalankan proses penilaian tugas secara efisien dan terstruktur.

## 2. Proposed Solution
Untuk mengatasi masalah bisnis di atas, solusi yang diusulkan adalah membangun **Student Task Management System**, yaitu sebuah aplikasi berbasis web terintegrasi yang berfungsi sebagai platform terpusat untuk mengelola siklus tugas perkuliahan, mulai dari pembuatan, pengumpulan, hingga penilaian.
* **ASSUMPTION-04**: Diasumsikan aplikasi ini merupakan platform mandiri (*standalone web application*) yang berfokus penuh pada manajemen tugas perkuliahan untuk mengatasi masalah media yang terpisah.

## 3. Business Goals
* **Goal-01**: Menyediakan fasilitas bagi dosen untuk mengelola tugas perkuliahan secara terpusat.
* **Goal-02**: Menyediakan fasilitas bagi mahasiswa untuk memantau tugas dan tenggat waktu (*deadline*).
* **Goal-03**: Menyediakan fasilitas bagi administrator untuk mengelola pengguna dan mata kuliah.

## 4. Stakeholders and Needs
* **Lecturer (Dosen)**
    * Membuat tugas perkuliahan.
    * Menetapkan tenggat waktu (*deadline*) tugas.
    * Memberikan nilai pada hasil kerja mahasiswa.
    * Memberikan umpan balik (*feedback*) terhadap tugas yang dikumpulkan.
* **Student (Mahasiswa)**
    * Melihat daftar tugas perkuliahan.
    * Memantau status pengumpulan tugas.
    * Memantau tenggat waktu (*deadline*) tugas.
    * Mengumpulkan file tugas ke dalam sistem.
* **Administrator**
    * Mengelola data pengguna (akun user).
    * Mengelola data mata kuliah.
    * Mengatur konfigurasi sistem global.

## 5. Project Scope Boundary
* **In-Scope**:
    * Fitur autentikasi dan manajemen akun untuk aktor Lecturer, Student, dan Administrator.
    * Modul pembuatan tugas, pengaturan *deadline*, input nilai, dan pengisian umpan balik oleh Lecturer.
    * Modul unggah/pengumpulan file tugas dan pelacakan status oleh Student.
    * Modul manajemen data pengguna, manajemen data mata kuliah, dan pengaturan konfigurasi sistem oleh Administrator.
* **Out-of-Scope**:
    * (Tidak ada batasan ruang lingkup luar yang dinyatakan secara eksplisit dalam dokumen studi kasus awal. Seluruh potensi pengecualian atau perluasan fitur dialihkan ke bagian *Assumptions* dan *Open Questions*).

## 6. Assumptions and Constraints
* **ASSUMPTION-01**: Mahasiswa sudah memiliki akun sistem yang valid dan aktif sebelum dapat mengakses fitur tugas.
* **ASSUMPTION-02**: Dosen memiliki hak akses penuh dan otoritas untuk membuat serta menilai tugas pada mata kuliah yang diampunya.
* **ASSUMPTION-03**: Pengguna memiliki perangkat keras (komputer/laptop) dan peramban web (*web browser*) modern yang terhubung dengan koneksi internet.
* **ASSUMPTION-05**: Diasumsikan sistem ini tidak mencakup manajemen absensi/kehadiran harian mahasiswa maupun sistem pembayaran UKT/keuangan kampus.
* **CONSTRAINT-01**: Sistem harus berbasis web (*web-based system*).
* **CONSTRAINT-02**: Sistem harus memperhatikan keamanan data secara ketat, terutama kerahasiaan data nilai dan integritas berkas yang diunggah.
* **CONSTRAINT-03**: Sistem harus mendukung akses dari banyak pengguna secara bersamaan tanpa mengalami kegagalan sistem (*crash*).

## 7. Open Questions
* **OPEN QUESTION-01**: Apa saja format ekstensi file tugas yang diizinkan untuk diunggah oleh Student, dan berapa batas maksimal kapasitas (*file size*) per berkas?
* **OPEN QUESTION-02**: Berapa target parameter kuantitatif untuk keamanan (misalnya metode enkripsi data nilai) dan performa sistem (misalnya batas waktu respons dalam detik atau jumlah maksimal *concurrent users*)?
* **OPEN QUESTION-03**: Apakah sistem ini memerlukan integrasi langsung (sinkronisasi data) dengan Sistem Informasi Akademik (SIAKAD) eksternal milik kampus?
* **OPEN QUESTION-04**: Berapa batas toleransi persentase ketersediaan (*availability rate*) atau batas maksimal waktu mati (*downtime*) untuk memenuhi kriteria keandalan (*reliability*) sistem?
* **OPEN QUESTION-05**: Apakah sistem ke depannya akan membutuhkan fitur tambahan seperti komunikasi/obrolan langsung (*real-time chat*) atau integrasi kelas daring (*live streaming*)?

## 8. Quality Check Results

| Kriteria Mutu | Status | Catatan / Bukti Pemeriksaan |
| :--- | :---: | :--- |
| **Bebas Ambiguitas** | **PASSED** | Istilah subjektif seperti "kinerja tinggi", "cepat", atau "mudah" telah dieliminasi sepenuhnya dari dokumen. Target performa dialihkan ke bagian kualifikasi metrik pada *Open Questions*. |
| **Pemisahan Masalah & Solusi** | **PASSED** | Masalah operasional media terpisah (Section 1) telah dipisahkan secara tegas dari deskripsi solusi aplikasi yang ditawarkan (Section 2). |
| **Kepatuhan Fakta Kasus** | **PASSED** | Bagian *Out-of-Scope* telah dikosongkan dari klaim tanpa sumber. Dugaan fitur luar seperti absensi, chat, dan UKT telah dipindahkan secara objektif menjadi *Assumption* atau *Open Question*. |
| **Keterujian (*Testability*)** | **PASSED** | Seluruh batasan lingkup bersifat biner (*In-Scope*) sehingga dapat diverifikasi status implementasinya secara objektif. |
| **Kelebihan Asumsi & Pertanyaan** | **PASSED** | Elemen interpretatif di luar teks asli telah dilabeli secara eksplisit menggunakan format `ASSUMPTION-XX` dan `OPEN QUESTION-XX`. |
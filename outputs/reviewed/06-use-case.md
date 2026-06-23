# Use Case Specification - Student Task Management System

## 1. Actor Descriptions
* **Student**: Pengguna yang berinteraksi dengan sistem untuk melihat daftar tugas, memantau hitung mundur tenggat waktu, mengunggah berkas, dan melihat status pengumpulan tugas[cite: 1, 2].
* **Lecturer**: Pengguna yang memiliki otoritas penuh untuk membuat tugas, menetapkan deadline, memantau dasbor progres kelas, serta menginput nilai dan catatan umpan balik[cite: 1, 2].
* **Administrator**: Pengguna yang bertanggung jawab mengelola akun user, master data mata kuliah, pemetaan relasi kelas, dan mengatur konfigurasi global sistem[cite: 1, 2].

## 2. Use Case Diagram Overview
Sistem dibatasi oleh *System Boundary* "Student Task Management System"[cite: 1]. Use case dirancang terpusat di mana akses fungsionalitas utama aktor (Student, Lecturer, Administrator) diwajibkan melewati use case `Login & Autentikasi Terproteksi (FR-14)` melalui relasi `<<include>>` demi menjaga keamanan data.

## 3. Use Case Identification Table
| Use Case ID | Use Case Name | Primary Actor | Linked FR | Description |
| :--- | :--- | :--- | :--- | :--- |
| UC-01 | Login & Autentikasi Terproteksi | Student, Lecturer, Admin | FR-14 | Mengotentikasi pengguna masuk ke sistem berdasarkan hak akses aktor[cite: 2, 3]. |
| UC-02 | Melihat Daftar Tugas Aktif | Student | FR-03 | Menampilkan komponen seluruh daftar tugas perkuliahan yang aktif[cite: 2, 3]. |
| UC-03 | Memantau Hitung Mundur Deadline | Student | FR-04 | Menampilkan sisa waktu penunjuk batas akhir pengumpulan secara dinamis[cite: 3, 4]. |
| UC-04 | Mengunggah Berkas Jawaban Tugas | Student | FR-05 | Mengunggah file dokumen jawaban tugas elektronik ke server sistem[cite: 3]. |
| UC-05 | Memantau Status & Konfirmasi | Student | FR-06, FR-07 | Menampilkan status biner ("Sudah"/"Belum") dan indikator visual sukses[cite: 2, 3]. |
| UC-06 | Membuat Tugas & Batas Waktu | Lecturer | FR-01, FR-02 | Menginput tugas perkuliahan baru beserta detail jam/tanggal deadline[cite: 2, 3]. |
| UC-07 | Memantau Dasbor Progres Kelas | Lecturer | FR-08 | Melihat tabel rekapitulasi akumulasi progres pengumpulan tugas kelas[cite: 2, 3, 4]. |
| UC-08 | Memasukkan Nilai & Umpan Balik | Lecturer | FR-09, FR-10 | Menginput angka nilai evaluasi dan teks catatan umpan balik evaluasi[cite: 2, 3]. |
| UC-09 | Mengelola Data Akun Pengguna | Administrator | FR-11 | Menambah, mengubah, dan menonaktifkan akun kredensial pengguna[cite: 3]. |
| UC-10 | Mengelola Master Data Mata Kuliah | Administrator | FR-12 | Mengelola data objek kode dan nama mata kuliah kampus[cite: 2, 3]. |
| UC-11 | Memetakan Hubungan Kelas | Administrator | FR-13 | Memetakan hubungan data dosen, mahasiswa, dan mata kuliah ke kelas[cite: 2, 3]. |
| UC-12 | Mengatur Konfigurasi Global | Administrator | FR-15 | Mengatur kontrol akses konfigurasi teknis sistem secara global[cite: 2, 3]. |
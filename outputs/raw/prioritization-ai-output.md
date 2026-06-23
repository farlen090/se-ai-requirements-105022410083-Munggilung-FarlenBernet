# Prioritized Requirements

| ID | Requirement | Priority | Reason |
| :--- | :--- | :---: | :--- |
| FR-01 | Sistem harus memungkinkan Lecturer membuat tugas perkuliahan baru. | Must | Fungsionalitas fondasi utama; siklus manajemen tugas tidak dapat berjalan tanpa adanya komponen tugas yang dibuat. |
| FR-02 | Sistem harus memungkinkan Lecturer menetapkan tanggal dan jam batas akhir (*deadline*) pengumpulan tugas. | Must | Inti penyelesaian masalah bisnis untuk mengatasi kesulitan pemantauan tenggat waktu secara terpusat. |
| FR-03 | Sistem harus memungkinkan Student melihat daftar seluruh komponen tugas aktif. | Must | Diperlukan agar aktor Student dapat mendeteksi beban kewajiban akademik akademis yang harus dikerjakan. |
| FR-04 | Sistem harus memungkinkan Student memantau sisa waktu hitung mundur penunjuk *deadline*. | Should | Meningkatkan kesadaran urgensi pengerjaan bagi Student, tetapi kegagalannya tidak menghentikan fungsi utama pengumpulan. |
| FR-05 | Sistem harus menyediakan fasilitas bagi Student untuk mengunggah berkas jawaban tugas elektronik. | Must | Fungsionalitas transaksional kritikal yang menjadi solusi utama atas kendala pengumpulan media terpisah. |
| FR-06 | Sistem harus menampilkan status biner pengumpulan berkas jawaban tugas ("Belum" / "Sudah"). | Must | Kebutuhan transparansi status pelacakan bagi Student agar mengetahui kepastian pengumpulan tugasnya. |
| FR-07 | Sistem harus menampilkan indikator visual konfirmasi keberhasilan setelah berkas jawaban sukses terunggah. | Should | Penting untuk aspek kenyamanan pengguna (bukti transaksi sukses), namun bukan pemenuh fungsionalitas inti masuknya data. |
| FR-08 | Sistem harus memungkinkan Lecturer melihat dasbor pantau rekapitulasi progres pengumpulan tugas kelas. | Must | Akses kontrol pemantauan operasional yang krusial bagi Lecturer sebelum dapat mengeksekusi penilaian terstruktur. |
| FR-09 | Sistem harus memungkinkan Lecturer memasukkan nilai evaluasi hasil kerja Student ke dalam sistem. | Must | Siklus penutup yang kritikal bagi manajemen tugas perkuliahan untuk memenuhi target bisnis efisiensi penilaian. |
| FR-10 | Sistem harus memungkinkan Lecturer memberikan teks catatan umpan balik hasil evaluasi tugas. | Should | Menambah kualitas evaluasi akademik, tetapi pengisian nilai angka utama tetap dapat berjalan secara mandiri tanpa teks ini. |
| FR-11 | Sistem harus menyediakan fungsi bagi Administrator untuk menambah, mengubah, dan menonaktifkan akun user. | Must | Kebutuhan hulu yang mutlak demi pengadaan kredensial autentikasi pengguna sebelum platform dapat digunakan. |
| FR-12 | Sistem harus menyediakan fungsi bagi Administrator untuk mengelola master data mata kuliah kampus. | Must | Diperlukan sebagai kesatuan data master akademik yang mengikat kepemilikan komponen objek tugas perkuliahan. |
| FR-13 | Sistem harus memungkinkan Administrator memetakan hubungan data dosen, mahasiswa, dan mata kuliah ke kelas. | Must | Aturan bisnis fundamental untuk membatasi hak operasional Lecturer dan Student hanya pada ruang lingkup kelasnya. |
| FR-14 | Sistem harus memproteksi hak akses pengguna menggunakan sistem autentikasi login terproteksi per aktor. | Must | Parameter keamanan kritis untuk menjamin kerahasiaan data nilai dan integritas berkas dari akses luar ilegal. |
| FR-15 | Sistem harus menyediakan akses kontrol bagi Administrator untuk mengatur konfigurasi global sistem. | Could | Berguna untuk tata kelola konfigurasi menyeluruh, namun parameter sistem awal dapat diatur secara manual (*hardcoded*) pada fase awal. |

# Dependency Analysis

| Requirement | Depends On |
| :--- | :--- |
| FR-01 | FR-11, FR-12, FR-13 |
| FR-02 | FR-01 |
| FR-03 | FR-01, FR-13 |
| FR-04 | FR-02, FR-03 |
| FR-05 | FR-01, FR-13, FR-14 |
| FR-06 | FR-05 |
| FR-07 | FR-05 |
| FR-08 | FR-01, FR-05, FR-13 |
| FR-09 | FR-05, FR-08 |
| FR-10 | FR-09 |
| FR-13 | FR-11, FR-12 |
| FR-15 | FR-14 |

# Negotiation Notes
1. **Prioritas Urutan Hulu-Hilir**: Master data manajemen pengguna (`FR-11`), pengelolaan mata kuliah (`FR-12`), and pemetaan hubungan ruang kelas (`FR-13`) dikunci sebagai status **Must** karena pembentukan struktur data ini menjadi prasyarat mutlak sebelum fitur transaksional perkuliahan (`FR-01`, `FR-05`, `FR-09`) dapat dieksekusi secara teknis.
2. **Optimalisasi Ruang Lingkup Pertama**: Elemen kosmetik pembantu operasional pengguna seperti hitung mundur dinamis (`FR-04`), notifikasi konfirmasi sukses visual (`FR-07`), and teks catatan umpan balik naratif (`FR-10`) dialihkan ke status **Should** agar tim pengembang dapat memfokuskan alokasi daya kerja pada penyelesaian alur simpan data utama.
3. **Penundaan Elemen Eksternal**: Berdasarkan daftar ketidakpastian pada dokumen acuan, gagasan integrasi sinkronisasi otomatis dengan SIAKAD eksternal kampus (`OPEN QUESTION-10`) secara formal ditangguhkan ke dalam kategori **Won't Have** untuk implementasi rilis fase pertama ini demi menjaga kestabilan *timeline* proyek.

# Quality Check Results

| Kriteria Mutu | Status | Catatan / Bukti Pemeriksaan |
| :--- | :---: | :--- |
| **Prioritas Komprehensif** | **PASSED** | Seluruh 15 Functional Requirements dari dokumen acuan `03-requirments.md` telah dipetakan tanpa adanya item yang terlewat. |
| **Justifikasi Transparan** | **PASSED** | Setiap komponen baris penggolongan MoSCoW didukung alasan bisnis dan teknis yang objektif pada kolom *Reason*. |
| **Penetapan Status Kritis** | **PASSED** | Kebutuhan fondasi struktural, transaksi utama, dan proteksi keamanan dasar telah dilabeli secara ketat menggunakan bobot **Must**. |
| **Dokumentasi Dependensi** | **PASSED** | Hubungan ketergantungan sekuensial antarsistem telah dianalisis secara runtut menggunakan tabel *Dependency Analysis*. |
| **Kepatuhan Data Sumber** | **PASSED** | Tidak terdapat penambahan requirement fungsional baru buatan sendiri; data murni diekstrak dari dokumen logis yang tersedia. |
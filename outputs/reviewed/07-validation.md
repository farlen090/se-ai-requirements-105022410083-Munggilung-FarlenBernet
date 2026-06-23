# Requirements Validation Report

## 1. Validation Methodology
Validasi kebutuhan fungsional dilakukan dengan menguji kesesuaian antara *Functional Requirements* (FR) dan *Acceptance Criteria* (AC) yang melekat pada setiap *User Story* menggunakan pendekatan pengujian berbasis skenario kelayakan (*Acceptance Testing*)[cite: 3, 4].

## 2. Acceptance Test Scenarios

### Scenario 1: Pembuatan Tugas Berbatas Waktu (US-01 -> FR-01, FR-02)
* **Given**: Lecturer telah berhasil login dan berada pada form input pembuatan tugas baru[cite: 3, 4].
* **When**: Lecturer mengisi judul, deskripsi tugas, namun mengosongkan kolom tanggal atau jam batas akhir pengumpulan, lalu menekan tombol simpan[cite: 4].
* **Then**: Sistem menolak pembuatan tugas dan memunculkan pesan validasi error sesuai aturan aturan `AC-01.02`[cite: 4].

### Scenario 2: Pemantauan Daftar Tugas dan Hitung Mundur (US-02 -> FR-03, FR-04)
* **Given**: Student berada di halaman utama Dasbor Student setelah autentikasi[cite: 4].
* **When**: Sistem memuat halaman tugas perkuliahan[cite: 1, 2].
* **Then**: Sistem menampilkan nama tugas yang belum lewat deadline (`AC-02.01`) lengkap dengan sisa waktu pengerjaan dalam format penunjuk hari dan jam yang berkurang dinamis (`AC-02.02`)[cite: 4].

### Scenario 3: Pengunggahan Berkas Jawaban (US-03 -> FR-05, FR-06, FR-07)
* **Given**: Student membuka halaman detail tugas yang berstatus aktif[cite: 2].
* **When**: Student menekan tombol unggah berkas, memilih file dari penyimpanan lokal, dan mengirimkannya ke sistem[cite: 4].
* **Then**: Sistem menyimpan berkas di server, mengubah status biner menjadi "Sudah" (`FR-06`), dan menampilkan teks/ikon hijau konfirmasi sukses sesuai `AC-03.02`[cite: 3, 4].

### Scenario 4: Pemantauan Progres Kelas (US-04 -> FR-08)
* **Given**: Lecturer membuka modul dasbor pantau rekapitulasi progres kelas[cite: 3].
* **When**: Lecturer melihat tabel rekapitulasi pengumpulan tugas[cite: 4].
* **Then**: Sistem menampilkan status biner "Sudah"/"Belum" untuk tiap nama mahasiswa (`AC-04.01`) serta rasio jumlah total berkas masuk dibanding total mahasiswa kelas (`AC-04.02`)[cite: 4].

### Scenario 5: Penginputan Evaluasi Nilai & Feedback (US-05 -> FR-09, FR-10)
* **Given**: Lecturer memeriksa hasil kerja salah satu berkas tugas elektronik mahasiswa[cite: 3].
* **When**: Lecturer mengisi kolom angka nilai, mengisi area teks catatan umpan balik, dan menekan tombol simpan[cite: 4].
* **Then**: Sistem menyimpan data, otomatis memperbarui status rekap nilai mahasiswa, dan mengunci data sesuai prasyarat `CONSTRAINT-02`[cite: 1, 4].

### Scenario 6: Pemetaan Hubungan Struktur Akademik (US-06 -> FR-13)
* **Given**: Administrator berada pada antarmuka pengelolaan relasi struktur data akademik[cite: 4].
* **When**: Administrator memilih nama dosen, daftar mahasiswa, nama mata kuliah, lalu menyimpannya ke dalam satu ID kelas[cite: 4].
* **Then**: Sistem mengunci relasi kelas (`AC-06.01`) dan otomatis membuka hak akses ruang tugas bagi Lecturer dan Student terkait (`AC-06.02`)[cite: 4].
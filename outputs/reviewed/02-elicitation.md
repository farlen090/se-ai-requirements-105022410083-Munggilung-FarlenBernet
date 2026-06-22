# Requirements Elicitation

## 1. Elicitation Techniques
1. **Document Analysis**: Menganalisis berkas `01-inception.md` dan `CASE.md` untuk menyaring kebutuhan mendasar yang eksplisit.
2. **Structured Interview**: Menyusun daftar pertanyaan terarah bagi setiap stakeholder guna mengonfirmasi kebutuhan implisit.

## 2. Stakeholder Interview Questions

### Lecturer
* **Pertanyaan 1**: Bagaimana langkah alur kerja yang diinginkan ketika membuat komponen tugas baru di dalam sistem?
* **Pertanyaan 2**: Jenis umpan balik seperti apa yang ingin Anda berikan kepada mahasiswa (apakah berupa teks catatan atau nilai)?
* **Pertanyaan 3**: Apakah ada kebijakan toleransi waktu pengumpulan berkas setelah batas *deadline* terlewati?

### Student
* **Pertanyaan 1**: Atribut informasi apa saja yang wajib ditampilkan pada komponen daftar tugas aktif mahasiswa?
* **Pertanyaan 2**: Bagaimana indikator visual konfirmasi sukses yang Anda harapkan setelah berhasil mengunggah berkas jawaban?
* **Pertanyaan 3**: Apakah mahasiswa diizinkan melakukan pembatalan berkas tugas sebelum melewati batas tenggat waktu?

### Administrator
* **Pertanyaan 1**: Bagaimana mekanisme teknis yang diinginkan untuk membuat atau melakukan impor data akun pengguna baru?
* **Pertanyaan 2**: Atribut data apa saja yang wajib dicatat ketika mengelola master data mata kuliah di dalam sistem?
* **Pertanyaan 3**: Parameter konfigurasi global apa saja yang perlu dikendalikan oleh Administrator melalui sistem ini?

## 3. Explicit Needs

| ID | Stakeholder | Need | Source |
| :--- | :--- | :--- | :--- |
| EN-01 | Lecturer | Membuat tugas perkuliahan. | CASE.md |
| EN-02 | Lecturer | Menetapkan tenggat waktu tugas. | CASE.md |
| EN-03 | Lecturer | Memberikan nilai hasil kerja. | CASE.md |
| EN-04 | Lecturer | Memberikan umpan balik tugas. | CASE.md |
| EN-05 | Student | Melihat daftar tugas perkuliahan. | CASE.md |
| EN-06 | Student | Memantau status pengumpulan. | CASE.md |
| EN-07 | Student | Memantau tenggat waktu tugas. | CASE.md |
| EN-08 | Student | Mengumpulkan file tugas ke sistem. | CASE.md |
| EN-09 | Admin | Mengelola data akun pengguna. | CASE.md |
| EN-10 | Admin | Mengelola data mata kuliah. | CASE.md |
| EN-11 | Admin | Mengatur konfigurasi global. | CASE.md |

## 4. Implicit Needs

| ID | Stakeholder | Need | Reasoning |
| :--- | :--- | :--- | :--- |
| IN-01 | All | Akses login aman per aktor. | Melindungi kerahasiaan data nilai mahasiswa. |
| IN-02 | Lecturer | Melihat rekap pengumpulan kelas. | Memantau status keterlambatan mahasiswa. |
| IN-03 | Student | Menerima bukti sukses unggah berkas. | Memberikan kepastian data masuk ke server. |
| IN-04 | Admin | Pemetaan relasi kelas kuliah. | Menghubungkan user dengan mata kuliah. |

## 5. Elicitation Findings

| ID | Description | Stakeholder |
| :--- | :--- | :--- |
| EL-01 | Pembuatan komponen tugas perkuliahan oleh dosen. | Lecturer |
| EL-02 | Penentuan batas akhir jam dan tanggal *deadline* tugas. | Lecturer |
| EL-03 | Pengisian nilai evaluasi hasil kerja mahasiswa. | Lecturer |
| EL-04 | Pemberian teks catatan umpan balik hasil evaluasi. | Lecturer |
| EL-05 | Penampilan daftar komponen seluruh tugas aktif mahasiswa. | Student |
| EL-06 | Penampilan status biner pengumpulan berkas jawaban. | Student |
| EL-07 | Penampilan penunjuk waktu batas akhir pengumpulan. | Student |
| EL-08 | Fasilitas unggah berkas jawaban tugas ke sistem. | Student |
| EL-09 | Fungsi pengelolaan data akun pengguna oleh admin. | Admin |
| EL-10 | Fungsi pengelolaan master data mata kuliah kampus. | Admin |
| EL-11 | Kontrol akses pengaturan konfigurasi global sistem. | Admin |
| EL-12 | Sistem autentikasi login terproteksi per aktor. | All |
| EL-13 | Dasbor pantau rekapitulasi progres pengumpulan tugas. | Lecturer |
| EL-14 | Indikator visual konfirmasi keberhasilan unggah berkas. | Student |
| EL-15 | Modul pemetaan hubungan data user dan mata kuliah. | Admin |

## 6. Open Questions
* **OPEN QUESTION-06**: Apakah diperlukan sistem pengingat (*reminder*) bagi Student sebelum batas *deadline* pengumpulan berakhir?
* **OPEN QUESTION-07**: Apakah pengisian umpan balik oleh Lecturer bersifat wajib untuk setiap mahasiswa, atau bersifat opsional?
* **OPEN QUESTION-08**: Apakah sistem harus menyimpan histori versi berkas (*versioning*) jika Student mengunggah ulang file tugasnya?
* **OPEN QUESTION-09**: Apakah ada batasan maksimal kapasitas ukuran berkas (*file size*) dan format ekstensi file yang diizinkan?

## 7. Summary
Proses *elicitation* berhasil menyaring 11 kebutuhan eksplisit (`EN-01` s.d `EN-11`) dan mengidentifikasi 4 kebutuhan implisit (`IN-01` s.d `IN-04`) untuk *Student Task Management System*. Seluruh temuan kebutuhan gabungan telah dipetakan secara rapi dengan penomoran unik (`EL-01` s.d `EL-15`). Kebutuhan yang belum pasti metrik kuantitatifnya dicatat pada bagian *Open Questions*.
# Functional and Non-Functional Requirements

## 1. Functional Requirements

| ID | Requirement | Source |
| :--- | :--- | :--- |
| FR-01 | Sistem harus memungkinkan Lecturer membuat tugas perkuliahan baru. | EL-01, EN-01 |
| FR-02 | Sistem harus memungkinkan Lecturer menetapkan tanggal dan jam batas akhir (*deadline*) pengumpulan tugas. | EL-02, EN-02 |
| FR-03 | Sistem harus memungkinkan Student melihat daftar seluruh komponen tugas aktif. | EL-05, EN-05 |
| FR-04 | Sistem harus memungkinkan Student memantau sisa waktu hitung mundur penunjuk *deadline*. | EL-07, EN-07 |
| FR-05 | Sistem harus menyediakan fasilitas bagi Student untuk mengunggah berkas jawaban tugas elektronik. | EL-08, EN-08 |
| FR-06 | Sistem harus menampilkan status biner pengumpulan berkas jawaban tugas ("Belum" / "Sudah"). | EL-06, EN-06 |
| FR-07 | Sistem harus menampilkan indikator visual konfirmasi keberhasilan setelah berkas jawaban sukses terunggah. | EL-14, IN-03 |
| FR-08 | Sistem harus memungkinkan Lecturer melihat dasbor pantau rekapitulasi progres pengumpulan tugas kelas. | EL-13, IN-02 |
| FR-09 | Sistem harus memungkinkan Lecturer memasukkan nilai evaluasi hasil kerja Student ke dalam sistem. | EL-03, EN-03 |
| FR-10 | Sistem harus memungkinkan Lecturer memberikan teks catatan umpan balik hasil evaluasi tugas. | EL-04, EN-04 |
| FR-11 | Sistem harus menyediakan fungsi bagi Administrator untuk menambah, mengubah, dan menonaktifkan akun user. | EL-09, EN-09 |
| FR-12 | Sistem harus menyediakan fungsi bagi Administrator untuk mengelola master data mata kuliah kampus. | EL-10, EN-10 |
| FR-13 | Sistem harus memungkinkan Administrator memetakan hubungan data dosen, mahasiswa, dan mata kuliah ke kelas. | EL-15, IN-04 |
| FR-14 | Sistem harus memproteksi hak akses pengguna menggunakan sistem autentikasi login terproteksi per aktor. | EL-12, IN-01 |
| FR-15 | Sistem harus menyediakan akses kontrol bagi Administrator untuk mengatur konfigurasi global sistem. | EL-11, EN-11 |

## 2. Non-Functional Requirements

| ID | Kategori | Requirement | Source |
| :--- | :--- | :--- | :--- |
| NFR-01 | Usability | Sistem wajib menampilkan pesan konfirmasi biner visual yang jelas setelah proses transaksi unggah berkas sukses dilakukan. | IN-03, CASE.md |
| NFR-02 | Security | Sistem wajib menerapkan proteksi enkripsi atau pembatasan hak akses ketat untuk menjaga kerahasiaan data nilai mahasiswa. | IN-01, CASE.md |

## 3. Business Rules

| ID | Description | Source |
| :--- | :--- | :--- |
| BR-01 | Mahasiswa wajib memiliki status akun aktif dan terdaftar di dalam kelas mata kuliah terkait agar dapat melakukan pengumpulan tugas. | ASSUMPTION-01, IN-04 |
| BR-02 | Dosen hanya memiliki otoritas penuh untuk membuat komponen tugas dan menginput nilai pada kelas mata kuliah yang diampunya. | ASSUMPTION-02, IN-04 |

## 4. Open Questions
* **OPEN QUESTION-02**: Berapa batas waktu respons (dalam detik) dan jumlah maksimal *concurrent users* saat diakses bersamaan untuk menguji kriteria kuantitatif kinerja sistem? (Berasal dari `NFR-03`)
* **OPEN QUESTION-04**: Berapa target persentase ketersediaan (*availability rate*) atau batas waktu toleransi mati (*downtime*) untuk menguji kriteria kuantitatif keandalan sistem? (Berasal dari `NFR-04`)
* **OPEN QUESTION-10**: Apakah data mata kuliah dan akun user harus disinkronisasikan langsung secara otomatis dengan SIAKAD eksternal? (Dipindahkan dari `BR-03`)

## 5. Quality Check Results

| Kriteria Mutu | Status | Catatan / Bukti Pemeriksaan |
| :--- | :---: | :--- |
| **Bebas Ambiguitas & Keterujian** | **PASSED** | Kalimat kualitatif subjektif telah dihilangkan. NFR yang belum memiliki parameter uji kuantitatif dipindahkan ke *Open Questions*. |
| **Pemisahan Berkas** | **PASSED** | Dokumen ini hanya berfokus pada spesifikasi inti FR, NFR, dan BR tanpa tercampur dengan User Stories. |
| **Ketertelusuran (*Traceability*)** | **PASSED** | Seluruh FR, NFR, dan BR memiliki pemetaan kode sumber yang jelas ke dokumen `02-elicitation.md`. |
| **Penyaringan Aturan Bisnis** | **PASSED** | Elemen ketidakpastian (`BR-03` lama) telah didegradasi ke bagian *Open Questions* sebagai `OPEN QUESTION-10`. |
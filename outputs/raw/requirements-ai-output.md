# Functional Requirements

| ID | Requirement | Source |
| :--- | :--- | :--- |
| FR-01 | Sistem harus memungkinkan Lecturer membuat tugas perkuliahan baru. | EL-01, EN-01 |
| FR-02 | Sistem harus memungkinkan Lecturer menetapkan tanggal dan jam batas akhir (*deadline*) pengumpulan tugas. | EL-02, EN-02 |
| FR-03 | Sistem harus memungkinkan Student melihat daftar seluruh komponen tugas aktif. | EL-05, EN-05 |
| FR-04 | Sistem harus memungkinkan Student memantau sisa waktu hitung mundur penunjuk *deadline*. | EL-07, EN-07 |
| FR-05 | Sistem harus menyediakan fasilitas bagi Student untuk mengunggah berkas jawaban tugas elektronik. | EL-08, EN-08 |
| FR-06 | Sistem harus menampilkan status biner pengumpulan berkas jawaban tugas (contoh: "Belum" / "Sudah"). | EL-06, EN-06 |
| FR-07 | Sistem harus menampilkan indikator visual konfirmasi keberhasilan setelah berkas jawaban sukses terunggah. | EL-14, IN-03 |
| FR-08 | Sistem harus memungkinkan Lecturer melihat dasbor pantau rekapitulasi progres pengumpulan tugas kelas. | EL-13, IN-02 |
| FR-09 | Sistem harus memungkinkan Lecturer memasukkan nilai evaluasi hasil kerja Student ke dalam sistem. | EL-03, EN-03 |
| FR-10 | Sistem harus memungkinkan Lecturer memberikan teks catatan umpan balik hasil evaluasi tugas. | EL-04, EN-04 |
| FR-11 | Sistem harus menyediakan fungsi bagi Administrator untuk menambah, mengubah, dan menonaktifkan akun user. | EL-09, EN-09 |
| FR-12 | Sistem harus menyediakan fungsi bagi Administrator untuk mengelola master data mata kuliah kampus. | EL-10, EN-10 |
| FR-13 | Sistem harus memungkinkan Administrator memetakan hubungan data dosen, mahasiswa, dan mata kuliah ke kelas. | EL-15, IN-04 |
| FR-14 | Sistem harus memproteksi hak akses pengguna menggunakan sistem autentikasi login terproteksi per aktor. | EL-12, IN-01 |
| FR-15 | Sistem harus menyediakan akses kontrol bagi Administrator untuk mengatur konfigurasi global sistem. | EL-11, EN-11 |

# Non-Functional Requirements

| ID | Kategori | Requirement | Source |
| :--- | :--- | :--- | :--- |
| NFR-01 | Usability | Sistem wajib menampilkan pesan konfirmasi biner visual yang jelas setelah proses transaksi unggah berkas sukses dilakukan. | IN-03, CASE.md |
| NFR-02 | Security | Sistem wajib menerapkan proteksi enkripsi atau pembatasan hak akses ketat untuk menjaga kerahasiaan data nilai mahasiswa. | IN-01, CASE.md |
| NFR-03 | Performance | OPEN QUESTION-02: Berapa batas waktu respons (dalam detik) dan jumlah maksimal *concurrent users* saat diakses bersamaan? | CONSTRAINT-03 |
| NFR-04 | Reliability | OPEN QUESTION-04: Berapa target persentase ketersediaan (*availability rate*) atau batas waktu toleransi mati (*downtime*)? | CASE.md |

# Business Rules

| ID | Description | Source |
| :--- | :--- | :--- |
| BR-01 | Mahasiswa wajib memiliki status akun aktif dan terdaftar di dalam kelas mata kuliah terkait agar dapat melakukan pengumpulan tugas. | ASSUMPTION-01, IN-04 |
| BR-02 | Dosen hanya memiliki otoritas penuh untuk membuat komponen tugas dan menginput nilai pada kelas mata kuliah yang diampunya. | ASSUMPTION-02, IN-04 |
| BR-03 | OPEN QUESTION-03: Apakah data mata kuliah dan akun user harus disinkronisasikan langsung secara otomatis dengan SIAKAD eksternal? | OPEN QUESTION-03 |

# User Stories

### US-01
As a Lecturer  
I want to create a new assignment and set its deadline  
So that students know the requirements and the submission limit  

#### Acceptance Criteria
* AC-01.01: Sistem menyediakan form input judul, deskripsi tugas, tanggal batas akhir, dan jam batas akhir pengumpulan.
* AC-01.02: Sistem menolak pembuatan tugas jika kolom tanggal atau jam batas akhir dikosongkan.

---

### US-02
As a Student  
I want to view the list of active assignments and their countdowns  
So that I can prioritize my tasks and submit them before they expire  

#### Acceptance Criteria
* AC-02.01: Dasbor Student menampilkan daftar nama tugas yang belum melewati tenggat waktu.
* AC-02.02: Setiap item tugas menampilkan sisa waktu pengerjaan dalam format penunjuk hari dan jam yang berkurang secara dinamis.

---

### US-03
As a Student  
I want to upload my assignment file into the system  
So that my lecturer can receive and evaluate my work  

#### Acceptance Criteria
* AC-03.01: Sistem menyediakan tombol unggah file yang memicu jendela pemilihan berkas penyimpanan lokal pengguna.
* AC-03.02: Sistem menampilkan indikator visual sukses (seperti teks atau ikon hijau) setelah berkas berhasil disimpan di server.

---

### US-04
As a Lecturer  
I want to monitor the submission progress dashboard for my class  
So that I can instantly track which students have or have not submitted their files  

#### Acceptance Criteria
* AC-04.01: Sistem menampilkan tabel rekapitulasi nama mahasiswa di kelas, lengkap dengan status biner "Sudah" atau "Belum" mengumpulkan.
* AC-04.02: Sistem menampilkan jumlah total akumulasi berkas yang telah masuk dibandingkan jumlah total mahasiswa di kelas tersebut.

---

### US-05
As a Lecturer  
I want to submit grades and text feedback for student work  
So that students can see their performance evaluation results  

#### Acceptance Criteria
* AC-05.01: Sistem menyediakan kolom input angka untuk nilai dan area teks (*text area*) untuk catatan umpan balik pada halaman evaluasi kerja mahasiswa.
* AC-05.02: Nilai dan umpan balik yang disimpan otomatis memperbarui status data nilai mahasiswa yang bersangkutan secara rapi.

---

### US-06
As an Administrator  
I want to map lecturers, students, and courses into specific classes  
So that the academic structure works correctly and user relations are established  

#### Acceptance Criteria
* AC-06.01: Sistem menyediakan antarmuka untuk memilih nama dosen, daftar mahasiswa, dan nama mata kuliah untuk dikelompokkan ke satu ID kelas.
* AC-06.02: Ketika kelas berhasil disimpan, Lecturer dan Student yang terdaftar otomatis mendapatkan akses ke ruang tugas kelas tersebut.

## Skill 3 - Requirements Elaboration and Specification

### AI Output File

outputs/raw/requirements-ai-output.md

### Kelebihan Output AI

* Menghasilkan Functional Requirements yang lengkap dan dapat ditelusuri ke hasil elicitation.
* Menghasilkan Non-Functional Requirements sesuai kebutuhan sistem.
* Menyediakan Business Rules yang relevan dengan studi kasus.
* Menghasilkan User Stories dan Acceptance Criteria yang terstruktur.

### Problems Found

1. Beberapa Non-Functional Requirements masih berbentuk Open Question.
2. Business Rule BR-03 bukan aturan bisnis melainkan pertanyaan terbuka.
3. Terdapat beberapa istilah yang perlu dikonsistenkan dengan dokumen sebelumnya.

### Student Corrections

1. Memperjelas NFR yang masih belum memiliki parameter kuantitatif.
2. Memindahkan BR-03 ke bagian Open Questions.
3. Menyamakan istilah stakeholder menjadi Administrator.

### Final Output

outputs/reviewed/03-requirements.md

outputs/reviewed/04-user-stories.md

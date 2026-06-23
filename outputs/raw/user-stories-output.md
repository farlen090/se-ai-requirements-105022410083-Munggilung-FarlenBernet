# User Stories - Student Task Management System (Raw AI Draft)

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
As an Admin  
I want to map lecturers, students, and courses into specific classes  
So that the academic structure works correctly and user relations are established  

#### Acceptance Criteria
* AC-06.01: Sistem menyediakan antarmuka untuk memilih nama dosen, daftar mahasiswa, dan nama mata kuliah untuk dikelompokkan ke satu ID kelas.
* AC-06.02: Ketika kelas berhasil disimpan, Lecturer dan Student yang terdaftar otomatis mendapatkan akses ke ruang tugas kelas tersebut.
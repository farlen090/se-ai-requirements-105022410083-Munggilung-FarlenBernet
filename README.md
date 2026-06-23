# Student Task Management System - Requirements Engineering Artifacts

Repositori ini berisi seluruh artefak Requirements Engineering untuk pengembangan **Student Task Management System** yang dikerjakan menggunakan metode kolaborasi *AI-Assisted Requirements Engineering*. Proyek ini mencakup perancangan *reusable AI skills*, analisis kebutuhan terstruktur, manajemen prioritas, pelacakan evaluasi keluaran AI, hingga matriks ketertelusuran kebutuhan akhir.

---

## 1. Project Information
* **Nama Pengembang:** [Munggilung, Farlen Bernet]
* **NIM:** [105022410083]
* **Kelas:** [Software Engineering - A]
* **AI Tool / Model:** Gemini 1.5 Pro / GPT-4o Collaboration

---

## 2. Use Case Diagram
Berikut adalah diagram fungsionalitas sistem yang menggambarkan interaksi antara aktor *Lecturer*, *Student*, dan *Administrator* terhadap batas sistem:

![Use Case Diagram](use-case-diagram.png)

*Catatan: Pastikan kamu menaruh file gambar diagram dengan nama `use-case-diagram.png` di folder utama proyekmu agar gambar ini langsung muncul di GitHub.*

---

## 3. Comprehensive Traceability Matrix
Matriks ini menghubungkan konsistensi seluruh artefak kebutuhan secara *end-to-end*, mulai dari fase Inception awal, temuan Elicitation (Explicit & Implicit Needs), spesifikasi Functional Requirements (FR), hingga User Stories (US) beserta Acceptance Criteria (AC).

| Inception ID | Elicitation Needs ID | Functional Requirement ID | User Story ID | Target Feature Summary |
| :---: | :---: | :---: | :---: | :--- |
| EL-01 / EL-02 | EN-01 / EN-02 | FR-01 / FR-02 | US-01 | Pembuatan tugas baru beserta tenggat waktu (*deadline*) oleh Lecturer. |
| EL-05 / EL-07 | EN-05 / EN-07 | FR-03 / FR-04 | US-02 | Dasbor pemantauan daftar tugas aktif dan sisa waktu hitung mundur bagi Student. |
| EL-08 / EL-06 / EL-14 | EN-08 / EN-06 / IN-03 | FR-05 / FR-06 / FR-07 | US-03 | Fasilitas unggah berkas jawaban elektronik, status biner, dan konfirmasi sukses bagi Student. |
| EL-13 | IN-02 | FR-08 | US-04 | Dasbor rekapitulasi progres pengumpulan tugas kelas secara *real-time* untuk Lecturer. |
| EL-03 / EL-04 | EN-03 / EN-04 | FR-09 / FR-10 | US-05 | Pengisian nilai evaluasi angka dan catatan umpan balik naratif oleh Lecturer. |
| EL-09 / EL-10 / EL-15 | EN-09 / EN-10 / IN-04 | FR-11 / FR-12 / FR-13 | US-06 | Pengelolaan akun user, master data mata kuliah, dan pemetaan relasi kelas oleh Administrator. |
| EL-12 / EL-11 | IN-01 / EN-11 | FR-14 / FR-15 | - | Autentikasi login terproteksi per aktor dan akses kontrol konfigurasi global sistem. |

---

## 4. Repository Structure Checklist
Seluruh dokumen telah disusun secara terstruktur sesuai dengan arsitektur folder wajib rekayasa kebutuhan perangkat lunak:
* 📁 **`skills/`** : Berisi berkas panduan instruksi kerja terstruktur (`SKILL.md`) untuk mengarahkan AI di setiap tahapan.
* 📁 **`outputs/raw/`** : Berisi draf dokumen mentah (*raw output*) hasil generasi pertama AI.
* 📁 **`outputs/reviewed/`** : Berisi dokumen spesifikasi final yang telah melalui proses validasi, pembersihan ambiguitas, dan penataan oleh manusia (*human review*).
* 📁 **`evaluation/`** : Berisi file `ai-output-review.md` yang mencatat kelebihan, kekurangan, dan koreksi perbaikan kritis mahasiswa terhadap kinerja AI.
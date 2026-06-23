# Student Task Management System - Requirements Engineering Artifacts

Repositori ini berisi seluruh artefak Requirements Engineering untuk pengembangan **Student Task Management System** yang dikerjakan menggunakan metode kolaborasi *AI-Assisted Requirements Engineering*. Proyek ini mencakup perancangan *reusable AI skills*, analisis kebutuhan terstruktur, manajemen prioritas, pelacakan evaluasi keluaran AI, hingga matriks ketertelusuran kebutuhan akhir.

---

## 1. Project Information
* **Nama Pengembang:** Munggilung, Farlen Bernet
* **NIM:** 105022410083
* **Kelas:** Software Engineering - A
* **AI Tool / Model:** Gemini 1.5 Pro / GPT-4o Collaboration

---

## 2. Use Case Diagram
Berikut adalah diagram fungsionalitas sistem yang menggambarkan interaksi antara aktor *Lecturer*, *Student*, dan *Administrator* terhadap batas sistem:

![Use Case Diagram](use%20case%20diagram.png)

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
* 📁 **`evaluation/`** : Berisi catatan evaluasi luaran AI dan hasil uji coba ulang reusability.

---

## 5. Final Outputs
Berikut adalah tautan langsung menuju seluruh dokumen spesifikasi kebutuhan yang telah divalidasi (*human-reviewed*):
* [01 - Project Inception](outputs/reviewed/01-inception.md)
* [02 - Requirements Elicitation](outputs/reviewed/02-elicitation.md)
* [03 - System Requirements Specification](outputs/reviewed/03-requirements.md)
* [04 - User Stories and Acceptance Criteria](outputs/reviewed/04-user-stories.md)
* [05 - Requirements Prioritization](outputs/reviewed/05-prioritization.md)
* [06 - Use Case Specifications](outputs/reviewed/06-use-case.md)

---

## 6. AI Usage & Configuration
* **Execution Date:** Juni 2026
* **Skills Tested:** Skill 1 (Project Inception) & Skill 2 (Requirements Elicitation)
* **Major Corrections Made:** 1. Menghapus fungsionalitas spekulatif buatan AI (fitur *live chat* antar-user) yang di luar batas *scope* dokumen inisiasi.
  2. Mengoreksi istilah tidak baku dan tidak konsisten seperti penggunaan kata "Admin" menjadi "Administrator" secara global.
  3. Mengubah kriteria kualitas non-fungsional yang abstrak (*"proses harus cepat"*) menjadi batasan metrik kuantitatif (*"waktu respons halaman < 3 detik"*) pada berkas ulasan.

---

## 7. Reflection
* **Kelebihan AI:** AI sangat andal dan cepat dalam menyusun struktur penulisan kalimat bersyarat seperti skenario *Acceptance Criteria* biner dan memetakan draf awal *User Stories* dari sudut pandang berbagai aktor tanpa ada yang terlewat.
* **Kelemahan & Kesalahan AI:** AI sering kali melakukan halusinasi dengan menambahkan fitur-fitur "siluman" di luar ruang lingkup yang disepakati, serta cenderung menggunakan kata-kata kualitatif yang ambigu dan tidak dapat diuji (*untestable*).
* **Pentingnya Human Review:** Peran manusia sebagai *Requirements Engineer* mutlak diperlukan untuk melakukan kurasi ketat, menyelaraskan batasan logika bisnis riil, menjaga standarisasi nomenklatur aktor, dan memastikan setiap kebutuhan dapat diukur dan divalidasi secara mekanis sebelum masuk ke fase baseline pengembangan.
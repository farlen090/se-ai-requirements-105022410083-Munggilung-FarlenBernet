# AI Output Review

## Skill 1 - Project Inception and Stakeholder Discovery
* **AI Output File**: `outputs/raw/inception-ai-output.md`
* **Problems Found**:
    1. Penomoran section tidak konsisten.
    2. Constraint "kinerja tinggi" masih ambigu.
    3. Beberapa out-of-scope belum jelas.
* **Student Corrections**:
    1. Memperbaiki penomoran.
    2. Mengubah istilah ambigu menjadi lebih terukur atau OPEN QUESTION.
    3. Memisahkan masalah dan solusi secara lebih jelas.
    4. Menambahkan quality check.
* **Final Output**: `outputs/reviewed/01-inception.md`

---

## Skill 2 - Requirements Elicitation
* **AI Output File**: `outputs/raw/elicitation-ai-output.md`
* **Kelebihan Output AI**:
    * Berhasil mengidentifikasi kebutuhan eksplisit berdasarkan stakeholder.
    * Berhasil memisahkan kebutuhan eksplisit dan implisit.
    * Menyediakan pertanyaan wawancara untuk setiap stakeholder.
    * Menyediakan open questions untuk validasi lebih lanjut.
* **Problems Found**:
    1. Menggunakan ID EL-XX untuk Explicit Needs dan Implicit Needs.
    2. Beberapa kebutuhan implisit belum memiliki dasar yang kuat dari dokumen sumber.
    3. Istilah "Modul relasi plot dosen-mhs-matkul" kurang jelas.
    4. Traceability terhadap Open Questions dari Skill 1 belum terlihat.
* **Student Corrections**:
    1. Menggunakan ID EN-XX untuk Explicit Needs.
    2. Menggunakan ID IN-XX untuk Implicit Needs.
    3. Memperjelas kebutuhan implisit yang ambigu.
    4. Menyesuaikan temuan elicitation agar lebih mudah ditelusuri ke stakeholder.
* **Final Output**: `outputs/reviewed/02-elicitation.md`[cite: 6]

---

## Skill 3 - Requirements Elaboration and Specification
* **AI Output File**: `outputs/raw/requirements-ai-output.md`[cite: 6]
* **Kelebihan Output AI**:
    * Menghasilkan daftar lengkap 15 fungsionalitas utama (FR-01 s.d FR-15).
    * Berhasil menyusun skenario User Stories dengan format baku *As a... I want... So that...*.
* **Problems Found**:
    1. AI menggunakan kata-kata subjektif tidak terukur pada Non-Functional Requirements seperti "respon cepat".
    2. Format penamaan file keluaran tidak sinkron dengan struktur repositori yang diminta instruksi tugas.
* **Student Corrections**:
    1. Melakukan kalibrasi metrik NFR dan memisahkan aturan bisnis (Business Rules) secara ketat.
    2. Memisahkan dokumen spesifikasi menjadi dua file sesuai standar repositori, yaitu `03-requirements.md` dan `04-user-stories.md`.
* **Final Output**: `outputs/reviewed/03-requirements.md` dan `outputs/reviewed/04-user-stories.md`[cite: 6]

---

## Skill 4 - Requirements Prioritization and Negotiation
* **AI Output File**: `outputs/raw/prioritization-ai-output.md`[cite: 6]
* **Kelebihan Output AI**:
    * Seluruh Functional Requirements (FR-01 sampai FR-15) berhasil diprioritaskan menggunakan metode MoSCoW.
    * Setiap prioritas memiliki alasan yang jelas.
    * Dependency Analysis membantu memahami urutan implementasi requirement.
    * Negotiation Notes menjelaskan dasar pengambilan keputusan prioritas.
* **Kekurangan Output AI**:
    1. Terdapat typo pada nama file sumber "03-requirments.md" yang seharusnya "03-requirements.md".
    2. FR-12 tidak muncul pada tabel Dependency Analysis meskipun menjadi requirement penting.
    3. Beberapa alasan prioritas masih terlalu panjang dan dapat diringkas.
    4. Status Won't Have untuk integrasi SIAKAD belum menggunakan format requirement ID karena berasal dari Open Question.
* **Perbaikan yang Dilakukan**:
    1. Memperbaiki typo nama file sumber.
    2. Menambahkan FR-12 pada analisis dependensi.
    3. Merapikan kalimat alasan prioritas agar lebih ringkas.
    4. Memastikan seluruh keputusan prioritas tetap konsisten dengan dokumen requirements sebelumnya.
* **Final Output**: `outputs/reviewed/05-prioritization.md`[cite: 6]

---

## Skill 5 - Requirements Validation and Change Management
* **AI Output File**: `outputs/raw/validation-ai-output.md`[cite: 6]
* **Problems Found**:
    1. AI gagal menyediakan matriks ketertelusuran yang mengikat komponen hulu ke hilir secara biner.
    2. Simulasi dampak perubahan (Change Request) belum memetakan requirement ID spesifik yang terdampak.
* **Student Corrections**:
    1. Membantu AI menstrukturkan skenario validasi berbasis kriteria penerimaan (Acceptance Criteria).
    2. Mengisi file analisis dampak `08-change-request.md` dan memetakan penelusuran hubungan dokumen pada `requirements-traceability.md`.
* **Final Output**: `07-validation.md`, `08-change-request.md`, dan `requirements-traceability.md`[cite: 6]
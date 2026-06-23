# AI Output Review

## Skill 1 - Project Inception and Stakeholder Discovery

### AI Output File
outputs/raw/inception-ai-output.md

### Problems Found
1. Penomoran section tidak konsisten.
2. Constraint "kinerja tinggi" masih ambigu.
3. Beberapa out-of-scope belum jelas.

### Student Corrections
1. Memperbaiki penomoran.
2. Mengubah istilah ambigu menjadi lebih terukur atau OPEN QUESTION.
3. Memisahkan masalah dan solusi secara lebih jelas.
4. Menambahkan quality check.

### Final Output
outputs/reviewed/01-inception.md

---

## Skill 2 - Requirements Elicitation

### AI Output File
outputs/raw/elicitation-ai-output.md

### Kelebihan Output AI
- Berhasil mengidentifikasi kebutuhan eksplisit berdasarkan stakeholder.
- Berhasil memisahkan kebutuhan eksplisit dan implisit.
- Menyediakan pertanyaan wawancara untuk setiap stakeholder.
- Menyediakan open questions untuk validasi lebih lanjut.

### Problems Found
1. Menggunakan ID EL-XX untuk Explicit Needs dan Implicit Needs.
2. Beberapa kebutuhan implisit belum memiliki dasar yang kuat dari dokumen sumber.
3. Istilah "Modul relasi plot dosen-mhs-matkul" kurang jelas.
4. Traceability terhadap Open Questions dari Skill 1 belum terlihat.

### Student Corrections
1. Menggunakan ID EN-XX untuk Explicit Needs.
2. Menggunakan ID IN-XX untuk Implicit Needs.
3. Memperjelas kebutuhan implisit yang ambigu.
4. Menyesuaikan temuan elicitation agar lebih mudah ditelusuri ke stakeholder.

### Final Output
outputs/reviewed/02-elicitation.md

# Review Skill 5 - Requirements Prioritization and Negotiation

## Kelebihan Output AI

* Seluruh Functional Requirements (FR-01 sampai FR-15) berhasil diprioritaskan menggunakan metode MoSCoW.
* Setiap prioritas memiliki alasan yang jelas.
* Dependency Analysis membantu memahami urutan implementasi requirement.
* Negotiation Notes menjelaskan dasar pengambilan keputusan prioritas.

## Kekurangan Output AI

* Terdapat typo pada nama file sumber "03-requirments.md" yang seharusnya "03-requirements.md".
* FR-12 tidak muncul pada tabel Dependency Analysis meskipun menjadi requirement penting.
* Beberapa alasan prioritas masih terlalu panjang dan dapat diringkas.
* Status Won't Have untuk integrasi SIAKAD belum menggunakan format requirement ID karena berasal dari Open Question.

## Perbaikan yang Dilakukan

* Memperbaiki typo nama file sumber.
* Menambahkan FR-12 pada analisis dependensi bila diperlukan.
* Merapikan kalimat alasan prioritas agar lebih ringkas.
* Memastikan seluruh keputusan prioritas tetap konsisten dengan dokumen requirements sebelumnya.

## Final Output

outputs/reviewed/05-prioritization.md
# Requirements Elicitation

## Purpose

Mengidentifikasi, menggali, dan mendokumentasikan kebutuhan stakeholder melalui proses requirements elicitation. Skill ini digunakan untuk menemukan kebutuhan eksplisit maupun implisit, menyusun pertanyaan elicitation yang relevan, serta menghasilkan temuan yang dapat digunakan pada tahap elaboration, specification, dan validation.

---

## When to Use

Gunakan setelah Project Inception and Stakeholder Discovery selesai dan stakeholder utama telah teridentifikasi.

---

## Inputs

- CASE.md
- outputs/reviewed/01-inception.md
- Catatan stakeholder (jika tersedia)
- Asumsi proyek (jika tersedia)
- Informasi tambahan dari pengguna

---

## Required Context

AI harus membaca dan memahami:

- CASE.md
- outputs/reviewed/01-inception.md
- inputs/stakeholder-notes.md (jika tersedia)
- inputs/assumptions.md (jika tersedia)

---

## Workflow

1. Baca seluruh informasi proyek dan stakeholder.
2. Identifikasi stakeholder utama.
3. Identifikasi tujuan dan kebutuhan masing-masing stakeholder.
4. Pilih teknik elicitation yang sesuai.
5. Buat daftar pertanyaan elicitation untuk setiap stakeholder.
6. Identifikasi kebutuhan eksplisit berdasarkan informasi yang tersedia.
7. Identifikasi kebutuhan implisit berdasarkan konteks bisnis.
8. Dokumentasikan seluruh temuan menggunakan ID EL-XX.
9. Tandai informasi yang belum dapat dipastikan sebagai OPEN QUESTION.
10. Jalankan quality checks.
11. Hasilkan output sesuai format yang ditentukan.

---

## Output Format

### Elicitation Techniques

### Stakeholder Interview Questions

#### Lecturer

#### Student

#### Administrator

### Explicit Needs

| ID | Stakeholder | Need | Source |
|----|------------|------|--------|

### Implicit Needs

| ID | Stakeholder | Need | Reasoning |
|----|------------|------|-----------|

### Elicitation Findings

| ID | Description | Stakeholder |
|----|------------|-------------|

### Open Questions

### Summary

---

## Rules

- Jangan membuat fakta yang tidak tersedia pada sumber.
- Gunakan ASSUMPTION untuk dugaan yang logis.
- Gunakan OPEN QUESTION untuk informasi yang belum diketahui.
- Gunakan ID EL-01, EL-02, dan seterusnya.
- Pisahkan kebutuhan eksplisit dan implisit.
- Setiap kebutuhan harus memiliki stakeholder yang jelas.
- Setiap temuan harus dapat ditelusuri ke stakeholder terkait.
- Hindari requirement yang ambigu.

---

## Quality Checks

Periksa bahwa:

- Semua stakeholder memiliki pertanyaan elicitation.
- Kebutuhan eksplisit dan implisit dipisahkan.
- Setiap temuan memiliki ID unik.
- Tidak ada requirement yang ambigu.
- Tidak ada requirement yang bertentangan.
- Open Questions telah didokumentasikan.
- Seluruh stakeholder telah tercakup.

---

## Failure Conditions

Hentikan proses dan minta klarifikasi apabila:

- Stakeholder belum teridentifikasi.
- Deskripsi proyek tidak tersedia.
- Informasi bertentangan.
- Informasi tidak cukup untuk melakukan elicitation.

---

## Example Invocation

Read:

- CASE.md
- outputs/reviewed/01-inception.md

Execute the Requirements Elicitation skill exactly as written.

Generate output according to the Output Format section.

Do not invent facts.

Mark assumptions as ASSUMPTION.

Mark unknown information as OPEN QUESTION.

---

## Expected Output Example

### Elicitation Findings

| ID | Description | Stakeholder |
|----|------------|-------------|
| EL-01 | Lecturer membutuhkan kemampuan membuat tugas baru. | Lecturer |
| EL-02 | Student membutuhkan kemampuan mengunggah file tugas. | Student |
| EL-03 | Administrator membutuhkan kemampuan mengelola akun pengguna. | Administrator |
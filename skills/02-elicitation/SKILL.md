# Requirements Elicitation

## Purpose

Mengidentifikasi, menggali, dan mendokumentasikan kebutuhan stakeholder melalui proses requirements elicitation. Skill ini membantu menemukan kebutuhan eksplisit maupun implisit, menyusun pertanyaan wawancara yang relevan, serta menghasilkan temuan elicitation yang dapat digunakan pada tahap elaboration dan specification.

## When to Use

Gunakan setelah tahap Project Inception and Stakeholder Discovery selesai dan stakeholder utama telah teridentifikasi.

## Inputs

* CASE.md
* outputs/reviewed/01-inception.md
* Catatan stakeholder (jika tersedia)
* Asumsi proyek (jika tersedia)
* Informasi tambahan dari pengguna

## Required Context

AI harus membaca:

* CASE.md
* outputs/reviewed/01-inception.md
* inputs/stakeholder-notes.md (jika tersedia)
* inputs/assumptions.md (jika tersedia)

## Workflow

1. Baca seluruh informasi proyek dan stakeholder.
2. Identifikasi stakeholder utama dan tujuan mereka.
3. Pilih teknik elicitation yang sesuai (interview, observation, questionnaire, document analysis).
4. Buat daftar pertanyaan elicitation untuk setiap stakeholder.
5. Identifikasi kebutuhan eksplisit berdasarkan informasi yang tersedia.
6. Identifikasi kebutuhan implisit yang logis berdasarkan konteks.
7. Tandai kebutuhan yang belum dapat dipastikan sebagai OPEN QUESTION.
8. Dokumentasikan seluruh temuan elicitation menggunakan ID EL-XX.
9. Jalankan quality checks.
10. Hentikan proses dan minta klarifikasi jika informasi tidak mencukupi.

## Output Format

### Elicitation Techniques

### Stakeholder Interview Questions

#### Lecturer

Q-01
Q-02
...

#### Student

Q-XX
...

#### Administrator

Q-XX
...

### Explicit Needs

| ID | Stakeholder | Need | Source |
| -- | ----------- | ---- | ------ |

### Implicit Needs

| ID | Stakeholder | Need | Reasoning |
| -- | ----------- | ---- | --------- |

### Elicitation Findings

| ID | Description | Stakeholder |
| -- | ----------- | ----------- |

### Open Questions

### Summary

## Rules

* Jangan membuat fakta yang tidak diberikan.
* Tandai asumsi menggunakan ASSUMPTION.
* Tandai informasi yang belum tersedia menggunakan OPEN QUESTION.
* Gunakan ID EL-01, EL-02, dan seterusnya.
* Pisahkan kebutuhan eksplisit dan implisit.
* Jangan menghasilkan kebutuhan yang tidak relevan dengan studi kasus.
* Jangan menganggap semua stakeholder memiliki kebutuhan yang sama.
* Setiap temuan harus dapat ditelusuri ke stakeholder yang relevan.

## Quality Checks

Periksa apakah:

* Semua stakeholder memiliki pertanyaan elicitation.
* Kebutuhan eksplisit dipisahkan dari kebutuhan implisit.
* Setiap temuan memiliki ID unik.
* Tidak ada kebutuhan yang bertentangan.
* Tidak ada kebutuhan yang ambigu.
* Seluruh temuan memiliki stakeholder yang jelas.
* Open question sudah didokumentasikan.

## Failure Conditions

Skill harus berhenti atau meminta klarifikasi apabila:

* Stakeholder belum teridentifikasi.
* Deskripsi proyek tidak tersedia.
* Informasi bertentangan.
* Tidak ada informasi yang cukup untuk menghasilkan kebutuhan.

## Example Invocation

Read CASE.md and outputs/reviewed/01-inception.md.

Execute the Requirements Elicitation skill exactly as written.

Generate the output using the defined structure.

Do not invent facts.

Mark assumptions and open questions explicitly.

## Expected Output Example

### Elicitation Findings

| ID    | Description                                                  | Stakeholder   |
| ----- | ------------------------------------------------------------ | ------------- |
| EL-01 | Lecturer membutuhkan kemampuan membuat tugas baru.           | Lecturer      |
| EL-02 | Student membutuhkan kemampuan mengunggah file tugas.         | Student       |
| EL-03 | Administrator membutuhkan kemampuan mengelola akun pengguna. | Administrator |

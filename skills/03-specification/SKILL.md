# Requirements Elaboration and Specification

## Purpose

Mengubah hasil requirements elicitation menjadi requirement yang lebih terstruktur, lengkap, konsisten, dan dapat diuji. Skill ini membantu menghasilkan Functional Requirements, Non-Functional Requirements, Business Rules, User Stories, dan Acceptance Criteria yang menjadi dasar pengembangan sistem.

## When to Use

Gunakan setelah tahap Requirements Elicitation selesai dan kebutuhan stakeholder telah diidentifikasi.

## Inputs

* CASE.md
* outputs/reviewed/01-inception.md
* outputs/reviewed/02-elicitation.md
* Catatan tambahan stakeholder (jika tersedia)

## Required Context

AI harus membaca:

* CASE.md
* outputs/reviewed/01-inception.md
* outputs/reviewed/02-elicitation.md

## Workflow

1. Baca seluruh dokumen proyek dan hasil elicitation.
2. Identifikasi kebutuhan yang telah tervalidasi.
3. Elaborasi kebutuhan menjadi requirement yang lebih rinci.
4. Kelompokkan requirement menjadi Functional Requirements dan Non-Functional Requirements.
5. Identifikasi Business Rules yang berlaku.
6. Buat User Stories berdasarkan kebutuhan stakeholder.
7. Buat Acceptance Criteria untuk setiap User Story.
8. Pastikan seluruh requirement dapat ditelusuri ke stakeholder atau hasil elicitation.
9. Tandai ketidakpastian sebagai OPEN QUESTION.
10. Jalankan Quality Checks.
11. Hentikan proses dan minta klarifikasi apabila informasi tidak mencukupi.

## Output Format

# Functional Requirements

| ID | Requirement | Source |
| -- | ----------- | ------ |

# Non-Functional Requirements

| ID | Requirement | Category | Source |
| -- | ----------- | -------- | ------ |

# Business Rules

| ID | Rule | Source |
| -- | ---- | ------ |

# User Stories

## US-XX

As a [Stakeholder]

I want [Goal]

So that [Benefit]

### Acceptance Criteria

* AC-XX
* AC-XX

# Open Questions

# Summary

## Rules

* Jangan membuat fakta baru tanpa dasar dari dokumen.
* Gunakan ID FR-XX untuk Functional Requirements.
* Gunakan ID NFR-XX untuk Non-Functional Requirements.
* Gunakan ID BR-XX untuk Business Rules.
* Gunakan ID US-XX untuk User Stories.
* Gunakan ID AC-XX untuk Acceptance Criteria.
* Setiap requirement harus jelas, spesifik, dan dapat diuji.
* Setiap requirement harus memiliki sumber atau traceability.
* Hindari istilah ambigu seperti cepat, mudah, baik, optimal, dan efisien tanpa ukuran yang jelas.
* Gunakan OPEN QUESTION jika informasi belum tersedia.

## Quality Checks

Periksa apakah:

* Minimal 8 Functional Requirements tersedia.
* Minimal 4 Non-Functional Requirements tersedia.
* Minimal 2 Business Rules tersedia.
* Minimal 6 User Stories tersedia.
* Setiap User Story memiliki minimal 2 Acceptance Criteria.
* Tidak ada requirement yang ambigu.
* Tidak ada requirement yang bertentangan.
* Seluruh requirement memiliki traceability yang jelas.

## Failure Conditions

Skill harus berhenti atau meminta klarifikasi apabila:

* Hasil elicitation tidak tersedia.
* Stakeholder belum teridentifikasi.
* Informasi proyek tidak cukup.
* Requirement saling bertentangan.

## Example Invocation

Read CASE.md, outputs/reviewed/01-inception.md, and outputs/reviewed/02-elicitation.md.

Execute the Requirements Elaboration and Specification skill exactly as written.

Generate the output using the defined structure.

Do not invent facts.

Mark assumptions and open questions explicitly.

## Expected Output Example

### Functional Requirements

| ID    | Requirement                          | Source |
| ----- | ------------------------------------ | ------ |
| FR-01 | Lecturer dapat membuat tugas baru.   | EN-01  |
| FR-02 | Student dapat mengunggah file tugas. | EN-08  |

### User Story

#### US-01

As a Lecturer

I want to create a new assignment

So that students can submit their work online

##### Acceptance Criteria

* AC-01: Sistem memungkinkan dosen memasukkan judul tugas.
* AC-02: Sistem memungkinkan dosen menentukan deadline.

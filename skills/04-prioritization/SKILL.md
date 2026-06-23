# Requirements Negotiation and Prioritization

## Purpose

Memprioritaskan functional requirements menggunakan metode MoSCoW (Must Have, Should Have, Could Have, Won't Have), mengidentifikasi dependensi requirement, serta mendokumentasikan alasan prioritas untuk mendukung pengambilan keputusan proyek.

## When to Use

Gunakan setelah Functional Requirements dan User Stories selesai dibuat.

## Inputs

* outputs/reviewed/03-requirements.md
* outputs/reviewed/04-user-stories.md

## Required Context

AI harus membaca seluruh daftar Functional Requirements, Business Rules, dan User Stories sebelum menentukan prioritas.

## Workflow

1. Baca seluruh Functional Requirements.
2. Identifikasi nilai bisnis setiap requirement.
3. Identifikasi requirement yang wajib agar sistem dapat berfungsi.
4. Identifikasi dependensi antar requirement.
5. Klasifikasikan setiap requirement menggunakan metode MoSCoW.
6. Berikan alasan prioritas untuk setiap requirement.
7. Identifikasi requirement yang dapat ditunda.
8. Dokumentasikan hasil prioritisasi.
9. Jalankan quality checks.
10. Hentikan proses jika requirement belum tersedia.

## Output Format

# Prioritized Requirements

| ID | Requirement | Priority | Reason |
|----|------------|----------|--------|

# Dependency Analysis

| Requirement | Depends On |
|------------|------------|

# Negotiation Notes

# Quality Check Results

## Rules

* Gunakan kategori Must, Should, Could, Won't.
* Setiap requirement harus memiliki prioritas.
* Setiap prioritas harus memiliki alasan.
* Jangan membuat requirement baru.
* Gunakan requirement yang berasal dari dokumen sebelumnya.
* Dokumentasikan dependensi jika ada.

## Quality Checks

Periksa apakah:

* Semua requirement memiliki prioritas.
* Tidak ada requirement tanpa alasan.
* Requirement kritis diberi prioritas Must.
* Tidak ada requirement yang hilang.
* Dependensi telah dicatat.

## Failure Conditions

Skill harus berhenti jika:

* Functional Requirements belum tersedia.
* User Stories belum tersedia.
* Requirement tidak dapat ditelusuri.

## Example Invocation

Read outputs/reviewed/03-requirements.md and outputs/reviewed/04-user-stories.md.

Execute the Requirements Negotiation and Prioritization skill exactly as written.

Generate the output using the defined structure.

Do not invent new requirements.

## Expected Output Example

| ID | Requirement | Priority | Reason |
|----|------------|----------|--------|
| FR-01 | Create Assignment | Must | Core functionality |
| FR-02 | Submit Assignment | Must | Core functionality |
| FR-03 | Assignment Reminder | Could | Additional feature |
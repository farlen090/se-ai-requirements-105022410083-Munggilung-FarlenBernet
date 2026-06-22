# outputs/raw/elicitation-ai-output.md

## Elicitation Techniques
1. **Document Analysis**: Menganalisis berkas `01-inception.md` dan `CASE.md`.
2. **Structured Interview**: Menyusun daftar pertanyaan terarah untuk stakeholder.

## Stakeholder Interview Questions

### Lecturer
* **Pertanyaan 1**: Bagaimana alur pembuatan tugas baru di sistem?
* **Pertanyaan 2**: Jenis umpan balik apa yang ingin diberikan (teks/file)?
* **Pertanyaan 3**: Apakah mahasiswa boleh mengumpulkan tugas setelah *deadline*?

### Student
* **Pertanyaan 1**: Informasi apa yang paling krusial pada daftar tugas aktif?
* **Pertanyaan 2**: Bagaimana indikator visual konfirmasi sukses mengunggah berkas?
* **Pertanyaan 3**: Apakah ada fitur pembatalan atau pembaruan berkas tugas?

### Administrator
* **Pertanyaan 1**: Bagaimana mekanisme impor/pembuatan data akun pengguna?
* **Pertanyaan 2**: Atribut apa yang wajib dicatat pada data mata kuliah?
* **Pertanyaan 3**: Parameter konfigurasi global apa saja yang perlu dikendalikan?

## Explicit Needs

| ID | Stakeholder | Need | Source |
| :--- | :--- | :--- | :--- |
| EL-01 | Lecturer | Membuat tugas perkuliahan. | CASE.md |
| EL-02 | Lecturer | Menetapkan tenggat waktu tugas. | CASE.md |
| EL-03 | Lecturer | Memberikan nilai hasil kerja. | CASE.md |
| EL-04 | Lecturer | Memberikan umpan balik tugas. | CASE.md |
| EL-05 | Student | Melihat daftar tugas perkuliahan. | CASE.md |
| EL-06 | Student | Memantau status pengumpulan tugas. | CASE.md |
| EL-07 | Student | Memantau tenggat waktu tugas. | CASE.md |
| EL-08 | Student | Mengumpulkan file tugas ke sistem. | CASE.md |
| EL-09 | Administrator | Mengelola data pengguna (akun user). | CASE.md |
| EL-10 | Administrator | Mengelola data mata kuliah. | CASE.md |
| EL-11 | Administrator | Mengatur konfigurasi sistem global. | CASE.md |

## Implicit Needs

| ID | Stakeholder | Need | Reasoning |
| :--- | :--- | :--- | :--- |
| EL-12 | All | Akses login aman per aktor. | Melindungi kerahasiaan data nilai. |
| EL-13 | Lecturer | Melihat rekap progres kelas. | Memantau mahasiswa yang belum mengumpul. |
| EL-14 | Student | Indikator sukses unggah berkas. | Kepastian data tersimpan di server. |
| EL-15 | Admin | Memetakan kelas kuliah. | Menghubungkan user dengan mata kuliah. |

## Elicitation Findings

| ID | Description | Stakeholder |
| :--- | :--- | :--- |
| EL-01 | Pembuatan komponen tugas perkuliahan. | Lecturer |
| EL-02 | Penentuan batas akhir jam/tanggal *deadline*. | Lecturer |
| EL-03 | Pengisian nilai evaluasi mahasiswa. | Lecturer |
| EL-04 | Pemberian catatan teks umpan balik. | Lecturer |
| EL-05 | Penampilan daftar tugas aktif mahasiswa. | Student |
| EL-06 | Penampilan status pengumpulan berkas. | Student |
| EL-07 | Penampilan waktu hitung mundur *deadline*. | Student |
| EL-08 | Unggah dokumen elektronik jawaban tugas. | Student |
| EL-09 | Fungsi tambah/ubah data akun pengguna. | Administrator |
| EL-10 | Fungsi pengelolaan master mata kuliah. | Administrator |
| EL-11 | Akses kontrol konfigurasi global. | Administrator |
| EL-12 | Sistem autentikasi login terproteksi. | All |
| EL-13 | Dasbor pantau pengumpulan tugas kelas. | Lecturer |
| EL-14 | Notifikasi visual sukses unggah berkas. | Student |
| EL-15 | Modul relasi plot dosen-mhs-matkul. | Administrator |

## Open Questions
* **OPEN QUESTION-06**: Apakah diperlukan sistem pengingat otomatis (*reminder*) bagi Student sebelum *deadline* berakhir?
* **OPEN QUESTION-07**: Apakah pengisian umpan balik oleh Lecturer bersifat wajib atau opsional?
* **OPEN QUESTION-08**: Apakah sistem menyimpan histori versi jika Student mengunggah ulang file tugasnya?
* **OPEN QUESTION-09**: Apakah ada batasan maksimal karakter deskripsi tugas oleh Lecturer?

## Summary
Proses *elicitation* berhasil menyaring 11 kebutuhan eksplisit dan 4 kebutuhan implisit untuk *Student Task Management System*. Daftar pertanyaan terstruktur disiapkan untuk validasi, sementara ketidakpastian dicatat pada *Open Questions*. Seluruh temuan menggunakan nomor ID unik (`EL-01` s.d `EL-15`) agar *traceable* ke tahap berikutnya.
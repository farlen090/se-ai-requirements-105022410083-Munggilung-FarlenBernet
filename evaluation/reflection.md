# Project Reflection: AI-Assisted Requirements Engineering

## 1. Bagian apa yang paling baik dikerjakan oleh AI dalam proses Requirements Engineering?
AI sangat andal dalam melakukan ekstraksi kebutuhan awal secara cepat dari dokumen mentah dasar (seperti mendata tugas utama dosen, mahasiswa, dan administrator). AI juga sangat baik dalam menstrukturkan format dokumen agar sesuai standar rekayasa perangkat lunak, termasuk menyusun User Stories dengan struktur baku *As a... I want to... So that...* beserta Acceptance Criteria fungsionalnya.

## 2. Kesalahan atau asumsi apa yang paling sering dibuat oleh AI?
AI seringkali tidak konsisten dalam mengelola sistem penomoran (*ID constraints*), seperti mencampur kode `EL-XX` untuk kebutuhan eksplisit dan implisit secara bersamaan. Selain itu, AI kerap membuat asumsi di luar cakupan (*unsupported assumptions*), menyisipkan pertanyaan terbuka (*Open Questions*) ke dalam tabel spesifikasi formal (*Business Rules*), serta melakukan kesalahan referensi dependensi teknis (misalnya melewatkan fungsionalitas data master penting seperti `FR-12` dalam analisis ketergantungan).

## 3. Bagaimana perubahan pada SKILL.md memperbaiki kualitas output?
Dengan memperketat pedoman instruksi pada `SKILL.md` (seperti kewajiban standardisasi identifikasi `EN-XX` dan `IN-XX`, aturan pembersihan kata-kata kualitatif subjektif, serta prosedur validasi dependensi hulu-hilir), AI dipaksa bekerja di dalam koridor logika yang ketat. Hasil pengerjaan ulang setelah skill diperbaiki terbukti bebas dari ambiguitas, memiliki penomoran yang rapi, dan referensi antarberkas yang sinkron.

## 4. Mengapa human review tetap diperlukan walaupun AI telah menggunakan workflow dan quality checks?
Karena AI tidak memiliki pemahaman konteks bisnis dunia nyata secara menyeluruh dan rawan mengalami kekeliruan struktural kecil yang fatal (seperti salah mengetik nama file acuan atau melewatkan dependensi data master). Manusia sebagai Requirements Engineer tetap memegang kendali penuh untuk menyaring logika spekulatif AI, memvalidasi kriteria kelayakan teknis, dan mengonfirmasi hasil negosiasi prioritas bersama pemangku kepentingan.

## 5. Bagaimana traceability membantu menjaga konsistensi antarartefak requirements?
Traceability mengikat seluruh elemen dari hulu ke hilir (dari *Elicitation Findings* `EL-XX`, dialirkan ke *Functional Requirements* `FR-XX`, dipetakan ke *User Story* `US-XX`, hingga ke skenario pengujian biner). Hal ini memastikan tidak ada kebutuhan pengguna yang hilang di tengah jalan, memudahkan analisis dampak jika ada perubahan di kemudian hari, dan mencegah munculnya fitur liar yang tidak memiliki dasar dokumen sumber.
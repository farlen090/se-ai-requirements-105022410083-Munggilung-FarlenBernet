# Change Request (CR) Log

## CR-01: Kebijakan Dispensasi Keterlambatan Pengumpulan (Grace Period)
* **Status**: Approved
* **Request Date**: 2026-06-23
* **Requested By**: Stakeholder Lecturer Group[cite: 1]
* **Description**: Dosen meminta penambahan masa toleransi keterlambatan (*grace period*) selama 15 menit setelah batas akhir tanggal dan jam *deadline* utama terlewati untuk menangani kendala jaringan internet sesaat mahasiswa[cite: 1, 2].
* **Impact Analysis**:
    * **Impact on FR**: Mengubah fungsi kontrol hitung mundur waktu `FR-04`[cite: 3].
    * **Impact on Data**: Mengubah status pengumpulan `FR-06` dari biner murni ("Belum"/"Sudah") menjadi status multi-kondisi: "Belum", "Sudah (Tepat Waktu)", dan "Sudah (Terlambat)"[cite: 3].
    * **Dependency**: Berpengaruh pada aturan bisnis `BR-01` dan `BR-02` terkait batas final otoritas waktu pengumpulan[cite: 3].

## CR-02: Batasan Kapasitas Maksimal dan Format Ekstensi File Upload
* **Status**: Approved
* **Request Date**: 2026-06-23
* **Requested By**: Administrator / IT Infrastructure Support[cite: 1]
* **Description**: Menjawab `OPEN QUESTION-01` dan `OPEN QUESTION-09` mengenai ketidakpastian batasan berkas tugas[cite: 1, 2]. Admin menetapkan regulasi keamanan bahwa format file yang diizinkan hanya berupa PDF, DOCX, dan ZIP dengan ukuran kapasitas maksimal sebesar 10MB per berkas[cite: 1, 2].
* **Impact Analysis**:
    * **Impact on FR**: Menambahkan sub-kondisi validasi sistem pada fasilitas unggah berkas milik Student (`FR-05`)[cite: 3].
    * **Impact on NFR**: Memperkuat parameter keamanan berkas masuk (`NFR-02`) dari ancaman file berbahaya (*malicious file upload*)[cite: 3].
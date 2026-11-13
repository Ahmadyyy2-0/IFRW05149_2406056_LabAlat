# PERTEMUAN 4: USE CASE DIAGRAM LANJUTAN: GENERALIZATION DAN COLLABORATION

## 1. Tujuan Praktikum

Setelah mengikuti praktikum ini, mahasiswa diharapkan mampu:

- Menyusun hierarki generalization aktor dengan arah panah dari aktor khusus menuju aktor umum tanpa menggambar ulang asosiasi yang diwarisi.
- Menyusun generalization use case beserta penjelasan perilaku yang diwarisi dan perilaku pembedanya.
- Menempatkan simbol collaboration (elips garis putus-putus) dan menghubungkannya dengan relasi realization menuju use case yang diwujudkan.
- Mengembangkan use case diagram kumulatif dengan mempertahankan elemen pertemuan sebelumnya serta menyusun use case description baru secara konsisten.

## 2. Dasar Teori

- Generalization Aktor: Hubungan pewarisan di mana aktor khusus mewarisi seluruh asosiasi aktor umum dan dapat memiliki asosiasi tambahan tersendiri (garis utuh berujung segitiga kosong menunjuk aktor umum).
- Generalization Use Case: Hubungan jenis di mana use case khusus mewarisi tujuan dan perilaku dasar use case umum, lalu menambahkan langkah pembeda (garis utuh berujung segitiga kosong menunjuk use case umum).
- Collaboration dan Realization: Collaboration merepresentasikan kerja sama elemen internal sistem untuk mewujudkan perilaku suatu use case, dihubungkan melalui relasi realization (garis putus-putus berujung segitiga kosong dari collaboration menuju use case).

## 3. Analisis

- Studi Kasus Laboratorium (LAB): Diagram kumulatif memuat 5 aktor, 12 use case, 2 collaboration, dan 17 hubungan. Aktor Mahasiswa dan Dosen mewarisi asosiasi Peminjam ke LAB-UC01 dan LAB-UC03, sementara Cetak Bukti Pengajuan tetap menjadi asosiasi khusus Mahasiswa. Fungsi Kelola Data Peralatan digeneralisasikan menjadi Tambah, Ubah, dan Hapus Data Peralatan, serta ditambahkan pencatatan pengembalian alat yang direalisasikan oleh LAB-CO01 dan LAB-CO02.

| NO | Elemen Baru / Perubahan (LAB) | Jenis Relasi | Alasan Pemodelan |
| :---: | :--- | :--- | :--- |
| 1 | Mahasiswa & Dosen → Peminjam | Generalization Aktor | Keduanya berbagi fungsi melihat ketersediaan dan mengajukan peminjaman. |
| 2 | LAB-UC08, UC09, UC10 → LAB-UC02 | Generalization Use Case | Spesialisasi kelola peralatan menjadi Tambah, Ubah, dan Hapus dengan hasil akhir berbeda. |
| 3 | LAB-UC11 → LAB-UC12 | «include» | Pemeriksaan kondisi peralatan (Baik, Rusak Ringan/Berat) wajib saat mencatat pengembalian. |
| 4 | LAB-CO01 → LAB-UC03 & LAB-CO02 → LAB-UC11 | Realization | Menunjukkan perwujudan internal sistem pada dua use case utama. |

- Tugas Praktik Akademik (SIA): Diagram kumulatif SIA menggabungkan fitur jadwal, KRS, dan layanan hasil studi (SIA-R07 s.d. SIA-R12). Hasil penyusunan elemen lanjutan disajikan pada tabel berikut:

| NO | Elemen Baru / Perubahan (SIA) | Jenis Relasi | Alasan Pemodelan |
| :---: | :--- | :--- | :--- |
| 1 | Mahasiswa & Dosen → Civitas Akademika | Generalization Aktor | Mewarisi fungsi bersama SIA-UC07 Lihat Kalender Akademik tanpa menggambar ulang asosiasi. |
| 2 | SIA-UC11, UC12, UC13 → SIA-UC10 | Generalization Use Case | Spesialisasi SIA-UC10 Kelola Data Mahasiswa menjadi Tambah, Ubah, dan Hapus Data Mahasiswa. |
| 3 | SIA-CO01 → SIA-UC08 | Realization | Merealisasikan perilaku internal use case Input Nilai Mata Kuliah. |
| 4 | SIA-CO02 → SIA-UC09 | Realization | Merealisasikan perilaku internal use case Lihat KHS. |

## 4. Kesimpulan

- Generalization menghilangkan duplikasi garis asosiasi dan memperjelas spesialisasi peran maupun fungsionalitas sistem secara hierarkis.
- Collaboration menandai perwujudan internal dari sebuah use case pada tahap analisis tanpa merinci urutan pesan antarobjek.
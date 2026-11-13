# PERTEMUAN 5: SKENARIO USE CASE: DARI DIAGRAM KE LANGKAH KEGIATAN

## 1. Tujuan Praktikum

Setelah mengikuti praktikum ini, mahasiswa diharapkan mampu:

- Menyusun tabel skenario lengkap yang memisahkan aksi aktor pada kolom Kegiatan dan tanggapan sistem pada kolom Respon sistem.
- Menerapkan penomoran langkah yang berlanjut secara konsisten dari Skenario Normal ke Skenario Alternative.
- Memetakan relasi include, extend, generalization aktor, generalization use case, dan collaboration ke dalam struktur tabel skenario.
- Menelaah kesesuaian tabel skenario terhadap diagram kumulatif acuan serta menyusun tabel skenario untuk tugas akademik.

## 2. Dasar Teori

- Skenario Use Case: Uraian langkah demi langkah interaksi antara aktor dan sistem dalam format tabel dua kolom (Kegiatan dan Respon sistem) yang terdiri atas Skenario Normal, Skenario Alternative, dan Skenario Akhir.
- Aturan Penomoran Berlanjut: Penomoran langkah pada Skenario Alternative melanjutkan nomor terakhir dari Skenario Normal dan merujuk langsung pada nomor langkah tempat percabangan terjadi agar tidak ambigu.
- Pemetaan Relasi ke Skenario: Include ditulis sebagai langkah rujukan pada Skenario Normal; extend menjadi cabang bersyarat pada Skenario Alternative; generalization aktor ditulis satu kali atas nama aktor umum; generalization use case memisahkan langkah bersama dan langkah pembeda; sedangkan collaboration hanya dicantumkan pada keterangan tabel.

## 3. Analisis

- Studi Kasus Laboratorium (LAB): Dilakukan telaah terhadap 12 tabel skenario (LAB-UC01 s.d. LAB-UC12) berdasarkan 17 hubungan pada diagram acuan Pertemuan 4. Hasil penelusuran kelompok skenario dirangkum pada tabel berikut:

| NO | Kelompok & ID Skenario | Relasi yang Ditelusur | Hasil Pencocokan terhadap Diagram |
| :---: | :--- | :--- | :--- |
| 1 | Peminjaman (LAB-UC01, UC03, UC04, UC05) | Generalization Peminjam, «include» UC04, «extend» UC05, Realization LAB-CO01 | Sesuai; UC04 dirujuk di Skenario Normal, UC05 bercabang di Skenario Alternative dengan kondisi cetak. |
| 2 | Pengelolaan Data (LAB-UC02, UC08, UC09, UC10) | Generalization Use Case ke LAB-UC02 | Sesuai; UC02 memuat langkah bersama, UC08–UC10 hanya memuat langkah pembeda (tambah, ubah, hapus). |
| 3 | Keputusan & Laporan (LAB-UC06, UC07) | Asosiasi tunggal Petugas & Kepala Lab | Sesuai; kedua tabel berdiri sendiri tanpa langkah include, extend, maupun generalization. |
| 4 | Pengembalian (LAB-UC11, UC12) | «include» UC12, Realization LAB-CO02 | Sesuai; pemeriksaan kondisi fisik dirujuk pada Skenario Normal tanpa menyalin langkah UC12. |

- Tugas Praktik Akademik (SIA): Disusun 7 tabel skenario (SIA-UC07 s.d. SIA-UC13) secara mandiri berdasarkan diagram acuan Pertemuan 4:

| NO | ID Skenario | Nama Use Case | Aktor | Aturan Pemetaan yang Diterapkan |
| :---: | :--- | :--- | :--- | :--- |
| 1 | SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | Generalization aktor; ditulis satu tabel untuk Mahasiswa dan Dosen. |
| 2 | SIA-UC08 | Input Nilai Mata Kuliah | Dosen | Prasyarat dosen pengampu, cabang nilai tidak sah, keterangan SIA-CO01. |
| 3 | SIA-UC09 | Lihat KHS | Mahasiswa | Menampilkan nilai terpublikasi, keterangan SIA-CO02. |
| 4 | SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | Skenario umum yang memuat langkah pengelolaan bersama. |
| 5 | SIA-UC11, UC12, UC13 | Tambah, Ubah, Hapus Data Mahasiswa | Admin Akademik | Generalization use case; memuat perilaku pembeda dan syarat bebas data aktif pada UC13. |

## 4. Kesimpulan

- Tabel skenario menjembatani struktur statis pada use case diagram menjadi alur interaksi operasional yang terurut dan dapat diuji per langkah.
- Pemisahan kolom Kegiatan dan Respon sistem serta penomoran berlanjut memastikan batas tanggung jawab antara pengguna dan sistem terbaca jelas.
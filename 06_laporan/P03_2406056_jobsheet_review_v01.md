# PERTEMUAN 3: USE CASE DIAGRAM DAN USE CASE DESCRIPTION

## 1. Tujuan Praktikum

Setelah mengikuti praktikum ini, mahasiswa diharapkan mampu:

- Menuliskan batas sistem, aktor, kebutuhan, aturan bisnis, dan asumsi dari skenario yang diberikan.
- Menentukan use case berdasarkan tujuan aktor, bukan berdasarkan rincian teknis atau tombol antarmuka.
- Membuat use case diagram yang konsisten dengan daftar kebutuhan dan relasi aktor-fungsi.
- Menyusun use case description yang memuat pemicu, prasyarat, alur utama, alur alternatif/pengecualian, dan pascakondisi.
- Menunjukkan keterlacakan setiap use case ke kebutuhan dan mendokumentasikan hasil revisi.

## 2. Dasar Teori

- Use Case Diagram: Diagram UML yang memvisualisasikan fungsionalitas sistem serta interaksi antara aktor eksternal dan sistem dari sudut pandang pengguna.
- Relasi Include: Menyatakan bahwa perilaku suatu use case wajib disertakan dalam use case penyerta (panah putus-putus terbuka mengarah ke use case yang disertakan).
- Relasi Extend: Menambahkan perilaku opsional ke use case dasar pada extension point dan kondisi tertentu tanpa mengurangi makna use case dasar jika tidak dijalankan (panah putus-putus terbuka mengarah ke use case dasar).
- Use Case Description: Dokumentasi tekstual terstruktur yang menjelaskan detail satu tujuan pengguna, mencakup pemicu, prasyarat, alur utama, alur alternatif, serta pascakondisi berhasil dan gagal.

## 3. Analisis

- Studi Kasus Laboratorium (LAB): Model mencakup 3 aktor (`Mahasiswa`, `Petugas laboratorium`, `Kepala laboratorium`) dan 7 use case (`LAB-UC01` s.d. `LAB-UC07`) berdasarkan kebutuhan `LAB-R01` s.d. `LAB-R06`. Relasi `«include»` diterapkan dari Ajukan peminjaman menuju Periksa ketersediaan karena validasi alat bersifat wajib, sedangkan `«extend»` diterapkan dari Cetak bukti pengajuan menuju Ajukan peminjaman dengan kondisi `[mahasiswa memilih cetak]`.

| NO | ID Use Case | Nama Use Case | Relasi / Peran | Alasan Pemodelan |
| :---: | :--- | :--- | :--- | :--- |
| 1 | LAB-UC01 | Lihat ketersediaan peralatan | Asosiasi (Mahasiswa) | Menyediakan informasi daftar alat sebelum pengajuan. |
| 2 | LAB-UC02 | Kelola data peralatan | Asosiasi (Petugas laboratorium) | Wewenang pengelolaan master data peralatan. |
| 3 | LAB-UC03 | Ajukan peminjaman | Asosiasi (Mahasiswa) | Fungsi utama pengajuan pinjam alat. |
| 4 | LAB-UC04 | Periksa ketersediaan | `«include»` dari LAB-UC03 | Validasi wajib terhadap jumlah dan rentang waktu alat. |
| 5 | LAB-UC05 | Cetak bukti pengajuan | `«extend»` ke LAB-UC03 | Tambahan opsional dengan kondisi `[mahasiswa memilih cetak]`. |
| 6 | LAB-UC06 | Proses keputusan peminjaman | Asosiasi (Petugas laboratorium) | Penetapan status disetujui atau ditolak. |
| 7 | LAB-UC07 | Lihat laporan peminjaman | Asosiasi (Kepala laboratorium) | Pemantauan rekapitulasi peminjaman. |

- Tugas Praktik Akademik (SIA): Model pengajuan KRS (`SIA-R03` s.d. `SIA-R06`) melibatkan aktor `Mahasiswa` dan `Dosen wali`. Rincian temuan dan penyempurnaan hasil -review- disajikan pada tabel berikut:

| NO | Temuan | Perbaikan yang diperlukan |
| :---: | :--- | :--- |
| 1 | Arah panah relasi `«include»` kurang jelas. | Memperjelas arah panah dari SIA-UC01 Ajukan KRS menuju SIA-UC02 Validasi KRS. |
| 2 | Arah panah relasi `«extend»` kurang jelas. | Memperjelas arah panah dari SIA-UC03 Unduh Bukti Pengajuan KRS menuju SIA-UC01 Ajukan KRS. |
| 3 | Keterangan extension point dan kondisi belum jelas. | Menambahkan extension point Konfirmasi penyimpanan dan kondisi `[pengajuan berhasil disimpan dan mahasiswa memilih unduh bukti]`. |
| 4 | Judul batas sistem belum lengkap. | Menggunakan judul Sistem Informasi Akademik (SIA) pada batas sistem. |
| 5 | Nama use case keputusan KRS perlu diperjelas. | Menggunakan nama Proses Keputusan KRS pada SIA-UC04. |
| 6 | Status pengajuan setelah berhasil disimpan perlu dicantumkan. | Menambahkan status Menunggu Persetujuan Dosen Wali setelah pengajuan KRS berhasil disimpan. |

| NO | Alasan |
| :---: | :--- |
| 1 | Validasi KRS merupakan bagian wajib dari proses pengajuan KRS. |
| 2 | Unduh bukti merupakan proses tambahan yang hanya dilakukan jika mahasiswa memilihnya. |
| 3 | Keterangan tersebut menjelaskan kapan proses unduh bukti dapat dilakukan. |
| 4 | Judul yang lengkap memperjelas nama sistem yang dimodelkan. |
| 5 | Nama tersebut menjelaskan aktivitas dosen wali dalam menyetujui atau menolak pengajuan KRS. |
| 6 | Status tersebut menjelaskan kondisi pengajuan sebelum diproses oleh dosen wali. |

## 4. Kesimpulan

- Relasi `«include»` dan `«extend»` memisahkan perilaku wajib dan perilaku opsional agar use case diagram tetap ringkas dan terstruktur.
- Use case diagram hanya memodelkan fungsi dan hubungannya, sedangkan urutan langkah dan penanganan kegagalan dijelaskan secara rinci di dalam use case description.
## 1. Tujuan Praktikum

Setelah mengikuti praktikum ini, mahasiswa diharapkan mampu:
- Menempatkan simbol dasar Use Case Diagram (aktor, *use case*, batas sistem, dan asosiasi) secara tepat sesuai contoh.
- Menggunakan penamaan aktor dan fungsi secara konsisten dengan skenario latihan.
- Mengisi identitas metadata artefak menggunakan template yang telah disiapkan.
- Menyimpan berkas sumber dan ekspor gambar dengan format penamaan, lokasi folder, serta nomor versi yang konsisten.
- Mengidentifikasi dan memperbaiki kesalahan notasi maupun dokumentasi berdasarkan hasil *review*.

## 2. Dasar Teori

- Pengertian UML: *Unified Modeling Language* (UML) adalah bahasa pemodelan standar yang digunakan untuk memvisualisasikan, merancang, dan mendokumentasikan sistem perangkat lunak berorientasi objek mulai dari tingkat abstrak hingga implementasi.
- **Elemen Utama UML**: Terdiri dari *building blocks* (benda/*things*, hubungan/*relationship*, dan diagram), aturan peletakan, serta mekanisme umum.
- **Notasi Dasar Use Case Diagram**:
  - **Actor**: Pengguna, sistem lain, atau proses eksternal yang berinteraksi dengan sistem (wajib berada di luar batas sistem).
  - **Use Case**: Fungsionalitas atau layanan yang disediakan oleh sistem bagi aktor, disimbolkan dengan bentuk elips dan diberi nama menggunakan kata kerja (wajib berada di dalam batas sistem).
  - **Batas Sistem (*System Boundary*)**: Kotak persegi panjang yang membatasi ruang lingkup sistem yang sedang dimodelkan.
  - **Association**: Garis utuh tanpa panah yang menghubungkan aktor dengan *use case* sebagai tanda partisipasi interaksi, bukan menunjukkan urutan langkah kegiatan.

 ## 3. Analisis

- **Studi Kasus Laboratorium (LAB)**: Penerapan notasi dasar dilakukan secara bertahap dimulai dari pembuatan batas sistem (*Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus*), penempatan aktor Mahasiswa dan Petugas laboratorium di luar kotak, peletakan dua *use case* (Lihat ketersediaan peralatan dan Kelola data peralatan) di dalam kotak, serta penarikan garis asosiasi sesuai hak aksesnya. Pada tahap ini relasi lanjutan (`«include»`, `«extend»`, generalisasi) belum digunakan agar fokus pada ketepatan notasi dasar.
- **Tugas Praktik Akademik (SIA)**: Dilakukan proses *debugging* atau koreksi terhadap diagram awal yang sengaja dibuat keliru, serta penyempurnaan relasi dan keterangan *use case*. Rincian temuan, perbaikan, dan alasannya disajikan pada tabel berikut:

| NO | Temuan | Perbaikan yang diperlukan |
| :---: | :--- | :--- |
| 1 | Aktor Mahasiswa diletakkan di dalam system boundary (batas sistem). | Pindahkan mahasiswa ke luar kotak. |
| 2 | Fungsi Lihat jadwal kuliah digambar sebagai kotak biasa. | Ubah notasi fungsi menjadi simbol elips (oval). |
| 3 | Aktor Mahasiswa dihubungkan dengan Kelola jadwal kuliah. | Mahasiswa → Lihat jadwal kuliah, dan Admin akademik → Kelola jadwal kuliah. |
| 4 | Identitas diagram menggunakan judul sistem laboratorium. | Ubah judul system boundary dan isi metadata menjadi Sistem Informasi Akademik. |

| NO | Alasan |
| :---: | :--- |
| 1 | Aktor merupakan entitas eksternal (pengguna/sistem luar) yang berinteraksi dengan sistem, sehingga secara notasi wajib berada di luar batas sistem. |
| 2 | Dalam standar notasi UML Use Case Diagram, use case disimbolkan dengan elips, sedangkan bentuk persegi digunakan untuk class, component, atau boundary. |
| 3 | Garis asosiasi harus sesuai dengan hak akses pada skenario. Mahasiswa hanya membaca jadwal, sedangkan pengelolaan data merupakan wewenang khusus Admin akademik. |
| 4 | Nama sistem pada artefak harus konsisten dengan skenario yang dibahas agar tidak terjadi ketidaksesuaian artefak (artifact mismatch). |

| NO | Temuan | Perbaikan yang diperlukan |
| :---: | :--- | :--- |
| 1 | Arah panah relasi «include» kurang jelas. | Memperjelas arah panah dari SIA-UC01 Ajukan KRS menuju SIA-UC02 Validasi KRS. |
| 2 | Arah panah relasi «extend» kurang jelas. | Memperjelas arah panah dari SIA-UC03 Unduh Bukti Pengajuan KRS menuju SIA-UC01 Ajukan KRS. |
| 3 | Keterangan extension point dan kondisi belum jelas. | Menambahkan extension point Konfirmasi penyimpanan dan kondisi [pengajuan berhasil disimpan dan mahasiswa memilih unduh bukti]. |
| 4 | Judul batas sistem belum lengkap. | Menggunakan judul Sistem Informasi Akademik (SIA) pada batas sistem. |
| 5 | Nama use case keputusan KRS perlu diperjelas. | Menggunakan nama Proses Keputusan KRS pada SIA-UC04. |
| 6 | Status pengajuan setelah berhasil disimpan perlu dicantumkan dalam deskripsi use case. | Menambahkan status Menunggu Persetujuan Dosen Wali setelah pengajuan KRS berhasil disimpan. |

| NO | Alasan |
| :---: | :--- |
| 1 | Validasi KRS merupakan bagian wajib dari proses pengajuan KRS. |
| 2 | Unduh bukti merupakan proses tambahan yang hanya dilakukan jika mahasiswa memilihnya. |
| 3 | Keterangan tersebut menjelaskan kapan proses unduh bukti dapat dilakukan. |
| 4 | Judul yang lengkap memperjelas nama sistem yang dimodelkan. |
| 5 | Nama tersebut menjelaskan aktivitas dosen wali dalam menyetujui atau menolak pengajuan KRS. |
| 6 | Status tersebut menjelaskan kondisi pengajuan sebelum diproses oleh dosen wali. |

 ## 4. Kesimpulan

- Penggunaan notasi UML yang tepat sangat penting agar model sistem dapat dipahami secara standar dan tidak menimbulkan ambiguitas antara pengguna eksternal (aktor) dan fungsionalitas internal sistem (*use case*).
- Garis asosiasi pada Use Case Diagram hanya menggambarkan partisipasi atau hak akses interaksi aktor terhadap fungsi sistem, bukan menggambarkan alur proses atau urutan eksekusi.
- Konsistensi penamaan, pengisian metadata, dan pengecekan ulang (*review*) menjamin keterlacakan antara skenario kebutuhan dengan artefak diagram yang dihasilkan.
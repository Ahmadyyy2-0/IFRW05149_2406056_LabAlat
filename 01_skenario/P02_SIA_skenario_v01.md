Skenario tugas: Mahasiswa melihat jadwal kuliah melalui Sistem Informasi Akademik. Admin akademik mengelola jadwal kuliah. Dalam latihan ini, mahasiswa tidak mengelola jadwal dan admin tidak dihubungkan dengan fungsi melihat jadwal sebagai pengguna mahasiswa.

## 2. Catatan Review / Perbaikan Notasi
| No | Temuan | Perbaikan yang Diperlukan | Alasan |
| :-: | :--- | :--- | :--- |
| 1 | Actor berada di dalam batas sistem. | Pindahkan actor Mahasiswa ke luar batas sistem. | Actor harus berada di luar batas sistem. |
| 2 | Lihat Jadwal digambar dalam bentuk kotak. | Gunakan bentuk oval (elips) untuk use case. | Use case standar UML berbentuk ova. |
| 3 | Judul batas sistem menggunakan nama laboratorium. | Ubah judul menjadi Sistem Informasi Akademik. | Nama sistem harus sesuai skenario. |
| 4 | Mahasiswa dihubungkan ke Kelola Jadwal Kuliah. | Putus hubungan tersebut dan hubungkan Admin Akademik ke Kelola Jadwal Kuliah. | Admin mengelola jadwal kuliah. |
# PERTEMUAN 6: ACTIVITY DIAGRAM: DARI SKENARIO KE ALUR AKTIVITAS

## 1. Tujuan Praktikum

Setelah mengikuti praktikum ini, mahasiswa diharapkan mampu:

- Menyusun alur utama activity diagram dari Skenario Normal dengan tepat satu initial node dan minimal satu activity final node tanpa alur terputus.
- Mengubah Skenario Alternative menjadi cabang decision dengan guard yang saling lepas, lalu menyatukannya kembali melalui merge atau mengakhirinya pada jalur akhir yang jelas.
- Menggunakan pasangan fork dan join untuk memodelkan proses yang berjalan secara paralel.
- Mengelompokkan setiap action ke dalam swimlane aktor maupun sistem yang sesuai dan menelusurkannya kembali ke tabel skenario.

## 2. Dasar Teori

- Activity Diagram: Diagram UML yang memodelkan alur kerja proses bisnis atau alur aktivitas sistem, mencakup urutan action, percabangan bersyarat, eksekusi paralel, serta pembagian tanggung jawab antar pelaku.
- Kosakata Dasar Activity Diagram: Terdiri atas initial node, action, control flow, decision beserta guard dalam kurung siku, merge, pasangan fork dan join, activity final node, serta swimlane (partisi aktivitas).
- Pemetaan Skenario ke Aktivitas: Skenario Normal menjadi alur utama; Skenario Alternative menjadi cabang decision; langkah include menjadi action wajib pada alur utama; langkah extend menjadi cabang decision bersyarat; dan kolom Kegiatan/Respon sistem dipetakan ke swimlane masing-masing pelaku.

## 3. Analisis

- Studi Kasus Laboratorium (LAB): Dihasilkan 7 activity diagram untuk 7 use case utama (LAB-UC01, UC02, UC03, UC05, UC06, UC07, dan UC11). Pemetaan elemen dan aturan kontrol alurnya disajikan pada tabel berikut:

| NO | Nama Activity Diagram (LAB) | Swimlane yang Digunakan | Unsur Kontrol & Keterangan Pemetaan |
| :---: | :--- | :--- | :--- |
| 1 | Activity Lihat Ketersediaan (LAB-UC01) | Peminjam, Sistem | Decision [tersedia] dan [tidak tersedia] bermuara ke merge. |
| 2 | Activity Kelola Data Peralatan (LAB-UC02) | Petugas Laboratorium, Sistem | Decision tiga cabang [tambah], [ubah], [hapus] yang menggabungkan UC08–UC10. |
| 3 | Activity Peminjaman (LAB-UC03) | Mahasiswa, Sistem, Petugas Lab | Memuat action include Periksa Ketersediaan (UC04) dan decision extend cetak bukti (UC05). |
| 4 | Activity Cetak Bukti Pengajuan (LAB-UC05) | Mahasiswa, Sistem | Dimulai dari extension point dengan decision [ya, memilih cetak] dan [tidak]. |
| 5 | Activity Proses Keputusan (LAB-UC06) | Petugas Laboratorium, Sistem | Tugas mandiri; memuat decision validitas pengajuan serta status [disetujui] dan [ditolak]. |
| 6 | Activity Pengembalian (LAB-UC11) | Mahasiswa, Sistem, Petugas Lab | Menggunakan fork dan join untuk pemeriksaan kondisi fisik (UC12) dan kelengkapan aksesori (unsur baru). |
| 7 | Activity Lihat Laporan (LAB-UC07) | Kepala Laboratorium, Sistem | Decision ketersediaan data periode [ada] dan [tidak ada]. |

- Tugas Praktik Akademik (SIA): Disusun satu activity diagram terpadu dari proses Input Nilai Mata Kuliah (SIA-UC08) hingga Lihat KHS (SIA-UC09). Rincian pemetaan alur dan partisinya disajikan pada tabel berikut:

| NO | Komponen Activity Diagram (SIA) | Implementasi pada Diagram |
| :---: | :--- | :--- |
| 1 | Swimlane (Partisi) | Terbagi menjadi 4 partisi: Dosen, Sistem, Admin Akademik, dan Mahasiswa. |
| 2 | Decision Kelengkapan Nilai | Cabang [lengkap] lanjut ke pengesahan Admin Akademik; [belum lengkap] kembali ke Dosen lalu masuk ke merge. |
| 3 | Fork dan Join Publikasi | Setelah nilai disahkan, fork menjalankan Menerbitkan KHS dan Mengirim pemberitahuan secara paralel, lalu disatukan oleh join sebelum Mahasiswa melihat KHS. |
| 4 | Initial & Final Node | Tepat satu initial node di swimlane Dosen dan satu activity final node setelah action Melihat KHS. |

## 4. Kesimpulan

- Activity diagram memvisualisasikan logika alur eksekusi dari tabel skenario secara utuh, termasuk kondisi percabangan dan proses paralel.
- Penggunaan swimlane mempertegas pembagian tugas antara aktor manusia dan sistem, sedangkan pasangan decision-merge serta fork-join menjaga konsistensi alur dari awal hingga akhir.
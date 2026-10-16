<!-- skenario tugas -->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

<!-- tabel kebutuhan -->
|  ID   |                             Kebutuhan_tugas                              |
|-------|--------------------------------------------------------------------------|
|SIA-R01|                  Mahasiswa dapat melihat jadwal kuliah                   |
|SIA-R02|               Admin akademik dapat mengelola jadwal kuliah               |
|SIA-R03|                      Mahasiswa dapat mengajukan KRS                      |
|SIA-R04|             Sistem memvalidasi KRS sebagai bagian pengajuan              |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
|SIA-R06|        Dosen wali dapat memproses persetujuan atau penolakan KRS         |


<!-- batas sistem dan aturan -->
Batas dan asumsi:
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.

<!-- tabel identifikasi aktor -->
|    Aktor     |                       Tujuan_terhadap_sistem                        |
|--------------|---------------------------------------------------------------------|
|  Mahasiswa   |Melihat jadwal kuliah, mengajukan KRS, dan mengunduh bukti pengajuan |
|Admin_akademik|                       Mengelola jadwal kuliah                       |
|    Sistem    |                           Memvalidasi KRS                           |
|  Dosen_wali  |                      memproses persetujuan KRS                      |


<!-- tabel susunan katalog use case -->
ID                              Nama_user_case                                  Peran_dalam_model
SIA-R01                         Lihat jadwal kuliah                             Fungsi utama mahasiswa
SIA-R02                         Kelola jadwal kuliah                            Fungsi utama Admin_akademik
SIA-R03                         Ajukan KRS                                      Fungsi utama mahasiswa
SIA-R04                         Validasi KRS                                    Fungsi utama sistem
SIA-R05                         Unduh bukti pengajuan                           Tambahan bersyarat pada UC03
SIA-R06                         
<!-- relasi include -->

<!-- relasi extend -->
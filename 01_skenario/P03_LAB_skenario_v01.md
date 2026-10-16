<!-- Deskripsi Skenario -->
Mahasiswa mengajukan peminjaman peralatan dengan memilih alat,
jumlah, dan rentang waktu. Sistem memeriksa ketersediaan. Jika
tersedia dan data lengkap, sistem menyimpan pengajuan berstatus
menunggu keputusan. Pada tampilan konfirmasi, mahasiswa dapat
memilih mencetak bukti pengajuan. Petugas mengelola data peralatan
serta menyetujui atau menolak pengajuan. Kepala laboratorium melihat
laporan peminjaman.

<!-- Tabel Kebutuhan -->
|  ID   |                                            Kebutuhan                                            |
|-------|-------------------------------------------------------------------------------------------------|
|LAB-R01|                         Mahasiswa dapat melihat ketersediaan peralatan                          |
|LAB-R02|                             Petugas dapat mengelola data peralatan                              |
|LAB-R03|Mahasiswa dapat mengajukan peminjaman; sistem memeriksa ketersediaan sebelum menyimpan pengajuan |
|LAB-R04|            Mahasiswa dapat mencetak bukti pada konfirmasi pengajuan jika memilihnya             |
|LAB-R05|                  Petugas dapat menetapkan persetujuan atau penolakan pengajuan                  |
|LAB-R06|                      Kepala laboratorium dapat melihat laporan peminjaman                       |

<!-- Tabel katalog use case -->
|   ID   |      Nama_use_case       |            Peran_dalam_model            |
|--------|--------------------------|-----------------------------------------|
|LAB-UC01|Lihatketersediaanperalatan|          Fungsiutamamahasiswa           |
|LAB-UC02|   Keloladataperalatan    |           Fungsiutamapetugas            |
|LAB-UC03|     Ajukan peminjaman    |          Fungsiutamamahasiswa           |
|LAB-UC04|   Periksaketersediaan    |       PerilakuyangdisertakanUC03        |
|LAB-UC05|   Cetakbuktipengajuan    |        TambahanbersyaratpadaUC03        |
|LAB-UC06|Proseskeputusanpeminjaman |          Fungsi utama petugas           |
|LAB-UC07|       Lihatlaporan       |peminjaman Fungsiutamakepalalaboratorium |

<!-- relasi include -->
LAB-UC03 «include» LAB-UC04
Alasan: pemeriksaan menjadi bagian validasi pengajuan.

<!-- relasi extend -->
LAB-UC05 «extend» LAB-UC03
Extension point: Bukti pengajuan tersedia.
Kondisi: [mahasiswa memilih cetak].
Alasan: pengajuan tetap berhasil tanpa pencetakan
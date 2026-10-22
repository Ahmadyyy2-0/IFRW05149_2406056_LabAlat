|       Elemen        |                              SIA-UC03 — Ajukan KRS                              |
|---------------------|---------------------------------------------------------------------------------|
|       Tujuan        |                    Menghasilkan pengajuan KRS yang tersimpan                    |
|     Aktor_utama     |                                    Mahasiswa                                    |
|  Sumber_kebutuhan   |                               SIA-R03 dan SIA-R05                               |
|       Pemicu        |                     Mahasiswa memilih fungsi pengajuan KRS                      |
|      Prasyarat      |Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia |
|Pascakondisi_berhasil|      Pengajuan KRS tersimpan dengan status Menunggu persetujuan dosen wali      |
| Pascakondisi_gagal  |              Tidak ada pengajuan KRS baru yang berhasil tersimpan               |
|       Include       |                             SIA-UC04 — Validasi KRS                             |
|   Extension_point   |          Bukti pengajuan tersedia, pada langkah konfirmasi penyimpanan          |
|       Extend        |                  SIA-UC05 jika [mahasiswa memilih unduh bukti]                  |

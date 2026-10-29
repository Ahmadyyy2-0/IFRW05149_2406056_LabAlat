<!-- tabel kebutuhan -->
|  ID   |                                          Kebutuhan_tugas                                           |
|-------|----------------------------------------------------------------------------------------------------|
|SIA-R01|                               Mahasiswa dapat melihat jadwal kuliah                                |
|SIA-R02|                            Admin akademik dapat mengelola jadwal kuliah                            |
|SIA-R03|                                   Mahasiswa dapat mengajukan KRS                                   |
|SIA-R04|                          Sistem memvalidasi KRS sebagai bagian pengajuan                           |
|SIA-R05|             Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan              |
|SIA-R06|                     Dosen wali dapat memproses persetujuan atau penolakan KRS                      |
|SIA-R07|          Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik.          |
|SIA-R08|                      Dosen dapat menginput nilai mata kuliah yang diampunya.                       |
|SIA-R09|           Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan.           |
|SIA-R10|                           Admin Akademik dapat mengelola data mahasiswa.                           |
|SIA-R11|Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa. |
|SIA-R12|     Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS.     |


<!-- tabel use case -->
|   ID   |      Nama_usecase       |         Peran_dalam_model         |
|--------|-------------------------|-----------------------------------|
|SIA-UC01|   Lihat_Jadwal_Kuliah   |      Fungsi_utama_Mahasiswa       |
|SIA-UC02|  Kelola_Jadwal_Kuliah   |    Fungsi_utama_Admin_Akademik    |
|SIA-UC03|       Ajukan_KRS        |      Fungsi_utama_Mahasiswa       |
|SIA-UC04|      Validasi_KRS       |Perilaku_yang_disertakan_pada_UC03 |
|SIA-UC05|Unduh_Bukti_Pengajuan_KRS|   Tambahan_bersyarat_pada_UC03    |
|SIA-UC06|  Proses_Keputusan_KRS   |      Fungsi_utama_Dosen_Wali      |
|SIA-UC07| Lihat_Kalender_Akademik | Fungsi_bersama_Civitas_Akademika  |
|SIA-UC08| Input_Nilai_Mata_Kuliah |    Fungsi_utama_Dosen_pengampu    |
|SIA-UC09|        Lihat_KHS        |      Fungsi_utama_Mahasiswa       |
|SIA-UC10|  Kelola_Data_Mahasiswa  |           Use_case_umum           |
|SIA-UC11|  Tambah_Data_Mahasiswa  |     Use_case_khusus_dari_UC10     |
|SIA-UC12|   Ubah_Data_Mahasiswa   |     Use_case_khusus_dari_UC10     |
|SIA-UC13|  Hapus_Data_Mahasiswa   |     Use_case_khusus_dari_UC10     |

<!-- Generalisasi aktor -->
|   Aktor_Umum    |Aktor_Khusus|       Fungsi_yang_Diwarisi       |                                        Alasan                                         |
|-----------------|------------|----------------------------------|---------------------------------------------------------------------------------------|
|Civitas_Akademika| Mahasiswa  |Lihat_Kalender_Akademik_(SIA-UC07)|Mahasiswa_merupakan_bagian_dari_civitas_akademika_dan_dapat_melihat_kalender_akademik. |
|Civitas_Akademika|   Dosen    |Lihat_Kalender_Akademik_(SIA-UC07)|  Dosen_merupakan_bagian_dari_civitas_akademika_dan_dapat_melihat_kalender_akademik.   |

<!-- Generalisasi use case -->
|        Use_Case_Umum         |       Use_Case_Khusus        |    Aktor     |                         Perilaku_Pembeda                         |
|------------------------------|------------------------------|--------------|------------------------------------------------------------------|
|SIA-UC10_Kelola_Data_Mahasiswa|SIA-UC11_Tambah_Data_Mahasiswa|Admin_Akademik|                 Menambahkan_data_mahasiswa_baru.                 |
|SIA-UC10_Kelola_Data_Mahasiswa| SIA-UC12_Ubah_Data_Mahasiswa |Admin_Akademik|          Mengubah_data_mahasiswa_yang_sudah_tersimpan.           |
|SIA-UC10_Kelola_Data_Mahasiswa|SIA-UC13_Hapus_Data_Mahasiswa |Admin_Akademik|Menghapus_data_mahasiswa_yang_tidak_memiliki_data_akademik_aktif. |

<!-- collaboration -->
|ID_Collaboration|  Nama_Collaboration   |  Use_Case_yang_Direalisasikan   |
|----------------|-----------------------|---------------------------------|
|    SIA-CO01    |Input_Nilai_Mata_Kuliah|SIA-UC08_Input_Nilai_Mata_Kuliah |
|    SIA-CO02    |       Lihat_KHS       |       SIA-UC09_Lihat_KHS        |


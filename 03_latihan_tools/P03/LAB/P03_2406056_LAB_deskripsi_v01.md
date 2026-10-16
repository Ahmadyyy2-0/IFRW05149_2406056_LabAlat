|       Elemen        |               LAB-UC03—Ajukanpeminjaman                |
|---------------------|--------------------------------------------------------|
|       Tujuan        |      Menghasilkanpengajuanpeminjamanyangtersimpan      |
|     Aktor_utama     |                       Mahasiswa                        |
|  Sumber_kebutuhan   |                   LAB-R03danLAB-R04                    |
|       Pemicu        |       Mahasiswamemilihfungsipengajuanpeminjaman        |
|      Prasyarat      |   Mahasiswatelahterautentikasi;dataperalatantersedia   |
|Pascakondisi_berhasil|PengajuantersimpandengannomordanstatusMenunggukeputusan |
| Pascakondisi_gagal  |       Tidakadapengajuanbaruyangberhasiltersimpan       |
|       Include       |              LAB-UC04—Periksaketersediaan              |
|   Extension_point   |          Buktipengajuantersedia,padalangkah6           |
|       Extend        |         LAB-UC05jika[mahasiswa memilih cetak]          |


Elemen	                                                                                        Deskripsi
ID	                                                                                            SIA-UC08
Nama_use_case	                                                                                InputNilaiMataKuliah
Sumber_kebutuhan	                                                                            SIA-R08
Tujuan	                                                                                        Memasukkan nilai mahasiswa untuk mata kuliah yang diampu.
Aktor_utama	                                                                                    Dosen
Pemicu	                                                                                        Dosen memilih fungsi input nilai mata kuliah.
Prasyarat	                                                                                    Dosen telah login dan merupakan dosen pengampu mata kuliah yang akan diinput nilainya.
Alur_utama	                                                                                    1. Dosen membuka menu input nilai. 2. Sistem menampilkan mata kuliah yang diampu dosen. 3. Dosen memilih mata kuliah dan mahasiswa. 4. Dosen memasukkan nilai. 5. Sistem memeriksa rentang nilai. 6. Sistem menyimpan nilai yang valid dan menampilkan konfirmasi berhasil.
Alur_alternatif	                                                                                Jika nilai berada di luar rentang yang sah, sistem menolak nilai tersebut, menampilkan pesan kesalahan, dan meminta dosen memasukkan nilai yang benar.
Pascakondisi_berhasil                                                                           Nilai yang valid tersimpan untuk mahasiswa dan mata kuliah yang dipilih.
Pascakondisi_gagal	                                                                            Nilai tidak tersimpan atau tidak berubah apabila input tidak valid atau proses penyimpanan gagal. Sistem menampilkan informasi kegagalan.
Collaboration	                                                                                SIA-CO01: Input Nilai Mata Kuliah
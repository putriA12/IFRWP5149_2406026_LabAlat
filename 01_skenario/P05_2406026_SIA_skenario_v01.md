<!-- P05 SIA Skenario: Layanan Hasil Studi -->
Diagram acuan: diagram SIA Pertemuan 4 (tidak diubah).

<!-- usecase skenario -->
<!-- Tabel 5.15 
Skenario Use Case SIA-UC07 Lihat Kalender Akademik -->
----------------------------------------------------------------------------------------------------------------------------------------
| Nama use case | SIA-UC07 Lihat Kalender Akademik                                                                                      |
| Aktor         | Civitas Akademika (berlaku untuk Mahasiswa dan Dosen)                                                                 |
| Tujuan        | Civitas akademika dapat mengetahui jadwal kegiatan akademik pada semester yang dipilih                                |
| Deskripsi     | Civitas Akademika membuka fungsi kalender akademik, memilih semester, dan melihat kalender akademik semester tersebut |

| Kegiatan             | Respon sistem                                                                                                      |
--------------------------------------------------------------------------------------------------------------------------------------------|
| skenario Normal      | 1. Civitas Akademika membuka fungsi Lihat Kalender Akademik                                                        | 
|                      | 2. Sistem menampilkan daftar semester                                                                              |
|                      | 3. Civitas Akademika memilih semester                                                                              |     
|                      | 4. Sistem menampilkan kalender akademik semester terpilih beserta nama kegiatan, tanggal mulai, dan tanggal selesai|
| Skenario Alternative | 5. Kalender akademik semester yang dipilih belum tersedia (cabang dari langkah 4)                                  |
|                      | 6. Sistem menampilkan pesan kalender akademik belum tersedia untuk semester tersebut                               |
| Skenario Akhir       | Use case selesai jika kalender akademik semester terpilih ditampilkan; jika kalender belum tersedia, use case selesai dengan pesan tersebut|
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
Keterangan: ditulis satu kali atas nama Civitas Akademika. Mahasiswa dan Dosen mewarisi use case ini lewat generalization aktor, sehingga tidak ada tabel terpisah untuk keduanya.

<!-- Tabel 5.16 S
kenario Use Case SIA-UC08 Input Nilai Mata Kuliah -->
-------------------------------------------------------------------------|
| Nama use case | SIA-UC08 Input Nilai Mata Kuliah                       |
| Aktor         | Dosen                                                  |
| Tujuan        | Nilai mahasiswa pada mata kuliah yang diampu tersimpan |
| Deskripsi     | Dosen pengampu memilih mata kuliah, mengisi nilai mahasiswa, dan menyimpan nilai. Prasyarat: dosen adalah pengampu mata kuliah tersebut |

| Kegiatan              | Respon sistem                                                                             |
--------------------------------------------------------------------------------------------------------------------|
| Skenario Normal       | 1. Dosen membuka fungsi Input Nilai Mata Kuliah                                           | 
|                       | 2. Sistem memeriksa dosen sebagai pengampu dan menampilkan daftar mata kuliah yang diampu |
|                       | 3. Dosen memilih mata kuliah                                                              | 
|                       | 4. Sistem menampilkan daftar mahasiswa peserta beserta isian nilai                        |
|                       | 5. Dosen mengisi nilai setiap mahasiswa                                                   | 
|                       | 6. Sistem memeriksa nilai berada dalam rentang yang sah                                   |
|                       | 7. Dosen menyimpan nilai                                                                  | 
|                       | 8. Sistem menyimpan nilai dan menampilkan konfirmasi                                      |
| Skenario Alternative  | 9. Nilai yang diisi di luar rentang yang sah (cabang dari langkah 6)                      | 
|                       | 10. Sistem menolak penyimpanan dan meminta dosen memperbaiki nilai                        |
|                       | 11. Dosen bukan pengampu mata kuliah yang dipilih (cabang dari langkah 2)                 | 
|                       | 12. Sistem menolak akses dan menampilkan pesan hanya dosen pengampu yang dapat menginput nilai |
| Skenario Akhir        | Use case selesai jika nilai tersimpan; jika nilai di luar rentang yang sah atau dosen bukan pengampu, nilai tidak tersimpan |
-------------------------------------------------------------------------------------------------------------------------------------------------------
Keterangan: use case ini direalisasikan oleh collaboration SIA-CO01 Input Nilai Mata Kuliah. Collaboration tersebut tidak mempunyai langkah kegiatan pada tabel ini.

<!-- Tabel 5.17 
Skenario Use Case SIA-UC09 Lihat KHS -->
---------------------------------------------------------------------------------------------------------------|
| Aktor         | Mahasiswa                                                                                    |
| Tujuan        | Mahasiswa dapat mengetahui hasil studinya pada semester yang dipilih                         |
| Deskripsi     | Mahasiswa memilih semester dan melihat KHS yang hanya memuat nilai yang sudah dipublikasikan |

| Kegiatan             | Respon sistem                                                                                       |
-----------------------------------------------------------------------------------------------------------------------------|
| Skenario Normal      | 1. Mahasiswa membuka fungsi Lihat KHS                                                               | 
|                      | 2. Sistem menampilkan daftar semester milik mahasiswa                                               |
|                      | 3. Mahasiswa memilih semester                                                                       | 
|                      | 4. Sistem menampilkan KHS semester terpilih beserta mata kuliah dan nilai yang sudah dipublikasikan |
| skenario Alternative | 5. Tidak ada nilai yang sudah dipublikasikan pada semester terpilih (cabang dari langkah 4)         | 
|                      | 6. Sistem menampilkan pesan nilai belum dipublikasikan                                              |
| Skenario Akhir       | Use case selesai jika KHS dengan nilai yang sudah dipublikasikan ditampilkan; jika belum ada nilai dipublikasikan, use case selesai dengan pesan tersebut|
------------------------------------------------------------------------------------------------------------------------------------------------
Keterangan: use case ini direalisasikan oleh collaboration SIA-CO02 Lihat KHS. Collaboration tersebut tidak mempunyai langkah kegiatan pada tabel ini.


<!-- Tabel 5.18 
Skenario Use Case SIA-UC10 Kelola Data Mahasiswa -->
---------------------------------------------------------------------------------------------------------------|
|Nama use case  | SIA-UC10 Kelola Data Mahasiswa                                                               |
| Aktor         | Admin Akademik                                                                               |
| Tujuan        | Data mahasiswa terkelola melalui satu fungsi pengelolaan bersama                             |
| Deskripsi     | Admin membuka fungsi pengelolaan data mahasiswa, memilih bentuk pengelolaan, dan menyimpan perubahan. Bentuk tambah, ubah, dan hapus dijabarkan pada tabel khususnya masing-masing  

| Kegiatan             | Respon sistem                                                                                       |
-----------------------------------------------------------------------------------------------------------------------------|
| Skenario Normal      | 1. Admin Akademik membuka fungsi Kelola Data Mahasiswa                                              |
|                      | 2. Sistem menampilkan daftar data mahasiswa                                                         |
|                      | 3. Admin Akademik memilih bentuk pengelolaan, yaitu tambah, ubah, atau hapus                        | 
|                      | 4. Sistem menampilkan formulir sesuai bentuk pengelolaan yang dipilih                               |
|                      | 5. Admin Akademik mengisi atau mengonfirmasi data                                                   | 
|                      | 6. Sistem memeriksa kelengkapan dan keabsahan data                                                  |
|                      | 7. Admin Akademik menyimpan perubahan                                                               | 
|                      | 8. Sistem menyimpan perubahan dan menampilkan konfirmasi                                            |
| skenario Alternative | 9. Data tidak lengkap atau tidak sah (cabang dari langkah)                                          |
|                      | 10. Sistem menolak penyimpanan dan menampilkan pesan kesalahan data                                 |
| Skenario Akhir       | Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak lengkap atau tidak sah, perubahan tidak tersimpan                                                                                                                                 |
------------------------------------------------------------------------------------------------------------------------------------------------                                                                                

<!-- Tabel 5.19 
Skenario Use Case SIA-UC11 Tambah Data Mahasiswa -->
---------------------------------------------------------------------------------------------------------------|
| Nama use case | SIA-UC11 Tambah Data Mahasiswa                                                               |
| Aktor         | Admin Akademik                                                                               |
| Tujuan        | Data mahasiswa baru tersimpan sebagai bentuk khusus dari pengelolaan data  mahasiswa                                                                                                      |
| Deskripsi     | Admin mengisi data mahasiswa baru dan menyimpannya; langkah bersama mengikuti Tabel skenario SIA-UC10 |

| Kegiatan       | Respon sistem                                                                                |
----------------------------------------------------------------------------------------------------------------|
| kenario Normal       | 1. Admin Akademik membuka fungsi Tambah Data Mahasiswa                                 |
|                      | 2. Sistem menampilkan formulir data mahasiswa baru                                     |
|                      | 3. Admin Akademik mengisi data mahasiswa baru                                          |
|                      | 4. Sistem memeriksa kelengkapan data                                                   |
|                      | 5. Admin Akademik menyimpan data                                                       |
|                      | 6. Sistem menyimpan data mahasiswa baru dan menampilkan konfirmasi                     |
| Skenario Alternative | 7. Data tidak lengkap (cabang dari langkah 4)                                          |
|                      | 8. Sistem menolak penyimpanan dan meminta admin melengkapi data                        |
| Skenario Akhir       | Use case selesai jika data mahasiswa baru tersimpan; jika data tidak lengkap, data tidak tersimpan |
-----------------------------------------------------------------------------------------------------------------------------
Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa baru tersimpan. Langkah bersama mengikuti Tabel skenario SIA-UC10.

<!-- Tabel 5.20 
Skenario Use Case SIA-UC12 Ubah Data Mahasiswa -->
-----------------------------------------------------------------------------------------------------------------------------------------------------
| Nama use case         | SIA-UC12 Ubah Data Mahasiswa                                                                                               |
| Akto                  | Admin Akademik                                                                                                             |
| Tujuan                | Data mahasiswa berubah sebagai bentuk khusus dari pengelolaan data mahasiswa                                               |
| Deskripsi             | Admin memilih data mahasiswa, mengubah datanya, dan menyimpan perubahan; langkah bersama mengikuti Tabel skenario SIA-UC10 |


| Kegiatan             | Respon sistem                                                                          |
----------------------------------------------------------------------------------------------------------------|
| kenario Normal       | 1. Admin Akademik memilih data mahasiswa yang akan diubah                              |
|                      | 2. Sistem menampilkan data mahasiswa saat ini                                          |
|                      | 3. Admin Akademik mengubah data mahasiswa                                              |
|                      | 4. Sistem memeriksa perubahan data                                                     |
|                      | 5. Admin Akademik menyimpan perubahan                                                  |
|                      | 6. Sistem menyimpan data yang diubah dan menampilkan konfirmasi                        |
| Skenario Alternative | 7. Data mahasiswa tidak ditemukan (cabang dari langkah 2)                              |
|                      | 8. Sistem menampilkan pesan data mahasiswa tidak ditemukan                             |
| Skenario Akhir       | Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak ditemukan, perubahan tidak tersimpan |
-----------------------------------------------------------------------------------------------------------------------------

Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa berubah. Langkah bersama mengikuti Tabel skenario SIA-UC10.


<!-- Tabel 5.21 
Skenario Use Case SIA-UC13 Hapus Data Mahasiswa -->
-----------------------------------------------------------------------------------------------------------------------------------------------------
| Nama use case         | SIA-UC13 Hapus Data Mahasiswa                                                                                              |
| Akto                  | Admin Akademik                                                                                                             |
| Tujuan                | Data mahasiswa terhapus sebagai bentuk khusus dari pengelolaan data mahasiswa                                              |
| Deskripsi             | Admin memilih data mahasiswa, mengonfirmasi penghapusan, dan sistem menghapus data tersebut; langkah bersama mengikuti Tabel skenario SIA-UC10 |


| Kegiatan             | Respon sistem                                                                                                   |
-----------------------------------------------------------------------------------------------------------------------------------------|
| kenario Normal       | 1. Admin Akademik memilih data mahasiswa yang akan dihapus                                                      |
|                      | 2. Sistem memeriksa mahasiswa tidak memiliki data akademik aktif                                                |
|                      | 3. Admin Akademik mengonfirmasi penghapusan                                                                     |
|                      | 4. Sistem menghapus data mahasiswa dan menampilkan konfirmasi penghapusan                                       |
| Skenario Alternative | 5. Mahasiswa memiliki data akademik aktif (cabang dari langkah 2)                                               |
|                      | 6. Sistem menolak penghapusan dan menampilkan pesan mahasiswa masih memiliki data akademik aktif                |
| Skenario Akhir       | Use case selesai jika data mahasiswa terhapus; jika mahasiswa memiliki data akademik aktif, data tidak terhapus |
------------------------------------------------------------------------------------------------------------------------------------------
Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa terhapus, dengan syarat tidak ada data akademik aktif. Langkah bersama mengikuti Tabel skenario SIA-UC10.


Lembar Penelusuran terhadap Diagram SIA P04
--------------------------------------------------------------------------------------------------------------------------------------------------------------
| Tabel         | Relasi yang ditelusur pada diagram                                                  | Hasil pencocokan 
--------------------------------------------------------------------------------------------------------------------------------------------------------------
| 5.15 SIA-UC07 | Asosiasi Civitas Akademika ke Lihat Kalender Akademik; generalization aktor         | Cocok; ditulis satu kali atas nama Civitas Akademika |
                  Mahasiswa ke Civitas Akademika dan Dosen ke Civitas Akademika                       |                                                      |
| 5.16 SIA-UC08 | Asosiasi Dosen ke Input Nilai Mata Kuliah; realization collaboration SIA-CO01       | Cocok; collaboration hanya disebut di keterangan     |
| 5.17 SIA-UC09 | Asosiasi Mahasiswa ke Lihat KHS; realization collaboration SIA-CO02                 | Cocok; collaboration hanya disebut di keterangan     |
| 5.18 SIA-UC10 | Asosiasi Admin Akademik ke Kelola Data Mahasiswa; menjadi use case umum bagi        | Cocok; memuat perilaku bersama                       |
                  UC11, UC12, UC13                                                                    | 
| 5.19 SIA-UC11 | Generalization Tambah Data Mahasiswa ke Kelola Data Mahasiswa                       | Cocok; hanya memuat perilaku pembeda                 |
| 5.20 SIA-UC12 | Generalization Ubah Data Mahasiswa; panah pada diagram menuju Tambah Data           | Perlu konfirmasi; tabel mengikuti Tabel 5.14 (khusus dari 
                  Mahasiswa, bukan Kelola Data Mahasiswa                                              | UC10)                                                |
| 5.21 SIA-UC13 | Generalization Hapus Data Mahasiswa ke Kelola Data Mahasiswa                        | Cocok; syarat tidak ada data akademik aktif |

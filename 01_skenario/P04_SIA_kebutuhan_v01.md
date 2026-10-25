<!-- SKENARIO-->
Tugas ini berbeda dari tugas pertemuan sebelumnya. Tugas Pertemuan 2 adalah jadwal kuliah dan tugas Pertemuan 3  adalah jadwal kuliah dan tugas Pertemuan 3 adalah pengajuan KRS. Tugas Pertemuan 4 adalah layanan hasil studi, dengan teknik generalization dan collaboration yang sama seperti studi kasus, tetapi diterapkan pada skenario baru tanpa contoh jawaban. Skenario tugas berikut fiktif untuk praktikum dan berbeda dari tugas Pertemuan 2 (jadwal kuliah) dan Pertemuan 3 (pengajuan KRS).

Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin Akademik mengelola data mahasiswa: menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh collaboration yang bersesuaian.
2 use case utama : Kuliah dan Lihat KHS.

<!-- Kebutuhan sistem -->
| ID | Kebutuhan |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik. |
| SIA-R08 | Dosen memasukkan nilai untuk mata kuliah yang diajarnya. |
| SIA-R09 | Mahasiswa melihat KHS untuk semester yang nilainya telah diumumkan. |
| SIA-R10 | Admin Akademik mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa memiliki tiga tindakan khusus: menambah, mengubah, dan menghapus data mahasiswa. |
| SIA-R12 | Model menunjukkan kolaborasi yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |

<!-- BATAS DAN ASUMSI -->
1. Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02 (Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap mempunyai identitas berbeda.
2. Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
3. Kalender akademik pada tugas ini adalah agenda resmi institusi (awal semester, batas KRS, masa ujian, dan sejenisnya); jangan menyamakannya dengan jadwal kuliah pada Pertemuan 2.
4. Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai yang diinput belum terpublikasi sebelum dinyatakan resmi oleh ketentuan tugas ini: KHS hanya menampilkan nilai yang sudah dipublikasikan.
5. Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif. Ketentuan ini fiktif untuk latihan.
6. Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari Pertemuan 3. Pembayaran dan perancangan basis data berada di luar tugas ini.

<!--Langkah 2: Identifikasi Aktor dan Use Case  -->
Diagram tugas ini bersifat kumulatif. Katalog yang disusun adalah katalog gabungan. Fungsi lama tetap dicantumkan, yaitu SIA-UC01 Lihat Jadwal Kuliah dan SIA-UC02 Kelola Jadwal Kuliah dari Pertemuan 2, serta SIA-UC03 Ajukan KRS, SIA-UC04 Validasi KRS, SIA-UC05 Unduh Bukti Pengajuan KRS, dan SIA-UC06 Proses Keputusan KRS dari Pertemuan 3, lengkap dengan relasi include dan extend di antara ketiganya.

Fungsi baru dimulai dari SIA-UC07: SIA-UC07 Lihat Kalender Akademik, SIA-UC08 Input Nilai Mata Kuliah, SIA-UC09 Lihat KHS, SIA-UC10 Kelola Data Mahasiswa sebagai use case umum, serta SIA-UC11 Tambah Data Mahasiswa, SIA-UC12 Ubah Data Mahasiswa, dan SIA-UC13 Hapus Data Mahasiswa sebagai use case khusus.

Tentukan aktor umum Civitas Akademika, dua aktor khususnya yaitu Mahasiswa dan Dosen, serta Admin Akademik dan Dosen Wali yang tetap dari pertemuan sebelumnya. Institut Teknologi Garut S1 Teknik Informatika Praktikum Analisis dan Desain Berorientasi Objek | 65
Setiap baris katalog memuat ID, nama, aktor terkait, sumber kebutuhan, dan tanda tetap atau baru.

<!-- USECASE KUMULATIFF -->
| ID       | Nama Use Case             | Aktor Terkait       | Sumber Kebutuhan | Status |
------------------------------------------------------------------------------------------
| SIA-UC01 | Lihat Jadwal Kuliah       | Mahasiswa           | Pertemuan 2      | Tetap |
| SIA-UC02 | Kelola Jadwal Kuliah      | Admin Akademik      | Pertemuan 2      | Tetap |
| SIA-UC03 | Ajukan KRS                | Mahasiswa           | Pertemuan 3      | Tetap |
| SIA-UC04 | Validasi KRS              | Periksa diagram P03 | Pertemuan 3      | Tetap |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa           | Pertemuan 3      | Tetap |
| SIA-UC06 | Proses Keputusan KRS      | Dosen Wali          | Pertemuan 3      | Tetap |
| SIA-UC07 | Lihat Kalender Akademik   | Civitas Akademika   | SIA-R07          | Baru  |
| SIA-UC08 | Input Nilai Mata Kuliah   | Dosen               | SIA-R08          | Baru  |
| SIA-UC09 | Lihat KHS                 | Mahasiswa           | SIA-R09          | Baru  |
| SIA-UC10 | Kelola Data Mahasiswa     | Admin Akademik      | SIA-R10          | Baru  |
| SIA-UC11 | Tambah Data Mahasiswa     | Admin Akademik      | SIA-R11          | Baru  |
| SIA-UC12 | Ubah Data Mahasiswa       | Admin Akademik      | SIA-R11          | Baru  | 
| SIA-UC13 | Hapus Data Mahasiswa      | Admin Akademik      | SIA-R11          | Baru  |

<!--Langkah 3: Tetapkan Generalization Aktor  -->
Mahasiswa dan Dosen merupakan aktor khusus dari aktor umum Civitas Akademika. Fungsi yang diwarisi adalah melihat kalender akademik. Asosiasi untuk fungsi bersama tersebut digambar satu kali dari aktor umum Civitas Akademika ke use case Lihat Kalender Akademik. Generalisasi aktor digunakan karena Mahasiswa dan Dosen sama-sama memiliki fungsi melihat kalender akademik sebagai Civitas Akademika.

<!--Langkah 4: Tetapkan Generalization Use Case  -->
Use case umum adalah SIA-UC10 Kelola Data Mahasiswa. Use case khususnya adalah:
- SIA-UC11 Tambah Data Mahasiswa: Admin Akademik menambahkan data mahasiswa baru.
- SIA-UC12 Ubah Data Mahasiswa: Admin Akademik mengubah data mahasiswa yang sudah ada.
- SIA-UC13 Hapus Data Mahasiswa: Admin Akademik menghapus data mahasiswa yang tidak memiliki data akademik aktif.
Setiap use case khusus terhubung ke use case umum melalui relasi generalization. Arah panah generalization menunjuk ke use case umum Kelola Data Mahasiswa.

<!--Langkah 5: Tetapkan Collaboration  -->
| ID Collaboration | Nama Collaboration      | Use Case yang Direalisasikan     |
---------------------------------------------------------------------------------
| SIA-CO01         | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02         | Lihat KHS               | SIA-UC09 Lihat KHS               |

<!-- Langkah 6: Susun Use Case Description -->
(INPUT MATA KULIAH) 
-------------------
Nama Use Case   : Input Nilai Mata Kuliah
ID Use Case     : SIA-UC08
Aktor Utama     : Dosen
Sumber Kebutuhan: SIA-R08
Collaboration   : SIA-CO01 Input Nilai Mata Kuliah
Deskripsi       : Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir.

(Lihat KHS)
-----------
Nama Use Case   : Lihat KHS
ID Use Case     : SIA-UC09
Aktor Utama     : Mahasiswa
Sumber Kebutuhan: SIA-R09
Collaboration   : SIA-CO02 Lihat KHS
Deskripsi       : Mahasiswa dapat melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. KHS hanya menampilkan nilai yang sudah             dipublikasikan.

Prasyarat dan alur utama
-----------------------------------------------------------------------------------------
Prasyarat       : 1. Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
                  2. Dosen merupakan pengampu mata kuliah yang akan diinput nilainya.
                  3. Masa perkuliahan telah berakhir.
Alur Utama      : 1. Dosen memilih mata kuliah yang diampunya.
                  2. Dosen memasukkan nilai mata kuliah.
                  3. Sistem memeriksa nilai yang dimasukkan.
                  4. Sistem menerima input apabila nilai berada dalam rentang yang sah.
Alur Alternatif : Jika nilai berada di luar rentang yang sah, sistem menolak input nilai.
Pascakondisi Berhasil: Nilai berhasil diinput sesuai ketentuan tugas.
Pascakondisi Gagal: Nilai ditolak apabila berada di luar rentang yang sah.

<!--Langkah 8: Uji Konsistensi, Review, dan Revisi  -->
Periksa tiga situasi berikut dan tuliskan hasilnya pada berkas kebutuhan tugas:
---------------------------------------------------------------------------------
• Situasi A: Mahasiswa melihat kalender akademik tanpa garis asosiasi langsung dari Mahasiswa. (langsung dari Mahasiswa: jelaskan mengapa hal itu tetap benar menurut diagram (pewarisan dari Civitas Akademika))
    Hasil: Hal tersebut tetap benar menurut diagram karena Mahasiswa merupakan aktor khusus dari Civitas Akademika dan mewarisi fungsi melihat kalender akademik melalui generalisasi aktor.
----------------------------------------------------------------------------------
• Situasi B: Dosen yang bukan pengampu mencoba menginput nilai.(tuliskan hasil yang harus terjadi menurut deskripsi Input Nilai Mata Kuliah)
    Hasil: Dosen tersebut tidak memenuhi prasyarat use case Input Nilai Mata Kuliah. Input nilai tidak boleh dilakukan oleh dosen yang bukan pengampu mata kuliah tersebut.

• Situasi C: Admin Akademik menghapus data mahasiswa yang masih memiliki data akademik aktif (tuliskan hasil yang harus terjadi menurut aturan tugas)
    Hasil: Penghapusan ditolak karena aturan tugas menyatakan bahwa Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif.

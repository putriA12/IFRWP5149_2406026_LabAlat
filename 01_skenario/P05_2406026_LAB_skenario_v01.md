<!-- P05 LAB Lembar Telaah Skenario: Peminjaman dan Pengembalian Peralatan Laboratorium -->
Diagram acuan: diagram kumulatif P04 LAB (5 aktor, 12 use case, 2 collaboration, 17 hubungan). Diagram tidak diubah.

<!-- Check C.4 -->
- Seluruh field tabel terisi: Nama use case, Aktor, Tujuan, Deskripsi, kolom Kegiatan dan Respon sistem, Skenario Normal, Skenario Alternative, Skenario Akhir.
- Langkah berurutan, satu aksi per langkah, penomoran berlanjut dari Skenario Normal ke Skenario Alternative tanpa pengulangan nomor.
- Kolom Kegiatan hanya berisi aksi aktor; kolom Respon sistem hanya berisi tanggapan sistem.
- Data yang dimasukkan dan ditampilkan disebut eksplisit (nama field, nilai, status).
- Include ditulis sebagai langkah rujukan pada Skenario Normal (nama, ID, tabel yang disertakan), tanpa menyalin langkahnya.
- Extend ditulis sebagai cabang bersyarat pada Skenario Alternative dengan condition dan extension point, serta rujukan ke tabel use case tambahan.
- Generalization aktor: skenario aktor umum ditulis satu kali, tidak ada tabel ganda untuk aktor khusus.
- Generalization use case: skenario umum memuat perilaku bersama; skenario khusus memuat perilaku pembeda dan merujuk ke skenario umum.
- Collaboration disebut pada keterangan tabel dan tidak diberi langkah kegiatan sendiri.
- Setiap tabel punya Skenario Alternative dan Skenario Akhir.
- Nama, ID, aktor, condition, dan extension point sama persis dengan diagram P04.
- Catatan Kepala Laboratorium: LAB-UC07 berdiri sendiri, tanpa include, extend, generalization, atau realization.
- Berkas diagram P04 tidak diubah; dokumen disimpan di `01_skenario` dengan nama dan versi benar.

<!-- Lembar penelusuran per tabel -->
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| Tabel | Relasi yang ditelusur | Hasil pencocokan |
|---|---|---|
| 5.3 LAB-UC01 Lihat Ketersediaan Peralatan | Asosiasi Peminjam ke UC01; generalization aktor Mahasiswa dan Dosen ke Peminjam | |
| 5.1 LAB-UC03 Ajukan Peminjaman | Asosiasi Peminjam ke UC03; include ke LAB-UC04 (langkah 2); extend dari LAB-UC05 dengan condition [mahasiswa memilih cetak] dan extension point Bukti pengajuan tersedia (langkah 11 dan 12); realization LAB-CO01 | |
| 5.4 LAB-UC04 Periksa Ketersediaan | Include dari LAB-UC03; tidak ada interaksi langsung dengan aktor | |
| 5.5 LAB-UC05 Cetak Bukti Pengajuan | Extend ke LAB-UC03; asosiasi khusus Mahasiswa | |
| 5.6 LAB-UC02 Kelola Data Peralatan | Asosiasi Petugas Laboratorium ke UC02; use case umum bagi UC08, UC09, UC10 | |
| 5.7 LAB-UC08 Tambah Data Peralatan | Generalization UC08 ke UC02 | |
| 5.8 LAB-UC09 Ubah Data Peralatan | Generalization UC09 ke UC02 | |
| 5.9 LAB-UC10 Hapus Data Peralatan | Generalization UC10 ke UC02 | |
| 5.10 LAB-UC06 Proses Keputusan Peminjaman | Asosiasi Petugas Laboratorium ke UC06; tanpa relasi antar use case | |
| 5.11 LAB-UC07 Lihat Laporan Peminjaman | Asosiasi Kepala Laboratorium ke UC07; tanpa relasi lain | |
| 5.12 LAB-UC11 Catat Pengembalian Peralatan | Asosiasi Petugas Laboratorium ke UC11; include ke LAB-UC12 (langkah 6); realization LAB-CO02 | |
| 5.13 LAB-UC12 Periksa Kondisi Peralatan | Include dari LAB-UC11 | |

<!-- Catatan temuan awal -->
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Pola jobsheet: langkah ganjil di kolom Kegiatan, langkah genap di kolom Respon sistem.
1. UC04 dan UC12 (kolom Kegiatan):UC04 langkah 1 ("Alur pengajuan memanggil ...") dan langkah 3 ("Sistem menyatakan peralatan tersedia") ada di kolom Kegiatan, padahal bukan aksi aktor. UC12 langkah 1 ("Alur pengembalian memanggil ...") juga begitu. UC04 langkah 4 ("Alur pengajuan melanjutkan ...") ada di kolom Respon sistem tetapi bukan tanggapan sistem.
2. UC04 dan UC12 (deskripsi)     : Deskripsi menyatakan tidak ada interaksi langsung dengan aktor, tetapi UC12 langkah 3 berisi aksi aktor ("Petugas memilih nilai kondisi peralatan").
3. UC11 langkah 4 dan 5          : Keduanya aksi sistem berurutan. Langkah 5 ("Sistem memeriksa status peminjaman harus Dipinjam") ada di kolom Kegiatan, padahal kolom itu hanya untuk aksi aktor.
4. UC11 langkah 9                : "Petugas melihat konfirmasi" bukan aksi yang mengubah apa pun; periksa apakah layak menjadi satu langkah.
5. UC06 langkah 5                : Dicatat sebagai cabang dari langkah 4, padahal keputusan menolak ditetapkan pada langkah 3. Periksa apakah rujukan cabangnya sudah tepat.

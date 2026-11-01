No	|                                                                   Kesimpulan
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1	| Pertemuan 5 berfokus pada penulisan skenario use case dari diagram kumulatif Pertemuan 4; tidak ada diagram, use case, aktor, atau kebutuhan baru.
2	| Tabel skenario memuat baris Nama use case, Aktor, Tujuan, dan Deskripsi, kolom Kegiatan dan Respon sistem, Skenario Normal, Skenario Alternative, dan Skenario Akhir tanpa field kosong.
3	| Setiap langkah berisi satu aksi, kolom Kegiatan hanya berisi aksi aktor, kolom Respon sistem hanya berisi tanggapan sistem, dan penomoran berlanjut dari Skenario Normal ke Skenario Alternative.
4	| Relasi include dipetakan menjadi langkah rujukan pada Skenario Normal, sedangkan relasi extend dipetakan menjadi cabang bersyarat pada Skenario Alternative dengan condition dan extension point.
5	| Aktor Civitas Akademika menjadi aktor umum, sehingga SIA-UC07 Lihat Kalender Akademik ditulis satu kali dan berlaku untuk Mahasiswa dan Dosen.
6	| SIA-UC10 Kelola Data Mahasiswa menjadi skenario umum, sedangkan SIA-UC11, SIA-UC12, dan SIA-UC13 hanya memuat perilaku pembeda dan merujuk ke skenario umum.
7	| Collaboration SIA-CO01 dan SIA-CO02 hanya disebut pada keterangan tabel SIA-UC08 dan SIA-UC09 dan tidak diberi langkah kegiatan sendiri.
8	| Aturan khusus SIA diterapkan: nilai hanya diinput dosen pengampu, nilai di luar rentang yang sah ditolak, KHS hanya menampilkan nilai yang sudah dipublikasikan, dan data mahasiswa hanya dihapus bila  tidak memiliki data akademik aktif.
9	| Penelaahan 12 tabel studi kasus LAB menemukan beberapa langkah yang tidak sesuai kaidah kolom, yaitu pada tabel UC04, UC11, dan UC12.
10	| Pemeriksaan akhir meliputi checklist C.4, kesesuaian nama, ID, dan aktor dengan diagram P04, kesamaan isi berkas .md dengan .drawio, diagram P04 yang tidak diubah, serta konfirmasi arah panah Ubah Data Mahasiswa pada diagram.
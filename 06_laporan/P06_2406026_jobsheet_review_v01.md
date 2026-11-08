No	|                                                                   Kesimpulan
-----------------------------------------------------------------------------------------------------------------------------------------
1	| Pertemuan 6 berfokus pada penggambaran satu activity diagram utuh Input Nilai Mata Kuliah sampai Lihat KHS dari tabel skenario SIA-UC08 dan SIA-UC09 Pertemuan 5; diagram Pertemuan 4 hanya menjadi acuan nama aktor dan tidak diubah.
2	| Diagram memakai empat swimlane, yaitu Dosen, Sistem, Admin Akademik, dan Mahasiswa, dan setiap action ditempatkan pada swimlane aktornya.
3	| Diagram memiliki tepat satu initial node dan tepat satu activity final node.
4	| Alur utama mengikuti langkah SIA-UC08 dari membuka fungsi Input Nilai Mata Kuliah sampai Sistem menyimpan nilai dan menampilkan konfirmasi, bergantian antara swimlane Dosen dan Sistem.
5	| Decision Nilai sudah lengkap memiliki guard [lengkap] dan [belum lengkap]; cabang [belum lengkap] menuju Dosen untuk melengkapi nilai, lalu bergabung kembali melalui merge sebelum pengesahan.
6	| Setelah Admin Akademik mengesahkan nilai, Sistem menyiapkan publikasi, lalu fork membagi alur menjadi Menerbitkan KHS pada portal akademik dan Mengirim pemberitahuan hasil studi, yang disatukan oleh join sebelum Mahasiswa melihat KHS.
7	| Langkah SIA-UC09 Lihat KHS diringkas menjadi satu action Melihat KHS pada swimlane Mahasiswa.
8	| Action pengesahan oleh Admin Akademik, penyiapan publikasi, pengiriman pemberitahuan, dan decision kelengkapan nilai berasal dari ketentuan jobsheet, bukan dari tabel skenario Pertemuan 5.
9	| Pemeriksaan dosen pengampu dan rentang nilai yang sah tetap digambar sebagai action; cabang penolakannya tidak digambar karena di luar cakupan tugas.
10	| Pemeriksaan akhir meliputi checklist C.4 (kelengkapan guard, pasangan fork dan join, kesesuaian swimlane dengan aktor), penyimpanan berkas P06_SIA_activity_v01.drawio pada folder 04_model_analisis/P06/SIA, dan ekspor PNG dengan nama yang sama.
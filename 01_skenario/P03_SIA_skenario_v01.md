Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan. 

ID       |          Kebutuhan tugas 
-----------------------------------------------------------------------------------------------
SIA-R01  | Mahasiswa dapat melihat jadwal kuliah 
SIA-R02  | Admin akademik dapat mengelola jadwal kuliah 
SIA-R03  | Mahasiswa dapat mengajukan KRS 
SIA-R04  | Sistem memvalidasi KRS sebagai bagian pengajuan 
SIA-R05  | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan 
SIA-R06  | Dosen wali dapat memproses persetujuan atau penolakan KRS 

Batas dan asumsi: 
• Pengguna telah terautentikasi. 
• Data mata kuliah, prasyarat, dan jadwal tersedia. 
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan. 
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan. 
• KRS tersimpan belum berarti disetujui. 
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas. 

  Aktor                |          Kebutuhan tugas 
-----------------------------------------------------------------------------------------------
Mahasiswa              | Mahasiswa dapat melihat  jadwal kuliah, mengajukan KRS, mengunduh bukti jika memilihnya pada konfirmasi pengajuan
Admin akademik         | dapat mengelola jadwal kuliah 
Dosen wali             | dapat memproses persetujuan atau penolakan KRS 

Identifikasi Aktor dan Use Case SIA :
ID         |Nama Use Case                  |Peran dalam Model
-----------------------------------------------------------------------------------
SIA-R01    |Melihat Jadwal Kuliah          |Fungsi utama mahasiswa
SIA-R02    |Mengelola Jadwal Kuliah        |Fungsi utama admin akademik
SIA-R03    |Mengajukan KRS                 |Fungsi utama mahasiswa
SIA-R04    |Memvalidasi KRS                |Perilaku yang disertakan di SIA-R03
SIA-R05    |Mengunduh Bukti Pengajuan      |Tambahan bersyarat (extend) pada SIA-R03
SIA-R06    |Menyetujui / Menolak KRS       |Fungsi utama dosen wali


Tetapkan Relasi : 
  Sumber               |          Hubungan        |    Tujuan   
-----------------------------------------------------------------------------------------------
Mahasiswa              | Asosiasi                 |  SIA-R01
Mahasiswa              | Asosiasi                 |  SIA-R03
Mahasiswa              | Asosiasi                 |  SIA-R05
Admin Akademik         | Asosiasi                 |  SIA-R02
Dosen wali             | Asosiasi                 |  SIA-R06

Keputusan Pemodelan :
 Sumber                |          Hubungan        |    Tujuan   |    Alasan
-----------------------------------------------------------------------------------------------
SIA-R03                | <<include>>              |  SIA-R04    | pemeriksaan menjadi bagian validasi pengajuan KRS.
SIA-R05                | <<extend>>               |  SIA-R03    | Extension point: Bukti pengajuan tersedia.
                                                                  Kondisi: [mahasiswa memilih cetak].
                                                                  Alasan: pengajuan tetap berhasil tanpa pencetakan.

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

Deskripsi Use Case : 
1. SIA-R03 — Mengajukan KRS
    Tujuan                 : Menghasilkan pengajuan KRS yang tersimpan di sistem.
    Aktor Utama            : Mahasiswa
    Sumber Kebutuhan       : SIA-R03 dan SIA-R04
    Pemicu                 : Mahasiswa memilih fungsi pengajuan KRS.
    Prasyarat              : - Mahasiswa telah terautentikasi 
                             - Jadwal kuliah tersedia.
    Pascakondisi Berhasil  : Pengajuan KRS berhasil tersimpan dan dapat diproses oleh dosen wali.
    Pascakondisi Gagal     : Pengajuan KRS tidak tersimpan apabila validasi gagal.
    Relasi Use Case        : - Include : SIA-R04 — Memvalidasi KRS.
                             - Extend  : SIA-R05 — Mengunduh Bukti Pengajuan, jika mahasiswa memilih opsi unduh.
    Extension Point        : Bukti pengajuan tersedia setelah pengajuan berhasil dikonfirmasi.

2. SIA-R04 — Memvalidasi KRS
    Tujuan                 : Memastikan pengajuan KRS memenuhi aturan akademik yang berlaku.
    Aktor Utama            : Sistem
    Sumber Kebutuhan       : SIA-R04
    Pemicu                 : Mahasiswa mengajukan KRS melalui SIA-R03.
    Prasyarat              : Mahasiswa telah mengisi data KRS yang akan diajukan.
    Pascakondisi Berhasil  : KRS dinyatakan valid dan proses pengajuan dapat dilanjutkan.
    Pascakondisi Gagal     : Sistem menampilkan informasi kesalahan validasi dan pengajuan tidak dilanjutkan sampai kesalahan diperbaiki.
    Relasi Use Case        : - Include : Dipanggil oleh SIA-R03 — Mengajukan KRS.
                             - Extend  : Tidak ada.
    Alur Alternatif        : Jika validasi gagal, sistem menampilkan alasan kegagalan dan mahasiswa dapat memperbaiki data KRS.

3. SIA-R05 — Mengunduh Bukti Pengajuan KRS
    |          Elemen         |          SIA-R05 — Mengunduh Bukti Pengajuan KRS                                                                     |
    ------------------------------------------------------------------------------------------------------------------------------------------------ |
    | Tujuan                  | Menyediakan bukti pengajuan KRS yang dapat diunduh oleh mahasiswa setelah pengajuan berhasil.                        |
    | Aktor Utama             | Mahasiswa                                                                                                            |
    | Sumber Kebutuhan        | SIA-R05                                                                                                              |
    | Pemicu                  | Mahasiswa memilih opsi unduh bukti setelah pengajuan KRS berhasil divalidasi dan dikonfirmasi.                       |
    | Prasyarat               | Pengajuan KRS telah lolos validasi, berhasil disimpan, dan bukti pengajuan tersedia.                                 |
    | Pascakondisi Berhasil   | Bukti pengajuan KRS berhasil diunduh oleh mahasiswa, sedangkan data pengajuan tetap tersimpan di sistem.             |
    | Pascakondisi Gagal      | Sistem menampilkan informasi bahwa bukti pengajuan gagal diunduh. Data pengajuan KRS tetap tersimpan.                |
    | Relasi Use Case         | SIA-R03 — Mengajukan KRS, jika pengajuan berhasil dan mahasiswa memilih opsi unduh bukti.                            |
    | Alur Alternatif 1       | Jika mahasiswa tidak memilih opsi unduh bukti, proses pengajuan KRS tetap selesai tanpa menjalankan SIA-R05.         |
    | Alur Alternatif 2       | Jika validasi KRS gagal, pengajuan tidak dilanjutkan sebagai pengajuan berhasil dan opsi unduh bukti tidak tersedia. |
    | Include                 | Tidak ada.                                                                                                           |

4. SIA-R06 — Memproses Keputusan KRS
    Tujuan                 : Memproses keputusan persetujuan atau penolakan pengajuan KRS mahasiswa.
    Aktor Utama            : Dosen Wali
    Sumber Kebutuhan       : SIA-R06
    Pemicu                 : Dosen wali memilih pengajuan KRS mahasiswa untuk diproses.
    Prasyarat              : Dosen wali telah terautentikasi dan pengajuan KRS tersedia untuk diperiksa.
    Pascakondisi Berhasil  : Keputusan dosen wali tersimpan di sistem dan status pengajuan diperbarui menjadi Disetujui atau Ditolak.
    Pascakondisi Gagal     : Keputusan tidak tersimpan dan status pengajuan tetap seperti sebelumnya.
    Relasi Use Case        : - Include : Tidak ada.
                             - Extend  : Tidak ada.
    Alur Alternatif        : - Disetujui : Dosen wali menyetujui KRS, sistem menyimpan keputusan dan memperbarui status menjadi Disetujui.
                             - Ditolak   : Dosen wali menolak KRS, sistem menyimpan keputusan dan memperbarui status menjadi Ditolak. Jika diperlukan, alasan penolakan dicatat agar mahasiswa dapat melakukan perbaikan.


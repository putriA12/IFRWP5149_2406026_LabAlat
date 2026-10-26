1. SIA-UC07 — Lihat Kalender Akademik
    Tujuan                 : Menyediakan informasi kalender akademik resmi kepada civitas akademika.
    Aktor Utama            : Civitas Akademika
    Sumber Kebutuhan       : SIA-R07
    Pemicu                 : Mahasiswa atau dosen memilih fungsi Lihat Kalender Akademik.
    Prasyarat              : Pengguna telah terautentikasi.
    Pascakondisi Berhasil  : Informasi kalender akademik resmi berhasil ditampilkan.
    Pascakondisi Gagal     : Kalender akademik tidak dapat ditampilkan dan sistem memberikan informasi kegagalan.
    Relasi Use Case        : Tidak ada.

2. SIA-UC08 — Input Nilai Mata Kuliah
    Tujuan                 : Memungkinkan dosen memasukkan nilai mahasiswa untuk mata kuliah yang diajarkannya.
    Aktor Utama            : Dosen
    Sumber Kebutuhan       : SIA-R08
    Pemicu                 : Dosen memilih fungsi Input Nilai Mata Kuliah setelah perkuliahan selesai.
    Prasyarat              : Dosen telah terautentikasi dan mengajar mata kuliah yang akan diinput nilainya.
    Pascakondisi Berhasil  : Nilai mahasiswa berhasil disimpan dan menunggu pengumuman resmi.
    Pascakondisi Gagal     : Nilai tidak berhasil disimpan apabila data tidak valid atau dosen tidak berwenang menginput nilai mata kuliah tersebut.
    Relasi Use Case        : Realization oleh SIA-CO01 — Input Nilai Mata Kuliah.
    Alur Alternatif        : Jika dosen bukan pengajar mata kuliah yang dipilih, sistem menolak proses input nilai. Jika nilai tidak sesuai rentang yang diperbolehkan, sistem menampilkan informasi kesalahan dan meminta dosen memperbaiki nilai.

3. SIA-UC09 — Lihat KHS
    Tujuan                 : Memungkinkan mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya telah diumumkan.
    Aktor Utama            : Mahasiswa
    Sumber Kebutuhan       : SIA-R09
    Pemicu                 : Mahasiswa memilih fungsi Lihat KHS dan menentukan semester yang ingin dilihat.
    Prasyarat              : Mahasiswa telah terautentikasi.
    Pascakondisi Berhasil  : KHS untuk semester yang dipilih ditampilkan dengan nilai yang telah diumumkan secara resmi.
    Pascakondisi Gagal     : KHS tidak dapat ditampilkan apabila data tidak tersedia atau terjadi kegagalan sistem.
    Relasi Use Case        : Realization oleh SIA-CO02 — Lihat KHS.
    Alur Alternatif        : Jika nilai semester belum diumumkan secara resmi, KHS untuk semester tersebut belum tersedia untuk ditampilkan.

4. SIA-UC10 — Kelola Data Mahasiswa
    
Tujuan                 : Memungkinkan admin akademik mengelola data mahasiswa melalui fungsi tambah, ubah, dan hapus data.
Aktor Utama            : Admin Akademik
Sumber Kebutuhan       : SIA-R10 dan SIA-R11
Pemicu                 : Admin akademik memilih fungsi Kelola Data Mahasiswa.
Prasyarat              : Admin akademik telah terautentikasi dan memiliki hak akses pengelolaan data mahasiswa.
Pascakondisi Berhasil  : Data mahasiswa berhasil ditambah, diubah, atau dihapus sesuai tindakan yang dipilih.
Pascakondisi Gagal     : Pengelolaan data tidak berhasil dilakukan apabila data tidak valid atau tindakan tidak memenuhi ketentuan.
Relasi Use Case        : Generalization:
                         - SIA-UC11 — Tambah Data Mahasiswa.
                         - SIA-UC12 — Ubah Data Mahasiswa.
                         - SIA-UC13 — Hapus Data Mahasiswa.

5. SIA-UC11 — Tambah Data Mahasiswa
    Tujuan                 : Menambahkan data mahasiswa baru ke dalam sistem informasi akademik.
    Aktor Utama            : Admin Akademik
    Sumber Kebutuhan       : SIA-R11
    Pemicu                 : Admin akademik memilih fungsi Tambah Data Mahasiswa.
    Prasyarat              : Admin akademik telah terautentikasi dan memiliki hak akses untuk menambahkan data mahasiswa.
    Pascakondisi Berhasil  : Data mahasiswa baru berhasil disimpan dalam sistem.
    Pascakondisi Gagal     : Data mahasiswa tidak tersimpan apabila data tidak lengkap, tidak valid, atau terjadi duplikasi sesuai aturan sistem.
    Relasi Use Case        : Generalization dari SIA-UC10 — Kelola Data Mahasiswa.

6. SIA-UC12 — Ubah Data Mahasiswa
    Tujuan                 : Memperbarui data mahasiswa yang telah tersimpan dalam sistem informasi akademik.
    Aktor Utama            : Admin Akademik
    Sumber Kebutuhan       : SIA-R11
    Pemicu                 : Admin akademik memilih data mahasiswa dan menjalankan fungsi Ubah Data Mahasiswa.
    Prasyarat              : Admin akademik telah terautentikasi, memiliki hak akses, dan data mahasiswa yang akan diubah tersedia.
    Pascakondisi Berhasil  : Perubahan data mahasiswa berhasil disimpan.
    Pascakondisi Gagal     : Perubahan tidak tersimpan apabila data tidak valid atau proses pembaruan mengalami kegagalan.
    Relasi Use Case        : Generalization dari SIA-UC10 — Kelola Data Mahasiswa.

7. SIA-UC13 — Hapus Data Mahasiswa
    Tujuan                 : Menghapus data mahasiswa dari sistem sesuai ketentuan pengelolaan data akademik.
    Aktor Utama            : Admin Akademik
    Sumber Kebutuhan       : SIA-R11
    Pemicu                 : Admin akademik memilih data mahasiswa dan menjalankan fungsi Hapus Data Mahasiswa.
    Prasyarat              : Admin akademik telah terautentikasi, memiliki hak akses, dan data mahasiswa yang akan dihapus tersedia.
    Pascakondisi Berhasil  : Data mahasiswa berhasil dihapus apabila memenuhi ketentuan penghapusan.
    Pascakondisi Gagal     : Data mahasiswa tidak dihapus apabila masih memiliki data akademik aktif.
    Relasi Use Case        : Generalization dari SIA-UC10 — Kelola Data Mahasiswa.
    Alur Alternatif        : Jika mahasiswa masih memiliki data akademik aktif, sistem menolak penghapusan dan memberikan informasi kepada admin akademik.



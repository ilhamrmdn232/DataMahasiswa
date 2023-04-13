# Tugas Pemrograman Mobile 2
## Profile
<body>
    <table border="1">
        <tr>
            <th> Nama</th>
            <th>NIM</th>
            <th>Kelas</th>
        </tr>
        <tr>
            <td>Ilham Ramadhan</td>
            <td>312110609</td>
            <td>TI.21.A.1</td>
        </tr>
    </table>
</body>

## Beginning
## Latihan 1

![Latihan 1](img/lat1.png)

### Penjelasan
<p>Program data Absensi Mahasiswa tsb diambil dari URL https://tifupb.id/data dengan JSON dan ditampilkan nya dalam bentuk tabel.
</p>

- Baris pertama <?php merupakan tag pembuka untuk mengawali kode PHP.
- Baris kedua mendefinisikan variabel $url dengan nilai 'https://tifupb.id/data'. Variabel tsb akan digunakan untuk menyimpan alamat URL dari data yang akan diambil.
- Baris ketiga menggunakan fungsi file_get_contents() untuk mengambil isi dari URL yang tersimpan pada variabel $url dan kemudian disimpan dalam variabel $data.
- Baris keempat menggunakan fungsi json_decode() untuk mengubah format data dari JSON ke dalam bentuk array PHP. Hasilnya kemudian disimpan dalam variabel $mahasiswa.
- Baris keenam hingga baris ke-16 adalah kode HTML yang akan menampilkan data dalam bentuk tabel.
- Baris kesepuluh hingga baris ke-14 adalah bagian dari kode HTML yang akan menampilkan header tabel dengan dua kolom yaitu "No." dan "Nama".
- Baris ke-15 mendefinisikan variabel $no dengan nilai 1 yang akan digunakan untuk menampilkan nomor urut pada setiap data mahasiswa.
- Baris ke-16 hingga baris ke-23 menggunakan perulangan foreach untuk menampilkan data mahasiswa dalam bentuk tabel. Setiap item data mahasiswa diambil dari variabel $mahasiswa dan diakses dengan indeks 'Nama'. Kemudian data tersebut akan ditampilkan dalam satu baris tabel dengan nomor urut yang diincrement setiap kali menampilkan data mahasiswa baru.
- Baris ke-24 menutup perulangan foreach.
- Baris terakhir </html> menandakan akhir dari dokumen HTML.
- Baris terakhir ?> merupakan tag penutup untuk mengakhiri kode PHP.

## Next
## Latihan 2

![Latihan 2](img/lat2.png)

### Penjelasan
<p>Program latihan 2 diatas adalah sebuah skrip PHP yang sudah dipercantik menggunakan CSS dan digunakan untuk menampilkan data mahasiswa beserta detail absensi dari URL https://tifupb.id/tugas1. Berikut penjelasan untuk setiap bagian dari kode tersebut:</p>

- Variabel $url diinisialisasi dengan URL tempat data absensi disimpan.
- Kemudian, fungsi file_get_contents() digunakan untuk membaca seluruh konten dari URL tersebut. Hasilnya disimpan dalam variabel $data.
- Lalu, fungsi json_decode() digunakan untuk mengubah data dalam format JSON menjadi array PHP yang dapat lebih mudah ditampilkan. Hasilnya disimpan dalam variabel $absensi.
- Variabel $total_absensi diinisialisasi dengan panjang array $absensi.
- Variabel $data_per_halaman diinisialisasi dengan jumlah data yang akan ditampilkan per halaman.
- Variabel $total_halaman diinisialisasi dengan jumlah halaman yang dibutuhkan untuk menampilkan seluruh data. Hal ini dihitung dengan menggunakan fungsi ceil() untuk membulatkan hasil dari $total_absensi / $data_per_halaman.
- Variabel $page diinisialisasi dengan angka halaman yang diminta pengguna. Jika halaman tidak ditentukan, maka $page diisi dengan angka 1.
- Variabel $start_index diinisialisasi dengan indeks data pertama yang akan ditampilkan pada halaman tersebut.
- Variabel $end_index diinisialisasi dengan indeks data terakhir yang akan ditampilkan pada halaman tersebut.
- Selanjutnya, skrip PHP beralih ke bagian HTML, di mana sebuah tabel digunakan untuk menampilkan data mahasiswa beserta detail absensi mereka.
- Bagian awal tabel terdiri dari caption yang memberikan informasi tentang jenis data yang ditampilkan (yaitu data mahasiswa).
- Baris header tabel (thead) terdiri dari kolom-kolom yang akan menampilkan informasi tentang NIM, nama, dan status kehadiran pada setiap sesi perkuliahan.
- Baris isi tabel (tbody) akan menampilkan data mahasiswa yang diambil dari variabel $absensi. Untuk menampilkan data pada setiap kolom, dilakukan iterasi dari $start_index sampai $end_index. Jika indeks data yang ingin ditampilkan melebihi jumlah data absensi yang tersedia, maka iterasi dihentikan.
- Pada bagian "Action" kolom, terdapat tombol "Lihat Detail" yang akan menampilkan detail absensi mahasiswa tertentu ketika diklik.
- Setelah selesai menampilkan data pada tabel, dilakukan penambahan navigasi halaman yang terdiri dari beberapa halaman. Setiap halaman direpresentasikan oleh sebuah angka dan link ke halaman tersebut.
- Tombol navigasi terdiri dari tombol untuk menuju halaman pertama, tombol untuk menuju halaman sebelumnya, tombol untuk menuju halaman berikutnya, dan tombol untuk menuju halaman terakhir. Tombol navigasi tersebut akan di-generate secara dinamis dengan menggunakan iterasi for.


## Done

# Terima Kasih
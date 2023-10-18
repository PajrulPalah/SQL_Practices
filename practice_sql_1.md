# SQL_Practices
## Belajar kasus SQL
Buat Database Siswa Buat tabel data siswa, tabel data pelajaran, table data nilai Isi masing-masing tabel dengan Data Dummy
Buat query untuk menampilkan laporan rata-rata nilai setiap pelajaran
Buat query untuk menampilkan laporan siapa siswa yang mendapatkan nilai tertinggi untuk setiap pelajaran

Langkah-langkah penyelesaian
langkah 1 membuat nama data base dengan nama " db_siswa_sd"

```{r}
CREATE DATABASE db_siswa_sd;
```
langkah selanjutnya adalah membuat tabel
tabel yang pertama adalah tabel data siswa

```{r}
CREATE TABLE data_siswa (
    id_siswa INTEGER PRIMARY KEY,
    nama_siswa text not null,
    jenis_kelamin text not null,
    alamat text not null,
    tahun_lahir text not null,
    tahun_masuk text not null,
    nama_kelas text not null
);
```

Memasukkan data siswa ke dalam tabel data_siswa 
ada sebanyak 30 data siswa yang terdiri dari id_siswa, nama_siswa, jenis_kelamin, alamat, tahun_lahir, tahun_masuk, nama_kelas)
```{r}
INSERT INTO data_siswa (id_siswa, nama_siswa, jenis_kelamin, alamat, tahun_lahir, tahun_masuk, nama_kelas) VALUES
    (11001, 'Budi Susanto', 'Laki-Laki', 'Kabupaten Cianjur', 2002, 2008, 'Kelas A'),
    (11002, 'Siti Rahmawati', 'Perempuan', 'Kabupaten Bogor', 2001, 2008, 'Kelas B'),
    (11003, 'Agus Prabowo', 'Laki-Laki', 'Kabupaten Karawang', 2003, 2008, 'Kelas C'),
    (11004, 'Rina Fitriani', 'Perempuan', 'Kabupaten Cianjur', 2002, 2008, 'Kelas B'),
    (11005, 'Dian Purnomo', 'Laki-Laki', 'Kabupaten Bogor', 2001, 2008, 'Kelas A'),
    (11006, 'Lina Sari', 'Perempuan', 'Kabupaten Karawang', 2003, 2008, 'Kelas C'),
    (11007, 'Joko Santoso', 'Laki-Laki', 'Kabupaten Cianjur', 2001, 2008, 'Kelas A'),
    (11008, 'Maya Indah', 'Perempuan', 'Kabupaten Bogor', 2002, 2008, 'Kelas B'),
    (11009, 'Adi Nugroho', 'Laki-Laki', 'Kabupaten Karawang', 2003, 2008, 'Kelas C'),
    (11010, 'Nurul Hidayah', 'Perempuan', 'Kabupaten Cianjur', 2001, 2008, 'Kelas A'),
    (11011, 'Heri Saputra', 'Laki-Laki', 'Kabupaten Bogor', 2002, 2008, 'Kelas B'),
    (11012, 'Sari Dewi', 'Perempuan', 'Kabupaten Karawang', 2003, 2008, 'Kelas C'),
    (11013, 'Iwan Setiawan', 'Laki-Laki', 'Kabupaten Cianjur', 2002, 2008, 'Kelas B'),
    (11014, 'Rika Wulandari', 'Perempuan', 'Kabupaten Bogor', 2001, 2008, 'Kelas C'),
    (11015, 'Andi Kurniawan', 'Laki-Laki', 'Kabupaten Karawang', 2003, 2008, 'Kelas A'),
    (11016, 'Yuli Sari', 'Perempuan', 'Kabupaten Cianjur', 2001, 2008, 'Kelas A'),
    (11017, 'Wahyu Prasetyo', 'Laki-Laki', 'Kabupaten Bogor', 2002, 2008, 'Kelas B'),
    (11018, 'Rini Anggraeni', 'Perempuan', 'Kabupaten Karawang', 2003, 2008, 'Kelas C'),
    (11019, 'Arif Wijaya', 'Laki-Laki', 'Kabupaten Cianjur', 2002, 2008, 'Kelas A'),
    (11020, 'Nia Utami', 'Perempuan', 'Kabupaten Bogor', 2001, 2008, 'Kelas B'),
    (11021, 'Denny Hartono', 'Laki-Laki', 'Kabupaten Karawang', 2003, 2008, 'Kelas A'),
    (11022, 'Siti Aminah', 'Perempuan', 'Kabupaten Cianjur', 2001, 2008, 'Kelas C'),
    (11023, 'Hadi Suryanto', 'Laki-Laki', 'Kabupaten Bogor', 2002, 2008, 'Kelas B'),
    (11024, 'Dewi Nurul', 'Perempuan', 'Kabupaten Karawang', 2003, 2008, 'Kelas C'),
    (11025, 'Mulyono Putra', 'Laki-Laki', 'Kabupaten Cianjur', 2001, 2008, 'Kelas A'),
    (11026, 'Yuli Astuti', 'Perempuan', 'Kabupaten Bogor', 2002, 2008, 'Kelas B'),
    (11027, 'Dedi Suhendar', 'Laki-Laki', 'Kabupaten Karawang', 2003, 2008, 'Kelas B'),
    (11028, 'Lia Damayanti', 'Perempuan', 'Kabupaten Cianjur', 2002, 2008, 'Kelas B'),
    (11029, 'Bayu Pranoto', 'Laki-Laki', 'Kabupaten Bogor', 2001, 2008, 'Kelas A'),
    (11030, 'Rina Widiastuti', 'Perempuan', 'Kabupaten Karawang', 2003, 2008, 'Kelas C');
```

langkah kedua adalah membuat tabel data mata pelajaran 
yang terdiri dari mata_pelajaran dan jumlah_jam
 
```{r}
CREATE TABLE data_pelajaran (
    mata_pelajaran text not null,
    jumlah_jam text not null
);
```

Mengisi tabel data pelajaran
```{r}
INSERT INTO data_pelajaran (mata_pelajaran, jumlah_jam)
VALUES
    ('Matematika', '120 Menit'),
    ('IPA', '120 Menit'),
    ('IPS', '80 Menit'),
    ('Bahasa Indonesia', '80'),
    ('Seni Budaya', '40 Menit');
 ```   
 
 Langkah ke 3 adalah membuat tabel data nilai siswa
```{r}  
CREATE TABLE data_nilai (
    id_siswa Integer Primary key ,
    matematika INT,
    bahasa_indonesia INT,
    ipa INT,
    ips INT,
    seni_budaya INT
);
```

selanjutnya adalah memasukan data nilai siswa berdasarkan mata pelajaran dan id siswa
masukkan data nilai untuk 30 siswa
```{r}
INSERT INTO data_nilai (id_siswa, matematika, bahasa_indonesia, ipa, ips, seni_budaya)
VALUES
    (11001, 70, 75, 60, 90, 80),
    (11002, 85, 65, 88, 72, 70),
    (11003, 75, 80, 70, 78, 85),
    (11004, 92, 68, 77, 82, 75),
    (11005, 88, 70, 90, 68, 79),
    (11006, 76, 82, 89, 74, 91),
    (11007, 70, 75, 60, 90, 80),
    (11008, 85, 65, 88, 72, 70),
    (11009, 75, 80, 70, 78, 85),
    (11010, 92, 68, 77, 82, 75),
    (11011, 88, 70, 90, 68, 79),
    (11012, 76, 82, 89, 74, 91),
    (11013, 70, 75, 60, 90, 80),
    (11014, 85, 65, 88, 72, 70),
    (11015, 75, 80, 70, 78, 85),
    (11016, 92, 68, 77, 82, 75),
    (11017, 88, 70, 90, 68, 79),
    (11018, 76, 82, 89, 74, 91),
    (11019, 70, 75, 60, 90, 80),
    (11020, 85, 65, 88, 72, 70),
    (11021, 75, 80, 70, 78, 85),
    (11022, 92, 68, 77, 82, 75),
    (11023, 88, 70, 90, 68, 79),
    (11024, 76, 82, 89, 74, 91),
    (11025, 70, 75, 60, 90, 80),
    (11026, 85, 65, 88, 72, 70),
    (11027, 75, 80, 70, 78, 85),
    (11028, 92, 68, 77, 82, 75),
    (11029, 88, 70, 90, 68, 79),
    (11030, 76, 82, 89, 74, 91);
```

Menggabungkah tabel data siswa dan tabel data nilai
```{r}   
   SELECT 
    ds.id_siswa,
    ds.nama_siswa,
    ds.jenis_kelamin,
    ds.alamat,
    ds.tahun_lahir,
    ds.tahun_masuk,
    ds.nama_kelas,
    dn.matematika,
    dn.bahasa_indonesia,
    dn.ipa,
    dn.ips,
    dn.seni_budaya
FROM data_siswa ds
JOIN data_nilai dn ON ds.id_siswa = dn.id_siswa;
```

mencari nilai maximum dari setiap mata pelajatan
```{r}
SELECT
    MAX(matematika) AS nilai_tertinggi_matematika,
    MAX(bahasa_indonesia) AS nilai_tertinggi_bahasa_indonesia,
    MAX(ipa) AS nilai_tertinggi_ipa,
    MAX(ips) AS nilai_tertinggi_ips,
    MAX(seni_budaya) AS nilai_tertinggi_seni_budaya
FROM data_nilai;
```

mencari rata-rata nilai dari setiap mata pelajaran 
```{r}
SELECT
    AVG(matematika) AS rata_rata_matematika,
    AVG(bahasa_indonesia) AS rata_rata_bahasa_indonesia,
    AVG(ipa) AS rata_rata_ipa,
    AVG(ips) AS rata_rata_ips,
    AVG(seni_budaya) AS rata_rata_seni_budaya
FROM data_nilai
```

Mengurutkan nilai tertinggi dan rata-rata setiap mata pelajaran
```{r}
SELECT
    ds.id_siswa,
    ds.nama_siswa, 
    ds.jenis_kelamin,
    dn.matematika,
    dn.bahasa_indonesia,
    dn.ipa,
    dn.ips,
    dn.seni_budaya,
    (dn.matematika + dn.bahasa_indonesia + dn.ipa + dn.ips + dn.seni_budaya) / 5 as rata_rata_nilai
FROM data_siswa ds
JOIN data_nilai dn ON ds.id_siswa = dn.id_siswa
ORDER BY rata_rata_nilai DESC;
```

mencari nilai tertinggi dari setiap mata pelajaran
pelajaran matematika 
```{r}
select 
ds.id_siswa,
ds.nama_siswa,
ds.jenis_kelamin,
ds.alamat,
dn.matematika as top_nilai_matematika
from data_siswa ds 
join data_nilai dn on ds.id_siswa = dn.id_siswa 
order by top_nilai_matematika desc
limit 5;
```

mencari jumlah perempuan
```{r}
select 
count(jenis_kelamin) as total_jenis_perempuan
from data_siswa
where jenis_kelamin = 'Perempuan';
```

mencari jumlah laki-laki 
```{r}
select
count(jenis_kelamin) as total_jenis_laki_laki
from data_siswa
where jenis_kelamin ='Laki-Laki';
```

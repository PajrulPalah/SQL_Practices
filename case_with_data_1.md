
# SQL FOR Data Analysis Case 1
## Query Analisis Data

Berikut adalah beberapa query analisis data menggunakan SQL:

1. **Total Harga per Kode di SAC:** Ambil total harga untuk setiap 'kode' di kota 'SAC' dan urutkan berdasarkan 'kode' dari yang terawal hingga yang terakhir.

2. **Total Keuntungan per Kota:** Hitung total keuntungan untuk setiap 'kota' dan urutkan dari total harga tertinggi ke terendah.

3. **Rata-rata Harga per Kaki Persegi di SAC:** Hitung rata-rata harga properti per kaki persegi untuk setiap 'kode' di kota 'SAC' menggunakan fungsi window dan bulatkan ke 0 desimal.

4. **5 Kode Teratas di SAC:** Berdasarkan query pada poin 3, dapatkan 5 nilai 'kode' di kota 'SAC' dengan rata-rata harga properti per kaki persegi tertinggi.

5. **Rata-rata Harga per Kamar Tidur:** Hitung rata-rata harga properti per kamar tidur untuk setiap 'tipe' dan 'kode' di kota 'CHO'.

Jika ingin belajar pakai dataset langsung bisa link berikut:

Tapi Request dulu ya
[Link ke Dokumen Google Sheets](https://docs.google.com/spreadsheets/d/1SAYrh4oL0S1UuwqkPXmZcwIhGPMzmM2YZ9176qHEChk/edit#gid=0)


```(r)
-- 1. Ambil data total price di masing-masing code di kota SAC kemudian urutkan berdasarkan code paling awal hingga akhir.
SELECT code, SUM(price) AS total_price
FROM `property_dataset.transakasi_properti`
WHERE city = 'SAC'
GROUP BY code
ORDER BY code;

-- 2. Ambil data total profit di masing-masing city kemudian urutkan berdasarkan total price tertinggi ke terendah.
SELECT city, SUM(price) AS total_price
FROM `property_dataset.transakasi_properti`
GROUP BY city
ORDER BY total_price DESC;

-- 3. Hitunglah rata-rata harga properti per square feet di masing code di kota SAC menggunakan window function dan bulatkan menjadi 0 angka di belakang koma (0 desimal).
SELECT city, code, ROUND(AVG(price / sq__ft), 0) AS avg_price_per_sqft
FROM `property_dataset.transakasi_properti`
WHERE city = 'SAC'
GROUP BY city, code;

-- 4. Dari query pada poin c, dapatkan 5 code di kota SAC dengan rata-rata harga properti per square feet paling tinggi.
WITH AvgPricePerSqft AS (
    SELECT city, code, ROUND(AVG(price / sq__ft), 0) AS avg_price_per_sqft
    FROM `property_dataset.transakasi_properti`
    WHERE city = 'SAC'
    GROUP BY city, code
)
SELECT city, code, avg_price_per_sqft
FROM AvgPricePerSqft
ORDER BY avg_price_per_sqft DESC
LIMIT 5;

-- 5. Hitunglah rata-rata harga properti per kasur tidur di masing-masing tipe properti, di masing-masing code, di kota CHO.
SELECT city, code, type, beds, AVG(price / beds) AS avg_price_per_bedroom
FROM `property_dataset.transakasi_properti`
WHERE city = 'CHO'
GROUP BY city, code, type, beds;

-- ternyata ketika perhitungan kita menemukan angka nol pada tabel
-- langkah selanjutnya adalah mencari data yang terdapat angka nol pada tabel
SELECT *
FROM `property_dataset.transakasi_properti`
WHERE city = 'CHO' AND beds = 0 AND baths = 0 ;

-- sebelum kita menghapus kita memastikan bahwa ada ada di city CHO yang nilainya lebih dari 0 sehingga bisa dilakukan kalkulasi
SELECT *
FROM `property_dataset.transakasi_properti`
WHERE city = 'CHO' AND beds > 0 AND baths > 0 ;

-- oke ketika sudah dipastikan bahwa nilai dari setiap kolom tersebut lebih dari nol
-- langkah selanjutnya adalah mengitung nilai yang lebih dari nol saja untuk 
SELECT city, code, type, ROUND(AVG(price / beds),2) AS avg_price_per_bedroom
FROM `property_dataset.transakasi_properti`
WHERE city = 'CHO' AND beds > 0
GROUP BY city, code, type;
```

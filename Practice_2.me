# SQL Practices 2

## Belajar SQL Membuat Tabel Employee
```{r}
create table EMPLOYEE(
EmpId integer primary key,
firstname text not null,
lastname text not null,
dept text not null,
gender text not null,
birth date not null,
joinyear integer not null,
salId integer not null
);
```

Membuat tabel gaji karyawan
```{r}
CREATE TABLE SALARY (
  salId INTEGER PRIMARY KEY,
  cost INTEGER not null
);
```

Memasukan data pada tabel employee
```{r}
INSERT INTO EMPLOYEE VALUES (0004, 'Clark', 'Davidson', 'Sales', 'male', '1990-03-15', 2010, 2);
INSERT INTO EMPLOYEE VALUES (00014, 'Dave', 'Bokir', 'Accounting', 'male', '1993-08-12', 2010, 3);
INSERT INTO EMPLOYEE VALUES (0005, 'Ava', 'Christy','Sales', 'female', '1991-01-01', 2013, 3);
INSERT INTO EMPLOYEE VALUES (0001, 'Tejo', 'Sukejo', 'Chief','male', '1970-03-31', 2007, 1);
INSERT INTO EMPLOYEE VALUES (00010, 'Anna', 'Kharisma', 'Data', 'female', '2000-12-20', 2018, 3);
INSERT INTO EMPLOYEE VALUES (0006, 'Wasto', 'Hendra', 'Accounting', 'male', '1998-08-01', 2011, 3);
INSERT INTO EMPLOYEE VALUES (0008, 'Cinta', 'Mika', 'Accounting', 'female', '2000-05-14', 2018, 3);
INSERT INTO EMPLOYEE VALUES (0007, 'Stephen', 'Williyam', 'Data', 'male', '1998-06-18', 2009, 3);
INSERT INTO EMPLOYEE VALUES (0002, 'Nur', 'Setianingsih', 'Chief', 'female', '1971-12-09', 2007, 1);
INSERT INTO EMPLOYEE VALUES (0003, 'Stephanie', 'Anggara', 'Chief', 'female', '1975-09-28', 2007, 1);
INSERT INTO EMPLOYEE VALUES (00015, 'Saleh', 'Al-Baraq', 'Sales', 'male', '1999-08-09', 2016, 3);
INSERT INTO EMPLOYEE VALUES (0009, 'Yujii', 'Akatora', 'Legal', 'male', '2000-04-16', 2017, 3);
INSERT INTO EMPLOYEE VALUES (00012, 'Fuka', 'Atambwaba', 'Legal', 'female', '1987-10-25', 2010, 2);
INSERT INTO EMPLOYEE VALUES (00013, 'Alana', 'Von Zeuckjer', 'Data', 'female', '1990-11-10', 2011, 2);
INSERT INTO EMPLOYEE VALUES (00011, 'Bucky', 'Black', 'Accounting', 'male', '2001-04-21', 2020, 4);
```

memasukan data pada tabel gaji/salary
```{r}
INSERT INTO SALARY VALUES (1, 20000000);
INSERT INTO SALARY VALUES (2, 15000000);
INSERT INTO SALARY VALUES (3, 10000000);
INSERT INTO SALARY VALUES (4, 5000000);
```

Berikut adalah contoh-contoh query SQL yang menggunakan beberapa fitur dan klausa yang telah Anda sebutkan:

1. Menggunakan GROUP BY Clause:

Menampilkan jumlah karyawan per departemen.
```{r}
SELECT dept, COUNT(*) as jumlah_karyawan
FROM EMPLOYEE
GROUP BY dept;
```
2. Menggunakan HAVING Clause:

Menampilkan departemen yang memiliki lebih dari 2 karyawan.
```{r}
SELECT dept, COUNT(*) as jumlah_karyawan
FROM EMPLOYEE
GROUP BY dept
HAVING COUNT(*) > 2;
```
3. Menggunakan CASE WHEN:
Menampilkan nama karyawan beserta status gaji berdasarkan besaran gaji.
```{r}
SELECT firstname, lastname,
    CASE
        WHEN SALARY.cost > 15000000 THEN 'Tinggi'
        WHEN SALARY.cost > 10000000 THEN 'Sedang'
        ELSE 'Rendah'
    END AS status_gaji
FROM EMPLOYEE
INNER JOIN SALARY ON EMPLOYEE.salId = SALARY.salId;
```

4. Menggunakan Views:

Membuat view yang menggabungkan data karyawan dan data gaji.
```{r}
CREATE VIEW EmployeeSalary AS
SELECT EMPLOYEE.*, SALARY.cost
FROM EMPLOYEE
INNER JOIN SALARY ON EMPLOYEE.salId = SALARY.salId;
```
-- Kemudian, Anda dapat mengambil data dari view ini

```{r}
SELECT * FROM EmployeeSalary;
```

5. Menggunakan Functions (DATE, STRING, MATH):

Contoh penggunaan fungsi-fungsi date, string, dan math dalam query sangat bervariasi tergantung pada apa yang Anda ingin lakukan. Berikut adalah contoh yang menggunakan beberapa fungsi date:
Menampilkan nama karyawan dan tahun bergabung
```{r}
SELECT firstname, lastname, year(joinyear) as tahun_bergabung
FROM EMPLOYEE;
```

Menampilkan rata-rata umur karyawan
```{r}
SELECT AVG(YEAR(NOW()) - YEAR(birth)) as rata_rata_umur
FROM EMPLOYEE;
```
6 Menggunakan Inner join, Left Join, Right Join, dan Full Join
INNER JOIN:
Menampilkan daftar karyawan beserta informasi gaji mereka.
```{r}
SELECT EMPLOYEE.firstname, EMPLOYEE.lastname, SALARY.cost
FROM EMPLOYEE
INNER JOIN SALARY ON EMPLOYEE.salId = SALARY.salId;
```

LEFT JOIN:

Menampilkan semua departemen dan daftar karyawan di dalamnya, termasuk departemen yang tidak memiliki karyawan.
```{r}
SELECT DEPARTMENTS.dept, EMPLOYEE.firstname, EMPLOYEE.lastname
FROM DEPARTMENTS
LEFT JOIN EMPLOYEE ON DEPARTMENTS.dept = EMPLOYEE.dept;
```

RIGHT JOIN:

Menampilkan semua karyawan dan informasi gaji mereka, termasuk karyawan yang tidak memiliki gaji.
```{r}
SELECT EMPLOYEE.firstname, EMPLOYEE.lastname, SALARY.cost
FROM EMPLOYEE
RIGHT JOIN SALARY ON EMPLOYEE.salId = SALARY.salId;
```

FULL JOIN:

Menampilkan semua karyawan dan informasi gaji mereka, termasuk karyawan yang tidak memiliki gaji, serta semua data gaji yang tidak memiliki karyawan terkait.
```{r}
SELECT EMPLOYEE.firstname, EMPLOYEE.lastname, SALARY.cost
FROM EMPLOYEE
FULL JOIN SALARY ON EMPLOYEE.salId = SALARY.salId;
```

7. Menggunakan Functions 
Menggunakan fungsi YEAR untuk menampilkan tahun bergabung karyawan:
```{r}
SELECT firstname, lastname, YEAR(joinyear) AS tahun_bergabung
FROM EMPLOYEE;
```
Fungsi STRING:
Menggunakan fungsi CONCAT untuk menggabungkan kolom string:
```{r}
SELECT CONCAT(firstname, ' ', lastname) AS nama_lengkap
FROM EMPLOYEE;
```
Menggunakan fungsi UPPER untuk mengonversi teks menjadi huruf besar:
```{r}
SELECT firstname, UPPER(lastname) AS nama_belakang_huruf_besar
FROM EMPLOYEE;
```
Fungsi MATH
Menggunakan fungsi NOW untuk mendapatkan tanggal dan waktu saat ini:
```{r}
SELECT firstname, lastname, NOW() AS waktu_sekarang
FROM EMPLOYEE;
```







# **MODUL 2**

## A. PENGENALAN DATA MANIPULATION LANGUAGE
DML merupakan singkatan dari Data Manipulation Language. Ini merupakan subset dari SQL (Structured Query Language) dengan perintah utamanya yaitu SELECT, INSERT, DELETE, dan UPDATE yang digunakan untuk memodifikasi, memasukkan, memperbarui, dan menghapus data dalam basis data relasional. Perintah DML digunakan untuk berinteraksi dengan data yang disimpan dalam tabel basis data.
Perintah DML sangat penting untuk mengelola dan mempertahankan integrasi sebuah basis data. 
Dengan menggunakan perintah DML, pengguna dapat memastikan bahwa data yang disimpan dalam basis data akurat, terbaru, dan relevan dengan kebutuhan.

## B. PERINTAH PADA DATA MANIPULATION LANGUAGE 
### 1. SELECT
SELECT merupakan perintah DML yang digunakan untuk memilih dan 
menampilkan nilai yang ada pada tabel. 
Berikut merupakan syntax penulisan untuk perintah SELECT :
- **Menampilkan seluruh data** 
- **Menampilkan data pada kolom tertentu** 
- **Menampilkan data kondisi tertentu** 
- **Menampilkan data berdasarkan nilai yang berbeda saja**
- **Menampilkan data secara terurut**

Selain syntax di atas, terdapat beberapa command tambahan yang dapat ditambahkan pada perintah SELECT seperti berikut: 
- **Menggabungkan dan menampilkan dua kolom** 
- **Menampilkan kolom dengan nama lain**
- **Menyalin data dari satu tabel ke dalam tabel baru (insert into)**

### 2. INSERT
INSERT merupakan perintah DML yang digunakan untuk menambahkan data pada tabel. Berikut merupakan penulisan syntax pada perintah INSERT:
- **Menampilkan data dengan kolom dan nilai yang spesifik** 
- **Menambahkan data hanya dengan memanggil value tanpa nama memanggil nama kolom**
- **Menambahkan beberapa baris data sekaligus**

### 3. UPDATE
UPDATE merupakan perintah yang berfungsi untuk mengubah ataupun 
memperbarui data yang sudah ada di dalam tabel. Berikut merupakan syntax yang digunakan pada perintah UPDATE

### 4. DELETE
DELETE seperti namanya merupakan sebuah perintah yang berfungsi untuk 
menghapus data yang ada di dalam tabel. Berikut merupakan syntax yang digunakan untuk melakukan perintah DELETE

## C. OPERATOR LOGIKA
### 1. AND
Operator AND digunakan untuk mengembalikan record data apabila kedua 
kondisi yang diberikan bernilai benar atau true. Berikut merupakan syntax yang digunakan untuk menggunakan operator AND

### 2. IN 
Operator IN digunakan untuk menggantikan kondisi OR yang berulang dalam SELECT, INSERT, UPDATE, atau DELETE. Kita juga dapat menggunakan NOT IN untuk meminimalkan list pada rows data yang kita gunakan. Berikut merupakan syntax yang digunakan untuk menggunakan operator IN

### 3. OR
Operator OR digunakan untuk mengembalikan record data apabila salah satu 
kondisi yang diberikan bernilai benar atau true. Berikut merupakan syntax yang digunakan untuk menggunakan operator OR

### 4. NOT 
Operator NOT digunakan untuk mengembalikan record data apabila kondisi 
yang diberikan bernilai tidak benar atau not true. Berikut merupakan syntax yang digunakan untuk menggunakan operator NOT

### 5. LIKE
Operator LIKE digunakan bersama dengan syntax WHERE untuk mencari pola yang ditentukan dalam sebuah kolom. Berikut merupakan syntax yang digunakan untuk menggunakan operator LIKE :
- % Digunakan untuk nol atau lebih dari satu karakter.
- _  Digunakan untuk hanya satu karakter, yang berarti panjangnya tetap.

## D. OPERASI HIMPUNAN
### 1. UNION (∪)
UNION merupakan operator yang mengembalikan nilai dari dua tabel atau lebih dengan menggabungkan perintah SELECT **tanpa mengembalikan nilai duplikat.** Ada beberapa aturan untuk menggunakan UNION yaitu kolom pada tabel yang digabungkan harus memiliki jumlah dan tipe data yang sama selain itu urutan kolom pada tabel yang digabungkan juga harus sama. Berikut merupakan syntax dari operator UNION : <br>
**SELECT** kolom-1, kolom-2, …, kolom-n **FROM** nama_tabel **WHERE** kondisi
<br>
**UNION**
<br>
**SELECT** kolom-1, kolom-2, …, kolom-n **FROM** nama_tabel **WHERE** kondisi;


UNION ALL merupakan operator yang mengembalikan nilai dari dua tabel atau lebih dengan menggabungkan perintah SELECT **dengan mengembalikan nilai duplikatnya.** Perbedaan UNION dan UNION ALL terletak pada pengembalian nilainya jika UNION tidak mengembalikan nilai duplikatnya sedangkan UNION ALL mengembalikan nilai duplikatnya. Berikut merupakan syntax dari UNION ALL : <br>
**SELECT** kolom-1, kolom-2, …, kolom-n 
<br>
**FROM** nama_tabel 
<br>
**WHERE** kondisi
<br>
<br>
**UNION ALL**
<br>
<br>
**SELECT** kolom-1, kolom-2, …, kolom-n 
<br>
**FROM** nama_tabel 
<br>
**WHERE** kondisi;

### 2. INTERSECT (∩)
INTERSECT merupakan operator yang mengambil irisan dari dua perintah SELECT. Berikut merupakan syntax dari INTERSECT : <br>
**SELECT** kolom-1, kolom-2, …, kolom-n **FROM** nama_tabel 
<br>
**WHERE** nama_kolom **IN** (
<br>
**SELECT** kolom-1, kolom-2, …, kolom-n **FROM** nama_tabel);


### 3. EXCEPT (-)
EXCEPT merupakan operator yang hanya mengembalikan data unik atau eksklusif pada tabel pertama tetapi yang tidak ada pada tabel kedua. Yang dimaksud data unik atau eksklusif tersebut yaitu tidak ada yang menyamai datanya pada tabel kedua. Berikut merupakan syntax dari EXCEPT :
<br>
<br>
**SELECT** kolom-1, kolom-2, …, kolom-n **FROM** nama_tabel
<br>
**WHERE** nama_kolom **NOT IN** (
<br>
**SELECT** kolom-1, kolom-2, …, kolom-n **FROM** nama_tabel);

## E. OPERATOR ARITMATIKA
### 1. Penjumlahan (+)
Penjumlahan digunakan untuk menambahkan dua nilai.

### 2. Pengurangan (-)
Pengurangan digunakan untuk mengurangkan satu nilai dari nilai lainnya.

### 3. Perkalian (*)
Perkalian digunakan untuk mengalikan dua nilai.

### 4. Pembagian (/)
Pembagian digunakan untuk membagi satu nilai dengan nilai lainnya.

### 5. Modulus (%)
Modulus digunakan untuk mendapatkan sisa hasil bagi dari kedua nilai.

## F. OPERATOR AGREGASI
Operator Agregasi atau biasa dikenal fungsi agregat merupakan operator yang digunakan untuk meringkas data dalam sebuah tabel. Operator ini dapat digunakan dalam berbagai pernyataan DML, seperti SELECT, GROUP BY, dll.
<br> Berikut merupakan contoh dari penggunaan operator agregasi di SQL : 
### 1. SUM
SUM digunakan untuk menghitung total nilai dalam satu kolom.
<br>
**SELECT SUM**(nama_kolom)
<br>
**FROM** nama_tabel;

### 2. AVG
AVG digunakan untuk menghitung rata-rata nilai dalam satu kolom.
<br>
**SELECT AVG**(nama_kolom)
<br>
**FROM** nama_tabel;

### 3. MIN
MIN digunakan untuk mencari nilai minimum pada suatu kolom.
<br>
**SELECT MIN**(nama_kolom)
<br>
**FROM** nama_tabel;

### 4. MAX
MAX digunakan untuk mencari nilai maksimum pada suatu kolom.
<br>
**SELECT MAX**(nama_kolom)
<br>
**FROM** nama_tabel;

### 5. COUNT
COUNT digunakan untuk menghitung jumlah baris yang ada pada tabel.
<br>
**SELECT COUNT**(nama_kolom)
<br>
**FROM** nama_tabel;















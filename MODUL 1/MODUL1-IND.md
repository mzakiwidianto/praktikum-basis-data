# **MODUL 1**
###### Table of Content
[Pengantar Database](#1-pengantar-database)

[*Data Definition Language* (DDL)](#Data-Definition-Language-(DDL))

---
### 1. **Pengantar *Database***
- ### ***Database***
    <div align='justify'>
    Basis data (<i>database</i>) adalah suatu kumpulan data yang disusun dalam bentuk tabel-tabel yang saling berkaitan maupun berdiri sendiri dan disimpan secara bersama-sama pada suatu media. Basis data dapat digunakan oleh satu atau lebih program aplikasi secara optimal, data disimpan tanpa mengalami ketergantungan pada program yang akan menggunakannya.
    </div>

- ### DBMS (*Database Management System*)
    <div align='justify'>
    DBMS ini merupakan sebuah software atau sistem yang telah dirancang sedemikian rupa untuk dapat mengolah sebuah database dan menjalankan operasi terhadap data yang akan diminta oleh pengguna-penggunanya. Tujuan utama dari penggunaan DBMS ini yaitu untuk dapat menghindari kekacauan ketika kita ingin melakukan pengolahan data yang jumlah nya sangat besar.
    <br>
    <br>
    Contoh dari DBMS sendiri yaitu: 
    <br><ul><li>MySQL</li>
    <li>Microsoft Access</li> 
    <li>Airtable</li> 
    <li>Oracle</li> 
    <li>SQL Server</li>
    </div>

- ### SQL
    <div align='justify'>
    SQL (<i>Structured Query Language</i>) adalah bahasa komputer yang menjadi standar ANSI (<i>American National Standard Institute</i>) untuk mengakses dan memanipulasi data dalam basis data relasional.
    <br>
    <br>
    Fungsi SQL meliputi:
    <br>
    <b><ul><li>Menjalankan <i>query</i> dalam <i>database</i></b></li>
    SQL digunakan untuk menjalankan query atau perintah untuk mengambil data tertentu dari basis data relasional.
    <br>
    <br>
    <b><li>Memasukkan data ke dalam <i>database</i></b></li>
    SQL juga digunakan untuk memasukkan data baru ke dalam basis data relasional. Data baru dapat dimasukkan ke dalam tabel menggunakan perintah INSERT. 
    <br>
    <br>
    <b><li>Mengubah data dalam <i>database</i></b></li>
    SQL memungkinkan pengguna untuk mengubah data dalam basis data relasional dengan menggunakan perintah UPDATE. Perintah ini memungkinkan pengguna untuk mengubah nilai yang ada dalam kolom tabel.
    <br>
    <br>
    <b><li>Menghapus data dalam <i>database</i></b></li>
    SQL juga memungkinkan pengguna untuk menghapus data dalam basis data relasional dengan menggunakan perintah DELETE. Perintah ini memungkinkan pengguna untuk menghapus satu atau beberapa baris data dari tabel. </ul>
    <br>
    SQL menggunakan command atau perintah yang dapat dikelompokkan menjadi 4, yaitu:
    <br>
    <br>
    <b><ul><li>DDL (<i>Data Definition Language</i>)</b></li>
    DDL digunakan untuk mendefinisikan atau mengelola objjek basis data seperti tabael, kolom, index, dan prosedur.
    <br>
    <br>
    <b><li>DML (<i>Data Manipulation Language</i>)</b></li>
    DML digunakan untuk memanipulasi data yang ada dalam basis data seperti menambah, mengubah, dan menghapus data. 
    <br>
    <br>
    <b><li>DCL (<i>Data Control Language</i>)</b></li>
    DCL digunakan untuk mengatur hak akses pengguna terhadap basis data seperti memberikan izin untuk membaca atau menulis pada tabel tertentu.
    <br>
    <br>
    <b><li>TCL (<i>Transaction Control Language</i>)</b></li>
    TCL digunakan untuk mengelola transaksi basis data seperti COMMIT (mengkonfirmasi transaksi) dan ROLLBACK (membatalkan transaksi).</ul>
    <br>
    </div>
- ### Tipe Data pada MySQL
    <div align='justify'>
    Tipe data adalah suatu bentuk pemodelan data yang dideklarasikan pada saat melakukan pembuatan tabel. Tipe data ini akan mempengaruhi setiap data yang akan dimasukkan ke dalam sebuah tabel. Data yang akan dimasukkan harus sesuai dengan tipe data yang dideklarasikan. Berbagai tipe data pada MySQL dapat dilihat sebagai berikut :
    </div>
    <br>
    
    | Tipe Data        | Deskripsi    |
    | :------------- |:-------------|
    | `Char (size)`      | Mendefinisikan String sepanjang “size” karakter. Bila “size” tidak disertakan maka panjang karakter adalah 1. |
    | `Varchar (size)`    | Mendefinisikan String yang panjangnya berubah-ubah sesuai kebutuhan. Panjang maksimum karakter adalah 4000.|
    | `Int (size)` | Digunakan untuk menyimpan data bilangan bulat positif dan negatif. |
    | `Time`     | Digunakan untuk menyimpan nilai waktu dengan format jam, menit, dan detik dalam rentang waktu 00:00:00 hingga 23:59:59.  |
    | `Date` | Mendefinisikan tanggal. Tanggal yang bisa disimpan antara 1 Januari 4712 SM dan 31 Desember 9999 M.|
    | `Decimal (size, d)`      | Tipe data untuk menyimpan angka desimal dengan presisi tertentu. Parameter size menentukan jumlah digit yang dapat disimpan, sedangkan parameter d menentukan jumlah digit yang ditempatkan setelah titik desimal.|
    | `Double` | Tipe data untuk menyimpan angka pecahan dengan presisi tinggi. Tipe data ini dapat menyimpan angka dengan jumlah digit yang lebih besar dibandingkan dengan tipe data FLOAT.|
    | `Float`      | Tipe data untuk menyimpan angka pecahan dengan presisi yang lebih rendah daripada tipe data DOUBLE.|
    | `Boolean/Tinyint(1)` | Tipe data yang digunakan untuk menyimpan nilai boolean atau logika (true/false). Tipe data ini merupakan varian dari tipe data Tinyint dengan panjang 1.|
    | `Text`      | Tipe data yang digunakan untuk menyimpan teks dengan panjang yang sangat besar. Tipe data ini dapat menyimpan teks dengan panjang hingga 65,535 karakter.|
    | `Blob` | Tipe data yang digunakan untuk menyimpan data biner dengan panjang yang sangat besar. Tipe data ini dapat menyimpan data biner dengan panjang hingga 65,535 byte. |

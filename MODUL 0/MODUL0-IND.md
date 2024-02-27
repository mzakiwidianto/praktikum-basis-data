# **Modul 0**

## Instalasi Perangkat Lunak

---

### INSTALASI XAMPP UNTUK WINDOWS

> 1. Buka link berikut, [Download XAMPP](https://www.apachefriends.org/download.html)
> 2. Pada halaman tersebut, pilih pada bagian download untuk Windows. Pilih versi yang terbaru
![Image Download XAMPP 1](img/1.png)
> 3. Tunggu hingga file installernya selesai
> 4. Jika sudah selesai, buka file installer yang sudah didownload (jika muncul peringatan klik OK)
> 5. Jika sudah, maka tampilan instalasi XAMPP akan seperti ini.
![Image XAMPP Installation 2](img/2.png)
> 6. Klik next
![Image XAMPP Installation 3](img/3.png)
> 7. Biarkan pilihan ceklis yang default, lalu klik next
![Image XAMPP Installation 4](img/4.png)
> 8. Pilih lokasi folder yang diinginkan, jika tidak biarkan default lalu klik next
![Image XAMPP Installation 5](img/5.png)
> 9. Pilih language “English”, lalu klik next
![Image XAMPP Installation 6](img/6.png)
> 10. Klik next
![Image XAMPP Installation 7](img/7.png)
> 11. Tunggu sampai selesai
![Image XAMPP Installation 8](img/8.png)
> 12. Klik finish
![Image XAMPP Installation 9](img/9.png)
> 13. Berikut merupakan tampilan XAMPP untuk Windows
![Image XAMPP Installation 10](img/10.png)

---

### CARA MENGGANTI PORT XAMPP WINDOWS

> 1. Pada tampilan awal xampp, klik menu config pada bagian tab menu actions. Lalu klik Apache (httpd.conf)
![Image XAMPP Config 11](img/11.png)
> 2. Setelah file httpd.conf muncul, cari kode yang bertuliskan `Listen 80` dan `ServerName localhost:80`. Setelah itu ubah angka **80 menjadi 8080**, lalu save.
![Image XAMPP Config 12](img/12.png)
![Image XAMPP Config 13](img/13.png)
![Image XAMPP Config 14](img/14.png)
![Image XAMPP Config 15](img/15.png)
> 3. Selanjutnya, ubah port apache pada menu “**Service and Port Setting**”, lalu sesuaikan port dengan yang telah diubah pada file “httpd.conf” tadi
![Image XAMPP Config 16](img/16.png)
![Image XAMPP Config 17](img/17.png)
> 4. Setelah di save, tampilan port di xampp telah berubah, lalu klik stop
![Image XAMPP Config 18](img/18.png)
> 5. Untuk mengganti port mysql sama seperti apache, hanya saja cari code di “my.ini” pada config mysql yang bertuliskan `port=3306` dan diubah menjadi `port=3308`
![Image XAMPP Config 19](img/19.png)
![Image XAMPP Config 20](img/20.png)
![Image XAMPP Config 21](img/21.png)
> 6. Setelah disave, jangan lupa untuk mengubah port mysql di config xampp seperti yang dilakukan pada port apache sebelumnya
![Image XAMPP Config 22](img/22.png)
![Image XAMPP Config 23](img/23.png)
![Image XAMPP Config 24](img/24.png)
> 7. Lalu buka browser dan ketik **localhost:8080**
> 8. Maka tampilannya akan seperti ini
![Image XAMPP Config 25](img/25.png)
> 9. Selanjutnya, klik phpmyadmin. Maka tampilannya akan seperti ini dan phpmyadmin sudah dapat digunakan
![Image XAMPP Config 26](img/26.png)

---

### INSTALASI XAMPP UNTUK MAC OS

> 1. Buka link berikut, [Download XAMPP](https://www.apachefriends.org/download.html)
> 2. Pada halaman tersebut, pilih pada bagian download untuk OS X. Pilih versi yang terbaru.
![Image XAMPP Installation 27](img/27.png)
> 3. Tunggu hingga file installernya selesai
> 4. Jika sudah selesai, open file installer yang sudah dilakukan download dan klik untuk melakukan installasi
![Image XAMPP Installation 28](img/28.png)
> 5. Jika sudah, maka tampilan instalasi XAMPP akan seperti ini. Lalu, klik next.
![Image XAMPP Installation 29](img/29.png)
> 6. Biarkan komponen default terpilih, lalu klik next.
![Image XAMPP Installation 30](img/30.png)
> 7. Installer akan menampilkan direktori aplikasi yang akan dilakukan penginstallan, lalu klik next.
![Image XAMPP Installation 31](img/31.png)
> 8. Klik next untuk memulai install.
![Image XAMPP Installation 32](img/32.png)
> 9. Tunggu sampai proses instalasi selesai.
![Image XAMPP Installation 33](img/33.png)
> 10. Setelah proses instalasi selesai, klik finish.
![Image XAMPP Installation 34](img/34.png)
> 11. Berikut merupakan tampilan XAMPP untuk Mac OS.
![Image XAMPP Installation 35](img/35.png)

---

### CARA MENGGANTI PORT XAMPP MAC OS

> 1. Pada tampilan awal xampp, klik Apache Web Server lalu klik Configure. Kemudian buka Conf File.
![Image XAMPP Config 36](img/36.png)
> 2. Setelah file httpd.conf muncul, cari kode yang bertuliskan `Listen 80` dan `ServerName localhost:80`. Setelah itu ubah angka **80 menjadi 8080**, lalu save.
![Image XAMPP Config 37](img/37.png)
![Image XAMPP Config 38](img/38.png)
![Image XAMPP Config 39](img/39.png)
![Image XAMPP Config 40](img/40.png)
> 3. Selanjutnya, ubah port apache pada menu “**Service and Port Setting**”, lalu sesuaikan port dengan yang telah diubah pada file “httpd.conf” tadi
![Image XAMPP Config 41](img/41.png)
> 4. Untuk mengganti port mysql sama seperti apache, hanya saja cari code di “my.ini” pada config mysql yang bertuliskan `port=3306` dan diubah menjadi `port=3308`
![Image XAMPP Config 42](img/42.png)
![Image XAMPP Config 43](img/43.png)
![Image XAMPP Config 44](img/44.png)
> 5. Selanjutnya, ubah port MySQL, lalu sesuaikan port dengan yang telah diubah pada file “my.cnf” tadi
![Image XAMPP Config 45](img/45.png)
> 6. Start MySQL Database, lalu jalankan aplikasi
![Image XAMPP Config 46](img/46.png)
![Image XAMPP Config 47](img/47.png)
> 7. Maka tampilannya akan seperti ini
![Image XAMPP Config 48](img/48.png)
> 8. Selanjutnya, klik phpmyadmin. Maka tampilannya akan seperti ini dan phpmyadmin sudah dapat digunakan
![Image XAMPP Config 49](img/49.png)
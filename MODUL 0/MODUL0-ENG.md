# **Modul 0**

## Software 

- WINDOWS
    - [XAMPP INSTALLATION FOR WINDOWS](#xampp-installation-for-windows)
    - [HOW TO CHANGE XAMPP PORT FOR WINDOWS](#how-to-change-xampp-port-for-windows)
- MAC OS
    - [XAMPP INSTALLATION FOR MAC OS](#xampp-installation-for-mac-os)
    - [HOW TO CHANGE XAMPP PORT FOR MAC OS](#how-to-change-xampp-port-for-mac-os)

---

### XAMPP INSTALLATION FOR WINDOWS

> 1. Open the following link, [Download XAMPP](https://www.apachefriends.org/download.html)
> 2. On the page, select the download section for Windows. Choose the latest 

![Image Download XAMPP 1](img/1.png)

> 3. Wait for the installer file to finish
> 4. When finished, open the downloaded installer file (if a warning appears click OK)
> 5. The XAMPP installation will look like this.

![Image XAMPP Installation 2](img/2.png)

> 6. Click next

![Image XAMPP Installation 3](img/3.png)

> 7. Leave the default checkbox option, then click next

![Image XAMPP Installation 4](img/4.png)

> 8. Select the desired folder location, if not leave the default then click next

![Image XAMPP Installation 5](img/5.png)

> 9. Select "English" language, then click next

![Image XAMPP Installation 6](img/6.png)

> 10. Click next

![Image XAMPP Installation 7](img/7.png)

> 11. Wait until finished

![Image XAMPP Installation 8](img/8.png)

> 12. Click 

![Image XAMPP Installation 9](img/9.png)

> 13. The following is a view of XAMPP for Windows

![Image XAMPP Installation 10](img/10.png)

---

### HOW TO CHANGE XAMPP PORT FOR WINDOWS

> 1. In the xampp initial view, click the config menu on the actions menu tab. Then click Apache (httpd.conf)

![Image XAMPP Config 11](img/11.png)

> 2. After the httpd.conf file appears, look for the code that says `Listen 80` and `ServerName localhost:80`. After that change the number **80 to 8080**, then save.

![Image XAMPP Config 12](img/12.png)

![Image XAMPP Config 13](img/13.png)

![Image XAMPP Config 14](img/14.png)

![Image XAMPP Config 15](img/15.png)

> 3. Next, change the apache port in the "**Service and Port Setting**" menu, then adjust the port to what was changed in the "httpd.conf" file earlier.

![Image XAMPP Config 16](img/16.png)

![Image XAMPP Config 17](img/17.png)

> 4. After saving, the port display in xampp has changed, then click stop.

![Image XAMPP Config 18](img/18.png)

> 5. To change the mysql port, it's the same as apache, just look for the code in "my.ini" in the mysql config that says `port=3306` and change it to `port=3308`

![Image XAMPP Config 19](img/19.png)

![Image XAMPP Config 20](img/20.png)

![Image XAMPP Config 21](img/21.png)

> 6. After saving, don't forget to change the mysql port in the xampp config as you did with the apache port earlier.

![Image XAMPP Config 22](img/22.png)

![Image XAMPP Config 23](img/23.png)

![Image XAMPP Config 24](img/24.png)

> 7. Then open a browser and type **localhost:8080**
> 8. Then it will look like this

![Image XAMPP Config 25](img/25.png)

> 9. Next, click phpmyadmin. Then it will look like this and phpmyadmin can be 

![Image XAMPP Config 26](img/26.png)

---

### XAMPP INSTALLATION FOR MAC OS

> 1. Go to the following link, [Download XAMPP](https://www.apachefriends.org/download.html)

> 2. On the page, select the download section for OS X. Select the latest version.

![Image XAMPP Installation 27](img/27.png)

> 3. Wait for the installer file to finish
> 4. When finished, open the downloaded installer file and click to install.

![Image XAMPP Installation 28](img/28.png)

> 5. The XAMPP installation display will be like this. Then, click next.

![Image XAMPP Installation 29](img/29.png)

> 6. Leave the default component selected, then click next.

![Image XAMPP Installation 30](img/30.png)

> 7. The installer will display the directory of the application to be installed, then click next.

![Image XAMPP Installation 31](img/31.png)

> 8. Click next to start the installation.

![Image XAMPP Installation 32](img/32.png)

> 9. Wait for the installation process to finish.

![Image XAMPP Installation 33](img/33.png)

> 10. Once the installation process is complete, click finish.

![Image XAMPP Installation 34](img/34.png)

> 11. The following is a view of XAMPP for Mac OS.

![Image XAMPP Installation 35](img/35.png)

---

### HOW TO CHANGE XAMPP PORT FOR MAC OS

> 1. In the xampp initial view, click Apache Web Server and then click Configure. Then open Conf File.

![Image XAMPP Config 36](img/36.png)

> 2. After the httpd.conf file appears, look for the code that says `Listen 80` and `ServerName localhost:80`. After that change the number **80 to 8080**, then save.

![Image XAMPP Config 37](img/37.png)

![Image XAMPP Config 38](img/38.png)

![Image XAMPP Config 39](img/39.png)

![Image XAMPP Config 40](img/40.png)

> 3. Next, change the apache port in the "**Service and Port Setting**" menu, then adjust the port to what was changed in the "httpd.conf" file earlier.

![Image XAMPP Config 41](img/41.png)

> 4. To change the mysql port, it's the same as apache, just look for the code in "my.ini" in the mysql config that says `port=3306` and change it to `port=3308`.

![Image XAMPP Config 42](img/42.png)

![Image XAMPP Config 43](img/43.png)

![Image XAMPP Config 44](img/44.png)

> 5. Next, change the MySQL port, then adjust the port to what was changed in the "my.cnf" file earlier

![Image XAMPP Config 45](img/45.png)

> 6. Start MySQL Database, then run the application

![Image XAMPP Config 46](img/46.png)

![Image XAMPP Config 47](img/47.png)

> 7. Then it will look like this

![Image XAMPP Config 48](img/48.png)

> 8. Next, click phpmyadmin. Then it will look like this and phpmyadmin can be used

![Image XAMPP Config 49](img/49.png)
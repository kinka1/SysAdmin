# Mail server

1. konfigurasi db.kelompok5.local

![](../assets/1.png)

2. Konfigurasi db.kelompok1.local.inv.

![](../assets/2.png)

3. jalankan nslookup mail.kelompok5.local

![](../assets/3.png)

4. Install systemd-timesyncd untuk Network Time Protocol.

![](../assets/4.png)

5. Set timezone ke Jakarta, ntp true, dan local rtc false.

![](../assets/5.png)

6. Konfigurasi file timesyncd.conf di /etc/systemd dan ubah pool menjadi yang paling dekat agar delaynya pendek.

![](../assets/6.png)

7. Restart service dan cek statusnya.

![](../assets/7.png)

8. Cek tanggalnya.

![](../assets/8.png)

9. Install Apache 2.

![](../assets/9.png)

10. Ubah ServerTokens menjadi Prod.

![](../assets/10.png)

11. Tambahkan ServerName sesuai kelompok.

![](../assets/11.png)

12. Ubah ServerAdmin sesuai kleompok.

![](../assets/12.png)

13. Reload Apache.

![](../assets/13.png)

14. Cek apakah webserver berhasil berjalan.

![](../assets/14.png)

15. Install PHP dengan `sudo apt -y install php8.2 php8.2-mbstring php-pear`

16. Install PHP FPM dengan `sudo apt -y install php-fpm`.

17. Konfigurasi file default-ssl.conf.

![](../assets/17.png)


18. Lakukan setenvif di ae2enmod proxy_fcgi dan load confignya.

![](../assets/18.png)

19. Restart servicenya.

![](../assets/19.png)

20. Install maria db dengan `sudo apt -y install mariadb-server`

21. Ubah charset ke utf8mb4 di file `/etc/mysql/mariadb.conf.d/50-server.cnf`, lalu restart mariadb.

22. Jalankan sudo mysql_secure_installation.

23. Install sudo nano apt -y install postfix sasl2-bin lalu pilih No Configuration.

24. Copy file config /usr/share/postfix/main.cf.dist ke /etc/postfix/main.cf

![](../assets/24.png)
![](../assets/24-b.png)
![](../assets/24-c.png)
![](../assets/24-d.png)
![](../assets/24-e.png)
![](../assets/24-f.png)
![](../assets/24-g.png)
![](../assets/24-h.png)
![](../assets/249.png)
![](../assets/24j.png)
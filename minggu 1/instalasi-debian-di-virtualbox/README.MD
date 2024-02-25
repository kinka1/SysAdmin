# INSTALASI DEBIAN DI VIRTUALBOX 

1. Download [Virtual Box](https://www.virtualbox.org/wiki/Downloads) dan [Debian](https://www.debian.org/download) terlebih dahulu.
2. Install Virtual Box dan buka Virtual Boxnya.
3. Klik Icon + (Add) di kanan atas Virtual Box. Lalu isi ISO Image sesuai dengan path saat mendownload ISO Debian tadi. Lalu centang "Skip Unattended Installation" agar kita bisa secara manual mengonfigurasi Debiannya.

![](../../assets/minggu-1/pic%20(2).png)

4. Lalu buat memory (RAM) sebanyak 4GB. Dan untuk prosesornya di sini saya memilih 4 cores.

![](../../assets/minggu-1/pic%20(3).png)

5. Buat storagenya sebanyak 25GB.

![](../../assets/minggu-1/pic%20(4).png)

6. Akan muncul summary mengenai Machine Name, OS Type, Hardware, dan Disk. Cek dulu dan pastikan bahwa sudah sesuai dengan apa yang kita inginkan lalu klik Finish.

![](../../assets/minggu-1/pic%20(5).png)

7. Lalu start debiannya dan akan muncul installer menunya. Klik Graphical Install.

![](../../assets/minggu-1/pic%20(6).png)

8. Setelah itu kita akan diarahkan untuk mengonfigurasi lokasi, keyboard, dan bahasa.

![](../../assets/minggu-1/pic%20(7).png)
![](../../assets/minggu-1/pic%20(8).png)
![](../../assets/minggu-1/pic%20(9).png)
![](../../assets/minggu-1/pic%20(10).png)
![](../../assets/minggu-1/pic%20(11).png)
![](../../assets/minggu-1/pic%20(12).png)
![](../../assets/minggu-1/pic%20(13).png)

9. Di sini kita akan mengonfigurasi networknya. Isi hostname dengan format "sysadmin-NRP". Lalu domainnya dikosongi saja.

![](../../assets/minggu-1/2.png)
![](../../assets/minggu-1/pic%20(16).png)

10. Setelah itu konfigurasi untuk informasi user.

![](../../assets/minggu-1/pic%20(19).png)
![](../../assets/minggu-1/pic%20(20).png)

11. Lalu kita akan mengonfigurasi partisi disknya. Pilih manual. Untuk partisinya sebagai berikut:
- 20GB, beginning, primary, ext4, mount point: /
- 5GB, end, primary, ext 4, mount point: /storage
- 1.8GB, end, logical, swap area.

![](../../assets/minggu-1/pic%20(21).png)
![](../../assets/minggu-1/pic%20(22).png)
![](../../assets/minggu-1/pic%20(23).png)
![](../../assets/minggu-1/7.png)
![](../../assets/minggu-1/6.png)

12. Kita akan masuk ke finalisasi instalasinya. Pilih "no" untuk scan more media. Pilih lokasi "Indonesia" dan untuk mirrornya bisa pilih "deb.debian.org" atau yang terdekat dari lokasi kita sekarang. Untuk http proxy dikosongi saja. Dan untuk software selection, saya menambah centang Web Server dan SSH Server.

![](../../assets/minggu-1/pic%20(27).png)
![](../../assets/minggu-1/pic%20(28).png)
![](../../assets/minggu-1/pic%20(29).png)
![](../../assets/minggu-1/pic%20(30).png)
![](../../assets/minggu-1/pic%20(31).png)
![](../../assets/minggu-1/pic%20(32).png)

13. Tunggu instalasi hingga selesai. Nanti akan muncul konfigurasi Boot Loader, pilih Yes. Tunggu beberapa saat, lalu instalasi Debian sudah berhasil.
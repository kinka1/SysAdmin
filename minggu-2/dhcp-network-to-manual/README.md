DHCP (Dynamic Host Configuration Protocol) adalah protokol jaringan yang digunakan untuk secara otomatis mengonfigurasi perangkat dalam suatu jaringan IP. Protokol ini memungkinkan perangkat untuk secara dinamis mendapatkan alamat IP, subnet mask, gateway default, server DNS, dan konfigurasi jaringan lainnya dari server DHCP dalam jaringan.


### 1. ke wired
<div align="center">
    <img src="../../assets/1.png" alt="" width="70%">
</div>
tekan pengaturan kabel

### 2. tambah wired/ethernet

<div align="center">
    <img src="../../assets/2.png" alt="" width="70%">
</div>
tekan ikon tambah yang berada disamping ethernet

### 3. setting wired
<div align="center">
    <img src="../../assets/3.png" alt="" width="70%">
</div>
menuju ke IPv4 terus pilih bagian manual masukan alamat terserah anda. jangan lupa isi dns. disini contoh alamat 10.0.2.16 dengan netmask 255.255.255.0 dan gateway 10.0.2.2 menggunakan dns 8.8.8.8

### 4. uji coba
<div align="center">
    <img src="../../assets/4.png" alt="" width="70%">
</div>
cek ip di terminal menggunakan command ip addr jika muncul alamat ip sesuai dengan alamat yang dimasukan maka anda hanya perlu mengecek apakah terhubung ke dns 8.8.8.8

ping ke 8.8.8.8:
<div align="center">
    <img src="../../assets/ping_8.8.8.8.jpg" alt="" width="70%">
</div>

ping ke detik.com:
<div align="center">
    <img src="../../assets/ping_detik.com.jpg" alt="" width="70%">
</div>

ping ke google.com:
<div align="center">
    <img src="../../assets/ping_google.com.jpg" alt="" width="70%">
</div>
---

marp: true
theme: uncover
_class: invert

---

# **System Administrasi**

---
## *The software sources*


### The sources.list file
Untuk mengedit dan memodifikasi file source.list, gunakan salah satu perintah berikut (dalam mode administrator):

`nano /etc/apt/sources.list`        

Detail mengenai berbagai informasi yang ditemukan dalam file'sources.list' (garis-garis yang dimulai dengan "#" hanyalah komentar): 
• `deb` : berarti repository biner 
• `deb-src` : berarti repositori sumber 
• `http:...` atau `https:...`:  alamat Internet server repository 
• `bookworm` atau `Bookworm-security`: cabang di pohon repositori 
• `main` atau `non-free-firmware`: bagian repositori.

---

### Repositori dan Komponen Paket dalam Debian

- Repositori : Debian mengatur paket perangkat lunaknya dalam repositori. Repositori ini dibagi menjadi cabang dan bagian/komponen.

- Cabang Testing dan Unstable : Untuk informasi lebih lanjut tentang cabang "testing" dan "unstable," baca bab 8.9.

- Bagian Repositori: Ada 4 bagian dalam repositori resmi Debian:
  - Main: Mematuhi DFSG tanpa dependensi "non-free".
  - Non-free-firmware: Firmware non-bebas yang disertakan secara default sejak Debian 12.
  - Contrib: Mematuhi DFSG dengan beberapa dependensi "non-free".
  - Non-free: Tidak mematuhi DFSG.

- DFSG(Debian Free Software Guidelines) adalah Pedoman Perangkat Lunak Bebas Debian. Hanya paket dalam bagian Main yang didukung secara resmi oleh proyek Debian dan merupakan perangkat lunak 100% bebas.

---

### Repositori BackPorts

- Repositori backports adalah repositori khusus Debian yang berisi versi lebih baru dari beberapa aplikasi. Repositori ini tidak diaktifkan secara default, tetapi tidak menimbulkan risiko khusus bagi sistem .

- Mekanisme BackPorts : 
Backport adalah mekanisme yang memungkinkan sebuah aplikasi yang saat ini berada di repositori pengembangan Debian, untuk dipindahkan kembali ke versi "stable".

- "Backports" tidak ada hubungannya dengan "backdoors" yang digunakan untuk memata-matai komputer yang menjalankan sistem propietari.

---

### Modifikasi Repositori

- Risiko yang diambil dengan menggunakan komponen "contrib" atau "non-free" dari cabang arsip: 
    - Kekurangan kebebasan untuk jenis paket ini.
    - Kekurangan dukungan oleh proyek Debian 
    - Kontaminasi sistem Debian yang sepenuhnya bebas.
- Untuk mengubah sumber perangkat lunak, cukup edit berkas 'sources.list'. Buka terminal dalam mode administrator (bab 3.8.3), dan masukkan:
`apt edit-sources`
- Perintah ini membuka berkas yang sesuai dengan editor teks default (nano atau vim). Setelah selesai dengan modifikasi, simpan berkas ( `[Ctrl]+x`  dengan nano, atau   `:wq` dengan vim).that 

---

## APT in Terminal

---
### 'User' command to search and display information

Perintah-perintah ini dapat dijalankan sebagai `user`, karena mereka tidak mempengaruhi sistem.

`apt show foo` => menampilkan informasi tentang package foo
`apt search foo` => Cari paket yang sesuai dengan foo
`apt-cache policy foo` => Tampilkan versi foo yang tersedia

---

### 'Administrator' mode commands for system maintenance

harus mengeksekusi `su` untuk merubah ke mode administrator, perintah yang dapat dijalankan antara lain :
`apt full-upgrade` => update package yang diinstal, dengan menambahkan / 
`apt remove foo`    => Menghapus paket foo, tetapi tidak file configuratrion
`apt install foo`   => install package yang diinginkan
`apt upgrade`   => Pembaruan aman dari paket yang diinstal
`apt clean`     => Membersihkan cache lokal dari paket yang usang

---

## Software : the simplified package manager

---

### Pencarian aplikasi
- untuk melakukan pencarian dengan mengklik tombol pencarian (simbol kaca pembesar), atau dengan memilih salah satu dari kategori yang ditampilkan.

### Menginstall aplikasi 
- untuk menginstal sebuah aplikasi dengan mudah dengan mengklik area deskripsi aplikasi dan tombol "Instal". Password administrator akan diminta. ikuti progres instalasi di jendela utama dan langsung menjalankan aplikasi yang baru diunduh.

---

### Menghapus Aplikasi

- menghapus sebuah aplikasi dengan mudah dengan mengunjungi kategori "Terinstal" (di bagian atas antarmuka) dan kemudian dengan mengklik tombol "Hapus". nanti akan diminta untuk konfirmasi.

### Pembaruan Aplikasi

- Untuk memperbarui sistem  dari bagian yang ditunjuk "Pembaruan" yang akan menunjukkan pembaruan yang tersedia dan/atau sudah diunduh. Jika tidak ada pembaruan yang tersedia, dapat memeriksa repositori dengan menggunakan tombol yang ditunjuk di bagian kiri atas

---

### Pembaruan Otomatis dengan Software

Untuk memanfaatkan sistem  tanpa perlu khawatir tentang pembaruan, untuk mengaktifkan mekanisme pembaruan otomatis. Dari menu "Software", pilih "Preferensi Pembaruan". Entri-entri di sana dijelaskan dengan jelas.

---

### Search and install with Discover

Untuk menemukan sebuah aplikasi, ketik namanya di kolom pencarian yang disediakan atau kunjungi berbagai kategori di Discover. Kemudian, sebuah klik pada tombol "Instal" sudah cukup:
- Mencari Aplikasi dengan Discover
- Menelusuri Kategori dengan Discover

### Install Plasma desktop widgets and addons

Discover memungkinkan user untuk menambahkan komponen tambahan ke lingkungan Plasma. 

---

### Uninstalling an application with Discover

Dengan Discover, cukup kunjungi kategori "Terinstal" kemudian klik "Hapus".

### Discover: updating your applications

Ketika KDE memberi tahu user tentang satu atau lebih pembaruan, "Discover" yang melakukannya. Untuk memeriksa pembaruan "secara manual", klik tombol yang ditunjuk:

Discover: Memeriksa Pembaruan
Cukup klik "Perbarui semua" dan konfirmasi dengan password administrator.

---
### Discover: managing repositories

Perpustakaan perangkat lunak KDE memungkinkan  untuk mengubah sumber aplikasi tanpa menggunakan terminal. Pergi ke bagian "Pengaturan" Discover, entri-entri menampilkan alamat repositori dari sources.list

---

## Synaptic: the comprehensive package manager

---
Synaptic adalah antarmuka grafis komprehensif dari manajer paket Debian. Ini memungkinkan visi menyeluruh terhadap paket-paket yang ditawarkan, baik yang terinstal maupun yang belum. Ini jauh lebih detail daripada Pusat Perangkat Lunak atau Discover (lihat bab sebelumnya) karena menampilkan seluruh rangkaian paket yang tersedia (termasuk perpustakaan).

Ini menyediakan fungsionalitas yang sama dengan apt. user perlu memasukkan sandi administrator untuk membuka dan menggunakan Synaptic.
Koneksi Internet yang aktif juga diperlukan untuk menginstal atau memperbarui perangkat lunak.

---

### 

- Jendela Synaptic dibagi menjadi 4 area: toolbar di bagian atas, panel kiri untuk pengurutan dan pemilihan paket, panel tengah menampilkan daftar paket, dan di bawahnya, panel yang menampilkan deskripsi paket yang saat ini dipilih.
- Di depan setiap paket, terdapat kotak kecil (putih untuk paket yang belum diinstal, hijau ketika sudah diinstal, merah ketika rusak). Di sebelah kotak status ini, logo Debian menunjukkan bahwa paket ini "bebas" (sebagai kebebasan).
- Jangan ragu untuk mengklik semua menu yang berbeda untuk menjelajahi Synaptic dan menjadi lebih familiar dengannya. Ini adalah cara yang baik untuk menemukan berbagai fungsinya.
- Jangan takut merusak sistem Anda karena tidak akan terjadi apa-apa sampai Anda mengklik tombol "Terapkan". Selain itu, pesan meminta konfirmasi akan selalu ditampilkan terlebih dahulu.
- Hal pertama yang harus dilakukan saat membuka Synaptic adalah mengklik tombol "Muat Ulang" untuk memperbarui semua informasi (metadata) mengenai repositori, paket, dan aplikasi yang tersedia.
---
### Monitoring dan Logging
- Debian 12 memiliki utilitas seperti top untuk memantau aktivitas sistem.
- Log sistem tersimpan di direktori /var/log.
---
## Kesimpulan 

- Memahami dasar-dasar administrasi Debian 12 penting untuk mengelola sistem dengan efisien dan efektif.
- Dengan menguasai manajemen pengguna, paket, layanan, serta monitoring dan logging, Anda dapat menjaga sistem Debian 12 Anda berjalan dengan lancar

---
# Bagaimana sebuah klien konek ke dns dan bagaimana si DNS itu melakukan proses iterative untuk querynya?

## Koneksi Klien ke DNS:

1. Permintaan DNS: Ketika pengguna memasukkan nama domain di browser, aplikasi, atau perangkat, perangkat tersebut akan mengirimkan permintaan DNS ke resolver DNS.
2. Resolver DNS: Resolver DNS adalah server yang menerima permintaan DNS dari klien. Resolver DNS kemudian akan mencari alamat IP yang sesuai dengan nama domain.
3. Root Server: Resolver DNS pertama kali akan menanyakan Root Server. Root Server adalah server DNS yang menyimpan informasi tentang server DNS lain yang bertanggung jawab untuk domain tingkat atas (TLD) seperti .com, .net, dan .org.
4. TLD Server: Root Server akan mengarahkan resolver DNS ke TLD Server yang bertanggung jawab untuk TLD yang dicari.
5. Authoritative Name Server: TLD Server kemudian akan mengarahkan resolver DNS ke Authoritative Name Server (ANS) yang menyimpan informasi tentang nama domain yang dicari.
6. Jawaban DNS: ANS akan memberikan jawaban DNS kepada resolver DNS, yang berisi alamat IP yang sesuai dengan nama domain.
7. Resolver DNS: Resolver DNS kemudian akan memberikan alamat IP tersebut kepada klien.
8. Koneksi ke Server Web: Klien kemudian dapat menggunakan alamat IP tersebut untuk terhubung ke server web yang terkait dengan nama domain.

## Proses Iterative Query:

Proses iterative query adalah proses di mana resolver DNS secara bertahap mencari alamat IP yang sesuai dengan nama domain dengan menanyakan server DNS lain. Berikut adalah langkah-langkahnya:

1. Resolver DNS: Resolver DNS memulai dengan mengirimkan permintaan DNS ke Root Server.
2. Root Server: Root Server akan memberikan daftar TLD Server yang bertanggung jawab untuk TLD yang dicari.
3. Resolver DNS: Resolver DNS kemudian akan memilih salah satu TLD Server dan mengirimkan permintaan DNS ke server tersebut.
4. TLD Server: TLD Server akan memberikan daftar ANS yang menyimpan informasi tentang nama domain yang dicari.
5. Resolver DNS: Resolver DNS kemudian akan memilih salah satu ANS dan mengirimkan permintaan DNS ke server tersebut.
6. Authoritative Name Server: ANS akan memberikan jawaban DNS kepada resolver DNS, yang berisi alamat IP yang sesuai dengan nama domain.
7. Resolver DNS: Resolver DNS kemudian akan memberikan alamat IP tersebut kepada klien.

Proses iterative query ini akan terus berulang sampai resolver DNS mendapatkan jawaban DNS yang berisi alamat IP yang sesuai dengan nama domain.
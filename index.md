# LAPORAN PRAKTIKUM 14
## Praktikum Jaringan Komputer

Dosen Pengampu: JOHAN ERICKA WAHYUPRAKASA, M.Kom

```markdown
DATA DIRI
Nama    : Taufik Ardiansyah Putra
Kelas   : Praktikum Jaringan Komputer B
NIM     : 200605110071
```
 
### Tujuan
Buatlah tutorial instalasi web server step by step (distro bebas) yang berisi :
-	instalasi web server (apache / nginx / dll)
-	instalasi php
-	instalasi & konfigurasi database server (mysql / mariadb / dll)
-	instalasi ftp server (proftpd / vsftpd / dll)
-	pembuatan user dengan home direktori di direktori website
-	upload file website ke server melalui ftp (website bebas bisa wordpress / semacamnya asal memiliki akses ke database / bukan website statis)
tutorial di buat dalam sebuah blog yang berisi identitas anda. paste alamat URL blog di tugas ini

 
  •	Instalasi web server (apache)
1. Lakukan update terlebih dahulu dengan perintah sudo apt-get updatee

![image](https://user-images.githubusercontent.com/74701531/169015439-5fe95c22-0a8f-4b6f-afb8-3149f1affc19.png)

2. Setelah itu install apache2 dengan perintah sudo apt-get install apache2

  ![image](https://user-images.githubusercontent.com/74701531/169015471-73fece81-4db7-4796-99d4-536fbe067e1d.png)

  3. Cek status dari Apache2 dengan perintah sudo service apache2

  ![image](https://user-images.githubusercontent.com/74701531/169016748-b29af140-868f-44c2-b3ea-5f996c37c412.png)

  4. Cek hasil web service di browser


   ![image](https://user-images.githubusercontent.com/74701531/169016802-6069834b-4726-46b0-bec6-3f96484bee25.png)


  •	Instalasi PHP

  1. Lakukan update terlebih dahulu dengan perintah sudo apt-get update

  ![image](https://user-images.githubusercontent.com/74701531/169016913-aef07d77-e3f7-44fd-b445-0682146a8294.png)

  2. Setelah itu install apache2 dengan perintah sudo apt-get install php

  ![image](https://user-images.githubusercontent.com/74701531/169017038-2f84534a-4232-404b-8f10-47637030d674.png)

  3. Cek versi PHP

  ![image](https://user-images.githubusercontent.com/74701531/169017072-1ffe3c5a-c49a-4300-a90a-cb20d25e2c27.png)

  4. Cek status PHP pada web service

  - Menuju direktori PHP, kemudian hapis file index.html

  ![image](https://user-images.githubusercontent.com/74701531/169017094-d1354fb4-9cf0-4dc4-ac11-c8a17fd43273.png)

  - Buat file info PHP dengan perintah sudo nano info.php

  ![image](https://user-images.githubusercontent.com/74701531/169017125-30400576-7bb9-44f4-8fcf-9c82b9302f71.png)

  5. Ketikkan script seperti gambar dibawah ini

  ![image](https://user-images.githubusercontent.com/74701531/169017150-943325e1-05f3-4d2f-b130-496efb1d6d89.png)

  6.	Akses file info.php tersebut di browser
 
  ![image](https://user-images.githubusercontent.com/74701531/169017169-e18d2186-0768-461c-a6aa-cb0faff93c26.png)


  •	Instalasi & konfigurasi database server (mysql, mariadb)

  1. Lakukan update terlebih dahulu dengan perintah sudo apt-get update

  ![image](https://user-images.githubusercontent.com/74701531/169019109-add04b02-2070-4831-b961-7e34e1a11e12.png)

  2. Setelah itu install apache2 dengan perintah sudo apt-get install mariadb-server

  ![image](https://user-images.githubusercontent.com/74701531/169019143-8c3cb243-7f4f-4b8e-9177-21d316b0957a.png)

  3. Kemudian kita harus mengamankan database server kita dengan perintah sudo mysql_secure_installation

  ![image](https://user-images.githubusercontent.com/74701531/169019167-4e5458e0-4015-4fbd-b15a-20ca4e3cb4cd.png)

  - Masukkan ‘Y’ untuk memasuki proses authentication

  ![image](https://user-images.githubusercontent.com/74701531/169019184-637239ae-7c8e-4cf9-9e92-af814ac2ab64.png)

  - Masukkan ‘n’ agar katasandi dari root user tidak diubah

  ![image](https://user-images.githubusercontent.com/74701531/169019196-7fe283fc-606d-484e-9801-85eb9ed69c2f.png)

  - Masukkan ‘n’ agar user tanpa nama tidak dapat mengakses database server

  ![image](https://user-images.githubusercontent.com/74701531/169019214-46a1b082-e358-4149-b07d-69a8df4839a3.png)

  - Masukkan ‘n’ agar root user dapat mengakses database dengan remote (jarak jauh)

  ![image](https://user-images.githubusercontent.com/74701531/169019222-3c88c1f8-257b-4d50-b8f9-44dd16b70de2.png)

  - Masukkan ‘Y’ agar database test yang dapat diakses oleh semua orang dihapus

  ![image](https://user-images.githubusercontent.com/74701531/169019238-85e49568-e1b7-43c4-82e0-477d5abeee4d.png)

  - Masukkan ‘Y’ agar semua pengaturan yang telah kita buat tadi dapat diproses saat ini

  ![image](https://user-images.githubusercontent.com/74701531/169019261-bfae6615-efdd-455f-afba-55dca6ba102a.png)

  4. Akses database dengan perintah sudo mysql -u root -p, kemudian masukkan password root

  ![image](https://user-images.githubusercontent.com/74701531/169019297-98e740f6-36cc-4b58-b6ab-8393b0a895d6.png)

  5. Masukkan perintah create database wordpress untuk membuat database baru bernama wordpress.

  ![image](https://user-images.githubusercontent.com/74701531/169019308-203d11bb-a0e9-4334-b42a-6a7e9ffcab08.png)

  6. Berikan perintah show databases untuk melihat daftar database yang sudah dibuat

  ![image](https://user-images.githubusercontent.com/74701531/169019322-2a5bfcf8-540b-498f-93c9-0755b9402f1c.png)

  7.	Masukkan ‘Exit’ untuk keluar

  ![image](https://user-images.githubusercontent.com/74701531/169019332-639a32e1-2903-43c1-92bf-e1445bf09e5b.png)


  •	Instalasi file server (proftpd)

  1. Lakukan update terlebih dahulu dengan perintah sudo apt-get update

  ![image](https://user-images.githubusercontent.com/74701531/169019384-d4f22165-0474-4b3a-bcce-3ee9ed12a729.png)

  2. Setelah itu install apache2 dengan perintah sudo apt-get install proftpd-basic

  ![image](https://user-images.githubusercontent.com/74701531/169019420-78808b9d-b45f-4b64-a3ab-7090b3a62bc6.png)

  3. Cek status dari proftpd dengan perintah sudo service proftpd status

 
   ![image](https://user-images.githubusercontent.com/74701531/169019440-4d706aed-36de-4c66-9a3b-efe4d9fb30f2.png)


  •	Pembuatan user dengan home direktori di direktori website

  1. Buat home direktori dan user yang ingin kita berikan direktori tersebut

  ![image](https://user-images.githubusercontent.com/74701531/169019466-f433e148-0df6-49fd-be5b-302ae58ad0ad.png) 

  2. Buat katasandi pada user yang telah dibuat dengan perintah sudo passwd <namauser>, lalu berikan katasandi dengan minimal 8 karakter

  ![image](https://user-images.githubusercontent.com/74701531/169019489-0c804742-3f12-424a-8b56-7e1a58a58ed5.png)

  3. Cek user yang telah dibuat dengan perintah cat /etc/passwd

  ![image](https://user-images.githubusercontent.com/74701531/169019511-17cde794-4385-46a1-8d8a-d560faa51bda.png)

  4. Tes koneksi ke user admin menggunakan cmd dengan perintah ssh <namauser>@<ipserver>

  ![image](https://user-images.githubusercontent.com/74701531/169019517-2ff400e7-88c0-4d1a-9e56-1e167c834e4d.png)

  5. Restart FTP Server dengan perintah sudo service proftpd restart

  ![image](https://user-images.githubusercontent.com/74701531/169019529-08aa27a6-2c7a-4f8a-91ad-83a67cecb790.png)

  6. Cek permission pada direktori home yang telah dibuat

  ![image](https://user-images.githubusercontent.com/74701531/169019542-587abd74-754d-48a6-b018-c151de1f47c1.png)

  7. Kemudian berikan izin pada user admin untuk melakukan write dengan perintah sudo chmod -R 757 <direktoritujuan>

  ![image](https://user-images.githubusercontent.com/74701531/169019553-e0b259a8-f85a-4e6d-9d9f-ad16f7c204d0.png)

  8. Buka aplikasi filezilla client pada device client dan masukkan Host, Username, Password dan Port sesuai dengan server kalian.

  ![image](https://user-images.githubusercontent.com/74701531/169019587-8204b895-41b5-4c2e-8461-2def361c3c2a.png)

  Catatan :
  - Host		: 192.168.1.19 (IP Server)
  - Username	: Admin (Nama user yang akan dipakai)
  - Password	: Katasandi dari user Admin
  - Port		: 21 (Port default dari FTP)

  
  9. Klik ‘Quickconnect’, lalu klik ‘ok’ untuk masuk ke FTP Server yang dituju

  ![image](https://user-images.githubusercontent.com/74701531/169019597-e46a23ea-7d49-48b0-a60c-b92157573250.png)

  10.	Tes koneksi dengan membuat file baru di Filezilla
 
  ![image](https://user-images.githubusercontent.com/74701531/169019607-f33bd701-0952-4a07-9c87-2dc2c3406659.png)
  
  ![image](https://user-images.githubusercontent.com/74701531/169019646-5f6d4f94-17c9-419c-9821-1919c4adfd1d.png)

  11. File selesai di upload
  
  ![image](https://user-images.githubusercontent.com/74701531/169019713-6da1e1e0-059f-4b7f-82cd-f7c743db4f13.png)

  
  •	Upload file website ke server melalui FTP (Wordpress)

  1. Unduh file Wordpress terlebih dahulu di https://wordpress.org/download/ 

  ![image](https://user-images.githubusercontent.com/74701531/169019736-4045d5fe-42b3-4bd9-9143-05dcc21eccd0.png)

  2. Upload file zip wordpress ke server menggunakan Filezilla melalui ftp server. Cukup klik 2x pada file yang ingin di upload (sisi kiri)

  ![image](https://user-images.githubusercontent.com/74701531/169019752-d2af3164-f4c4-43cf-8795-4aaed71920ce.png)

  3. Install Unzip di server dengan perintah sudo apt-get install unzip

  ![image](https://user-images.githubusercontent.com/74701531/169019771-eaf64487-c476-44ac-b3d3-54d62fda2667.png)

  4. Menuju direktori home, kemudian unzip file wordpressnya

  ![image](https://user-images.githubusercontent.com/74701531/169019783-da9f9745-617d-41df-a21c-d71ef106f1af.png)

  5. Install ekstensi Php-Mysql terlebih dahulu denagn perintah sudo apt-get install php-mysql

  ![image](https://user-images.githubusercontent.com/74701531/169019831-b1bcc3df-50ea-408b-be9d-24ae053e63d5.png)

  6. Restart web server dengan perintah sudo service apache2 restart

  ![image](https://user-images.githubusercontent.com/74701531/169019856-02462e6b-28d6-41a7-b6a2-58c4539088de.png)

  7. Masuk ke database server dengan perintah sudo mysql -u root -p. Masukkan password dan ketika sudah masuk, buat user baru dengan perintah create user ‘<namauser>’@’localhost’ identified by <password>;. Setalah itu ketikkan perintah grant all privileges on wordpress.*to ‘<namauser>’@’localhost’;. Terakhir, ketikkan perintah flush privileges untuk apply konfigurasi pada privileges.

  ![image](https://user-images.githubusercontent.com/74701531/169019868-239d1803-c7a6-42e7-9ec7-55f99a038537.png)

  8. Cek hasil privileges tadi pada user admin (user yang telah diberikan privilege)

  ![image](https://user-images.githubusercontent.com/74701531/169019878-d46c7a1a-4da5-46b7-aca0-5a6d0d924d6c.png)

  9. Buka alamat wordpress (<IP Server>/wordpress) di browser client, lalu klik “Let’s Go”

  ![image](https://user-images.githubusercontent.com/74701531/169019890-1048946c-88bd-46a8-b551-79d7f8125f0d.png)

  10. Masukkan data sesuai dengan server kalian

  ![image](https://user-images.githubusercontent.com/74701531/169019899-a7af6098-846f-4d1a-9e7e-e72b98053043.png)

  11. Salin script yang ada didalam box yang telah disediakan, kemudian klik “Run Installation”

  ![image](https://user-images.githubusercontent.com/74701531/169019943-ba8ffaaf-00a5-48cc-adb9-532a712c6d57.png)

  12. Buat file wp-config.php didalam direktori wordpress

  ![image](https://user-images.githubusercontent.com/74701531/169019961-8985c6c7-e2fc-489e-9348-635cff9203dd.png)

  13. Tempel script yang telah disalin sebelumnya kedalam file baru tersebut, kemudian save

  ![image](https://user-images.githubusercontent.com/74701531/169019970-6e6fa939-e459-4f5f-ae49-1cf49873b4c5.png)

  14. Kembali ke website wordpress, klik tombol “Run Installation”

  ![image](https://user-images.githubusercontent.com/74701531/169019986-ceb21da5-c1c4-4bd7-adb1-02a84088aa3b.png)

  15. Isi sesuai dengan yang kalian inginkan pada website yang akan kalian buat, setelah itu klik “Install Wordpress”

  ![image](https://user-images.githubusercontent.com/74701531/169019998-cb3cbd99-fee8-452a-b3e1-c298ea1fe526.png)

  Catatan :
  -	Site Title			: Judul Website
  -	Username			  : admin (Nama user yang akan dipakai)
  -	Password			  : Katasandi dari user
  -	Your Email			: email dari user
  -	Search Engine	 Visibility	: Memasukkan site ke dalam search engine

  16. Klik “Log In”

  ![image](https://user-images.githubusercontent.com/74701531/169020006-ad69c785-1c60-465b-9803-ed83ae53be56.png)

  17. Masuk dengan akun yang telah dibuat

  ![image](https://user-images.githubusercontent.com/74701531/169020016-8f31b132-24f6-4c81-a79f-73e55fc879f1.png)

  18.	Kemudian kita akan masuk ke dashboard utama dari wordpress

  ![image](https://user-images.githubusercontent.com/74701531/169020025-cbdbe134-28cc-4203-828f-3221b99acbc4.png)

  19.	Selesai

  ![image](https://user-images.githubusercontent.com/74701531/169020033-a6ebd410-a7b3-472c-b1f3-746a6fb3c127.png)

 


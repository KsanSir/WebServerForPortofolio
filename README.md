# WEBSITE SERVER #

Tugas yang di buat pada final project kali ini adalah WEB Server Untuk Saya tampilkan Portofolio saya. menggunakan WebServer Ubuntu 22.04

***

## Apa Itu Web Server? ##
Web server adalah perangkat lunak atau perangkat keras yang menyediakan layanan untuk mengakses halaman web atau konten web melalui internet. Fungsi utama dari web server adalah melayani permintaan dari klien (biasanya browser web) dengan menyediakan halaman web yang diminta. Ketika seseorang mengakses situs web melalui browser mereka, permintaan dikirim ke web server, dan web server ini kemudian mengirimkan halaman web tersebut kembali ke browser pengguna. Untuk contoh dari penggunaannya adalah sebagai berikut :

![Screenshot 2023-12-19 235747](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/4acf821a-636e-4868-ab0b-a1d7829c8e11)

## OS Server ##
Ubuntu 22.04 64bit

***
## Bahan dan Alat Serta Service Yang Di Gunakan ##
1. File ISO Ubuntu 22.04, dapat di download di https://ubuntu.com/download/desktop
2. SSH Server
4. Apache2
5. Ngrok
***

## Update Progress ##
1. 17 Desember 2023 Instalasi SSH Server
2. 17 Desember 2023 Instalasi DHCP Server
3. 17 Desember 2023  Instalasi Apache2 dan Mysql
5. 16 Desember 2023 Instalasi Ubuntu pada Virtualbox
***

## Panduan Instalasi ##

- Install Git terlebih dahulu
```
khent@WebServer: sudo apt update && upgrade
```
#

- Dilanjut untuk install Apache2 serta cek status apache

```
khent@WebServer: sudo apt install Apache2
khent@WebServer: sudo systemctl status Apache

```

- Dilanjut untuk mengubah kepemilikan folder '/var/www/html' ke www-data serta Beri Izin anggota grup untuk mengubah folder '/var/www/html'

```
khent@WebServer: sudo chown -R www-data:www-data /var/www/html
khent@WebServer: sudo chmod -R g+rw /var/www/html
khent@WebServer: sudo usermod -a -G www-data [my username]

```

- Tambahkan Rule untuk Apache di Firewall

```
khent@WebServer: sudo ufw allow 'Apache'
khent@WebServer: sudo ufw status

```

- Install Mysql
```
khent@WebServer: sudo apt install mysql-server
khent@WebServer: sudo mysqk_secure_installation

```

- Install PHP
```
khent@WebServer: sudo apt install php libaapache2-mod-php php-mysql

```

- Install SSH dan Configurasikan SSH Tersebut https://ubuntu.com/server/docs/service-openssh
```
khent@WebServer: sudo apt install openssh-client
khent@WebServer: sudo apt install openssh-server

```

- Install NGROK
```
khent@WebServer: sudo apt update
khent@WebServer: sudo apt install snapd
khent@WebServer: sudo snap install ngrok

```

## WEB Server For Portofolio ##
Untuk web server ini saya tidak membutuhkan database karena saya hanya ingin menampikan data diri saya saja secara lengkap saja.

- Berikut Beberapa Hasil Dokumentasi Mulai dari Install Apache sampai dengan Ngrok

![VirtualBox_WebServer_18_12_2023_17_03_29](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/90f2d632-7d59-4fa2-bb6f-f18e9c6fb77f)

![VirtualBox_WebServer_18_12_2023_17_52_27](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/3f4216e9-7ca4-4be4-b813-f74fe6f4e285)

![VirtualBox_WebServer_18_12_2023_17_43_54](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/412ed563-7b7a-43a4-8381-b393d9e0f5e0)

![VirtualBox_WebServer_18_12_2023_17_48_28](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/b0deb5df-a6f3-43fa-bf12-770e8b091e13)

![VirtualBox_WebServer_18_12_2023_17_55_01](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/6196bad6-059f-4277-9a28-fa02db99e523)

![VirtualBox_WebServer_18_12_2023_17_23_35](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/191f61a2-d45c-4b6c-a7dc-89490258e657)

![VirtualBox_WebServer_18_12_2023_17_24_18](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/0a5dadd1-7f49-41a0-b963-7a3446513f1e)

![VirtualBox_WebServer_18_12_2023_17_24_55](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/f6186ed3-db38-4056-a34e-abcd8a13ff28)

![VirtualBox_WebServer_18_12_2023_18_03_11](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/25fa8537-6e8a-409b-b991-89ba2981cb6b)

![VirtualBox_WebServer_18_12_2023_18_03_02](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/b6f335ca-f899-42e9-966c-b2bb3f4e00e3)

![VirtualBox_WebServer_18_12_2023_18_03_47](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/ecd53d83-5f11-450f-a24c-38f73816cf66)

![VirtualBox_WebServer_18_12_2023_18_03_29](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/7c2ea66f-1c97-42c6-a289-65aa1cd6b7d8)

![Screenshot 2023-12-19 234929](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/8a174ece-9d77-4faa-9a28-2c7d550f8d69)

![Screenshot 2023-12-19 235050](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/5fc3c090-3879-4300-9f19-df3e48baa30b)

![Screenshot 2023-12-19 235136](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/1af46694-e016-4152-8f94-092c5c075048)

![Screenshot 2023-12-19 235209](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/afd2ab95-1060-43bf-a600-9da30f6543e7)

![Screenshot 2023-12-19 235546](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/e0a58539-84aa-45e5-9bcc-4134730998b1)

![Screenshot 2023-12-19 235700](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/d3e16dff-eb06-4b77-8f7c-f3f209263ceb)

![Screenshot 2023-12-19 235747](https://github.com/KsanSir/WebServerForPortofolio/assets/142091461/6e181036-66a4-4844-a65e-be2cf73f543b)

- SEKIAN DARI SAYA TERIMAKASIH

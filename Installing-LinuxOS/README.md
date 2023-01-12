# Introduction to DevOps
## 1.	Divinisi DevOps
Devops adalah penghubung antara tim development dengan tim operational, bertugas untuk mempercepat proses development hingga rilis produk ke public yang divisualisasikan sebagai proses loop yang tidak terbatas yang terdiri dari :
-	Plan	-  Realese
-	Code	-  Deploy
-	Build	-  Operate
-	Test	- Monitor

## 2.	Sebutkan Lifecycle Devops dan jelaskan Definisinya

-	Plan : Proses perencanaan untuk seluruh alur kerja yang dibutuhkan sebelum developer mengerjakan kode program dan juga mengoptimalkan dampak bisnis dan menghasilkan program yang di harapkan untuk di produk ke public.
-	Code : Pada tahap ini team development akan mulai bekerja untuk membuat code program untuk sebuah aplikasi yang sudah direcanakan sebelumnya, pada tahap ini team Development harus berkerjasama dengan team operation agar aplikasi yang dibuat dapat berjalan dengan baik.
-	Built : Pada tahap ini, team development akan membuild code yang sudah dibuat pada tahap sebelumnya bertujuan untuk melihat apakah masih terdapat error atau tidak saat setelah di build.
-	Test : merupakan tahap pengetesan aplikasi yang sudah dibuat oleh developers, pengetesan dilakukan secara internal untuk mengetahui apakah ada masalah fungsionalitas atau tidak, jika terdapat masalah fungsionalitas makan akan dilaporkan ke developers untuk  diperbaiki.
-	Realese : Di tahap ini, build yang sudah melalui serangkaian pengetesan dan dinyatakan lolos dan sudah sesuai dengan yang di rencanakan, maka team development akan membuat sebuah versi rilis dari produk tersebut.
-	Deploy : aplikasi yang sudah di realese oleh team development akan dijalankan ke server oleh operation team sebelum digunakan oleh public.
-	Operate : Tahap ini aplikasi yang sudah selesai dijalankan pada server dan sudah dapat digunakan secara public, dan memastikan kalua tidak terjadi masalah Ketika sedang digunakan oleh user (public)
-	Monitor : Untuk Proses ini, team operations akan melakukan pemantauan terhadap aplikasi yang sudah berjalan dan digunakan oleh user(public). Pemantauan meliputi ifrastruktur, sistem, dan aplikasi sudah berjalan lancar 





## 3.	Installasi ubuntu Server menggunakan VMware

Untuk spesifikas yang digunakan pada VMware sebagai berikut : 2 CPU 1GB ram 20GB storage lalu melakukan setup ip static dan install openSSH server

-	Software yang digunakan bisa menggunakan VMware, virtualbox, atau QEMU, disini saya menggunakan VMware
-	Open Aplikasi VMware yang sudah terinstall
![image1](https://user-images.githubusercontent.com/68781074/212050165-80ff9ae5-d01d-45cd-a47f-87c32826a338.png)
-	Pada Home pilih “Create A New Virtual Machine”
![image2](https://user-images.githubusercontent.com/68781074/212050207-52549039-cd98-47c1-85c2-d0b159477339.png)
-	Browse .ISO ubuntu server yang sudah didownload, disini saya menggunakan ubuntu server 20.04.5 LTS
![image3](https://user-images.githubusercontent.com/68781074/212050290-ccc86f3a-5a1e-4874-9811-f05d84ecce0a.png)
-	Masukan Full name, Username dan Password

![image4](https://user-images.githubusercontent.com/68781074/212050357-fed8b64a-5344-4108-bf08-7416b1eaf669.png)
-	Lalu klik Next saja

![image5](https://user-images.githubusercontent.com/68781074/212050396-0f98c1e7-f8ce-4bd7-b9ec-1945f7ef456e.png)
-	Maximum Disk yang digunakan adalah 20GB dan pilih Split Virtual Disk into multiple File

![image6](https://user-images.githubusercontent.com/68781074/212051104-52fc3442-baba-4e43-8360-690e644b6630.png)
-	Lalu Selanjutnya pilih Customize Hardware

![image7](https://user-images.githubusercontent.com/68781074/212051134-904213d7-6fb3-492a-a943-7460da4d64e9.png)
-	Memory Rubah ke 2GB

![image8](https://user-images.githubusercontent.com/68781074/212051338-95c0f6d6-4c88-41bb-918c-014f3665d2d7.png)
-	Processors tetep 2 CORE

![image9](https://user-images.githubusercontent.com/68781074/212051371-1a64d6fe-f39b-42b3-bbf3-1e236d05ee86.png)
-	Dan pada Di Network Adapter pilih Bridged

![image10](https://user-images.githubusercontent.com/68781074/212051427-891ac5e7-5db7-4af1-b220-2ac744bb89ec.png)
-	Setelah itu Klik Finish

![image11](https://user-images.githubusercontent.com/68781074/212051463-dbb32574-9f13-45f3-9add-77e681980fc7.png)
-	Proses Instalasi Ubuntu Server

![image12](https://user-images.githubusercontent.com/68781074/212051546-94b91210-187d-4f90-aeb3-a58ec6b9f8a8.png)
-	Pilih Bahasa yang akan digunakan

![image13](https://user-images.githubusercontent.com/68781074/212051564-c9cd5d9f-0adc-45d2-b470-b7cb9b6a7bd2.png)
-	Pilih Continue Without Updating

![image14](https://user-images.githubusercontent.com/68781074/212051599-cd0334f2-5575-4171-977e-a85a64491dea.png)
-	Lalu Pilih Done

![image15](https://user-images.githubusercontent.com/68781074/212051695-c426aabd-65f4-4357-9e07-1c4a8f1ccfc7.png)
-	Lalu disini ip yang digunakan akan di rubah ke static terlebih dahulu dengan cara pilih ens33 lalu pilih Edit IPv4

![image16](https://user-images.githubusercontent.com/68781074/212051717-b44a0b10-7f46-4fdf-9424-888015fd87fa.png)
-	IPv4 Method ganti ke Manual

![image17](https://user-images.githubusercontent.com/68781074/212051750-2322b519-4347-412a-843d-1b7f7c7b4e91.png)
-	Masukan Subnet, IP Address, dll (menggunakan IP dari laptop/pc masing-masing) lalu save

![image18](https://user-images.githubusercontent.com/68781074/212051774-e66c3bb0-0fb9-4502-b2bd-04714155ffae.png)
-	Network yang digunakan sudah menjadi static lalu tekan Done

![image19](https://user-images.githubusercontent.com/68781074/212051792-6b412e3e-1631-40df-9a66-90b56ad6ad91.png)
-	Skip bagian Proxy Address dan Mirror Address

![image20](https://user-images.githubusercontent.com/68781074/212051812-8442de19-5353-43ef-b25b-2bc4c7d95089.png)

![image21](https://user-images.githubusercontent.com/68781074/212051845-5390115a-7beb-4d28-a187-7fe9aa523579.png)
-	Untuk Storage yang digunakan pilih Custom Storage Layout

![image22](https://user-images.githubusercontent.com/68781074/212051880-eb43631d-9ab1-4470-81b2-dfb890d3ecca.png)
-	Pilih Add GPT Partition

![image23](https://user-images.githubusercontent.com/68781074/212051909-37a3583b-c035-49c8-ba4c-2bdcf3db9612.png)
-	Untuk Swap menggunakan 4GB

 ![image24](https://user-images.githubusercontent.com/68781074/212051940-44cf7270-99d2-4efd-a85c-79d7c635ebd7.png)
-	Dan Untuk partisinya menggunakan sisa dari Swap

![image25](https://user-images.githubusercontent.com/68781074/212051967-cb4e4cd4-7d01-4fe5-a43d-c415a20e2e3e.png)
-	Lalu tekan Done

![image26](https://user-images.githubusercontent.com/68781074/212051985-965f3627-e42f-457b-a4ff-9bdebbe7c6bd.png)
-	Lalu tekan Continue untuk melanjutkan

![image27](https://user-images.githubusercontent.com/68781074/212052046-c2a0e911-aaab-4b74-85b3-505709b9ccf6.png)
-	Lengkapi pada bagian Profile Setup

![image28](https://user-images.githubusercontent.com/68781074/212052073-32350a54-cfa5-4cbc-9a6a-59e7d55e4169.png)
-	Centang Install OpenSSH Server

![image29](https://user-images.githubusercontent.com/68781074/212052096-852f3fe0-c328-4de7-b709-516ef78dd338.png)
-	Dimenu ini banyak pilihan software yang dapat diinstall, tapi kita skip ini terlebih dahulu dengan tekan Done

![image30](https://user-images.githubusercontent.com/68781074/212052116-5829455d-fc00-4b39-97ce-b40b58a06e25.png)
-	Installing System
-	Reboot Now

![image31](https://user-images.githubusercontent.com/68781074/212052127-7cd4966a-10f1-4fca-a104-eb72ad0ea3e0.png)
-	Proses Reboot

![image32](https://user-images.githubusercontent.com/68781074/212052142-5c425bbe-7adc-4c66-9f49-7c736b3d2c62.png)
-	Login menggunakan username dan password yang sudah dibuat

![image33](https://user-images.githubusercontent.com/68781074/212052157-95383759-6dcd-4a9f-b4d6-bf0480356bf9.png)
-	Untuk mengetes apakah terkoneksi ke internet atau tidak dapat melakukan PING ke DNS google.com

![image34](https://user-images.githubusercontent.com/68781074/212052175-62625cab-2d7a-4966-b398-99ee1fb09895.png)

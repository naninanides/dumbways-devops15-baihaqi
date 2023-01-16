# Application in Server
Task 3
1. Menjalankan aplikasi Webserver (nginx/apache2)
2. Menjalankan 3 aplikasi "hello world" menggunakan nodejs, golang dan python
3. Gunakan localtunnel untuk menjalankan "Hello world!" nodejs
Challenge :
Jalankan "Hello world" di python3 melalui port 5000 (gunakan flask), lalu akses dengan localtunnel
Gunakan PM2

1-	Menjalan kan aplikasi webserver (nginx/apache)
-	di task sebelumnya sudah pernah untuk menjalankan nginx, maka di task kali ini saya akan menjalankan aplikasi apache
-	terlebih dahulu untuk menginstall apache dengan command >sudo apt install apache2

![image1](https://user-images.githubusercontent.com/68781074/212092907-42b19f34-7b4e-4a2c-bd6b-6ea04a54b35a.png)


-	Kalau terdapat error seperti diatas, tandanya si apache ini bentrok dengan nginx, terlebih dahulu kita non aktifkan dulu nginxnya dengan cara sudo systemctl stop nginx dan untuk mengecek statusnya dengan cara sudo systemctl status nginx

![image2](https://user-images.githubusercontent.com/68781074/212092943-a9997fd3-80ad-44a9-b008-8fd474865226.png)

-	Lalu kita sudah bisa menginstall apache

![image3](https://user-images.githubusercontent.com/68781074/212092974-01afd4d1-9add-40ab-9df1-929495e4426f.png)

-	Setelah itu kita tinggal membuka apache di web dengan memasukan IP server dan hasilnya akan seperti ini
 
![image4](https://user-images.githubusercontent.com/68781074/212093001-56ce92d9-90a4-4386-8dbc-e400d459428d.png)

2-	Menjalankan hello word menggunakan 3 aplikasi “nodejs, golang, dan python”
-	Nodejs
(1)	Karena sebelumnya sudah menginstall nodejs untuk install localtunnel maka kita di sini tinggal menjalankan perinta npm init -y untuk menginstall package js

![image5](https://user-images.githubusercontent.com/68781074/212093016-a9662253-8cdd-403e-8ed9-0f5d89a20efb.png)

(2)	Lalu Langkah selanjutnya kita sudah bisa membuat file untuk aplikasi Hello Wordnya dengan perintah nano hello.js 

![image6](https://user-images.githubusercontent.com/68781074/212093040-b3d429bd-980a-442e-82f5-ebc38987eb72.png)

(3)	Lalu untuk menjalankan aplikasi sederhana yang kita buat, bisa kita lakukan perintah node hello.js

![image7](https://user-images.githubusercontent.com/68781074/212093050-ddb7ac86-8219-4978-aaa9-ae7cee76ee08.png)

(4)	Setelah itu kita masukan port dari node.js ini, karena portnya itu adalah 3000 maka kita buka di web dengan IP lalu ditambahkan dengan port dari node.js maka hasilnya akan seperti ini

![image8](https://user-images.githubusercontent.com/68781074/212093070-395c715e-53ef-40ed-8715-7962d20e50c7.png)

(5)	Kita sudah berhasil menjalankan aplikasi Hello word  menggunakan Node.JS

-	GOLANG
(1)	Langkah yang pertama kita lakukan disini adalah untuk mendownload dan menginstall Golangnya terlebih dahulu dengan perintah wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su 

![image9](https://user-images.githubusercontent.com/68781074/212093137-85442ad8-354c-45aa-8005-5954299ce0cf.png)

(2)	Lalu kita ekstrak package yang sudah kita download dari website golang  dengan perintah rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit

![image10](https://user-images.githubusercontent.com/68781074/212093163-4b4551a7-6b43-4e9d-ac66-c9f8da205b1f.png)

(3)	Lalu selanjutnya kita akan memasukan path go ke dalam .bashrc lalu masukan PATH di bagian paling bawah dan untuk scrip pathnya export PATH=$PATH:/usr/local/go/bin

![image11](https://user-images.githubusercontent.com/68781074/212093182-a4f9a45f-af53-436e-a429-c21a88d8996f.png)

(4)	Untuk mengecek apakah golang sudah terinstall dan melihat versionnya dapat mengetikan perinta go version

![image12](https://user-images.githubusercontent.com/68781074/212093200-1e25e8a5-b239-434f-b584-19f04c34ad4b.png)

(5)	Selanjutnya kita membuat file aplikasinya menggunakan nano hello.go

![image13](https://user-images.githubusercontent.com/68781074/212093218-5cf0ada9-3bd1-4db7-ba23-308215b55fa9.png)

(6)	Kita bisa mencoba untuk menjalankan aplikasinya menggunakan go run hello.go

![image14](https://user-images.githubusercontent.com/68781074/212093249-724bb99f-59bf-49a6-b6f0-2bab451b93a9.png)

(7)	Jika ingin membuild aplikasi tersebut kita bisa menjalankan perintah go build hello.go

![image15](https://user-images.githubusercontent.com/68781074/212093272-584e1176-e016-4e6b-a70d-c8a8cd0a0975.png)

(8)	Dan untuk menjalankan aplikasi yang sudah di build kita bisa menjalankan perintah ./hello

![image16](https://user-images.githubusercontent.com/68781074/212093292-f36ede3c-0b90-4602-b10a-518dd9f9d179.png)

-	Python
(1)	Untuk membuat aplikasi hello word menggunakan python cuku mudah, terlebih karena python sudah ada di ubuntu tanpa harus menginstallnya lagi cukup menggunakan perintah sudo apt update dan sudo apt upgrade

![image17](https://user-images.githubusercontent.com/68781074/212093307-0ee0bcff-ff0b-4894-9e6f-8251bab7d3b0.png)

(2)	Lalu untuk membuat aplikasi dengan menggunakan perinta nano hello.py dan untuk scrip yang digunakan hanya seperti yang di gambar.

![image18](https://user-images.githubusercontent.com/68781074/212093326-5d99039e-b1bf-491f-84e9-2d1b05dc6720.png)

(3)	Setelah itu di save dan kita jalankan aplikasinya menggunakan perintah python3 hello.py

![image19](https://user-images.githubusercontent.com/68781074/212093341-983e3152-7ef7-4db4-bb7f-f2b6da2ba996.png)

3-	Menggunakan localtunnel untuk menjalankan “hello world” nodejs
-	Membuka aplikasi hello word pada nodejs lewat localtunnel caranya cukup mudah, kita tinggal memakai aplikasi yang sebelumnya saja dan karena localtunnel sudah kita install juga sebelumnya maka yang diperlukan hanya untuk membuat link webnya dan juga membuka port nodejs
-	Menggunakan fitur split pada terminal dan membuka dua terminal agar saat menjalankan nodejs dan juga membuka port tidak bentrok

![image20](https://user-images.githubusercontent.com/68781074/212093356-3dc9a305-d051-4f20-90ce-30cd17db4d37.png)

-	Lalu tinggal kita akses lewat browser

![image21](https://user-images.githubusercontent.com/68781074/212093375-7f976513-2172-4ace-84f3-9b9689e06ce4.png)

-	Lalu ada untuk python bisa juga menggunakan flask untuk aplikasi python dengan memasukan scrip pada di gambar

![image22](https://user-images.githubusercontent.com/68781074/212093396-73393a22-f80e-486c-81b7-ce9b454a083a.png)

-	Dan untuk membuka aplikasi sederhana python yang menggunakan flask bisa melalui browser ataupun dengan curl pada terminal, biasanya kalau tidak bisa dibuka pada browser itu dikarenakan masih menggunakan localhost dimana hanya bisa dibuka pada servernya saja. Maka dari itu kita melakukan curl pada terminal untuk melihat isi dari aplikasi sederhana yang terlah di buat

![image23](https://user-images.githubusercontent.com/68781074/212093430-bd31b3aa-8fb2-49e0-859b-f7a3eab03bf1.png)

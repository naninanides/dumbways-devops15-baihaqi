## Networking & Linux Shell
Dumbways kelas 2

## 1.	Perbedaan IP Privat & IP Public
-	ip privat adalah IP yang dirancang untuk digunakan secara lokal dan biasanya sudah ditetapkan pada perangkat PC atau Laptop
-	IP Public adalah IP yang dirancang untuk digunakan secara global dan biasanya yang menetapkan IP public sudah dari ISP yang kita gunakan dan IP yang di dapat bisa berubah-ubah
## 2.	Perbedaan Clien to server & Peer to Peer
-	Client to server yaitu adalah penyedia jaringan yang berbasis jaringan yang dapat diakses oleh semua client computer, biasa digunakan untuk mendeploykan sebuah web service ataupun sebuah aplikasi dikarenakan memiliki akses dengan kecepatan yang tinggi dan untuk keamanan serta backup data lebih baik
-	Peer to peer ini adalah sebuah jaringan private dimana yang menjadi penyedia jaringan bukanlah sebuah server melainkan sebuah komputer yang digunakan oleh user masing-masing yang bertindak sebagai server ataupun client,
## 3.	Menjalankan NGINX di server Ubuntu 20.04 LTS
-	Terlebih dahulu login kedalam ubuntu server 

![image1](https://user-images.githubusercontent.com/68781074/212066622-05430e8e-0a48-4312-aa5e-5002845aed09.png)
-	Lakukan update terlebih dahulu menggunakan command sudo apt update

![image2](https://user-images.githubusercontent.com/68781074/212066664-9d7a8cad-a937-4b1b-b450-41ef5e4155ff.png)
-	Lalu setelah itu gunakan command sudo apt upgrade untuk melakukan installasi (disini tidak terjadi apa-apa karena sebelumnya sudah saya install untuk updatenya)

![image3](https://user-images.githubusercontent.com/68781074/212066692-1cead49e-0092-4153-98b2-28e6186cbd82.png)
-	Lalu periksa terlebih dahulu apakah aplikasi NGINX sudah terinstall atau belum dengan command sudo systemctl status nginx.service jika sudah terinstall maka tampilannya akan seperti ini

![image4](https://user-images.githubusercontent.com/68781074/212066715-b82ce672-659b-4cfe-acda-4113b1e87227.png)
-	Kalau belum terinstall tampilannya akan seperti ini

![image5](https://user-images.githubusercontent.com/68781074/212066731-601d34d4-581f-4a9b-a925-813e11abfeed.png)
-	Untuk menjalankan aplikasi NGINX menggunakan command sudo systemctl start nginx.service

![image6](https://user-images.githubusercontent.com/68781074/212066750-ec1725e9-3163-4f06-ba9f-891617b042fa.png)
-	Untuk mengecek apakah NGINX sudah berjalan atau belum bisa memasukan ip dari server kita kedalam browser

![image7](https://user-images.githubusercontent.com/68781074/212066928-6a85ff99-5637-4fb5-9529-8d8cd0dc3ae0.png)
## 4.	3 Command shell yang belum di presentasikan
-	Wget : command shell yang digunakan untuk mendownload suatu file
-	Sort : command shell yang digunakan untuk menyortir sebuah file
-	Find : command shell untuk mencari sebuah file ataupun directory

## 5.	Install node version manager dan jalankan nginx di Localtunnel
-	Pertama kita harus meremote ip kita terlebih dahulu dengan cara mengetik command ssh einzam(user)@192.168.1.25(IP). Nanti akan muncul Are You Sure You Want To Continue  Connecting lalu ketik Yes lalu nanti akan dimintai password dari server yang sudah di buat (sebelumnya saya sudah melakukan step ini jadi tidak ada ada pilihan tersebut)

![image8](https://user-images.githubusercontent.com/68781074/212067099-4b2102f0-b6b0-41d2-97c2-49ae58febfbf.png)
-	selanjutnya kita harus menginstal nvm terlebih dahulu dengan command linux curl tapi terlebih dahulu install curl

![image9](https://user-images.githubusercontent.com/68781074/212067166-5ed5d9df-62f4-4c97-94f7-80cf966d9984.png)
-	Lalu selanjutnya mendownload nvm menggunakan command linux
>curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

![image10](https://user-images.githubusercontent.com/68781074/212067199-c62505c3-39bf-42c6-b41b-9f5252d4c155.png)
-	Selanjutnya menginstall nvm menggunakan 
	>nvm install 14

![image11](https://user-images.githubusercontent.com/68781074/212067298-6b3866a8-cda2-461c-ac14-41b32c8281a7.png)
-	Lalu intall menginstall localtunnel dengan command npm yang sudah diinstall

![image12](https://user-images.githubusercontent.com/68781074/212067331-dd5b93c0-920b-462f-b81d-7544de98d893.png)
-	Lalu coba di akses nginx di browser menggunakan ip address server

![image13](https://user-images.githubusercontent.com/68781074/212067389-fef2c0f5-f68a-49d6-b638-08bad43d24f1.png)
-	Untuk menggunakan localtunnel pada aplikasi nginx yang sudah kita install, jalankan perintah
>lt –port 80

![image14](https://user-images.githubusercontent.com/68781074/212067413-30e985bd-91c7-414d-b0fe-399c17592a4b.png)
-	Kita akan mendapatkan url, kita bisa mengcopy url tersebut dan mengaksesnya di browser maka hasilnya akan seperti ini, lalu klik tombol click to continue

![image15](https://user-images.githubusercontent.com/68781074/212067436-d9f187df-9002-45b3-84dc-ee68ead25443.png)
-	Kalau berhasil, nanti akan diarahkan ke aplikasi nginx dan hasilnya seperti berikut

 ![image16](https://user-images.githubusercontent.com/68781074/212067477-4e9c3f1d-c7a5-443f-8187-29ef620e18f4.png)

 

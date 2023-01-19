# web server dan load balancing

### 1. Definisi Web Server
- Web Server adalah sebuah software yang memberikan layanan berupa data. Berfungsi untuk menerima permintaan HTTP atau HTTPS dari client atau di kenal dengan web browser (chrome atau firefox). Kemudian web server akan mengirimkan respon atas permintaan tersebut dalam bentuk halaman web.

### 2. Jalankan 2 VM
#### VM 1 : Jalankan aplikasi dumbflix-frontend
- untuk menjalankan aplikasi dumbflix-frontend, kita memerlukan file-file yang kita akan jalankan dan bisa di ambil dari repository pada [dumbflix-frontend](https://github.com/dumbwaysdev/dumbflix-frontend) kita akan mengclone kedalam server

![image](https://user-images.githubusercontent.com/68781074/213359453-4a88729e-804e-4617-9168-6f1cff461eb0.png)

- lalu setelah mengclone folder dumbflix-frontend kita perlu menginstall node terlebih dahulu

![image](https://user-images.githubusercontent.com/68781074/213359830-513ea094-3874-4d36-ad02-30adaf2b46a5.png)

![image](https://user-images.githubusercontent.com/68781074/213359845-be91505e-61e7-4171-8aaa-28b9ddad2417.png)

- setelah itu kita tinggal menjalankan aplikasi dumbflix-frontend

![image](https://user-images.githubusercontent.com/68781074/213359935-b857c0ee-f4a0-4ee1-955e-6d1bb5194646.png)

- lalu kita tinggal buka di web browser menggunakan IP dan port dari nodejs

![image](https://user-images.githubusercontent.com/68781074/213360048-c29daffa-e422-4582-b838-62f3fc25ff72.png)

### - untuk challange menjalankan aplikasi dengan pm2

- terlebih dahulu kita install pm2 di folder dumbflix-frontend global dengan perintah
> npm install pm2 --location=global 

![image](https://user-images.githubusercontent.com/68781074/213360803-233b725f-6e5e-4b87-b994-1dcabbc1ebb6.png)

- setelah terinstall kita bisa menjalankan aplikasi dumbflix-frontend menggunakan pm2

![image](https://user-images.githubusercontent.com/68781074/213360877-d04fd55a-6f71-4963-87c4-869af0c65a2b.png)

![image](https://user-images.githubusercontent.com/68781074/213360920-d1ceade1-babf-44d3-afb8-58292f1e07af.png)

#### VM 2 : Jalankan NGINX di server baru dan buat reverse proxy dengan 

- langkah pertama tentu kita akan menginstall terlebih dahulu nginx kalau belum ada pada server

![image](https://user-images.githubusercontent.com/68781074/213361120-088b2474-af8a-4993-af40-0ffdf8fd21d1.png)

- jika sudah terinstall langsung dapat di jalankan pada web browser menggunakan IP server

![image](https://user-images.githubusercontent.com/68781074/213361171-f0f61d9b-044c-4193-b647-a29dd5080c62.png)

- 

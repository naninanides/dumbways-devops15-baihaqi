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

### - buat konfigurasi reverse proxy menggunakan domain yang mengarah ke aplikasi pada VM 1
- langkah pertama kita masuk ke dalam folder nginx lalu kita buat directory dumbways

![image](https://user-images.githubusercontent.com/68781074/213384938-6ad52aff-c489-475c-9136-5f878ea4385e.png)

- setelah itu kita masuk kedalam folder yang sudah kita buat dan membuat file conf untuk reverse proxy dengan memasukan konfigurasi sebagai berikut dan IP yang digunakan adalah IP server dan menggunakan port 3000 karena kita akan menjalankan menggunakan nodejs

![image](https://user-images.githubusercontent.com/68781074/213385214-92016234-f365-4866-aaa5-bd5bcbcf6d69.png)

- lalu kita keluar dari folder dumbways, lalu kita mengedit file nginx.conf

![image](https://user-images.githubusercontent.com/68781074/213385377-738091b2-50b1-47eb-9590-e1b858bcdf01.png)

- disini kita menambahkan folder dari reverse proxy yang sudah kita buat tadi
- lalu kita cek apakah sudah berjalan konfigurasi yang sudah kita buat tadi

![image](https://user-images.githubusercontent.com/68781074/213385488-17768a0f-7903-4d3f-9e91-0f8bdf1b7cd5.png)

- lalu karena kita akan menjalankan domain di lokal kita perlu memasukan IP kita kedalam konfigurasi yang terdapat di folder C:\Windows\System32\drivers\etc (untuk Windows)
![image](https://user-images.githubusercontent.com/68781074/213364110-dfdd03db-1498-493c-8c26-7f2a9de226cd.png)

![image](https://user-images.githubusercontent.com/68781074/213385553-f51a99f6-14ff-4fb2-a6c4-67f01b784371.png)

- lalu kita save saja
- setelah itu kita reload nginx terlebih dahulu

![image](https://user-images.githubusercontent.com/68781074/213385677-08f0b24f-ba40-4c21-8cd2-3d9d3ce5adf9.png)
 
- lalu kita bisa kita cek di web browser menggunakan domain yang sudah kita buat tadi

![image](https://user-images.githubusercontent.com/68781074/213366636-88ee1c17-963a-4134-b813-dd1708f4d456.png)

- untuk membuat konfigurasi load balancer, kita bisa mengedit file bhq-rproxy.conf

![image](https://user-images.githubusercontent.com/68781074/213368622-f4270ca1-958b-4548-b5ba-a3ee2ebc599a.png)

- lalu jangan lupa untuk di restart/reload nginxnya dan di cek juga statusnya

![image](https://user-images.githubusercontent.com/68781074/213369049-2e46eef9-e3be-4a3c-9ef9-2d570b5ec3d0.png)

![image](https://user-images.githubusercontent.com/68781074/213369096-3b803816-23e4-4812-8c93-08d428720065.png)

- kita bisa mengecek apakah load balancer sudah berjalan atau tidak dengan menjalankan aplikasi nodejs

![image](https://user-images.githubusercontent.com/68781074/213386471-54385f4f-e4b0-4245-84b6-17b6d409942a.png)

![image](https://user-images.githubusercontent.com/68781074/213386567-8ef5a1fe-f7f9-443a-8c13-c6a8c882683c.png)


### 5. . Domain bisa diakses melalui web browser kalian

![image](https://user-images.githubusercontent.com/68781074/213385979-378903a3-e73c-4df6-8316-e45d588f64f0.png)


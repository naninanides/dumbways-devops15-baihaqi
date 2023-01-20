# Manage Server with Terminal

### 1. Apa itu terminal
- terminal adalah sebuah command promt atau shell yang dapat kita gunakan untuk membuat suatu file, membuat folder, bahkan membuat ataupun mengubah akses yang berbasis sebuah teks dan belum menjadi sebuah GUI (graphical unit interface)

### 2. Bash Scrip untuk update dan upgrade server lalu install aplikasi NGINX
- Untuk melakukan update dan upgrade menggunakan scrip BASH yang pertama kita lakukan adalah membuat file dengan format .sh dan juga scrip yang akan kita buat nanti menggunakan nano, kira-kira scripnya akan seperti ini.

![image](https://user-images.githubusercontent.com/68781074/212679596-f295086d-2284-43e4-a263-28d764d1538a.png)

- Lalu setelah itu kita save saja filenya, dan tinggal dijalankan saja scrip BASH yang sudah kita buat tadi

![image](https://user-images.githubusercontent.com/68781074/212679804-0d18a8e5-8416-40bf-8a56-917f7e24ab5b.png)

### 3.  BASH script untuk memberi akses ke port 22,80,443
- pertama kita akan membuat sebuah BASH sripnya terlebih dahulu untuk memberikan akses firewall ke port 22,80, dan 443 juga saya menambahkan akses untuk nginx

![image](https://user-images.githubusercontent.com/68781074/212647194-02de8260-562d-429f-a76f-dff6d93370ee.png)

- pertama kita cek terlebih dahulu apakah server kita sudah aktif atau belum firewallnya

![image](https://user-images.githubusercontent.com/68781074/212645503-21aaab4c-07ad-46fc-8d87-776d0350aa3b.png)

- jika belum aktif maka kita perlu mengaktifkannya terlebih dahulu

![image](https://user-images.githubusercontent.com/68781074/212647785-98017f5d-81be-4c2d-ad2f-4901a08769c5.png)

- kalau firewall sudah aktif maka kita tidak bisa melakukan remote untuk servernya

![image](https://user-images.githubusercontent.com/68781074/212647713-7ad58506-5912-4510-8e8b-36b8528fe38b.png)

- lalu yang kita lakukan setelah itu tinggal menjalankan scrip perintah untuk membuka akses server yang menggunakan port 22, 80, 443

![image](https://user-images.githubusercontent.com/68781074/212648047-7691c002-21e4-4153-9168-4015129aeb10.png)

- kita sudah bisa mengakses kembali servernya, dan sekarang server yang kita jalankan sudah terproteksi oleh firewall

![image](https://user-images.githubusercontent.com/68781074/212648302-5527fe7f-6c1d-47df-bf16-cd1a0ae10a74.png)

![image](https://user-images.githubusercontent.com/68781074/212648550-4f37dd89-bfc1-4300-8656-0725ac75ec84.png)

## 4. Text Manipulator (Cat,Grep,Echo & Sort)

-penggunaan Cat untuk melihat isi dari suatu file

![image](https://user-images.githubusercontent.com/68781074/212680384-6a876006-f0c2-4edd-8ab1-520031cd9fe4.png)

- adapun perintah Cat > (nama file) berfungsi untuk mengganti isi dari file tersebut tanpa menggunakan teks editor

![image](https://user-images.githubusercontent.com/68781074/212681138-9301404a-7d21-4547-868e-1fa280d3a0f4.png)

- ataupun untuk menambahkan sebuah teks kedalam file

![image](https://user-images.githubusercontent.com/68781074/212681361-3ea3fdb0-fcdc-406f-952d-b8353b34a3f4.png)

- lalu Fungsi Cat juga bisa digunakan untuk menggabungkan dari 2 file menjadi 1 file baru

![image](https://user-images.githubusercontent.com/68781074/212681504-ebdc6d98-8701-4021-b36f-e7306921bed8.png)

- Fungsi Grep digunakan untuk mencari suatu teks di dalam suatu file yang telah dibuat

![image](https://user-images.githubusercontent.com/68781074/212682138-81094561-d865-4e33-bfaa-f5a8e3d71030.png)

- dan jika fungsi grep di tambahkan dengan -c maka dia akan menghitung ada berapa kata yang terdapat dalam satu file

![image](https://user-images.githubusercontent.com/68781074/212682342-511e2537-7afc-4469-8f9b-6ea1b9f91e7f.png)

-  Lalu ada juga fungsi grep yang ditambahkan dengan * maka dia akan mencari semua file yang berisikan kata yang terdepat di teks

![image](https://user-images.githubusercontent.com/68781074/212682726-e3032ccf-d655-4c0f-a5b7-629c0d8cfe35.png)

- Lalu ada fungsi Echo, dimana perintah ini digunakan untuk mencetak teks kedalam terminal

![image](https://user-images.githubusercontent.com/68781074/212683323-38b8fb56-77ba-4872-ab0e-82c484f3da26.png)

- Fungsi echo juga dapat digunakan untuk mereplace teks yang ada didalam suatu file

![image](https://user-images.githubusercontent.com/68781074/212683789-5dcf14fd-74eb-4e57-a753-e54da9c87224.png)

- Lalu fungsi echo juga dapat digunakan untuk mmenyisipkan teks kedalam file

![image](https://user-images.githubusercontent.com/68781074/212684092-d8ca8782-e201-40a8-b3ca-4e7a18046f6d.png)

- Fungsi Sort digunakan untuk mengurutkan dari bilangan terkecil

![image](https://user-images.githubusercontent.com/68781074/212684609-5db53837-a9f9-4722-86ea-2e3cb3e5a27f.png)

- dan jika kita ingin membalik urutannya dari yang paling besar kita cukup menyisipkan fungsi -r saja

![image](https://user-images.githubusercontent.com/68781074/212684698-2dd21dca-37fd-441d-b4cb-7639ecbc24d2.png)


- Jika ingin mengganti kata dumbways menjad bootcamp dalam suatu file kita dapat menggunakan perintad sed -i 's/dumbways/bootcamp/g' file1

![image](https://user-images.githubusercontent.com/68781074/212685401-4b8fa926-a515-4de1-97d9-55c254f8aaf0.png)

## 5. Menggunakan NMON untuk tampilan CPU usage, RAM usage, Disk dan Resources OS & Proc

- pada terminal kita bisa langsung melakukan perintah nmon, dan jika nmon belum terinstall kita dapat menginstall menggunakan perintah sudo apt install nmon

![image](https://user-images.githubusercontent.com/68781074/212687091-d657d739-6c35-461a-9430-8b5b8eb4ff01.png)

- lalu jika sudah terinstal kita tinggal memasukan perintah nmon kedalam terminal, maka tampilan awalnya akan seperti ini

![image](https://user-images.githubusercontent.com/68781074/212687193-4c06d985-fea8-48a1-bf6c-7b89f7ddb357.png)

- karena kita ingin melihat tampilan CPU usage, RAM usage, Disk dan Resources OS & Proc maka kita tinggal memasukan perintah yang sudah di perlihatkan pada tampilan awal dari nmon tersebut:
- C untuk melihat CPU usage

![image](https://user-images.githubusercontent.com/68781074/212688199-5d09703c-bc63-4748-8efc-e18a700ba6c3.png)

- M untuk melihat Memory Usage atau RAM Usage

![image](https://user-images.githubusercontent.com/68781074/212688329-54ea4b3e-ff45-4298-a27b-05fae7b6f868.png)

- D untuk melihat Disk Usage

![image](https://user-images.githubusercontent.com/68781074/212688454-a08f3fcb-80da-4c23-9f9c-0224e8401a69.png)

- dan untuk melihat Resource yang digunakan dapat menggunakan command R

![image](https://user-images.githubusercontent.com/68781074/212688602-9171bfc4-5c5d-4cca-982c-b93a50dde725.png)

## 6. Challenge Install Node version manager menggunakan scrip bash dan jalankan node dengan kondisi ufw unable

- menggunakan teks editor nano untuk membuat scrip bash installing nvm

![image](https://user-images.githubusercontent.com/68781074/213597983-8e89385a-9212-499f-84f4-d97c6b23929a.png)

- lalu setelah itu kita jalankan scrip yang sudah dibuat untuk menginstall nvm

![image](https://user-images.githubusercontent.com/68781074/213598036-c1234c7a-ddd3-46dd-839a-02e6563b5ef6.png)

- selanjutnya jika ingin memberikan akses firewall ke dalam server, kita cukup menggunakan perintah sebagai berikut

![image](https://user-images.githubusercontent.com/68781074/213598234-c8f47b00-7ff8-4d99-ae49-6d8b53c14c3e.png)

- kita disini memberikan akses port dari nodejs dan juga python itulah kenapa kita memasukan port 3000 dan juga 5000

![image](https://user-images.githubusercontent.com/68781074/213598387-96b326e7-9d08-4e36-b8ee-2ea32d9367ba.png)

![image](https://user-images.githubusercontent.com/68781074/213598404-dcd8b458-f6c5-469d-b3d1-ef0982f16a39.png)

- untuk mengetesnya kita dapat menjalankan aplikasi nodejs di browser kita

![image](https://user-images.githubusercontent.com/68781074/213598468-443b9ec0-3454-4ee1-99e0-b828f02ab009.png)


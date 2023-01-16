# Manage Server with Terminal

### 1. Apa itu terminal
- terminal adalah sebuah command promt atau shell yang dapat kita gunakan untuk membuat suatu file, membuat folder, bahkan membuat ataupun mengubah akses yang berbasis sebuah teks dan belum menjadi sebuah GUI (graphical unit interface)

### 2. Bash Scrip untuk update dan upgrade server lalu install aplikasi NGINX
- Untuk melakukan update dan upgrade menggunakan scrip BASH yang pertama kita lakukan adalah membuat file dengan format .sh dan juga scrip yang akan kita buat nanti menggunakan nano, kira-kira scripnya akan seperti ini.

![image](https://user-images.githubusercontent.com/68781074/212644624-9498617e-c587-45da-957f-95f2b1a0be66.png)

- Lalu setelah itu kita save saja filenya, dan tinggal dijalankan saja scrip BASH yang sudah kita buat tadi

![image](https://user-images.githubusercontent.com/68781074/212644753-ef3c42b3-55b2-433a-bc1b-9847dac691ac.png)

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

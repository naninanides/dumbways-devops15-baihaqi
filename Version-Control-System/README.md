# Version Control System

## 1.  Jelaskan definisi distributed revision control! 
   - adalah sebuah tools yang digunakan untuk memanajemen perubahan dari code. Tools ini dapat membantu developer untuk mentracking setiap perubahan yang dilakukan            secara terus-menerus. pada dasarnya memiliki database terpusat yang bersifat online, jika ingin menggunakanya maka harus terhubung dengan jaringan.

## 2. Buat repository untuk tugas kalian di github
  - untuk pertama login dahulu kedalam akun git, lalu bisa di arahkan kursor ke arah menu (+) nanti di situ akan ada pilihan  new repository 

![image](https://user-images.githubusercontent.com/68781074/212219936-e04cdc01-d268-46b5-bb46-d458acecc651.png)

  - nanti untuk tampilan saat membuat new repository akan seperti ini, disini saya sudah membuat repository dengan format dumbways-devops15-baihaqi
  
  ![image](https://user-images.githubusercontent.com/68781074/212220288-dded185e-2c14-41dc-af9c-11dabdf531d5.png)

  - kalau misalkan belum membuat repository, maka akan di arahkan ke halaman berikut
  
  ![image](https://user-images.githubusercontent.com/68781074/212220681-095627e5-1548-4d2b-8495-dddc0999e9f9.png)

  - nah pada halaman ini, di bagian quick setup kita ubah dahulu dari https menjadi ssh karena link tersebut berguna nanti untuk meremote repository kita dari terminal
    dengan command (sebelumnya saya sudah meremote repository yang lain, makanya di sini commandnya sedikit berbeda)
    > git remote add origin git@github.com:naninanides/dumbways-devops15-test.git
  
  ![image](https://user-images.githubusercontent.com/68781074/212222949-78bfb9a2-2c62-49a7-923d-8d7509be48ca.png)

  - done. kita sudah membuat repository dan mengisi file kedalam repository dengan cara seperti pada gambar
  
 ![image](https://user-images.githubusercontent.com/68781074/212223437-661af83c-62ea-4b7f-9f2f-d3cf6ceaddd8.png)

  - maka repository kita akan terisi oleh file1 seperti pada gambar
  
  ![image](https://user-images.githubusercontent.com/68781074/212223504-5616a2bd-92e0-41f5-a76e-cbf101adc897.png)

## 3. Hubungkan ssh public key ke akun github

  - langkah pertama kita bisa melakukan perintah
  > ssh-keygen

![image](https://user-images.githubusercontent.com/68781074/212227337-7e5bc276-bf58-4bf8-ad1f-7fd98d34e8fe.png)

  - nanti akan terbuat file untuk ssh keynya, disini karena saya menamainya keygen maka yang muncul adalah keygen dan keygen.pub

![image](https://user-images.githubusercontent.com/68781074/212227702-ba824bed-a546-45e2-9b83-40a260c373bf.png)

  - lalu yang kita akan gunakan yaitu ssh yang keygen.pub
  
  ![image](https://user-images.githubusercontent.com/68781074/212227968-cddf29bf-d4a1-468d-aec0-46513ab8a419.png)
  
  
  - untuk memasukan sshnya kita bisa masuk ke setting

![image](https://user-images.githubusercontent.com/68781074/212228022-1da23eed-3755-4469-be1d-5a104a5b35b4.png)

  - lalu pilih SSH dan GPG key
  
![image](https://user-images.githubusercontent.com/68781074/212228071-6c5a8a8f-2ce3-4b79-b12b-a7d7eafcf521.png)

  - lalu klik new saja, nanti tampilannya akan seperti ini

![image](https://user-images.githubusercontent.com/68781074/212228210-b2f67f78-8341-4fe5-bc31-01b268ed2f7e.png)

  - nah kita ini key ini menggunakan ssd yang sudah kita buat tadi di terminal

![image](https://user-images.githubusercontent.com/68781074/212228296-030af78e-5ac6-47bd-9632-fe1f6ab5aef2.png)

  - selesai, kita sudah berhasil menghubungkan ssh public key ke dalam akun git

![image](https://user-images.githubusercontent.com/68781074/212228496-e13e02fc-2ea7-4d9d-8a30-1ba9ea6b9643.png)

  - untuk mengaktifkannya di terminal kita lalukan perintah
   > ssh -i ~/keygen -T git@github.com

![image](https://user-images.githubusercontent.com/68781074/212228665-667d7771-b9c6-4b03-902a-9c929331f257.png)

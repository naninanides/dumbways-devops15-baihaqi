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

  - nah kita isi key ini menggunakan ssh publick key yang sudah kita buat tadi di terminal

![image](https://user-images.githubusercontent.com/68781074/212228296-030af78e-5ac6-47bd-9632-fe1f6ab5aef2.png)

  - selesai, kita sudah berhasil menghubungkan ssh public key ke dalam akun git

![image](https://user-images.githubusercontent.com/68781074/212228496-e13e02fc-2ea7-4d9d-8a30-1ba9ea6b9643.png)

  - untuk mengaktifkannya di terminal kita lalukan perintah
   > ssh -i ~/keygen -T git@github.com

![image](https://user-images.githubusercontent.com/68781074/212228665-667d7771-b9c6-4b03-902a-9c929331f257.png)

## 4. Clone repository dumbflix-frontend & buat 3 branch

  -  langkah yang pertama kita buka repository yang akan kita clone
  
  ![image](https://user-images.githubusercontent.com/68781074/212247582-7c25c11a-cdd6-4088-bc81-0fb2bcd3787a.png)

  - lalu kita ambil code httpsnya untuk kita clone
  
  ![image](https://user-images.githubusercontent.com/68781074/212247635-2cad575f-5f9e-4640-8ef1-16ca23ae7771.png)

  - lalu kita clone repository tersebut lewat terminal dengan perintah 
   > git clone https://github.com/dumbwaysdev/dumbflix-frontend.git
   
   ![image](https://user-images.githubusercontent.com/68781074/212247812-14320039-71e2-4b15-ad64-f8887cd2c9f3.png)

  - lalu kita samakan apakah isi dari repositorynya sudah sama atau belum
  
  ![image](https://user-images.githubusercontent.com/68781074/212247936-b72c2629-5714-4796-b965-81ccf54fd44a.png)

  ![image](https://user-images.githubusercontent.com/68781074/212247944-a5472734-f008-406b-a30a-ef21c66a9200.png)

  - kalau kita ingin mencoba push ke repository yang sudah kita miliki, maka kita harus meremotenya terlebih dahulu
  
  ![image](https://user-images.githubusercontent.com/68781074/212248080-87ec37c8-9c76-41db-8976-cf18faefbfef.png)
  - kalau masih berupa https kita akan rubah terlebih dahulu ke ssh, karena kalau masih berupa link https kita tidak akan bisa melakukan push
  
  ![image](https://user-images.githubusercontent.com/68781074/212248280-326d4ae6-f39b-4555-a048-de6c0132b813.png)

  - maka dari itu kita rubah terlebih dahulu ke ssh
  
  ![image](https://user-images.githubusercontent.com/68781074/212248457-58e7ae6e-099f-4d46-b001-cca79f53c8a4.png)

  - nah kalau kita ingin mempush isi dari repository yang sudah kita clone, kita membuat repository baru terlebih dahulu lalu kita ubah remotenya menjadi ssh milik         repository yang baru kita buat
  
  ![image](https://user-images.githubusercontent.com/68781074/212250707-4170310e-e020-4700-ae42-4ac042364f79.png)

  ![image](https://user-images.githubusercontent.com/68781074/212250800-a75cdd21-bbf1-4daf-9088-d107a33c937b.png)
  
  - selanjutkan kita tinggal melakukan push ke dalam repository yang sudah kita buat tadi
  
  ![image](https://user-images.githubusercontent.com/68781074/212250866-ad0f23e1-dc7f-4980-8c29-8c5427513188.png)

  - done kit sudah melakukan clone repository
  
  ![image](https://user-images.githubusercontent.com/68781074/212250915-b6462a8d-b127-408f-8191-7a5c1b5ba905.png)

  
  - kita juga bisa membuat beberapa 3 branch baru menggunakan perintah
  > git branch (nama yang diinginkan)
  
  ![image](https://user-images.githubusercontent.com/68781074/212249389-59539ab9-7f86-4b92-8ebb-ee4759d25b8f.png)


# Terraform

## Jalankan Terraform di dalam local

1. langkah pertama yang kita lakukan adalah menginstall pada macos kita dapat mengikuti langkah yang sudah di sediakan oleh terraformnya seperti berikut

![image](https://user-images.githubusercontent.com/68781074/219845098-40f57649-8ba9-4517-96da-f71bce08aea9.png)

2. lalu kita sudah bisa menyiapkan untuk membuat scrip terraform kalau sudah berhasil menginstall

![Screen Shot 2023-02-18 at 13 41 51](https://user-images.githubusercontent.com/68781074/219845870-a393b9a8-cb2c-44fd-8801-2d06a7514179.png)

3. disini kita akan menginstall 2 VM dengan konfigurasi yang pertama adalah 2 core dan 2GB ram dan satu lagi 1 core dan 1GB ram

![Screen Shot 2023-02-18 at 13 47 56](https://user-images.githubusercontent.com/68781074/219845941-ace95432-3937-47a4-b916-4a614214192d.png)

![Screen Shot 2023-02-18 at 13 48 16](https://user-images.githubusercontent.com/68781074/219845954-74e0a769-e59d-4ddb-bedd-f3d19c2ec80a.png)

![Screen Shot 2023-02-18 at 13 48 24](https://user-images.githubusercontent.com/68781074/219845963-32136ff4-1c70-482f-98ae-d264a12fd1af.png)

4. lalu kita tinggal memasukan command terraform init

![Screen Shot 2023-02-18 at 13 49 11](https://user-images.githubusercontent.com/68781074/219846000-133cd772-7a71-432a-a387-3074b9743433.png)

5. sebelum kita menjalankan terraform scrip ini, kita akan melihat apa saja konfigurasi dari server yang akan kita buat menggunakan command terraform plan

![Screen Shot 2023-02-18 at 13 51 12](https://user-images.githubusercontent.com/68781074/219846082-5457a9b7-fe3b-4759-a902-8ccc667a31e8.png)

6. lalu kita bisa menjalankan terraform apply untuk menjalankan scrip terraform yang sudah kita buat tadi nanti akan di tanyakan untuk melanjutkan proses kita ketik yes saja

![Screen Shot 2023-02-18 at 13 52 23](https://user-images.githubusercontent.com/68781074/219846132-cdbd4cd7-808d-44e0-aa22-5757227224eb.png)

![Screen Shot 2023-02-14 at 13 57 00](https://user-images.githubusercontent.com/68781074/219846171-eba9360f-0599-4c68-9fa3-f49e39712559.png)

7. VM yang kita install melalui terraform sudah selesai

![Screen Shot 2023-02-18 at 14 00 15](https://user-images.githubusercontent.com/68781074/219846477-8a92227a-2467-47e3-8237-edb6452318cc.png)

![Screen Shot 2023-02-18 at 14 00 25](https://user-images.githubusercontent.com/68781074/219846480-7b000708-e454-4ae1-9524-b625e1d7dcc0.png)

![Screen Shot 2023-02-18 at 14 00 33](https://user-images.githubusercontent.com/68781074/219846490-98723457-17bd-4717-8a0e-594fd92b9747.png)

## membuat terraform scrip untuk GCP instance

1. langkah pertama kita bisa menyiapkan terlebih dahulu untuk terraform scripnya, kurang lebih seperti ini

![Screen Shot 2023-02-18 at 14 12 55](https://user-images.githubusercontent.com/68781074/219846988-31425d35-dee5-4faa-9cc7-12aa0c356fed.png)

![Screen Shot 2023-02-18 at 14 13 06](https://user-images.githubusercontent.com/68781074/219846999-1d15144e-58ba-4024-bed1-e1dcca8dbfab.png)

2. selanjut kita bisa melakukan terraform init dan plan untuk melihat terlebih dahulu apa saja yang akan di tambahkan resourcenya

![Screen Shot 2023-02-18 at 14 13 51](https://user-images.githubusercontent.com/68781074/219847022-a1315a23-326f-4aad-968f-77c3e1568477.png)

![Screen Shot 2023-02-18 at 14 14 02](https://user-images.githubusercontent.com/68781074/219847031-38da0ccb-3639-405a-adcd-fd3373fb063e.png)

![Screen Shot 2023-02-18 at 14 14 26](https://user-images.githubusercontent.com/68781074/219847051-bce817f6-7779-4593-af98-644a0e00316b.png)

![Screen Shot 2023-02-18 at 14 14 32](https://user-images.githubusercontent.com/68781074/219847054-81378100-0262-47d8-afba-73e8125524cf.png)

3. selanjutnya kita tinggal memasukan command terraform apply dan di Yes saja untuk melanjutkan prosesnya

![Screen Shot 2023-02-18 at 14 15 12](https://user-images.githubusercontent.com/68781074/219847076-eff243d6-90c0-41f5-b8af-0feb887ee18b.png)

![Screen Shot 2023-02-18 at 14 15 49](https://user-images.githubusercontent.com/68781074/219847094-0a3b6c35-68cf-4b68-bea9-0268cb8fcbb7.png)

4. instance yang kita buat tadi sudah ada di dalam GCP console dan sudah dapat kita gunakan

![Screen Shot 2023-02-18 at 14 16 42](https://user-images.githubusercontent.com/68781074/219847152-792f5500-b89e-49cd-8e7c-e2f8efff50b1.png)



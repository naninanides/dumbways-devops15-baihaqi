# Ansible

## Konfigurasi Ansible di local

1. pertama kita menginstall ansible terlebih dahulu di local kita, kita bisa mengikuti langkah-langkah yang sudah ada di dalam dokumentasi ansible
> https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

![Screen Shot 2023-02-18 at 14 27 53](https://user-images.githubusercontent.com/68781074/219847714-2e9b14e9-9e0c-40da-9750-40d453db331e.png)

https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

2. langkah pertama yang akan kita lakukan setelah menginstall ansible adalah melakukan setup untuk ansible.cfg dan juga file inventory

![Screen Shot 2023-02-18 at 14 31 12](https://user-images.githubusercontent.com/68781074/219847842-5ef5630b-7f98-41ff-a7b0-fd2a3817ff42.png)

3. untuk inventory kita akan memasukan ip dari target instance yang akan kita gunakan

![Screen Shot 2023-02-18 at 14 31 39](https://user-images.githubusercontent.com/68781074/219847877-c8fecee5-aca7-408d-9fd1-557540cd5342.png)

## membuat ansible playbook untuk appserver

1. langkah pertama yang kita akan install adalah menginstall docker lewat ansible playbook

![Screen Shot 2023-02-18 at 14 38 11](https://user-images.githubusercontent.com/68781074/219848168-09377c42-009f-495f-927c-47347aa9225a.png)

![Screen Shot 2023-02-18 at 14 38 21](https://user-images.githubusercontent.com/68781074/219848175-ec4dc241-6348-425a-b906-6f8c8a382483.png)

2. kita bisa mengecek syntax sudah benar atau belum menggunakan
> ansible-plabook nama_file --syntax-check

![Screen Shot 2023-02-18 at 14 44 10](https://user-images.githubusercontent.com/68781074/219848405-80df861f-5fca-46a5-8e66-9d4cd58062c7.png)

3. kita bisa menjalankan ansible playbook untuk menginstall doker terlebih dahulu

![Screen Shot 2023-02-14 at 23 40 12](https://user-images.githubusercontent.com/68781074/219848439-22f85cfc-a4e2-42d6-865d-267c0ddba8ae.png)

![Screen Shot 2023-02-18 at 14 49 42](https://user-images.githubusercontent.com/68781074/219848612-06a69e20-1417-4400-9061-52c55a8cf707.png)

4. lalu selanjutkan kita bisa membuat ansible playbook untuk pull dari repository docker dan menjalankannya lewat docker compose

![Screen Shot 2023-02-18 at 14 52 47](https://user-images.githubusercontent.com/68781074/219848738-a018f7c0-89ab-480e-b65d-7dfc019bf934.png)

5. karena kita akan menjalankan dengan docker compose saya di sini menyiapkan file docker compose yang akan di import kedalam instance dari local

![Screen Shot 2023-02-18 at 14 54 25](https://user-images.githubusercontent.com/68781074/219848817-73466a36-cc51-4f9b-b3cd-4e3a6d5d80b1.png)

6. lalu kita tinggal menjalankan saja ansible playbook yang sudah kita buat tadi

![Screen Shot 2023-02-16 at 17 58 21](https://user-images.githubusercontent.com/68781074/219848839-c1e1cb2f-5e35-4d85-8852-bdcf61e2da10.png)

7.aplikasi frontend kita sudah jalan on top docker 

![Screen Shot 2023-02-18 at 15 06 08](https://user-images.githubusercontent.com/68781074/219849351-85fb0194-5433-4236-8d2b-3d8812737efe.png)

![Screen Shot 2023-02-18 at 15 07 36](https://user-images.githubusercontent.com/68781074/219849445-63ce35ef-40b7-4627-aede-50cb34f11b4e.png)

## Ansible untuk Gateway

1. seperti sebelumnya kita tinggal siapkan saja ansible playbook untuk nginx dan juga konfigurasinya

![Screen Shot 2023-02-18 at 17 17 10](https://user-images.githubusercontent.com/68781074/219855037-cd12e2c7-ec00-4706-92d2-bf7e2f75d6fa.png)

![Screen Shot 2023-02-18 at 17 17 41](https://user-images.githubusercontent.com/68781074/219855056-58132115-0088-44e6-98e7-227b0ea0d16b.png)

![Screen Shot 2023-02-18 at 17 17 49](https://user-images.githubusercontent.com/68781074/219855071-490f8518-e984-4f2d-8195-97e166c8042c.png)

2. lalu jalankan seperti biasa ansible playbooknya

![Screen Shot 2023-02-16 at 17 54 57](https://user-images.githubusercontent.com/68781074/219855108-58537c1c-c4e1-4481-8e17-d52790166347.png)

3. bisa kita cek di dalam VM gatewaynya si nginx sudah terinstall atau belum

![Screen Shot 2023-02-18 at 17 23 21](https://user-images.githubusercontent.com/68781074/219855280-6f4d7ce8-5bbc-4064-9fd0-8346ee3b4f94.png)

4. dan untuk konfigurasi reverse networknya

![Screen Shot 2023-02-18 at 17 24 09](https://user-images.githubusercontent.com/68781074/219855317-b7b3ea03-511e-44a9-993b-31d61943ba07.png)

5. kita bisa cek apakah reverse proxynya sudah jalan atau blm

![Screen Shot 2023-02-18 at 17 24 46](https://user-images.githubusercontent.com/68781074/219855337-5d022f6a-cb60-47aa-a01f-0bc8471b1caa.png)


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

7. 

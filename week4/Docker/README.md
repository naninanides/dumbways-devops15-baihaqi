# Docker

## menjalankan Appserver menggunakan konfigurasi 2 CPU 2GB RAM 20GB

![image](https://user-images.githubusercontent.com/68781074/217252025-f1359fb8-90e5-4658-b724-54d232a75875.png)

## menjalankan Gateway menggunakan konfigurasi 1 CPU 1GB RAM 20GB

![image](https://user-images.githubusercontent.com/68781074/217252600-fd1086e7-1bb7-480b-b6ae-f1ee7d67725b.png)

## deploy aplikasi pada Appserver

1. instalasi docker didalam server

![image](https://user-images.githubusercontent.com/68781074/217256148-a62b9128-e879-4a2b-beb9-d932b82902e2.png)

2. buat konfigurasi Dockerfile untuk membuat image docker

![image](https://user-images.githubusercontent.com/68781074/217256539-6f264e03-512a-48b4-8322-74e78a3101f5.png)

3. lalu buat file docker compose dengan format YML

![image](https://user-images.githubusercontent.com/68781074/217256714-5ccf84b1-7a8f-45c1-a2d9-6c0a0be52a48.png)

4. lalu sebelum kita buat image, kita atur dulu config APInya menggunakan API yang sudah kita buat sebelumnya

![image](https://user-images.githubusercontent.com/68781074/217257050-44ea796b-32f7-4367-be3b-afcaed076da1.png)

5. lalu kita buat images untuk aplikasi frontend

![image](https://user-images.githubusercontent.com/68781074/217258080-eb6582fd-f0f9-4b21-ab4d-37800b19baa1.png)

6. lalu kita menjalankan docker images yang sudah kita buat tadi menggunakan 
  > docker compose up -d

![image](https://user-images.githubusercontent.com/68781074/217258543-9133f1d3-5ed4-427b-b4fb-2ed4d28285b2.png)

7. lalu saya akan membuat file docker compose untuk database yang akan kita gunakan nanti, disini saya buatnya di folder terpisahd dari frontend dan backend

![image](https://user-images.githubusercontent.com/68781074/217259007-868260f5-ba1c-4c45-842a-b8b0668c5b74.png)

8. lalu selanjutnya membuat file docker images dan compose di dalam folder backend

![image](https://user-images.githubusercontent.com/68781074/217259388-6b430e1b-5af8-4a31-92da-8ae0d09a8e94.png)

![image](https://user-images.githubusercontent.com/68781074/217259568-196bc882-8756-4b68-80ca-9f64fd02a51e.png)

9. sebelum kita menjalankan docker compose untuk database, kita akan merubah config yang berada didalam folder backend

![image](https://user-images.githubusercontent.com/68781074/217259859-bbd7b425-a369-4c1e-9c8f-8cf7a30702ae.png)

![image](https://user-images.githubusercontent.com/68781074/217259989-3d6ce6f4-35f3-48b2-8857-1db06ec802f6.png)

10. jika semua scrip sudah kita buat, kita bisa mengcompose database terlebih dahulu

![image](https://user-images.githubusercontent.com/68781074/217260622-dea1f992-e190-4c24-abb4-ce4e7d5a6779.png)

11. lalu setelah itu kita tinggal mengcompose images yang sudah kita buat tadi

![image](https://user-images.githubusercontent.com/68781074/217261278-35774f71-7b6d-40e7-bd60-8f132299b018.png)

![image](https://user-images.githubusercontent.com/68781074/217263152-0e76c629-89d2-4e68-b67e-4233a5847af8.png)

12. 

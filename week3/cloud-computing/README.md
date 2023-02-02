# Cloud Computing

## appserver - 1 CPU, 1GB RAM, 20GB Storage

![image](https://user-images.githubusercontent.com/68781074/215779283-99dacfb2-e700-4098-95b3-a8a9e3774136.png)

![image](https://user-images.githubusercontent.com/68781074/215779369-6cf6f6c1-b99c-41de-aff0-1e59cdcc9fba.png)

### Appserver : Jalankan aplikasi wayshub-frontend menggunakan nodeJS Gunakan PM2

1. lalukan ssh terlebih dahulu ke dalam server yang sudah kita buat di IDcloudhost

![image](https://user-images.githubusercontent.com/68781074/215781268-9f3cfe5d-523c-495d-b1de-9f6fc358d401.png)

2. lalu langkah selanjutnya setelah masuk kedalam server kita harus mengupdate terlebih dahulu dan menginstall aplikasi pendukung seperti nginx dan nodejs dan juga git (karena kita akan menjalankan aplikasi lewat nodejs dan git untuk mengclone reposity)

![image](https://user-images.githubusercontent.com/68781074/215781699-93fa8fd3-b33d-4ca8-a0e4-eb6247c4e7af.png)
![image](https://user-images.githubusercontent.com/68781074/215781940-09cddc42-d63f-4c18-9100-470dbe7c1031.png)
![image](https://user-images.githubusercontent.com/68781074/215785893-d18fc8d1-ff94-4c6e-90e5-47e4d379f361.png)
![image](https://user-images.githubusercontent.com/68781074/215785961-34ebb818-f3f0-4463-b5c1-a5c0a635383f.png)
![image](https://user-images.githubusercontent.com/68781074/215786484-c32d46f5-c9c7-4222-bbbd-fe14b5d28d1f.png)

3. setelah itu kita cek terlebih dahulu apakah nginx sudah berjalan atau belum

![image](https://user-images.githubusercontent.com/68781074/215786927-54585fc4-b9eb-46e7-80cc-cf9c6eb25acf.png)

4. lalu kita bisa langsung mengclone repositoty dari wayshub-frontend

![image](https://user-images.githubusercontent.com/68781074/215787335-e2eaf982-a0e0-4746-8469-233f7a02ecae.png)

5. lalu masukan command npm install di dalam folder wayshub-frontend

![image](https://user-images.githubusercontent.com/68781074/215789042-a5d24c97-5a82-455b-b4c8-e3820c7340ef.png)

![image](https://user-images.githubusercontent.com/68781074/215789127-51ba4914-d504-4e84-9199-a500df7d735c.png)

6. aplikasi waysub-frontend sudah dapat dijalankan

![image](https://user-images.githubusercontent.com/68781074/215789595-405809d5-d6d7-412c-a143-48ce2d68cf25.png)

7. untuk jalankan pm2 kita bisa menginstallnya setelah itu

![image](https://user-images.githubusercontent.com/68781074/215791394-b19987b9-b53c-4f93-9914-40b66dd8392c.png)

8. aplikasi wayshub-frontend sudah berjalan di pm2

![image](https://user-images.githubusercontent.com/68781074/215793284-f0ae7b19-6211-4c05-ae96-db12fabaf189.png)

## gateway - 1 CPU, 1GB RAM, 20GB Storage

![image](https://user-images.githubusercontent.com/68781074/215793924-1f931e53-b6d3-4604-b275-08440bb01a28.png)
![image](https://user-images.githubusercontent.com/68781074/215793840-c4767894-afcb-4c2c-89a8-8b202fe8b0a4.png)

1. seperti sebelumnya kita harus melakukan update terlebih dahulu lalu menginstall aplikasi seperti nginx, nodejs, dan git selanjutnya mengclone repository wayshub-frontned

![image](https://user-images.githubusercontent.com/68781074/216031653-103a1bbd-9f63-4dab-a536-398ea37e44a1.png)

![image](https://user-images.githubusercontent.com/68781074/216031875-406492f3-c4ca-45b7-aba9-e190482cd2c6.png)

2. setting reverse proxy dan lakukan pengecekan konfigurasi dari nginx dan setelah itu di restart nginx
 
![image](https://user-images.githubusercontent.com/68781074/216032077-3648b1e3-04ba-47ea-9a59-d199dbf087df.png)

![image](https://user-images.githubusercontent.com/68781074/216032127-e1e73766-51aa-4331-9c85-e4a6527d7bf8.png)

![image](https://user-images.githubusercontent.com/68781074/216032584-7463253b-8d6e-4553-a386-2026f4351e47.png)

3. lalu setelah itu menambahkan ip kedalam hosts

![image](https://user-images.githubusercontent.com/68781074/216032745-4068314c-933e-4ec4-81bf-879de4453ecc.png)

4. karena belum mendapatkan akses ke cloudflare maka di sini saya hanya akan melakukan curl di dalam terminal dengan hasil seperti ini

![image](https://user-images.githubusercontent.com/68781074/216033589-9959a0ea-57c5-4cb1-a905-f3d86148a288.png)

## Challenge : Firewall enable

1. pertama pastikan dahulu apakah firewall sudah berjalan atau belum

![image](https://user-images.githubusercontent.com/68781074/216036481-00b5f489-b022-416d-b72b-0bc4e35c8446.png)

2. lalu untuk mempercepat saya membuat bash scrip untuk membuka firewall ke port 22, 80, 443, 3000 dan 5000

![image](https://user-images.githubusercontent.com/68781074/216036741-b54efd86-c2d5-4560-9c2d-ef29b44b5b8f.png)

3. lalu jalankan saja bash scrip yang sudah kita buat tadi dan bisa di cek menggunakan command sudo ufw verbose

![image](https://user-images.githubusercontent.com/68781074/216037718-2a3ff7da-b426-4bab-aab4-9dbdf177d922.png)




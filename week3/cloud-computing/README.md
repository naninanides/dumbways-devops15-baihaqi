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

8. setelah itu lakukan npm run build terlebih dahulu untuk membuild packed dari wayshub-frontend

![image](https://user-images.githubusercontent.com/68781074/215791756-081fc2c1-a036-4e9d-9c11-e8c0121c8869.png)

9. aplikasi wayshub-frontend sudah berjalan di pm2

![image](https://user-images.githubusercontent.com/68781074/215793284-f0ae7b19-6211-4c05-ae96-db12fabaf189.png)

## gateway - 1 CPU, 1GB RAM, 20GB Storage

![image](https://user-images.githubusercontent.com/68781074/215793924-1f931e53-b6d3-4604-b275-08440bb01a28.png)
![image](https://user-images.githubusercontent.com/68781074/215793840-c4767894-afcb-4c2c-89a8-8b202fe8b0a4.png)


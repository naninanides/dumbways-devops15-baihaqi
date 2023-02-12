# CI/CD Jenkins

## install Jenkin on top docker

1. langkah pertama tentu kita akan menginstall docker terlebih dahulu, di sini saya menggunakan scrip yang sama untuk menginstall docker

![image](https://user-images.githubusercontent.com/68781074/218244092-9d67f8c1-7605-4468-acf0-8f1d3adbdb29.png)

2. lalu kita bisa menginstall jenkins on top docker menggunakan command seperti ini
> docker run -p 8080:8080 -p 50000:50000 --restart=on-failure -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts-jdk11

3. atau bisa juga menggunakan scrip untuk menginstall jenkins

![image](https://user-images.githubusercontent.com/68781074/218250168-ba6299f3-647e-4134-9aeb-dc4dd82ee59f.png)

4. lalu kita bisa login kedalam jenkinsnya

![image](https://user-images.githubusercontent.com/68781074/218246602-eab792a7-d377-4214-8261-ef50fc3f4871.png)

5. untuk password yang diminta kita bisa melihatnya menggunakan logs dari jenkins container

![image](https://user-images.githubusercontent.com/68781074/218246615-773b4a76-0e20-4e00-b165-81f0faedab71.png)

6. tampilan awal setelah login akan seperti ini, kita akan meilih select plugin to install

![image](https://user-images.githubusercontent.com/68781074/218246643-f90be7eb-ab47-4f70-8d97-fe8947fe68cb.png)

7. lalu kita cari sshagent dan kita pilih sshagent untuk plugin yang mau kita install

![image](https://user-images.githubusercontent.com/68781074/218246676-1e51c669-284f-4aa7-b109-ddc26c83438c.png)

8. proses installasi

![image](https://user-images.githubusercontent.com/68781074/218246762-9220d116-58d6-4324-a247-d0249d645a62.png)

9. masukan domain jenkinsnya

![image](https://user-images.githubusercontent.com/68781074/218250540-986ba855-8a3a-4fa6-b22b-d6a78f5c7131.png)

10. jenkins sudah selesai di isntall

![image](https://user-images.githubusercontent.com/68781074/218250548-fd9a4bc3-fa10-44da-ba6a-aa57e92c0955.png)

## setup jenkins

1. langkah pertama yang kita akan lakukan adalah setup untuk ssh credential jenkinsnya, kita bisa menggenerate ssh keynya terlebih dahulu

![image](https://user-images.githubusercontent.com/68781074/218247186-cf24404c-04ef-4639-9e30-bfc031846c98.png)

2. kita akan mengambil key dari ssh-keygen yang sudah kita generate tadi

![image](https://user-images.githubusercontent.com/68781074/218247215-779e49d5-a14f-416f-859f-0d2f8c99e6e3.png)

3. lalu pada dashboard klik manage jenkins lalu pilih manage credentials dan akan menambahkan credential untuk jenkins

![image](https://user-images.githubusercontent.com/68781074/218247270-3d9aef10-cf4f-43f6-8bfc-e1f0095a969f.png)

![image](https://user-images.githubusercontent.com/68781074/218247286-44b7ccf6-938c-4f63-8516-05adbacfce73.png)

![image](https://user-images.githubusercontent.com/68781074/218247288-5447eb71-0f0f-4c43-8660-d6c4cc536b27.png)

4. klik add credentials

![image](https://user-images.githubusercontent.com/68781074/218247297-9f410af5-3167-4d82-a84d-d7971c72d942.png)

5. lalu kita masukan form untuk new credentialsnya

![image](https://user-images.githubusercontent.com/68781074/218247348-0bcbfda2-7e26-4801-af59-6b4fadc5393e.png)


6. lalu selanjutnya kita akan memasukan public key kedalam akun git

![image](https://user-images.githubusercontent.com/68781074/218296833-3e5b757d-bc21-47f5-a32b-1a0dd7a43f3d.png)

![image](https://user-images.githubusercontent.com/68781074/218296859-c88d587e-badc-4b19-b110-ba6e86372ca6.png)

## membuat pipeline

1. untuk membuat pipeline bisa klik new item

![image](https://user-images.githubusercontent.com/68781074/218297075-bb2558ac-2b47-4c4a-a561-973484b8091d.png)

2. di setting general kita centang Github hook trigger dan pada pipeline kita pilih pipeline scrip from SCM

![image](https://user-images.githubusercontent.com/68781074/218297155-e122a722-689a-4bbf-8ba6-ac6712ee891f.png)

![image](https://user-images.githubusercontent.com/68781074/218297191-9b8ec4bd-8f2a-4673-8027-983b9bef6bba.png)


3. lalu kita siapkan file jenkinsnya

![image](https://user-images.githubusercontent.com/68781074/218297203-9d29fbc3-15f0-48ac-8563-7dfa8fcda6dd.png)

![image](https://user-images.githubusercontent.com/68781074/218297207-03a55122-34d5-40b7-a37d-13577bc73bac.png)

4. karena kita menggunakan notification discord maka ada scrip yang sudah di buat oleh plugin discord pada jenkins dapat di akses melalui

![image](https://user-images.githubusercontent.com/68781074/218297249-c8e6a196-77ab-43a1-a284-e847f6b276ca.png)

![image](https://user-images.githubusercontent.com/68781074/218297257-903579ba-b90d-4145-ac0b-3c0b6fb8a232.png)

5. untuk webhook URL bisa masuk kedalam discord dan chanel yang akan kita taruh bot untuk notificationnya

![image](https://user-images.githubusercontent.com/68781074/218297271-ff3f5626-9e74-48fc-b46e-c70193596921.png)

![image](https://user-images.githubusercontent.com/68781074/218297276-fd9f1b86-87b6-4947-adb0-815b812f89dd.png)

![image](https://user-images.githubusercontent.com/68781074/218297279-cd07a461-d354-4de5-92ee-18fa51e46d35.png)

6. isi saja formnya sesuai yang diinginkan

![image](https://user-images.githubusercontent.com/68781074/218297303-3e033302-f838-4637-8551-b5d05866bac4.png)

7. lalu klik generate saja maka akan keluar scrip untuk notif discordnya

![image](https://user-images.githubusercontent.com/68781074/218297358-85ef6ce9-08a8-4210-9b65-4f2bc85824fa.png)

8. lalu kita tinggal masukan saja di dalam scrip Jenkinsfile

![image](https://user-images.githubusercontent.com/68781074/218297373-8d6e4e3f-fd15-4dc3-99bc-b3a3edf3399f.png)

9. lalu kita atur webhook didalam repository github bertujuan agar jika ada perubahan pada repository dia akan otomatis memproses di jenkinsnya

![image](https://user-images.githubusercontent.com/68781074/218297417-c73096c8-a719-4bd4-981a-fedc59f65bba.png)

10. kalau sudah berhasil maka akan seperti ini

![image](https://user-images.githubusercontent.com/68781074/218297426-45c5bb5b-75ec-464b-a6eb-4a43c89277a6.png)

11. karena sudah selesai untuk mensetting jenkins dan github kita bisa langsung memasukan scrip kedalam Jenkinsfile

![image](https://user-images.githubusercontent.com/68781074/218297460-29e35890-274c-48c4-a51c-22f0978e58aa.png)

12. pipeline sedang berjalan dan notif discord sudah aktif

![image](https://user-images.githubusercontent.com/68781074/218297482-dbfebc69-4df3-4035-a639-bcc42c66caed.png)

13. Notification Discord sudah berjalan dengan baik

![image](https://user-images.githubusercontent.com/68781074/218297525-6d6dcc0f-8f87-4478-9ba5-2b38247c4657.png)

## push kedalam docker hub
1. pertama kita harus login kedalam docker hub dulu di dalam terminal

![image](https://user-images.githubusercontent.com/68781074/218297850-52a18390-07bc-4d8d-9650-5f1d08cf595c.png)

2. lalu kita buat scrip untuk docker push seperti ini

![image](https://user-images.githubusercontent.com/68781074/218298011-ebc151fa-6775-47c4-97e2-dc5eec81914f.png)

3. 

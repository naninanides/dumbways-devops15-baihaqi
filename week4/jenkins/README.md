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

2. di setting general kita centang Github hook trigger 

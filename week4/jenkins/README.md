# CI/CD Jenkins

## install Jenkin on top docker

1. langkah pertama tentu kita akan menginstall docker terlebih dahulu, di sini saya menggunakan scrip yang sama untuk menginstall docker

![image](https://user-images.githubusercontent.com/68781074/218244092-9d67f8c1-7605-4468-acf0-8f1d3adbdb29.png)

2. lalu kita bisa menginstall jenkins on top docker menggunakan command seperti ini
> docker run -p 8080:8080 -p 50000:50000 --restart=on-failure jenkins/jenkins:lts-jdk11

3. atau bisa juga menggunakan scrip untuk menginstall jenkins

![image](https://user-images.githubusercontent.com/68781074/218246018-1fc50733-4f43-4542-a795-235089f64751.png)

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

![6a21daeb](https://user-images.githubusercontent.com/68781074/218247119-5c33d3df-cbec-4dfe-bee4-9676d61edf55.png)

10. jenkins sudah selesai di isntall

![b530d4f2](https://user-images.githubusercontent.com/68781074/218247136-9fdccd7a-03e2-447c-bbb8-fd109f2f5656.png)

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


6. 


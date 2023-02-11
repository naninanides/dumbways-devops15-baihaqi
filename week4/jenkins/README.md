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

9. 

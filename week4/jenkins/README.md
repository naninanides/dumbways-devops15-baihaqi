# CI/CD Jenkins

## install Jenkin on top docker

1. langkah pertama tentu kita akan menginstall docker terlebih dahulu, di sini saya menggunakan scrip yang sama untuk menginstall docker

![image](https://user-images.githubusercontent.com/68781074/218244092-9d67f8c1-7605-4468-acf0-8f1d3adbdb29.png)

2. lalu kita bisa menginstall jenkins on top docker menggunakan command seperti ini
> docker run -p 8080:8080 -p 50000:50000 --restart=on-failure jenkins/jenkins:lts-jdk11

3. atau bisa juga menggunakan scrip untuk menginstall jenkins

![image](https://user-images.githubusercontent.com/68781074/218246018-1fc50733-4f43-4542-a795-235089f64751.png)

4. 

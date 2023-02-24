# Kubernetes

## install minikube dan docker

1. langkah pertama yaitu menginstall docker terlebih dahulu

![Screen Shot 2023-02-23 at 21 15 32](https://user-images.githubusercontent.com/68781074/220932738-42d7ad91-855e-4904-b98f-1d0cdec5f917.png)

2. setelah kita menginstall docker kita baru dapat menginstall minikubenya karena minikube tidak akan bisa jalan tanpa adanya docker 

![Screen Shot 2023-02-20 at 14 43 54](https://user-images.githubusercontent.com/68781074/220932918-be596b77-ea96-4efa-adc6-36a173a5a246.png)

3. langkah pertama yang bisa kita coba adalah menggunakan perintah
> kubectl get pods -a

![Screen Shot 2023-02-20 at 14 46 47](https://user-images.githubusercontent.com/68781074/220933338-8d5c28c5-7fce-4c4a-8bd7-1e04f7388186.png)

4. kita bisa mengikut langkah-langkah pada dokumentasi [minikube](https://minikube.sigs.k8s.io/docs/start/)

![Screen Shot 2023-02-23 at 21 20 35](https://user-images.githubusercontent.com/68781074/220933861-e3f72867-72e6-4a8e-a59e-0fe9683614ad.png)

![Screen Shot 2023-02-23 at 21 20 56](https://user-images.githubusercontent.com/68781074/220933930-26940e37-42a8-4ce6-90b2-9679f9870904.png)

![Screen Shot 2023-02-23 at 21 21 07](https://user-images.githubusercontent.com/68781074/220933978-d5cc41ad-b3ab-4ba9-8480-8329eca39995.png)

![Screen Shot 2023-02-23 at 21 34 13](https://user-images.githubusercontent.com/68781074/220937250-8522f10b-5a16-478e-b1ad-55923e908ab5.png)

## Deploy aplikasi frontend

1. siapkan file .yml untuk deployment dan service frontend

![Screen Shot 2023-02-23 at 21 39 57](https://user-images.githubusercontent.com/68781074/220938693-dfc94ce8-318c-4ba4-9ea6-267c2e79eddd.png)

2. lalu kita bisa mengcreate untuk aplikasi frontend

![Screen Shot 2023-02-23 at 21 41 40](https://user-images.githubusercontent.com/68781074/220939146-f2a65928-650e-44da-8078-7fd228960252.png)

3. kita cek terlebih dahulu dengan perintah
> kubectl get all

![Screen Shot 2023-02-23 at 21 43 15](https://user-images.githubusercontent.com/68781074/220939526-d0912c38-7e31-4c9a-b088-00c84108f613.png)

4. kita bisa melakukan perintah berikut untuk membuka aplikasi frontend kita yang sudah di deploy
> minikube service frontend

![Screen Shot 2023-02-23 at 21 44 55](https://user-images.githubusercontent.com/68781074/220939984-de6a7c6b-70d5-47e8-9aea-21c880006b6a.png)

5. aplikasi kita sudah terdeploy

![Screen Shot 2023-02-20 at 15 58 09](https://user-images.githubusercontent.com/68781074/220940082-141d43d7-63d5-44c3-b8a7-c9aad2112960.png)

6. disclaimer. karena saya menjalankan minikube ini di dalam localhost maka aplikasi yang terdeploy tidak dapat di akses dari luar karena ip yang digunakan adalah ip private dari localhost saya 

## Deploy Backend menggunakan stateless

1. untuk mendeploy backend menggunakan staless sebenernya scripnya tidak jauh berbeda dengan frontend

![Screen Shot 2023-02-24 at 7 50 50](https://user-images.githubusercontent.com/68781074/221064973-aa767a9f-25e1-4ac2-85fd-a4a8b4307e67.png)

2. lalu kita tinggal create deployment dan servicenya

![Screen Shot 2023-02-24 at 7 52 04](https://user-images.githubusercontent.com/68781074/221065126-2fa1d158-73fd-46c9-bc97-03549cbd487c.png)

![Screen Shot 2023-02-24 at 7 52 42](https://user-images.githubusercontent.com/68781074/221065214-357ffe57-f1c6-4d58-8928-cc43a2d8ddd5.png)


3. lalu langsung kita jalankan saja dengan minikube service

![Screen Shot 2023-02-24 at 7 53 05](https://user-images.githubusercontent.com/68781074/221065273-24f67f16-4954-411b-abae-42ba1189464c.png)


![Screen Shot 2023-02-24 at 7 53 20](https://user-images.githubusercontent.com/68781074/221065292-19d876b3-217b-494a-8101-bebc5a7e3767.png)


## Deploy Mysql menggunakan Statefull



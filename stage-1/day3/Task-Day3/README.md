# Syarat tugas :
## - Membuat repostiory di GitHub dengan nama "devops20-dumbways-<nama>"
## - Membuat folder task per harinya dengan file "README.md" (bisa dibuat per folder/directory)

# Task :
## 1. Cari perbedaan antara distro Ubuntu dan CentOS!

| Ubuntu        | CentOS        |
| ------------- |-------------| 
| Sering diupdate|Jarang Diupdate| 
| Lebih banyak pengguna dan komunitas developer|Lebih sedikit pengguna dan komunitas developer
| Bantuan lebih banyak, msalnya tutorial dan panduan gratis |tidak banyak bantuan yang disediakan| 
| Lebih mudah dipahami oleh pemula yang sebelumnya sudah pernah menggunakan Ubuntu desktop|Sulit dipahami oleh pemula karena distro  desktop yang dikeluarkan oleh RHEL tidak begitu banyak|
|Paket .deb diinstall menggunakan paket manager apt-get|Paket .rpm diinstall menggunakan paket manager yum|

## 2. Apa perbedaan dari CLI & GUI?
Indikator | CLI        | GUI        |
| ------------- | ------------- |-------------| 
| Layar|Sering terjadi pembaruan (upgrade)|Antarmuka stabil dan konsisten| 
| Penggunaan perintah| Menggunakan grafis dan visual|Hanya menggunakan teks|
| Pengoperasian| Lebih mudah sebab tidak perlu coding |Lebih kompleks dan membutuhkan skill coding| 
| Ruang penyimpanan| Membutuhkan ruang penyimpanan yang besar|Tidak membutuhkan ruang penyimpanan yang besar|
|Performa| Kinerja dan performa lebih lambat | Kinerja dan performa lebih cepat|
|Perangkat|Membutuhkan banyak perangkat seperti mouse, keyboard, dan sebagainya|Tidak membutuhkan banyak perangkat, hanya perlu keyboard|
|Tampilan|Dapat diubah agar lebih menarik|Tidak dapat diubah|
|Konektivitas|Mudah terhubung dengan perangkat lain|Lebih rumit dalam mengakses perangkat lain sebab membutuhkan izin|

## 3. Di VM masing-masing :
### 3a. Install nginx, lalu akses melalui browser/ `curl <ip kalian>`
![3a.install nginx](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/d87b4f314861597a8c7a813b6e69b2fde1bec9c5/week1/day3/Task-Day3/subject-matters/3a.%20install%20nginx.png)

### 3b. Ganti IP address kalian (bebas) lalu akses kembali nginx (`/etc/netplan`)

sebelum ke step 1, lakukan systemctl stop nginx. 

***step 1 : lakukan perubahan ip address di network adapter interface***
![3b.change-ip1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/d87b4f314861597a8c7a813b6e69b2fde1bec9c5/week1/day3/Task-Day3/subject-matters/3b.change%20ip-1.png)

###Note: jangan lupa untuk command *sudo net apply* setelah melakukan perubahan ip address

***step 2 : setelah configurasi perubahan ip address, lakukan systemctl start nginx kembali, lalu cek statusnya dengan command systemctl status nginx***

![3b.change-ip2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/d87b4f314861597a8c7a813b6e69b2fde1bec9c5/week1/day3/Task-Day3/subject-matters/3b.change%20ip-2.png)

***step 3 : akses kembali nginx, menggunakan ip address yang sudah diubah tadi***
![3b.change-ip3](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/d87b4f314861597a8c7a813b6e69b2fde1bec9c5/week1/day3/Task-Day3/subject-matters/3b.change-ip3.png)

## 4. Terangkan fungsi systemctl dan contoh commandnya (gunakan nginx)

***Systemctl adalah mengelola dan berinteraksi dengan sistem systemd dan manajer layanan . secara generalnya kita bisa melakukan penginstallan service, menghentikan serivce, dan melihat status service yang terpasang di distribusi linux kita.***

***contoh command systemctl***
![4.systemctl](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/d87b4f314861597a8c7a813b6e69b2fde1bec9c5/week1/day3/Task-Day3/subject-matters/4.systemctl%20.png)

# Challange :

## 1. Rubah nama hostname menjadi "dumbways"
   
   a. Before

   ![a.before](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/64d89305b30378389138d7efceea35383ff56323/week1/day3/Task-Day3/challange/before.png)

   b. After

   ![b.after](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/64d89305b30378389138d7efceea35383ff56323/week1/day3/Task-Day3/challange/after.png)

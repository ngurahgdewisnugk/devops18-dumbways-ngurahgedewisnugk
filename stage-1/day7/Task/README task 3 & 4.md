# 3. Jelaskan apa itu load balance.

   Load Balancing adalah suatu jaringan komputer yang menggunakan metode untuk mendistribusikan beban kerjaan pada dua atau bahkan lebih suatu koneksi jaringan secara seimbang agar pekerjaan dapat berjalan optimal dan tidak overload (kelebihan) beban pada salah satu jalur koneksi.

   Tujuannya adalah Jika kita memiliki website atau aplikasi yang telah digunakan hingga ribuan, ratusan atau bahkan jutaan pengguna maka kita harus melakukan load balancing pada aplikasi tersebut agar tidak down, karena beban akses pengguna dibagi ke beberapa server sekaligus.
   
# 4. implementasikan load balancing kepada aplikasi wayshub yang telah kalian gunakan.

* Pertama, di local kita, buat server lebih dari satu, disini saya implementasikan dalam 2 server dengan vm yang berbeda :

  - Server1 : menggunakan VMWare, dengan ip : 192.168.18.111 dan hostname : *dumbways*
    ![server1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/96343386-0618-4ca7-9b8d-c9399f215d87)

  - Server2 : menggunakan VirtualBox, dengan ip : 192.168.18.113 dan hostname : *ngurahdevops*
   ![server2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/8fc57e4c-2154-4bdc-bfe2-8297f59cf774)

* Kedua, lakukan instalasi aplikasi nodejs seperti server1 (*dumbways*) di server2 (*ngurahdevops*), dan deploy aplikasi, disini saya lakukan proses instalasi menggunakan bash script :
   ![bash-script install ](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/ee3d0af5-3233-40ff-b262-54ab566413cf)

  Setelah itu jangan lupa di cek versioning-nya (disarankan sama setiap server) disini saya jalankan cek menggunakan bash-script:
  - Server1 :

    ![version1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/74df2a1f-83b7-4fc1-8b4a-446d22c0c215)
    
  - Server2 :

    ![version2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/cc96484b-30c3-4cfc-a349-28a0dc9c1c34)

* Ketiga, Setelah itu kembali ke server1, lalu lakukan edit config yang sudah kita buat pada server1 dan buat konfigurasi seperi berikut untuk balancing:

 ![config load-balancing](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/5ae9ddf1-45e4-42f2-8a58-7a1117225c25)


* Keempat, pastikan lakukan pengecekan konfigurasi dengan melakukan command berikut, untuk memastikan konfigurasinya sudah **OK** dan **successfull** :

   ![cek-nginx](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/f457a806-4e20-4cd0-8a4c-aff85e2c3345)

* Kelima, setelah di cek dan statusnya **ok** dan **successfull**, lakukan command berikut agar service **nginx** kita merefresh systemnya dengan konfigrasi terbaru kita :
  ![nginx-service](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/b2d6b46c-6f9d-4cd8-9317-2e0dc0f426c7)

* Keenam, setelah itu lakukan update *etc/hosts* di local client kita, karna local client saya adalah os Windows, saya lakukan di local etc/host di direktori berikut *C:\Windows\System32\drivers\etc* :
  ![/etc/hosts](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/aa497474-2d4d-45e2-9ea2-c7fc9e3cd3e4)

* Ketujuh, jalankan aplikasi wayshubnya dengan command **npm run start** di kedua server (jangan lupa *change directory* ke direktori aplikasinya:

![image](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/a8d36340-e587-4b89-8240-2e2c02e6d4e0)

* Kedelapan, open browser dan akses domainnya :
  
  ![image](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/cb8eae20-c0ea-40af-9e19-7ecedca11a90)

* Kesembilan, setelah itu coba pastikan matikan aplikasi di server1 :
  ![dead-server1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/a2542199-3b91-4fc9-8b58-39af6483a225)

* Kesepuluh, apabila masih bisa diakses, sekarang coba matikan aplikasi di server2 :
  ![dead-server2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/ed9d0196-4dfc-4315-9e3b-f34db918badc)

Setelah dimatikan, kembali ke page **502 Bad gateway**, artinya konfirgurasi load balancing kita sudah sesuai ekspetasi. 




 


  


    
   



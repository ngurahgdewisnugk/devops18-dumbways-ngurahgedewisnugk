## Task 1 

a.	dir1 ==> file1 dan file2

b.	dir2 ==> file3 dan file4 

c.	dir3 ==> file5 dan file6  

![task1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/blob/df02248384060f5ba71fd1931554ea0500956f0f/stage-1/day4/img/task1.png)

## Task 2

* Step 1 : Cat

  untuk melihat isi file
  
  `Cat dir1/file1`
  
  ![cat](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/a80b324a-398d-49eb-a1ac-84eab3ecb26a)

  untuk menggabungkan 3 file ke 1 file

  `Cat dir1/file1 dir1/file2 dir2/file4 > dir3/file5`

  `Cat dir3/file5`
  
   ![combine](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/fa1d12e7-34ba-46bf-9e4a-24a4efb42c87)

* Step 2 : Sed

  Mengubah kata “Saya” menjadi “Nama Saya”

  `sed -i 's/Saya/Nama Saya/g' dir1/file1`

  ![sed](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/2321a540-2d95-47c1-b5a9-97e41bbe0898)

* Step 3 : Grep

  Mencari kata “Bootcamp” pada dir1/file2 

  `Grep Bootcamp dir1/file2`

  ![grep](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/0e1e8629-36b0-414d-a082-9fcbd9cf28ab)

  Menghitung Jumlah kata “Bootcamp” pada dir1/file2

  `grep -c Bootcamp dir1/file2`

  ![dir1/file2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/ac8bcada-6a13-430c-8bb9-3bed5eaa6c70)

  Mencari semua file dalam dir1 yang berisi kata “Bootcamp”

  `Grep Bootcamp dir1/*`

  ![Bootcamp](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/980040a0-0f7b-4bde-ba70-28660cbd9854)

  Step 4 : Sort

  Mengurutkan data angka berdasarkan ascending dalam direktori 2 file 3

  `sort dir2/file3`

  ![sort1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/08fa5c4a-8c09-422a-995c-985c3f923bd0)

  Mengurutkan data angka berdasarkan descending dalam direktori 2 file 3

  `sort -r dir2/file3`

  ![sort2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/02ea093e-090e-492a-b829-923348d5d75f)

  Step 5 : Echo

  Untuk mencetak string “semoga sukses dan lancar”

  `Echo “semoga sukses dan lancar”`

  ![echo1](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/27971474-77cc-4151-a821-e1e97f91ae0d)

  Untuk mencetak string “semoga sukses dan lancar” di dir2/file6

  `Echo “semoga sukses dan lancar” >> dir2/file6`

  ![echo2](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/5b9a9c51-3984-4c80-ae94-774e044ff628)

  untuk mereplace semua data di dir2/file6 dari “semoga sukses dan lancar” menjadi **"semoga sukses, lancar dan bahagia"**

  ![echo3](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/81780f64-4d71-4676-9e7b-78acec666e8d)

## Task 3 
  
  **A. HTOP**
  
  htop merupakan perintah untuk proses monitoring secara real-time yang interaktif untuk proses yang berjalan dari CPU, Memory dan Swap.

  ![HTOP](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/e522dc39-6958-45fa-8dec-8faf29413f14)

  Penjelasan : 
  1.	Jumlah Core yang dimiliki oleh server local, per satu core menggunakan beberapa thread
  2.	Mem : Total Pengunaan Memory 
  3.	Swp: Total Pengunaan Swap Memory (Memory Cadangan), digunakan Ketika pengunaan Memory Penuh
  4.	Task : Aplikasi Yang Sedang Berjalan Di Server local. 
  5.	Load Average : Rata – Rata Aplikasi yang Berjalan di Server local.
  6.	Uptime : Jumlah Waktu Berapa Lama Server Kita Berjalan dalam kondisi menyala.
  7.	PID : Identifikasi Proses sistem dalam bentuk ID  
  8.	USER : jumlah pengguna yang dimiliki oleh Server.
  9.	VIRT : jumlah memory yang digunakan oleh sistem.
  10.	Command : perintah yang sedang dijalankan oleh sistem.
  11.	Warna Hijau : Proses Memory yang sudah digunakan 
  12.	Warna Biru : Proses Memory Cadangan yang digunakan saat – saat tertentu. 
  13.	Warna Kuning : Proses Sisa Memory (Cache)
  14.	Warna Merah : Kernel Linux sedang memproses data di belakang layar.

  **B.NMON**
  
  Nmon adalah perintah yang dapat menampilkan informasi tentang berbagai utilitas seperti cpu, memori, disk, jaringan dll.

  Command nmon dalam cli linux dan akan muncul tampilan berikut.

  ![nmon](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/e6738650-6003-4d08-b85b-a73ba5f86421)

  *Tekan C untuk cek utilisasi CPU*

  ![utilisasi](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/5790d404-4374-468b-936e-09e5143ef612)

  *Tekan M untuk cek utilisasi Memory dan Swap*

  ![Mem](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/0cc0c475-fbd0-45c8-9ae8-f23e6ceb8d0f)

  *Tekan N untuk cek Statistik Error dalam Network Interface*

  ![network](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/9e7c24c7-3701-4b4a-bcc7-0539defc640f)

  *Tekan D untuk cek statistik dari Disk*

  ![Disk](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/cfc616b7-c16e-43c0-95b4-f10ff7e0a094)

## Task 4 

Step 1 --> mencetak string "apt get install nginx" di file **install-nginx**

command : `echo "apt get install nginx" >> step-installation/install-nginx`

![apt install nginx](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/4fd82f44-a1e2-4c4f-ab7e-eef3acfc6260)

step 2 --> memberikan command *bash* pada file **install-nginx**

command : `bash install-nginx`

![bash install](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/b4403e35-3c2e-4825-94e0-152e0f623990)

step 3 --> cek status service nginx 

command : `systemctl status nginx`

![systemctl](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/2b6477dc-742e-4a29-a722-4725377af5a5)

step 4 --> open browser, and check by localhost 

![test](https://github.com/ngurahgdewisnugk/devops20-dumbways-ngurahgedewisnugk/assets/88923635/526377ad-1b27-475d-92e4-f244ebe5c223)









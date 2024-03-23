# Step Menginstall Virtual Machine VMware
1. ## Silahkan untuk klik instalan VMware yang sudah di download 

1. ## Setelah itu klik “Next” lalu akan muncul page berikut  


1. ## Setelah itu klik “Next” Kembali, lalu akan muncul pop up berikut, apabila anda ingin mencentang WHP klik centang, apabila tidak lanjut klik “Next”
Note : Saya Menggunakan Windows Hypervisor Platform, karena saya menggunakan third-party hypervisor seperti WSL. 

1. ## Setelah itu klik “Next” Kembali

1. ## Setelah muncul page berikut, silahkan klik “Next” Kembali
Note : Untuk *check for product updates on startup* dan *Join VMware…..* optional boleh dicentang apa enggak.

1. ## Di page berikut, klik “Next”
Note : untuk shortcut optional, disesuaikan dengan kebutuhan 

1. ## Setelah di page berikut, klik Finish 

1. ## Tadaaa, instalasi VMware sudah selesai, dan siap untuk instalasi Virtual OS

\*Note : sebelum melakukan instalasi, pastikan VMware yang digunakan yang free non commercial use 


# Step Menginstall OS Linux (Ubuntu 20.04)
1. ## Untuk membuat Virtual Machine Baru, Klik “Create a New Virtual Machine”

1. ## Setelah muncul pop-up berikut, pilih “installer dic image file (iso)




1. ## Setelah muncul pop-up berikut, pilih installer os yang kalian gunakan di penyimpanan folder kalian.

1. ## setelah itu, klik “Next”.





1. ## setelah itu masuk ke page “Personalize Linux”, isilah sesuai yang diinginkan.

1. ## setelah itu naming nama virtual machine yang digunakan dan simpan VM tersebut di directory local yang ingin digunakan.





1. ## setelah itu sesuaikan “Specify Disk Capacity” yang dibutuhkan, dan tentukan virtual disk yang diinginkan.

1. ## setelah muncul page berikut, pilih “pilih customize hardware





1. ## sesuaikan kebutuhan memory untuk VM anda, disarankan 2 GB aja.

1. ## setelah itu tentukan jumlah processor core, disini saya gunakan 2 core




1. ## setelah itu pilih menu Network Adapter, pilih Network Connection yang Bridge dan lakukan Configure Adapters.

1. ## lalu pilih ceklis network adapter yang digunakan device anda, setelah itu klik “OK” dan “close”


1. ## setelah di page berikut, klik “Finish”

1. ## tunggu proses berjalan sambil menunggu arahan berikutnya.







1. ## pilih Bahasa yang diinginkan, lalu pilih “Done”.

1. ## setelah itu identify keyboard dan pilih “Done”

1. ## Setelah itu, kita di page Network Connections, di “IPv4 Method” enter dan pilih “Manual” 

1. ## Nah di tampilan ini kita akan menggunakan IP Status, sebelum mengisi sekarang buka cmd, lanjut ke Langkah berikutnya.






1. ## Di cmd ketik ipconfig lalu enter, di paling bawah ada “Wireless LAN adapter WI-FI” ada ipv4 address, Subnet Mask, dan Default Gateway, catat ketiga hal tersebut.









1. ## Lalu isi subnet sesuai CIDR subnet mask, terus isi address sesuai dengan CIDR class yang digunakan, isi gateway dengan Default Gateway, untuk name server kita gunakan DNSnya google.com, setelah itu save.

1. ## Lalu di storage configuration, pilih yang “Custom storage layout”









1. ## Pada free space dienter, lalu pilih “Add GPT Partition”.

1. ## Untuk free space pertama, pilih format ext4, dengan size 8 GB







1. ## Free space type ext 4 terbentuk.

1. ## Lalu kita lakukan Kembali sesuai step 24, namun untuk formatnya kita ubah menjadi swap dengan size 1.5GB.









1. ## Free space type swap kebentuk

1. ## Setelah pilih “Done” enter, dan akan muncul pop up berikut, lalu pilih bawah “Continue” lalu enter.

1. ## Di profile setup, isi form berikut untuk nama anda, nama server anda, username anda dan password yang mudah diingat.

1. ## Centang “install OpenSSH Server”, lalu pilih “Done” enter.

1. ## Bagian ini diskip, pilih “Done” enter.

1. ## Tunggu proses instalasi selesai, setelah selesai pilih “Reboot Now”.

1. ## Setelah reboot, login menggunakan username yang sudah kita buat tadi.

1. ## Masukan password yang sudah dibuat.

1. ## Sudah masuk ke dalam Linux OS Ubuntu

1. ## Setelah itu lakukan ping ke dns server yang kita setting di configure setting (contoh google.com)


ssh, scure shell. protokol jaringan yang memungkinkan pengguna untuk mengakses komputer jarak jauh. ssh menggunakan enkripsi untuk mengirim data antar komputer

SSH adalah protokol yang sangat populer untuk digunakan oleh administrator sistem dan pengguna yang ingin mengakses komputer lain dari jarak jauh. SSH dapat digunakan untuk berbagai tujuan, termasuk:

Mengakses file dan folder di komputer lain
Menjalankan program di komputer lain
Mengelola server
Mentransfer file antara dua komputer
Mendiagnosis masalah di komputer lain



Berikut adalah beberapa manfaat menggunakan SSH:

    Aman: SSH menggunakan enkripsi untuk melindungi data yang dikirim antara kedua komputer, sehingga data tidak dapat dicuri oleh pihak yang tidak berwenang.
    Andal: SSH adalah protokol yang andal dan jarang mengalami masalah.
    Fleksibel: SSH dapat digunakan untuk berbagai tujuan, termasuk mengakses file dan folder, menjalankan program, mengelola server, mentransfer file, dan mendiagnosis masalah.
    Mudah digunakan: SSH mudah digunakan dan dapat dipelajari dengan cepat.
    Jika Anda ingin mengakses komputer lain dari jarak jauh, SSH adalah pilihan yang bagus. SSH adalah protokol yang aman, andal, fleksibel, dan mudah digunakan.

----------------------------------------------------------------

perintah-perintah ssh

ssh: Perintah utama untuk memulai sesi SSH dengan server jarak jauh. Contohnya:
     `ssh username@ip/host`

ssh-keygen: Perintah untuk menghasilkan pasangan kunci SSH (kunci publik dan kunci pribadi). Kunci ini dapat digunakan untuk otentikasi aman tanpa memasukkan kata sandi setiap kali.
`ssh key-gen`

ssh-copy-id: Perintah untuk menyalin kunci publik ke server jarak jauh, memungkinkan Anda untuk masuk tanpa kata sandi.
`ssh-copy-id username@hostname`

scp: Perintah untuk mengirim dan menerima file secara aman melalui SSH. Ini mirip dengan perintah cp di terminal.
`scp /lokasi/lokal/file.txt username@hostname:/tujuan/remote/`
Mengunduh file dari server:
`scp username@hostname:/lokasi/remote/file.txt /tujuan/lokal/`

sftp: Perintah untuk menjalankan sesi transfer berkas yang interaktif melalui SSH. Mirip dengan FTP, tetapi lebih aman.
`sftp username@hostname`


ssh-agent: Manajer kunci SSH untuk mengelola kunci pribadi Anda dan memberikan otentikasi berbasis kunci selama sesi SSH.
`ssh-agent`

ssh-add: Menambahkan kunci pribadi ke ssh-agent untuk digunakan dalam otentikasi.
`ssh-add ~/.ssh/id_rsa`

sshfs: Menggunakan FUSE (Filesystem in Userspace), memungkinkan Anda untuk mengaitkan sistem berkas dari server jarak jauh ke sistem berkas lokal melalui SSH.
`sshfs username@hostname:/lokasi/remote /lokasi/lokal`

sshd: Ini adalah daemon server SSH yang berjalan di sisi server untuk menerima koneksi dari klien SSH.
`sudo service sshd start`  # Memulai layanan SSH
`sudo service sshd stop`  # Menghentikan layanan SSH
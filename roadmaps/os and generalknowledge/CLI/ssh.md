Perintah ssh memiliki sejumlah argumen yang dapat Anda gunakan untuk mengkonfigurasi dan mengatur sesi SSH Anda. Berikut adalah beberapa argumen yang umumnya digunakan:



- Username dan Hostname:
`username@hostname`: Menghubungkan ke server dengan menggunakan nama pengguna dan alamat IP atau nama domain host.

- Port:
`-p port`: Menghubungkan ke port yang berbeda di server. Port default untuk SSH adalah 22, tetapi Anda dapat menggantinya jika perlu.

- Identitas Kunci SSH:
`-i path_to_private_key`: Menggunakan kunci pribadi yang disebutkan untuk otentikasi. Jika tidak disediakan, perintah ssh akan mencoba menggunakan kunci yang ada di direktori ~/.ssh secara default.

- Perintah Eksekusi:
`ssh username@hostname "command"`: Menjalankan perintah di host yang ditargetkan setelah masuk melalui SSH. Ini berguna untuk menjalankan perintah pada server jarak jauh tanpa perlu masuk terlebih dahulu.

- Meneruskan Port (Port Forwarding):
`-L local_port:remote_host:remote_port`: Meneruskan lalu lintas dari port lokal ke port di server jarak jauh.
`-R remote_port:local_host:local_port`: Meneruskan lalu lintas dari port di server jarak jauh ke port lokal.

Menggunakan TTY (Terminal):
`-t`: Mengalihkan terminal TTY. Berguna jika Anda perlu menjalankan perintah yang membutuhkan interaksi terminal.

----------------------------------------------------------------
Opsi SSH Lainnya:
`-o option`: Mengatur opsi SSH tertentu, seperti mengaktifkan atau menonaktifkan opsi tertentu.

Opsi yang Mempengaruhi Keamanan:
    `-o StrictHostKeyChecking=no` : Menonaktifkan pemeriksaan fingerprint kunci host. 
    Perhatian: Ini dapat mengurangi keamanan karena memungkinkan serangan "man-in-the-middle".
    
    Mengatur Koneksi:
    `-o ConnectTimeout=seconds`: Mengatur batas waktu untuk mencoba koneksi sebelum dinyatakan gagal.
    `-o ServerAliveInterval=seconds`: Mengatur interval waktu pengiriman pesan "keep-alive" untuk menjaga koneksi tetap hidup.

    `-o LocalForward=local_port:remote_host:remote_port`: Meneruskan port lokal ke port di server jarak jauh.
    `-o RemoteForward=remote_port:local_host:local_port`: Meneruskan port di server jarak jauh ke port lokal.

    Opsi Lainnya:
    `-o UserKnownHostsFile=path`: Mengatur lokasi berkas yang berisi daftar kunci host yang diketahui.
    `-o IdentityFile=path`: Mengatur lokasi kunci pribadi yang akan digunakan untuk otentikasi.

    `ssh -o StrictHostKeyChecking=no -o ConnectTimeout=10 username@hostname`
----------------------------------------------------------------

Verbose Mode (Mode Detail):
`-v, -vv, -vvv`: Mengaktifkan mode verbose untuk mendapatkan informasi lebih rinci tentang proses koneksi.
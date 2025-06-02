ls = (list)

digunakan dalam command line untuk menampilkan daftar file dan direktori yang ada di dalam sebuah direktori.

`ls [options] [nama_direktori]`


Beberapa opsi yang umum digunakan bersama perintah ls:

`*` : melihat smua yang berada di daftar
`-l`: Menampilkan informasi lebih rinci dalam format daftar (long format). Informasi yang ditampilkan termasuk izin, jumlah tautan, pemilik, grup, ukuran file, tanggal modifikasi, dan nama file/direktori.

`-a`: Menampilkan semua file dan direktori, termasuk yang diawali dengan tanda titik (biasanya file tersembunyi).

`-lh`: Menggunakan format yang mudah dibaca manusia untuk ukuran file (B, KB, MB, GB, dst.).

`-lt`: Mengurutkan daftar berdasarkan tanggal modifikasi (terbaru ke terlama).

`-lr` : Membalikkan urutan daftar (terbalik).

`-R` : Membaca subsdirectory

`-S` : mensort file terbesar hingga terkecil

`ls -d a*/` :  menampilkan directory dengan awalan a


`-lah`:  gabungan beberapa option

`ls ~` membaca directory home 
`ls /` membaca directory filesystem 


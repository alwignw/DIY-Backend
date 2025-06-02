 Perintah cat (Concatenate) digunakan dalam command line untuk menampilkan isi dari satu atau beberapa file teks di layar terminal.

 cat [options] [nama_file]


`cat teks.txt`

`cat file1.txt file2.txt file3.txt`

`cat file1.txt file2.txt file3.txt`


-n: Menampilkan nomor baris pada setiap baris dalam output.
`cat -n teks.txt`


-b: Menampilkan nomor baris hanya pada baris yang tidak kosong.
`cat -b teks.txt`

-A: Menampilkan karakter kontrol sebagai tanda panah (^M, ^I, dll.).
cat -A teks.txt



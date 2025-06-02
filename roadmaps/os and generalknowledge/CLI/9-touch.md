Perintah touch digunakan dalam command line untuk membuat file kosong atau memperbarui tanggal dan waktu modifikasi dari file yang ada.


touch [options] [nama_file]


touch file.txt


-c: Hanya memperbarui tanggal dan waktu modifikasi jika file sudah ada. Jika file belum ada, tidak akan membuat file baru.
`touch -c file.txt`

-d: Menetapkan tanggal dan waktu modifikasi sesuai dengan argumen yang diberikan. Format tanggal adalah "YYYY-MM-DD HH:MM:SS".
`touch -d "2023-07-20 15:30:00" file.txt`


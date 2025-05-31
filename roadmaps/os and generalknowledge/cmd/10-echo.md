Perintah echo digunakan dalam command line untuk menampilkan teks atau pesan di layar terminal.


echo [options] [pesan]


echo "Halo dunia!"


nama="John"
echo "Nama saya adalah $nama"


-n: Mencegah karakter baris baru (newline) ditambahkan di akhir teks, sehingga output akan ditampilkan dalam baris yang sama.
echo -n "Ini adalah "
echo "satu baris"


-e: Memungkinkan interpretasi karakter khusus, seperti tanda panah (\t untuk tab, \n untuk newline).
echo -e "Baris pertama\nBaris kedua"



Tipe Instance Amazon EC2
Setelah mempelajari tentang EC2 instance dan peran pentingnya di AWS, mari kita bahas perkara berbagai tipe instance yang tersedia. Pikirkan kembali analogi kita soal kedai kopi, Anda mungkin ingat bahwa EC2 instance itu seperti pegawai di kedai kopi. Mereka melayani permintaan client.

Jika ingin memiliki kedai kopi yang mampu melayani banyak pelanggan, maka kita membutuhkan banyak pegawai, bukan? Tentunya para pegawai tersebut tak bisa semuanya berperan sebagai kasir. Harus ada seseorang yang membuat minuman, mengurusi makanan, dan mungkin yang dapat membuat seni latte keren agar pelanggan suka.

Seperti bisnis yang lain, ada berbagai tugas khusus yang perlu diselesaikan dan kerap kali membutuhkan keahlian yang berbeda-beda. Jika ingin bisnis kita beroperasi seefisien mungkin, maka pastikan karyawan memiliki keahlian yang sesuai dengan peran mereka.

Di kedai kopi kita memiliki berbagai jenis karyawan beserta perannya. Sama halnya dengan itu, AWS pun memiliki berbagai tipe EC2 instance yang dapat Anda jalankan dan terapkan ke dalam lingkungan AWS Anda.

Setiap tipe instance dikelompokkan dalam satu instance family (keluarga instance) dan dioptimalkan untuk jenis tugas tertentu. Tipe instance menawarkan berbagai kombinasi dari kapasitas CPU, memori, penyimpanan, jaringan, serta memberi Anda fleksibilitas untuk memilih kombinasi sumber daya yang sesuai untuk aplikasi Anda.

Instance family di Amazon EC2 memiliki fungsi yang berbeda-beda. Di antaranya ada general purpose, compute optimized, memory optimized, accelerated computing (komputasi terakselerasi), dan storage optimized. Berikut uraiannya:

General purpose instances (Instance tujuan umum)
Tipe ini memberikan keseimbangan yang baik dari segi sumber daya komputasi, memori, dan jaringan. Selain itu, opsi ini juga dapat digunakan untuk berbagai beban kerja yang beragam seperti server aplikasi web atau repositori kode.

Compute optimized instances (Instance teroptimasi untuk komputasi)
Tipe yang satu ini ideal untuk tugas komputasi yang intensif dan berpusat pada prosesor dengan performa tinggi, seperti server game, HPC (high-performance computing/komputasi dengan performa tinggi), atau bahkan pemodelan ilmiah.

Anda juga bisa menggunakan tipe compute optimized instances untuk beban kerja batch processing yang membutuhkan banyak proses transaksi di satu grup.

Memory optimized instances (Instance teroptimasi untuk memori)
Opsi ini didesain untuk memberikan performa tinggi untuk beban kerja yang memproses kumpulan data besar di dalam memori, seperti relasional dan nonrelasional database atau HPC (high-performance computing).

Accelerated computing instances (Instance terakselerasi untuk komputasi)
Tipe ini menggunakan perangkat keras akselerator untuk menjalankan beberapa fungsi secara lebih efisien dibandingkan dengan perangkat lunak yang berjalan pada CPU. Contohnya adalah penghitungan bilangan floating-point, pemrosesan grafik, dan data pattern matching (pencocokan pola data).

Storage optimized instance (Instance teroptimasi untuk penyimpanan)
Opsi ini didesain untuk beban kerja yang membutuhkan akses read (baca) dan write (tulis) yang tinggi dan berurutan untuk kumpulan data yang besar di penyimpanan lokal.

Contoh beban kerja yang sesuai untuk tipe ini mencakup sistem file terdistribusi, aplikasi data warehousing (gudang data), dan sistem online transaction processing (OLTP) berfrekuensi tinggi.

Dalam komputasi, istilah input/output operation per second (IOPS) adalah metrik yang mengukur kinerja perangkat penyimpanan. Ini menunjukkan berapa banyak operasi input atau output yang dapat dilakukan oleh perangkat dalam satu detik.

Singkatnya, Anda dapat menganggap operasi input sebagai data yang dimasukkan ke dalam sistem, seperti data yang dimasukkan ke dalam database. Sedangkan operasi output adalah data yang dihasilkan oleh sistem. Contoh output adalah hasil analitik yang dilakukan pada data dalam database.

Jika Anda memiliki aplikasi yang memerlukan IOPS tinggi, storage optimized instance dapat memberikan kinerja yang lebih baik dibandingkan dengan tipe lain yang tak teroptimasi untuk jenis kasus penggunaan ini.
Jika dianalogikan ke dalam skenario kedai kopi, kasir itu akan menjadi memory optimized instance, barista menjadi compute optimized instance, dan si pembuat seni pada latte adalah accelerated computing instance. Itulah tipe instance pada Amazon EC2. Yuk kita lanjut ke materi berikutnya!
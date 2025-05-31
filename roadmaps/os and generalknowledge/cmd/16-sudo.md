
sudo adalah singkatan dari "Super User Do" atau "Substitute User Do". Ini adalah perintah yang digunakan dalam sistem operasi berbasis Unix (termasuk Linux) yang memungkinkan pengguna untuk menjalankan perintah sebagai pengguna lain, biasanya sebagai pengguna "superuser" atau "root". Pengguna root memiliki hak akses penuh ke sistem dan dapat melakukan perubahan signifikan yang mungkin mempengaruhi keseluruhan sistem.

Penggunaan sudo penting untuk keamanan karena tidak selalu bijaksana untuk menjalankan perintah sebagai pengguna root secara terus-menerus. Dengan sudo, pengguna tidak perlu masuk sebagai pengguna root secara permanen, tetapi hanya untuk perintah tertentu yang memerlukannya.


sudo -i atau sudo su: Selain menjalankan perintah individual dengan sudo, pengguna juga dapat menggunakan sudo -i atau sudo su untuk beralih sepenuhnya ke akun superuser. Ini membuka sesi superuser interaktif dan memungkinkan pengguna menjalankan beberapa perintah sebagai superuser tanpa harus mengetikkan sudo setiap saat.
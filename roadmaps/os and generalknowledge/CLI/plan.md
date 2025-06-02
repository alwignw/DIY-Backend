Berikut adalah beberapa contoh perintah command line yang umum digunakan:

1. **`pwd` (Print Working Directory)**: Menampilkan direktori kerja saat ini.
   Contoh:
   ```
   pwd
   ```

2. **`ls` (List)**: Menampilkan daftar file dan direktori di direktori kerja saat ini.
   Contoh:
   ```
   ls
   ```

3. **`cd` (Change Directory)**: Mengubah direktori kerja saat ini. Misalnya, pindah ke direktori "Documents".
   Contoh:
   ```
   cd Documents
   ```

4. **`mkdir` (Make Directory)**: Membuat direktori baru dengan nama "new_folder".
   Contoh:
   ```
   mkdir new_folder
   ```

5. **`rm` (Remove)**: Menghapus file bernama "file.txt".
   Contoh:
   ```
   rm file.txt
   ```

6. **`cp` (Copy)**: Menyalin file "file.txt" ke direktori "backup".
   Contoh:
   ```
   cp file.txt backup/
   ```

7. **`mv` (Move)**: Memindahkan file "file.txt" ke direktori "documents".
   Contoh:
   ```
   mv file.txt documents/
   ```

8. **`touch` (Create Empty File)**: Membuat file kosong bernama "new_file.txt".
   Contoh:
   ```
   touch new_file.txt
   ```

9. **`cat` (Concatenate)**: Menampilkan isi teks dari file "file.txt".
   Contoh:
   ```
   cat file.txt
   ```

10. **`grep` (Global Regular Expression Print)**: Mencari kata "kata_kunci" dalam file "data.txt".
    Contoh:
    ```
    grep "kata_kunci" data.txt
    ```

11. **`echo` (Print)**: Menampilkan pesan teks "Halo dunia!" di layar.
    Contoh:
    ```
    echo "Halo dunia!"
    ```

12. **`man` (Manual)**: Menampilkan manual untuk perintah "ls".
    Contoh:
    ```
    man ls
    ```

13. **`df` (Disk Free)**: Menampilkan informasi tentang penggunaan ruang disk pada sistem.
    Contoh:
    ```
    df -h
    ```

14. **`ps` (Process Status)**: Menampilkan daftar proses yang sedang berjalan pada sistem.
    Contoh:
    ```
    ps aux
    ```

15. **`chmod` (Change Mode)**: Mengubah izin (permission) file "file.txt" menjadi read-write-execute untuk pemiliknya.
    Contoh:
    ```
    chmod u+rwx file.txt
    ```

16. **`find`**: Mencari file dengan ekstensi ".txt" di seluruh struktur direktori, mulai dari direktori kerja saat ini.
    Contoh:
    ```
    find . -name "*.txt"
    ```

17. **`tar`**: Membuat arsip (archive) file dan direktori menjadi file tarball.
    Contoh:
    ```
    tar -czvf arsip.tar.gz file.txt direktori/
    ```

18. **`ssh`**: Menghubungkan ke server jarak jauh melalui Secure Shell (SSH).
    Contoh:
    ```
    ssh username@alamat_ip
    ```

Ini adalah beberapa contoh perintah command line yang sering digunakan. Harap diingat bahwa efek dari setiap perintah bisa berbeda tergantung pada sistem operasi yang digunakan dan parameter yang diberikan. Pastikan untuk memahami dengan baik sebelum menggunakan perintah yang dapat memiliki dampak besar pada sistem Anda, seperti `rm` (untuk menghapus file) dan `chmod` (untuk mengubah izin).



Tentu! Berikut adalah beberapa contoh lain dari perintah command line yang sering digunakan:

19. **`ping`**: Memeriksa koneksi jaringan dengan mengirimkan paket ICMP ke host atau alamat IP tertentu.
    Contoh:
    ```
    ping google.com
    ```

20. **`ifconfig` (Interface Configuration)**: Menampilkan konfigurasi jaringan untuk antarmuka jaringan pada sistem.
    Contoh:
    ```
    ifconfig
    ```

21. **`wget`**: Mengunduh file dari Internet menggunakan URL.
    Contoh:
    ```
    wget https://example.com/file.txt
    ```

22. **`curl`**: Mengunduh atau mengirim data melalui URL menggunakan berbagai protokol.
    Contoh:
    ```
    curl -o file.txt https://example.com/file.txt
    ```

23. **`top`**: Menampilkan daftar proses berjalan secara real-time, berurutan berdasarkan penggunaan CPU.
    Contoh:
    ```
    top
    ```

24. **`grep` (Global Regular Expression Print)**: Menemukan pola teks dalam file atau output yang dihasilkan dari perintah lain.
    Contoh:
    ```
    cat file.txt | grep "kata_kunci"
    ```

25. **`sed` (Stream Editor)**: Mengedit dan memanipulasi teks pada aliran data, sering digunakan bersama dengan output dari perintah lain.
    Contoh:
    ```
    cat file.txt | sed 's/kata_lama/kata_baru/g'
    ```

26. **`wc` (Word Count)**: Menghitung jumlah baris, kata, dan karakter dalam sebuah file teks.
    Contoh:
    ```
    wc -l file.txt
    ```

27. **`head` dan `tail`**: Menampilkan beberapa baris pertama atau terakhir dari file teks.
    Contoh:
    ```
    head -n 5 file.txt
    tail -n 10 file.txt
    ```

28. **`history`**: Menampilkan riwayat perintah yang telah dijalankan pada shell.
    Contoh:
    ```
    history
    ```

29. **`date`**: Menampilkan tanggal dan waktu saat ini.
    Contoh:
    ```
    date
    ```

30. **`tar`**: Mengekstrak arsip (archive) dari file tarball.
    Contoh:
    ```
    tar -xzvf arsip.tar.gz
    ```

31. **`du` (Disk Usage)**: Menampilkan penggunaan ruang disk oleh direktori dan file.
    Contoh:
    ```
    du -sh /path/to/direktori
    ```

32. **`sudo` (Super User Do)**: Menjalankan perintah sebagai super pengguna (administrator) untuk mengakses operasi yang memerlukan izin khusus.
    Contoh:
    ```
    sudo apt-get update
    ```

Ingatlah bahwa daftar ini hanya sebagian kecil dari perintah command line yang ada. Ada banyak perintah lain yang dapat digunakan tergantung pada sistem operasi dan kebutuhan Anda. Semoga daftar ini membantu Anda memahami lebih banyak tentang command line dan mengelola sistem dengan lebih efisien. Selamat belajar dan eksplorasi lebih lanjut!


Tentu! Berikut adalah beberapa contoh perintah command line lainnya:

33. **`chmod` (Change Mode)**: Mengubah izin (permissions) file atau direktori. Misalnya, memberikan izin baca, tulis, dan eksekusi kepada pemilik, grup, atau pengguna lain.
    Contoh:
    ```
    chmod +rwx file.txt
    ```

34. **`chown` (Change Owner)**: Mengubah pemilik (owner) file atau direktori.
    Contoh:
    ```
    chown user:group file.txt
    ```

35. **`grep` (Global Regular Expression Print)**: Mencari teks dalam file atau output dari perintah lain berdasarkan pola yang diberikan.
    Contoh:
    ```
    grep "kata_kunci" file.txt
    ```

36. **`find`**: Mencari file atau direktori berdasarkan kriteria tertentu, seperti nama, ukuran, atau tanggal modifikasi.
    Contoh:
    ```
    find /path/to/direktori -name "*.txt"
    ```

37. **`ps` (Process Status)**: Menampilkan daftar proses yang berjalan pada sistem.
    Contoh:
    ```
    ps aux
    ```

38. **`kill`**: Menghentikan proses yang berjalan dengan mengirimkan sinyal ke proses tersebut.
    Contoh:
    ```
    kill PID
    ```

39. **`df` (Disk Free)**: Menampilkan informasi tentang penggunaan ruang disk pada sistem.
    Contoh:
    ```
    df -h
    ```

40. **`free`**: Menampilkan informasi tentang penggunaan memori pada sistem.
    Contoh:
    ```
    free -h
    ```

41. **`uptime`**: Menampilkan informasi tentang berapa lama sistem telah berjalan dan bekerja tanpa restart.
    Contoh:
    ```
    uptime
    ```

42. **`zip`**: Membuat file zip dari file atau direktori.
    Contoh:
    ```
    zip file.zip file.txt
    ```

43. **`unzip`**: Mengekstrak file dari file zip.
    Contoh:
    ```
    unzip file.zip
    ```

44. **`tar`**: Membuat atau mengekstrak arsip dari file tarball.
    Contoh:
    ```
    tar -czvf arsip.tar.gz file.txt direktori/
    ```

45. **`ssh`**: Menghubungkan ke server jarak jauh melalui SSH.
    Contoh:
    ```
    ssh username@alamat_ip
    ```

46. **`scp` (Secure Copy)**: Menyalin file antara host lokal dan host jarak jauh melalui SSH.
    Contoh:
    ```
    scp file.txt username@alamat_ip:/path/to/destination
    ```

47. **`man` (Manual)**: Menampilkan manual untuk perintah tertentu.
    Contoh:
    ```
    man ls
    ```

48. **`clear`**: Membersihkan layar terminal dan menggulungnya ke atas.
    Contoh:
    ```
    clear
    ```

Itu dia beberapa contoh perintah command line yang sering digunakan. Perlu diingat bahwa command line menawarkan banyak kemungkinan, dan setiap sistem operasi atau lingkungan shell bisa memiliki perintah yang berbeda. Semoga daftar ini bermanfaat untuk menambah pengetahuan Anda tentang command line. Selamat belajar dan eksplorasi lebih lanjut!
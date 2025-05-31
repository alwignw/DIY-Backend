Berikut beberapa **fakta menarik tentang Memcached** — baik dari sisi teknis maupun sisi keamanan dan sejarahnya:

---

### 🔹 1. **Awalnya dibuat untuk Friendster**

* Memcached pertama kali dikembangkan oleh **Brad Fitzpatrick** tahun **2003**.
* Tujuannya untuk **meningkatkan performa website Friendster** (media sosial populer sebelum Facebook).
* Sejak itu, Memcached menjadi teknologi caching yang digunakan oleh banyak perusahaan besar.

---

### 🔹 2. **Bersifat Open Source & Super Cepat**

* Memcached itu **gratis dan open source**.
* Disimpan di **RAM**, jadi kecepatan bacanya **sangat tinggi** dibandingkan baca dari database langsung.
* Ini yang bikin aplikasi seperti Facebook, Twitter, dan Wikipedia dulu pakai Memcached untuk **mengurangi beban database**.

---

### 🔹 3. **Stateless – tidak menyimpan data permanen**

* Data di Memcached hanya **sementara**.
* Kalau server restart, **semua data di Memcached hilang**.
* Jadi cocok hanya untuk caching, bukan penyimpanan utama.

---

### 🔹 4. **Sangat Sederhana**

* Memcached itu ringan banget.
* Tidak ada fitur yang rumit seperti query SQL, permission, dsb.
* Key-value saja. Seperti: `"user:123" => {nama: "Bos", saldo: 1 juta}`

---

### 🔹 5. **Tidak aman jika dibiarkan terbuka ke internet**

* Karena **tidak ada autentikasi bawaan**, siapa saja bisa baca/tulis ke server jika terbuka.
* Inilah yang menyebabkan **bisa dimanfaatkan dalam serangan DDoS**.

---

### 🔹 6. **Dipakai di perusahaan-perusahaan besar**

Beberapa contoh pengguna Memcached:

* **Facebook** – dulunya menggunakan ribuan server Memcached.
* **Twitter**
* **Reddit**
* **Wikipedia**
* Banyak platform ecommerce juga menggunakannya untuk caching produk, harga, dll.

---

### 🔹 7. **Alternatifnya: Redis**

* Redis mirip Memcached, tapi lebih modern.
* Redis mendukung lebih banyak tipe data dan bisa **menyimpan data secara permanen**, tidak hanya di RAM.
* Redis juga punya fitur keamanan dan clustering yang lebih baik.

---

### 🔹 8. **Tidak cocok untuk semua data**

* Karena data-nya cepat hilang (tidak permanen), Memcached **tidak cocok untuk menyimpan data penting** seperti transaksi, akun, dan sebagainya.

---

Kalau Bos ingin, saya bisa bantu install Memcached di laptop/VM sebagai latihan, atau tunjukkan bagaimana cara kerja cache Memcached di aplikasi nyata (misalnya dengan Node.js, Python, atau PHP).

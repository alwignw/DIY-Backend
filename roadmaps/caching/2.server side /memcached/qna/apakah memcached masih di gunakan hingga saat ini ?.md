Ya, **Memcached masih digunakan hingga saat ini**, **tapi...** penggunaannya semakin **terbatas dan spesifik**, karena ada **alternatif yang lebih kuat dan fleksibel** seperti **Redis**.

---

## ✅ **Kapan Memcached Masih Dipakai?**

1. **Aplikasi Lama (Legacy Systems)**

   * Banyak sistem lama yang masih jalan dengan Memcached, dan masih cukup cepat & stabil.
   * Migrasi ke Redis kadang dianggap tidak perlu kalau Memcached sudah cukup.

2. **Caching Simpel**

   * Jika hanya butuh **key-value cache sederhana** dan tidak butuh persistensi atau fitur kompleks.
   * Contohnya: menyimpan hasil query SQL sementara.

3. **Performa Tinggi & Ringan**

   * Memcached sangat ringan dan cepat, cocok untuk **aplikasi skala besar** yang sudah optimalkan caching logic-nya.

---

## ❌ **Kapan Mulai Ditinggalkan?**

1. **Tidak Ada Persistensi**

   * Kalau server restart, semua data hilang.
   * Redis bisa menyimpan data secara permanen (kalau disetting begitu).

2. **Tidak Ada Auth & Security**

   * Memcached tidak punya sistem login, user, atau permission. Jadi rawan kalau tidak dilindungi firewall.

3. **Fitur Terbatas**

   * Memcached hanya menyimpan string atau byte.
   * Redis bisa menyimpan:

     * List
     * Set
     * Hash
     * Sorted set
     * Stream
     * Pub/Sub, dll.

---

## 🔍 Fakta Menarik

| Fitur                         | Memcached | Redis           |
| ----------------------------- | --------- | --------------- |
| Simpel & ringan               | ✅         | ❌ (lebih berat) |
| Persisten (data tidak hilang) | ❌         | ✅               |
| Keamanan (auth/user)          | ❌         | ✅               |
| Tipe data kompleks            | ❌         | ✅               |
| Replikasi, cluster, backup    | ❌         | ✅               |

---

## 📌 Kesimpulan

* **Masih dipakai**, tapi:

  * Untuk **kasus ringan dan sangat spesifik**.
  * Biasanya oleh sistem **lama** atau yang **butuh performa tinggi tapi sederhana**.
* Kalau kamu memulai proyek baru, **Redis biasanya lebih direkomendasikan**, kecuali kamu butuh solusi caching super ringan saja.

Kalau Bos penasaran, saya bisa bantu install Redis dan bandingkan dengan Memcached secara langsung juga.

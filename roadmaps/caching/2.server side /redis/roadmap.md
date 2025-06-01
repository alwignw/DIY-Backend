Mantap, Bos! Setelah belajar Memcached, lanjut ke Redis adalah langkah tepat karena Redis lebih powerful (karena mendukung lebih banyak tipe data dan fitur seperti persistence, pub/sub, dll).

Berikut roadmap belajar Redis **step-by-step** untuk kamu kuasai dari dasar sampai mahir:

---

## 🛣️ Roadmap Belajar Redis

### 🟢 1. **Pengenalan Redis**

* Apa itu Redis dan perbedaannya dengan Memcached.
* Use case Redis: cache, queue, session store, leaderboard, pub/sub.
* Instalasi Redis:

  * Lokal (Windows, Linux, Mac).
  * Gunakan Docker untuk menjalankan Redis (`docker run redis`).

🔗 **Latihan:**

* Jalankan Redis server & Redis CLI (`redis-cli`).
* Lakukan command dasar: `SET`, `GET`, `DEL`, `EXISTS`, `KEYS`.

---

### 🟡 2. **Struktur Data di Redis**

Pelajari dan coba command-command untuk tiap tipe data:

* 🔹 String: `SET`, `GET`, `INCR`, `DECR`
* 🔸 List: `LPUSH`, `RPUSH`, `LPOP`, `LRANGE`
* 🔹 Set: `SADD`, `SREM`, `SMEMBERS`, `SINTER`
* 🔸 Sorted Set: `ZADD`, `ZRANGE`, `ZREM`, `ZREVRANK`
* 🔹 Hash: `HSET`, `HGET`, `HGETALL`, `HDEL`

🔗 **Latihan:**

* Buat simulasi todo list pakai List.
* Simulasi leaderboard pakai Sorted Set.

---

### 🟠 3. **Key Management & Expiry**

* TTL (Time to Live): `EXPIRE`, `TTL`, `PERSIST`
* Auto expire: `SET key value EX 60`
* Pattern matching: `KEYS`, `SCAN` (lebih aman untuk production)

🔗 **Latihan:**

* Buat cache user dengan TTL 60 detik.
* Coba `EXPIRE` lalu pantau `TTL`.

---

### 🟣 4. **Persistence**

Redis bisa simpan data ke disk:

* RDB snapshotting (`save`, `bgsave`)
* AOF (Append Only File)
* Kombinasi RDB + AOF

🔗 **Latihan:**

* Ubah konfigurasi Redis agar pakai AOF.
* Restart Redis dan pastikan data tetap ada.

---

### 🔵 5. **Atomic Operations & Transaction**

* MULTI, EXEC, DISCARD, WATCH
* Optimistic Locking pakai `WATCH`

🔗 **Latihan:**

* Simulasikan update saldo rekening pakai `WATCH` + `MULTI`.

---

### 🟤 6. **Pub/Sub**

Redis bisa jadi broker messaging:

* `PUBLISH`, `SUBSCRIBE`

🔗 **Latihan:**

* Buat chat sederhana pakai pub/sub dengan 2 terminal.

---

### 🔴 7. **Redis sebagai Queue**

* Gunakan List: `LPUSH` dan `RPOP`
* Redis Streams (fitur baru, seperti Kafka)

🔗 **Latihan:**

* Buat job queue sederhana pakai List.

---

### ⚪ 8. **Security dan Performance**

* Auth: `requirepass`
* Limit akses hanya dari IP tertentu.
* Monitor: `MONITOR`, `INFO`, `SLOWLOG`
* Gunakan `maxmemory` + `policy eviction`

---

### 🟩 9. **Redis di Production**

* Redis Sentinel: high availability.
* Redis Cluster: horizontal scaling.
* Client Library (pilih sesuai bahasa):

  * Node.js: `ioredis`, `redis`
  * Python: `redis-py`
  * Go: `go-redis`

🔗 **Latihan:**

* Buat koneksi Redis dari project Node.js kamu.
* Simpan session atau cache ke Redis.

---

### 🟦 10. **Bonus - Redis + Project Nyata**

* Simpan session login (user login state).
* Cache data API (misalnya: `/products`).
* Task Queue (misalnya: email sending queue).
* Real-time notification (via pub/sub).

---

## 📚 Rekomendasi Sumber Belajar

* [Redis.io Docs (Official)](https://redis.io/docs/)
* Redis Crash Course – YouTube (misal: Traversy Media)
* RedisInsight (GUI tool untuk eksplorasi Redis)

---

Kalau Bos butuh roadmap dalam bentuk tabel atau visual, saya bisa buatkan juga. Atau kalau sudah tahu pakai bahasa tertentu, saya bisa bantu kasih contoh Redis client sesuai bahasanya (Node.js, Python, dst).

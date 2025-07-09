Untuk melihat **port yang terbuka** dan **dipakai oleh proses di Linux**, kamu bisa gunakan beberapa perintah berikut:

---

### ✅ **1. Melihat port yang sedang listening (mendengarkan koneksi masuk)**

#### 🔹 Menggunakan `ss` (modern, pengganti `netstat`)

```bash
sudo ss -tuln
```

**Penjelasan:**

* `-t` = TCP
* `-u` = UDP
* `-l` = listening
* `-n` = tampilkan nomor port, bukan nama

Contoh output:

```
Netid  State      Local Address:Port   Peer Address:Port
tcp    LISTEN     0.0.0.0:22            0.0.0.0:*
tcp    LISTEN     127.0.0.1:3306        0.0.0.0:*
```

Berarti:

* Port **22** terbuka untuk SSH.
* Port **3306** untuk MySQL (hanya bisa diakses dari localhost).

---

### ✅ **2. Melihat port beserta proses yang menggunakannya**

```bash
sudo ss -tulnp
```

**Tambahan `-p` akan menampilkan proses dan PID.**

Contoh:

```
tcp   LISTEN  0.0.0.0:80     0.0.0.0:*   users:(("nginx",pid=1234,fd=6))
```

---

### ✅ **3. Atau gunakan `netstat` (jika tersedia)**

```bash
sudo netstat -tuln
```

Atau dengan proses:

```bash
sudo netstat -tulnp
```

Jika `netstat` belum terinstall:

```bash
sudo apt install net-tools
```

---

### ✅ **4. Atau gunakan `lsof` untuk melihat siapa pakai port tertentu**

Misalnya ingin tahu siapa pakai port 80:

```bash
sudo lsof -i :80
```

---

### ✅ **5. Melihat semua port yang terbuka dari luar (pakai `nmap`)**

```bash
sudo apt install nmap
nmap -sT -O localhost
```

---

Kalau kamu ingin saya bantu cari port tertentu (misalnya "apa yang pakai port 3000?"), cukup beri tahu saja.

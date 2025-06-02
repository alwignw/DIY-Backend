Untuk melihat **service apa saja yang sedang berjalan (running)** di Linux, kamu bisa gunakan salah satu dari perintah-perintah berikut, tergantung sistem init yang digunakan (biasanya `systemd` di distro modern seperti Ubuntu, Debian, CentOS 7+, dsb):

---

### ✅ **Jika menggunakan `systemd` (umum di Ubuntu 16+ / Debian 8+ / CentOS 7+)**

#### 🔹 Tampilkan semua service yang sedang *running*:

```bash
systemctl list-units --type=service --state=running
```

#### 🔹 Tampilkan semua service (termasuk yang tidak running):

```bash
systemctl list-units --type=service
```

#### 🔹 Tampilkan status dari service tertentu (misal: nginx)

```bash
systemctl status nginx
```

---

### ✅ **Jika tidak pakai `systemd` (sistem lama atau alternatif seperti Alpine Linux)**

#### 🔹 Gunakan `service` (init.d system):

```bash
service --status-all
```

> Tanda `+` artinya running, `-` artinya stopped, `?` artinya status tidak bisa ditentukan.

---

### ✅ **Gunakan `ps` untuk lihat semua proses berjalan (termasuk service, manual check)**

```bash
ps aux
```

Atau filter berdasarkan nama service:

```bash
ps aux | grep nginx
```

---

### ✅ **Gunakan `top` atau `htop` untuk monitor real-time**

* Jalankan:

```bash
top
```

* Atau install dan gunakan `htop` (lebih bagus):

```bash
sudo apt install htop
htop
```

---

Kalau kamu mau list semua service dan statusnya (running, dead, failed), kamu bisa pakai:

```bash
systemctl list-units --type=service --all
```

Mau saya bantu filter service tertentu atau jelaskan status-nya?

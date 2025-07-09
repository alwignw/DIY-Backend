Untuk melihat spesifikasi VPS (CPU, core, RAM, OS, dll) di Linux, kamu bisa gunakan beberapa perintah berikut di terminal:

---

### 🔧 1. **Melihat Spesifikasi CPU**

```bash
lscpu
```

Atau:

```bash
cat /proc/cpuinfo
```

Ini akan menunjukkan jumlah core, thread, model CPU, arsitektur, dan lainnya.

---

### 🔧 2. **Melihat RAM (Memory)**

```bash
free -h
```

Atau:

```bash
cat /proc/meminfo
```

---

### 🔧 3. **Melihat Informasi Sistem Operasi**

```bash
uname -a
```

Atau lebih detail:

```bash
lsb_release -a
```

Jika `lsb_release` tidak ditemukan, bisa install dulu:

```bash
sudo apt install lsb-release  # untuk Debian/Ubuntu
sudo yum install redhat-lsb   # untuk CentOS/RedHat
```

---

### 🔧 4. **Melihat Informasi Disk**

```bash
df -h
```

---

### 🔧 5. **Melihat Semua Informasi Hardware**

```bash
sudo lshw -short
```

Kalau belum ada `lshw`, install dulu:

```bash
sudo apt install lshw  # untuk Debian/Ubuntu
sudo yum install lshw  # untuk CentOS/RedHat
```

---

### 🔧 6. **Melihat Ringkasan Sistem (Semua Sekaligus)**

Gunakan:

```bash
neofetch
```

Atau:

```bash
screenfetch
```

> Jika belum ada, install dengan:

```bash
sudo apt install neofetch
```

---

Kalau kamu mau, saya bisa bantu buatkan script untuk menampilkan semuanya dalam satu kali jalan. Mau?

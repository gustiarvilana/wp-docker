# 📖 WordPress dengan Docker

Repositori ini menyediakan konfigurasi Docker untuk menjalankan WordPress dengan MySQL secara lokal menggunakan **Docker Compose**.

---

## 🛠 Persyaratan

Sebelum memulai, pastikan Anda sudah menginstal:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

## 🚀 Cara Menjalankan Proyek

### 1️⃣ **Clone Repository**

```sh
git clone https://github.com/username/repo-wordpress.git
cd repo-wordpress
```

### 2️⃣ **Jalankan Docker Compose**

```sh
docker-compose up -d
```

👉 Perintah ini akan menjalankan WordPress dan MySQL dalam mode _detached_ (latar belakang).

### 3️⃣ **Akses WordPress**

Buka browser dan akses:

```
http://localhost:8888
```

---

## 🔧 **Konfigurasi Database**

| Parameter         | Nilai         |
| ----------------- | ------------- |
| Database Host     | `db`          |
| Database Name     | `exampledb`   |
| Database User     | `dewo`        |
| Database Password | `examplepass` |

Ketika pertama kali mengakses WordPress, Anda akan diminta untuk memasukkan informasi database di atas.

---

## 🛑 **Menghentikan dan Menghapus Container**

Untuk menghentikan layanan tanpa menghapus data:

```sh
docker-compose down
```

Untuk menghentikan layanan dan menghapus semua volume/data:

```sh
docker-compose down -v
```

⚠️ **Peringatan:** Perintah `-v` akan menghapus semua data di MySQL.

---

## 📂 **Struktur Direktori**

```
repo-wordpress/
│── db/                # Data MySQL (persistent)
│── wordpress/         # Data WordPress (persistent)
│── docker-compose.yml # Konfigurasi Docker Compose
│── README.md          # Dokumentasi ini
```

---

## 📌 **Catatan**

- WordPress berjalan pada **port 8888** (bisa diubah di `docker-compose.yml`).
- MySQL berjalan pada **port 3376** (bisa diubah di `docker-compose.yml`).
- **Data tersimpan secara lokal** di folder `db/` dan `wordpress/`, jadi tidak hilang saat container dihapus.

---

## 🤝 **Kontribusi**

Jika Anda ingin menambahkan fitur atau perbaikan, silakan lakukan **Pull Request** atau buka **Issue**.

💡 Happy coding! 🚀

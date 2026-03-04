🎬 Sistem Database Cinema

Project ini merupakan implementasi database sistem cinema menggunakan MySQL/MariaDB yang dijalankan melalui XAMPP.
Database ini menyimpan data film, sutradara, dan genre serta relasi antar tabel menggunakan foreign key.

📌 Deskripsi Project

Database bernama:

db_cinema

Database ini memiliki 3 tabel utama:

sutradara

genre

film

Relasi antar tabel:

1 sutradara dapat memiliki banyak film

1 genre dapat memiliki banyak film

Tabel film memiliki foreign key ke sutradara dan genre

🛠️ Teknologi yang Digunakan

XAMPP

MariaDB (MySQL)

SQL QueryOke, ini gue buatin tampilan **README.md** yang rapi, profesional, dan enak diliat buat project kamu. Tinggal copy–paste ke file `README.md` di GitHub atau folder project kamu.

---

# 🎬 Sistem Database Cinema

Project ini merupakan implementasi database sistem cinema menggunakan **MySQL/MariaDB** yang dijalankan melalui **XAMPP**.
Database ini menyimpan data film, sutradara, dan genre serta relasi antar tabel menggunakan foreign key.

---

## 📌 Deskripsi Project

Database bernama:

```
db_cinema
```

Database ini memiliki 3 tabel utama:

* `sutradara`
* `genre`
* `film`

Relasi antar tabel:

* 1 sutradara dapat memiliki banyak film
* 1 genre dapat memiliki banyak film
* Tabel `film` memiliki foreign key ke `sutradara` dan `genre`

---

## 🛠️ Teknologi yang Digunakan

* XAMPP
* MariaDB (MySQL)
* SQL Query

---

## 🗄️ Struktur Database

### 1️⃣ Tabel `sutradara`

| Field          | Type         | Keterangan                   |
| -------------- | ------------ | ---------------------------- |
| id_sutradara   | INT (PK)     | Primary Key (Auto Increment) |
| nama_sutradara | VARCHAR(100) | Nama sutradara               |
| negara_asal    | VARCHAR(50)  | Negara asal                  |
| tahun_lahir    | INT          | Tahun lahir                  |

---

### 2️⃣ Tabel `genre`

| Field      | Type        | Keterangan                   |
| ---------- | ----------- | ---------------------------- |
| id_genre   | INT (PK)    | Primary Key (Auto Increment) |
| nama_genre | VARCHAR(50) | Nama genre                   |
| keterangan | TEXT        | Deskripsi genre              |

---

### 3️⃣ Tabel `film`

| Field        | Type         | Keterangan                     |
| ------------ | ------------ | ------------------------------ |
| id_film      | INT (PK)     | Primary Key (Auto Increment)   |
| judul_film   | VARCHAR(150) | Judul film                     |
| tahun_rilis  | INT          | Tahun rilis                    |
| durasi_menit | INT          | Durasi film                    |
| id_sutradara | INT (FK)     | Foreign Key ke tabel sutradara |
| id_genre     | INT (FK)     | Foreign Key ke tabel genre     |

---

## 🔗 Relasi Antar Tabel

```sql
FOREIGN KEY (id_sutradara) REFERENCES sutradara(id_sutradara)
FOREIGN KEY (id_genre) REFERENCES genre(id_genre)
```

---

## 🎥 Data Sample Film

Beberapa film yang dimasukkan sebagai contoh:

* Inception
* Pengabdi Setan
* Parasite
* Jurassic Park
* Barbie
* Dune
* The Irishman

---

## 🔎 Contoh Query Join

### ✅ INNER JOIN

Menampilkan judul film, nama sutradara, genre, dan tahun rilis:

```sql
SELECT
    film.judul_film,
    sutradara.nama_sutradara,
    genre.nama_genre,
    film.tahun_rilis
FROM film
INNER JOIN sutradara
    ON film.id_sutradara = sutradara.id_sutradara
INNER JOIN genre
    ON film.id_genre = genre.id_genre;
```

---

### ✅ LEFT JOIN

Menampilkan semua sutradara beserta filmnya:

```sql
SELECT
    sutradara.nama_sutradara,
    film.judul_film
FROM sutradara
LEFT JOIN film
    ON sutradara.id_sutradara = film.id_sutradara;
```

---

### ✅ RIGHT JOIN

Menampilkan genre beserta filmnya:

```sql
SELECT
    genre.nama_genre,
    film.judul_film
FROM genre
RIGHT JOIN film
    ON genre.id_genre = film.id_genre;
```

---

## 🚀 Cara Menjalankan Project

1. Install dan buka XAMPP
2. Jalankan Apache dan MySQL
3. Buka terminal / CMD
4. Login ke MySQL:

```
mysql -u root
```

5. Buat database:

```sql
CREATE DATABASE db_cinema;
USE db_cinema;
```

6. Jalankan seluruh query pembuatan tabel dan insert data

---

## 🎯 Tujuan Project

* Memahami konsep database relasional
* Memahami penggunaan Primary Key dan Foreign Key
* Menguasai penggunaan JOIN (INNER, LEFT, RIGHT)
* Melatih penulisan query SQL yang terstruktur

---

Kalau mau, gue bisa bikin versi yang:

* Lebih estetik buat GitHub (pakai badge & preview)
* Versi laporan buat dikumpulin ke guru
* Ditambah ERD diagram
* Atau dijadikan file PDF siap kirim

Tinggal bilang.


🗄️ Struktur Database
1️⃣ Tabel sutradara
Field	Type	Keterangan
id_sutradara	INT (PK)	Primary Key (Auto Increment)
nama_sutradara	VARCHAR(100)	Nama sutradara
negara_asal	VARCHAR(50)	Negara asal
tahun_lahir	INT	Tahun lahir
2️⃣ Tabel genre
Field	Type	Keterangan
id_genre	INT (PK)	Primary Key (Auto Increment)
nama_genre	VARCHAR(50)	Nama genre
keterangan	TEXT	Deskripsi genre
3️⃣ Tabel film
Field	Type	Keterangan
id_film	INT (PK)	Primary Key (Auto Increment)
judul_film	VARCHAR(150)	Judul film
tahun_rilis	INT	Tahun rilis
durasi_menit	INT	Durasi film
id_sutradara	INT (FK)	Foreign Key ke tabel sutradara
id_genre	INT (FK)	Foreign Key ke tabel genre
🔗 Relasi Antar Tabel
FOREIGN KEY (id_sutradara) REFERENCES sutradara(id_sutradara)
FOREIGN KEY (id_genre) REFERENCES genre(id_genre)
🎥 Data Sample Film

Beberapa film yang dimasukkan sebagai contoh:

Inception

Pengabdi Setan

Parasite

Jurassic Park

Barbie

Dune

The Irishman

🔎 Contoh Query Join
✅ INNER JOIN

Menampilkan judul film, nama sutradara, genre, dan tahun rilis:

SELECT
    film.judul_film,
    sutradara.nama_sutradara,
    genre.nama_genre,
    film.tahun_rilis
FROM film
INNER JOIN sutradara
    ON film.id_sutradara = sutradara.id_sutradara
INNER JOIN genre
    ON film.id_genre = genre.id_genre;
✅ LEFT JOIN

Menampilkan semua sutradara beserta filmnya:

SELECT
    sutradara.nama_sutradara,
    film.judul_film
FROM sutradara
LEFT JOIN film
    ON sutradara.id_sutradara = film.id_sutradara;
✅ RIGHT JOIN

Menampilkan genre beserta filmnya:

SELECT
    genre.nama_genre,
    film.judul_film
FROM genre
RIGHT JOIN film
    ON genre.id_genre = film.id_genre;
🚀 Cara Menjalankan Project

Install dan buka XAMPP

Jalankan Apache dan MySQL

Buka terminal / CMD

Login ke MySQL:

mysql -u root

Buat database:

CREATE DATABASE db_cinema;
USE db_cinema;

Jalankan seluruh query pembuatan tabel dan insert data

🎯 Tujuan Project

Memahami konsep database relasional

Memahami penggunaan Primary Key dan Foreign Key

Menguasai penggunaan JOIN (INNER, LEFT, RIGHT)

Melatih penulisan query SQL yang terstruktur

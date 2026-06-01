# Tugas Pertemuan 9 - Laravel

## Sistem Perpustakaan

Project ini dibuat untuk memenuhi tugas Pemrograman Web 2.

## Fitur

- Routing anggota
- Detail anggota
- Routing kategori buku
- Detail kategori
- Pencarian kategori

## Route

### Anggota
- /anggota
- /anggota/{id}

### Kategori
- /kategori
- /kategori/{id}
- /kategori/search/{keyword}

## Teknologi
- Laravel
- Bootstrap 5

## Screenshot

### Daftar Anggota
![Daftar Anggota](screenshots/anggota.png)

### Detail Anggota
![Detail Anggota](screenshots/detail-anggota.png)

### Daftar Kategori
![Daftar Kategori](screenshots/kategori.png)

### Detail Kategori
![Detail Kategori](screenshots/detail-kategori.png)

### Search Kategori
![Search Kategori](screenshots/search-kategori.png)


# Tugas Pertemuan 11 - Migration, Seeder, Accessor & Scope Laravel

## Identitas

* Nama: [Zahra Zahrani]
* NIM: [60324011]
* Mata Kuliah: Pemrograman Web 2


# Tugas 1 - Migration Tabel Kategori

## Migration

Membuat migration tabel `kategori` dengan struktur:

* id (Primary Key)
* nama_kategori (Unique)
* deskripsi (Nullable)
* icon (Nullable)
* warna (Nullable)
* created_at
* updated_at

### Screenshot Migration

![Migration Kategori](screenshots/migration-kategori.png)

---

## Model Kategori

Model `Kategori` dibuat dengan fillable:

```php
protected $fillable = [
    'nama_kategori',
    'deskripsi',
    'icon',
    'warna'
];
```

### Screenshot Model

![Model Kategori](screenshots/model-kategori.png)

---

## Seeder Kategori

Data kategori yang ditambahkan:

| Nama Kategori | Icon       | Warna   |
| ------------- | ---------- | ------- |
| Programming   | code-slash | primary |
| Database      | database   | success |
| Web Design    | palette    | info    |
| Networking    | wifi       | warning |
| Data Science  | graph-up   | danger  |

### Screenshot Seeder

![Seeder Kategori](screenshots/seeder-kategori.png)

### Screenshot Hasil Database

![Database Kategori](screenshots/database-kategori.png)

---

# Tugas 2 - Accessor & Scope

## Model Buku

### Accessor

#### Status Stok Badge

* Stok = 0 → Habis
* Stok 1–5 → Menipis
* Stok 6–15 → Sedang
* Stok > 15 → Aman

#### Tahun Label

* Tahun >= 2024 → Buku Baru
* Tahun < 2024 → Buku Lama

### Scope

* stokMenipis()
* hargaRange()
* terbaru()

---

## Model Anggota

### Accessor

#### Status Badge

* Aktif
* Nonaktif

#### Kategori Usia

* Umur < 20 → Remaja
* Umur 20–50 → Dewasa
* Umur > 50 → Senior

### Scope

* jenisKelamin()
* terdaftarBulanIni()

---

# Testing Route

Route yang digunakan:

```php
/test-accessor-scope
```

Fitur yang diuji:

* Status stok buku
* Label tahun buku
* Buku terbaru
* Buku stok menipis
* Status anggota
* Kategori usia anggota
* Anggota terdaftar bulan ini

### Screenshot Hasil Testing

![Testing Accessor Scope](screenshots/test-accessor-scope.png)

---

# Testing Kategori

## Daftar Kategori

![Daftar Kategori](screenshots/kategori-index.png)

## Detail Kategori

![Detail Kategori](screenshots/kategori-detail.png)

## Pencarian Kategori

![Pencarian Kategori](screenshots/kategori-search.png)

---



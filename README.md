
# 📦 Asset Management System (Django)

Sebuah aplikasi manajemen aset IT berbasis web menggunakan Django Framework.
Aplikasi ini memungkinkan pengguna untuk mencatat aset dan spesifikasinya sesuai jenis aset.

## ✨ Fitur Utama
- CRUD Asset (Create, Read, Update, Delete)
- Input spesifikasi aset (otomatis berdasarkan kategori)
- Django Admin Interface kustom
- Struktur data rapi dan relasi antar tabel jelas

## 🛠️ Teknologi yang Digunakan
- Python 3.13
- Django 5.1.6
- Database: SQLite (default Django) atau bisa diubah ke MySQL
- HTML5, CSS (Admin bawaan Django)

## 🧩 Alur Penggunaan Aplikasi

1. **Login** ke Django Admin.
2. **Tambah Asset**:
   - Isi nama, kategori, tanggal pembelian, dan status.
3. **Tambah Spesifikasi**:
   - Setelah asset ditambahkan, lengkapi spesifikasinya sesuai kategori.
   - Untuk PC: prosesor, RAM, penyimpanan, lain-lain.
   - Untuk Printer: jenis tinta, resolusi cetak, kecepatan cetak.
4. **Simpan** dan data siap untuk dipantau.

## 🔥 Flowchart User Journey

```
[Start] 
   ↓
[Login ke Django Admin] 
   ↓
[Klik Add di Asset] 
   ↓
[Isi Data Aset]
   ↓
[Simpan Asset]
   ↓
[Klik Tambah/Edit Spesifikasi]
   ↓
[Isi Spesifikasi Aset]
   ↓
[Simpan]
   ↓
[Asset + Spesifikasi Terdaftar]
   ↓
[End]
```

## 🗂️ Entity Relationship Diagram (ERD)
- **Asset** 
  - id (PK)
  - nama
  - kategori
  - tanggal_pembelian
  - status

- **Spesifikasi**
  - id (PK)
  - asset_id (FK ke Asset)
  - prosesor / jenis tinta
  - RAM / resolusi cetak
  - penyimpanan / kecepatan cetak
  - lain-lain

(Relasi: 1 Asset hanya punya 1 Spesifikasi — OneToOne Relationship)

## 🚀 Cara Menjalankan Project

1. Aktifkan virtual environment:
   ```bash
   .\env\Scripts\activate
   ```

2. Jalankan server Django:
   ```bash
   python manage.py runserver
   ```

3. Buka di browser:
   ```bash
   http://127.0.0.1:8000/admin
   ```

4. Login dan mulai input asset serta spesifikasi.

---

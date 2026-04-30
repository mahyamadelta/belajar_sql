# Catatan Belajar SQL: Hari ke-1
Hari ini saya fokus pada pondasi dasar paling dasar dalam SQL: **Bagaimana cara mengambil data dari database?**

## 1. Konsep Dasar SELECT
Perintah `SELECT` adalah perintah paling fundamental dalam SQL yang digunakan untuk menampilkan data dari satu atau lebih lebih tabel dari database.

**Sintaks Utama:**
- Mengambil seluruh kolom
  ```SQL
  -- Mengambil semua data dari tabel
  SELECT * FROM nama_tabel;

  -- Mengambil semua data dengan spesifikasi database (schema)
  SELECT * FROM nama_database.nama_tabel;
  ```
- Mengambil kolom tertentu
  Digunakan untuk mengambil kolom spesifik agar performa kueri lebih ringan.
  ```SQL
  -- Memilih kolom spesifik dipisahkan dengan koma
  SELECT * kolom_1, kolom_2, kolom_n FROM nama_database.nama_tabel
  ```

# 2. Menampilkan Nilai Unik dengan DISTINCT
Terkadang kita hanya ingin tahu ada kategori apa saja di suatu kolom tanpa melihat data yang berulang (duplikat).
``` SQL
-- Contoh: Studi kasus ingin melihat asal kota murid di suatu kelas
SELECT DISTINCT nama_kolom FROM nama_tabel;
```

# 3. Keyword yang Dipelajari
| Keyword | Fungsi |
| -------- | ------- |
| `SELECT` | Titik awal kueri untuk menentukan data mana yang ingin ditampilkan. |
| `*` (bintang) | Simbol untuk memilih semua kolom yang berada di tabel. |
| `FROM` | Menentukan asal tabel/database tempat data disimpan. |
| `DISTINCT` | Menampilkan data yang unik |

# Catatan Belajar SQL: Hari ke-2
Hari ini saya belajar tentang cara menyaring/mencari data agar hasil yang ditampilkan lebih spesifik menggunakan klausa `WHERE` dan bantuan `Wildcards`.

## 1. Klausa WHERE
`WHERE` digunakan untuk memfilter baris data berdasarkan kondisi tertentu.

**Sintaks Dasar:**
  ```SQL
  SELECT * FROM nama_tabel WHERE nama_kolom = kondisi;
  ```

**Contoh Penggunaan**
  ```SQL
  -- Mengambil data siswa yang berdomisili di Jakarta
  SELECT * FROM siswa
  WHERE provinsi = 'Jakarta';
  ```

# 2. Operator Perbandingan & Logika
SQL memungkinkan penggunaan operator matematika dan logika untuk membuat filter yang lebih kompleks.
**Operator Perbandingan:**
| Operator | Deskripsi | Contoh |
| -------- | ------- | ------- |
| = | Sama dengan | `WHERE usia = 10` |
| `!=` atau `<>` | Tidak sama dengan | `WHERE kelas != '11E' |
| `>` | Lebih besar dari | `WHERE nilai > 75` |
| `<` | Lebih kecil dari | `WHERE stok < 5` |
| `>=` | Lebih besar atau sama dengan | `WHERE usia >= 17` |
| `<=` | Lebih kecil atau sama dengan | `WHERE harga <= 50000` |

**Operator Logika (AND, OR, NOT):**
Digunakan untuk menghubungkan lebih dari satu kondisi.
```SQL
-- Contoh: Mengambil siswa bernama Budi yang berusia 14 tahun, 
-- ATAU semua siswa yang usianya di atas 10 tahun.
SELECT * FROM siswa
WHERE (nama = 'Budi' AND usia = 14) OR usia > 10;
```

# 3. Like Statement (Pencarian Pola)
Klausa `LIKE` digunakan bersama dengan _Wildcards_ untuk mencari pola teks tertentu dalam kolom.
A. Wildcard Persen (`%`)
Mewakili karakter dalam jumlah berapapun (nol, satu, atau banyak)
```SQL
-- Mencari nama yang berawalan "Bu" (Budi, Bungan, Burhan)
SELECT * FROM siswa
WHERE nama LIKE 'Bu%';
```

B. Wildcard Underscore (`_`)
Mewakili tepat satu karakter tunggal
```SQL
-- Mencari nama yang diawali "An" dan diikuti tepat 2 karakter setelahnya
-- Contoh: Andi (A-n-d-i)
SELECT * FROM siswa
WHERE nama LIKE 'An__';
```

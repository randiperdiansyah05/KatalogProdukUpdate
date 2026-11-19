# KatalogProdukUpdate

# KATALOG PRODUK

## 1. Deskripsi Project

Katalog Produk merupakan aplikasi desktop berbasis Java yang digunakan untuk mengelola data produk. Aplikasi ini dikembangkan menggunakan JavaFX sebagai antarmuka pengguna dan SQLite sebagai database untuk menyimpan data produk.

Aplikasi ini memungkinkan pengguna untuk menambahkan, melihat, memperbarui, dan menghapus data produk melalui tampilan katalog yang sederhana dan mudah digunakan.

## 2. Fitur Aplikasi

Aplikasi Katalog Produk memiliki beberapa fitur utama:

### A. Create (Tambah Produk)
- Menambahkan produk baru ke dalam katalog.
- Menginput nama produk.
- Menginput harga produk.
- Memilih foto produk yang tersedia.
- Menyimpan data produk ke database SQLite.

### B. Read (Menampilkan Produk)
- Menampilkan seluruh produk yang tersimpan di database.
- Menampilkan nama produk.
- Menampilkan harga produk.
- Menampilkan foto produk.
- Menampilkan ID produk.
- Menampilkan jumlah keseluruhan produk.

### C. Update (Memperbarui Produk)
- Memilih produk yang ingin diperbarui melalui tombol Update.
- Data produk yang dipilih otomatis ditampilkan kembali pada form.
- Mengubah nama produk.
- Mengubah harga produk.
- Mengganti foto produk.
- Menyimpan perubahan ke database.
- Menyediakan tombol Batal Update untuk membatalkan proses perubahan.

### D. Delete (Menghapus Produk)
- Menghapus produk melalui tombol Delete.
- Menampilkan konfirmasi sebelum produk dihapus.
- Menghapus data produk dari database SQLite.

- Memperbarui tampilan katalog setelah penghapusan berhasil.

  Before

<img width="752" height="540" alt="Cuplikan layar 2026-11-19 224748" src="https://github.com/user-attachments/assets/be319d5c-b9bb-4270-b28e-77eb8e743fdd" />

  After

  <img width="752" height="540" alt="Cuplikan layar 2026-11-19 224800" src="https://github.com/user-attachments/assets/405651f4-6162-40f5-86b8-5790a225242a" />  

## 3. Teknologi yang Digunakan

Teknologi Kegunaan 
Java 17 : Bahasa pemrograman
JavaFX 21 : Membuat antarmuka aplikasi
FXML : Mengatur struktur tampilan 
CSS : Mengatur desain dan tampilan aplikasi 
SQLite : Database penyimpanan produk 
JDBC : Menghubungkan Java dengan SQLite 
Maven : Mengelola dependency dan proses build 

## 4. Struktur Project

<img width="960" height="505" alt="Cuplikan layar 2026-11-19 224919" src="https://github.com/user-attachments/assets/f1b5d16b-c522-451a-bde2-0c6379a737ec" />



## 5. Penjelasan Komponen Program

### Model
`Produk.java`

Berfungsi sebagai representasi objek produk yang memiliki atribut:
- ID
- Nama
- Harga
- Foto

Atribut menggunakan access modifier private untuk menerapkan konsep encapsulation.

### Controller
`KatalogController.java`

Mengatur interaksi antara pengguna dengan aplikasi, seperti:
- Menambahkan produk.
- Menampilkan produk.
- Memperbarui produk.
- Menghapus produk.
- Melakukan validasi input.
- Menampilkan pesan informasi dan konfirmasi.

### Data
`ProdukRepository.java`

Berfungsi mengelola operasi database menggunakan JDBC dan perintah SQL, meliputi:
- INSERT untuk menambahkan produk.
- SELECT untuk mengambil data produk.
- UPDATE untuk memperbarui produk.
- DELETE untuk menghapus produk.

### Database
`Database.java`

Berfungsi mengatur koneksi SQLite dan membuat tabel produk secara otomatis apabila tabel belum tersedia.

### Main
`MainApp.java`

Merupakan class utama untuk menjalankan aplikasi, mempersiapkan database, dan menampilkan halaman katalog.

## 6. Struktur Database

Nama database: `katalog.db`

Nama tabel: `produk`

| Nama Kolom | Tipe Data | Keterangan |
|---|---|---|
| id | INTEGER | Primary Key |
| nama | TEXT | Nama produk |
| harga | INTEGER | Harga produk |
| foto | TEXT | Nama file foto produk |

Database dibuat secara otomatis di dalam folder `data` pada direktori kerja aplikasi ketika pertama kali dijalankan.

## 7. Validasi Data

Aplikasi menerapkan beberapa validasi:
- Nama produk tidak boleh kosong.
- Harga harus berupa angka bulat.
- Harga harus lebih besar dari nol.
- Foto produk wajib dipilih.
- Penghapusan produk harus melalui konfirmasi pengguna.

## 8. Cara Menjalankan Aplikasi

1. Pastikan Java Development Kit (JDK) 17 atau lebih baru sudah terinstal.
2. Buka project menggunakan NetBeans atau IDE yang mendukung Maven.
3. Tunggu proses pengunduhan dependency Maven selesai.
4. Pastikan konfigurasi JavaFX tersedia sesuai kebutuhan sistem.
5. Jalankan aplikasi melalui class `MainApp.java` atau gunakan perintah:

bash
mvn clean javafx:run

## 9. Tujuan Pengembangan

Project ini dibuat untuk menerapkan konsep pemrograman berorientasi objek (OOP), pengelolaan database, serta implementasi operasi CRUD dalam pengembangan aplikasi desktop menggunakan Java.

## 10. Penutup

Dengan adanya fitur Create, Read, Update, dan Delete, aplikasi Katalog Produk diharapkan dapat membantu proses pengelolaan data produk secara lebih mudah, terstruktur, dan efisien.

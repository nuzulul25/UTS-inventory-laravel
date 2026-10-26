# 👟 UTS Laravel - Sistem Inventori Toko Sepatu
Aplikasi web Sistem Inventori Toko Sepatu berbasis Laravel yang dirancang untuk mengelola data produk, kategori, supplier, 
serta pencatatan transaksi stok barang masuk (IN) dan keluar (OUT) secara multi-produk dengan arsitektur yang aman dan terstruktur.

# 🚀 Tentang Proyek
Proyek ini dibuat untuk memenuhi Ujian Tengah Semester (UTS) mata kuliah Pemrograman Web / Pemrograman Framework menggunakan
Laravel. Sistem ini mengimplementasikan konsep *Header-Detail* pada transaksi stok, manajemen hak akses berbasis *role* 
(Owner, Admin, Staf Gudang), serta pencatatan laporan rekapitulasi stok.

# ✨ Fitur Utama
* Autentikasi & Hak Akses (Role-Based): Pembagian hak akses antara Owner, Admin, dan Staf Gudang.
* Manajemen Data Master: Pengelolaan Data Sepatu (Produk), Kategori, dan Supplier.
* Transaksi Stok Multi-Produk: Pencatatan barang masuk (`IN`) dan barang keluar (`OUT`) dengan banyak produk dalam satu nomor transaksi (`StockTransaction` dan `StockTransactionDetail`).
* Laporan Transaksi Stok: Rekapitulasi pergerakan keluar-masuk barang lengkap dengan fitur cetak laporan (`print`).
* Manajemen Aset & Dashboard: Pemantauan total produk, aset toko, dan peringatan stok menipis (`<= 5`).

# 🗄️ ERD & Penjelasan Relasi
Sistem ini menggunakan relasi database relasional sebagai berikut:
* categories 1 ke Banyak products: Satu kategori dapat memiliki banyak produk sepatu.
* suppliers 1 ke Banyak stock_transactions: Satu supplier dapat menyuplai barang pada beberapa transaksi masuk.
* stock_transactions 1 ke Banyak stock_transaction_details: Model *Header-Detail* di mana satu transaksi utama dapat mencakup banyak item produk.
* products 1 ke Banyak stock_transaction_details: Produk tercatat di dalam detail transaksi pergerakan stok.

# 🔑 Akun Demo
Berikut adalah kredensial akun yang dapat digunakan untuk masuk ke dalam aplikasi berdasarkan *role*:
| Role | Email | Password |
| :--- | :--- | :--- |
| **Owner** | `owner@toko.com` | `password` |
| **Staf Gudang** | `staf@toko.com` | `password` |

# 🖼️ Screenshots Halaman Utama & Transaksi
* Halaman Utama
  <img width="945" height="445" alt="Halaman Utama" src="https://github.com/user-attachments/assets/7096658c-5863-4658-af6e-c546f4e5d667" />

* Transaksi Stok
<img width="952" height="439" alt="Transaksi Stok" src="https://github.com/user-attachments/assets/e4ea591e-0f03-4cc3-923c-83443c4dd0e6" />


* Laporan Transaksi
<img width="947" height="436" alt="Transaksi" src="https://github.com/user-attachments/assets/044e454d-7fce-4029-97bb-a16089697bb3" />


  


  

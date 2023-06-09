# Super Cashier

## I. LATAR BELAKANG

Membuat program kasir self-service dimana customer bisa langsung memasukkan jenis item, jumlah item, dan harga item yang dibeli dan fitur-fitur lainnya.

## II. REQUIREMENT ATAU OBJECTIVES
Membuat program yang dapat melakukan:
1. Input ID transaksi
2. Menambahkan nama item, jumlah item, dan harga item yang dibeli
3. Memperbaiki item yang dibeli jika ada salah input
4. Menghapus salah satu atau seluruh item pesanan
5. Mengecek daftar item pesanan
6. Menghitung total pesanan


### A. Fungsi dalam program:
1. Customer membuat ID transaksi customer: `trnsct_123 = transaction()`

2. Customer menambahkan nama item, jumlah item, dan harga item yang dibeli: 
`add_item([<nama item>`, `<jumlah item>`, `<harga per item>])`

3. Jika customer salah menambahkan item yang dibeli, customer bisa update:
- Nama item: `update_item_name(<nama item>, <update nama item>)`
- Jumlah item: `update_item_qty(<nama_item>, <update jumlah item>)`
- Harga item: `update_item_price(<nama_item>, <update harga item>)`

4. Jika customer batal membeli,
- Customer bisa menghapus salah satu item pesanan: `delete_item(<nama item>)`
- Customer bisa menghapus seluruh item pesanan: `reset_transaction()`

5. Jika sudah selesai input, customer bisa mengecek daftar item pesanan yang sudah ditambahkan: `check_order()`
Dengan ketentuan:
- Jika tidak ada kesalahan input, maka keluar pesan “Pemesanan sudah benar”
- Jika terjadi kesalahan input, maka keluar pesan “Terdapat kesalahan input data”
- Lalu mengeluarkan fungsi output pesanan yang sudah dibeli

6. Jika sudah mengecek, customer bisa menghitung total pesanan yang dibeli: `total_price()`. Dengan ketentuan:
- Jika total belanja > Rp200.000, makan dapat diskon 5%
- Jika total belanja > Rp300.000, makan dapat diskon 8%
- Jika total belanja > Rp500.000, makan dapat diskon 10%


### B. Alur program atau flowchart:
<img width="483" alt="Flowchart" src="https://github.com/zlippery/Cashier/assets/132915662/4d5faf93-046f-45c5-a0fe-c100d7855489">

## III. FUNCTIONS
Semua fungsi terdapat di dalam class Transaction
- Atribut parameter: `<nama item>`, `<jumlah item>`, `<harga per item>`
- Method `add_item`: Fungsi tambah item pesanan baru ke transaksi
- Method `update_item_name`: Fungsi mengubah nama item pesanan
- Method `update_item_qty`: Fungsi ini untuk mengubah jumlah item pesanan
- Method `update_item_price`: Fungsi ini untuk mengubah harga item pesanan
- Method `delete_item`: Fungsi ini untuk menghapus salah satu item pesanan
- Method `reset_transaction`: Fungsi ini untuk menghapus seluruh item pesanan atau reset transaksi
- Method `check_order`: Fungsi ini untuk mengecek daftar item pesanan yang sudah ditambahkan dan memanggil method show_transaction
- Method `show_transaction`: Fungsi ini untuk menampilkan daftar seluruh item pesanan
- Method `total_price`: Fungsi ini untuk menghitung total pesanan yang dibeli, total diskon, dan total bayar

## IV. TEST CASE
1. Customer menambah item `add_item`:
- Item: ayam goreng, qty: 2, harga: 20000
- Item: pasta gigi, qty: 3, harga 15000
<img width="521" alt="Cashier_Test 1" src="https://github.com/zlippery/Cashier/assets/132915662/3e0cb4a8-3d26-406a-b2bc-456f7af3a025">

2. Customer menghapus item `delete_item`
Item: pasta gigi
<img width="526" alt="Cashier_Test 2" src="https://github.com/zlippery/Cashier/assets/132915662/bdc11021-c81d-4aec-b4bb-ce1ed2fd76f2">

3. Customer menghapus seluruh pesanan yang ditambahkan `reset_transaction`
<img width="291" alt="Cashier_Test 3" src="https://github.com/zlippery/Cashier/assets/132915662/e38ce82a-6914-485b-b4ef-eebdaaaeee9d">

4. Customer menghitung total pesanan `total_price`:
- Item: ayam goreng, qty: 2, harga: 20000
- Item: pasta gigi, qty: 3, harga 15000
- Item: mainan mobil, qty: 1, harga 200000
- Item: mi instan, qty: 5, harga 3000
<img width="423" alt="Cashier_Test 4" src="https://github.com/zlippery/Super-Cashier/assets/132915662/fe2ea167-3bbe-46fd-8880-1227cb8bcc4f">


## V. CONCLUSION/FUTURE WORK
Super Cashier adalah program sederhana untuk mengelola transaksi pembelian barang. Customer dapat menambahkan item, mengubah nama item, jumlah, dan harga item, menghapus item, melakukan reset transaksi, melihat pesanan, dan menghitung total belanja. Setelah customer memilih menu "Total Price", akan ditampilkan item yang dibeli dan total yang harus dibayar. Program ini memberikan kemudahan dalam mengelola transaksi pembelian barang dengan interaksi yang jelas dan sederhana.

Rekomendasi improvement untuk kedepannya:
- Menerapkan Exception Handling, menggunakan blok try-except untuk menangkap error input
- Menambahkan Validasi Input untuk memastikan bahwa nilai yang dimasukkan oleh customer sesuai dengan ekspektasi fungsi
- Menggunakan Libraries Tambahan untuk menampilkan program lebih mudah dan enak dilihat

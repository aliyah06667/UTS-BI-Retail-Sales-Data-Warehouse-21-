# UTS BI Retail Sales Data Warehouse Project

<img width="2100" height="700" alt="Run with Jazz Party (1200 x 400 px) (6)" src="https://github.com/user-attachments/assets/8eba6d29-c7df-45d2-bf55-e977a2744438" />

**Nama Anggota:**

1. Nabila Imtiyaz Agustin (011)
2. Zahra Aulia Rahmah (020)
3. Aliyah Azzah Sekedang (021)

<details>
<summary><h2>📁 DESKRIPSI PROYEK<h2></summary>

Proyek ini bertujuan untuk merancang dan mengimplementasikan Data Warehouse berbasis star schema menggunakan dataset _**Sales Forecasting (Retail)**_. Data Warehouse dibangun untuk mendukung analisis tren penjualan berdasarkan dimensi waktu, toko, dan produk.

Melalui proyek ini dilakukan proses ETL (_Extract, Transform, Load_) untuk mengubah data mentah menjadi struktur terorganisir yang siap digunakan untuk analisis dan pengambilan keputusan bisnis.

---
</details>

<details>
<summary><h2>📁 LATAR BELAKANG<h2></summary>

Dalam era digital saat ini, perusahaan retail menghasilkan data transaksi dalam jumlah besar setiap harinya. Data tersebut mencakup informasi mengenai tanggal transaksi, jumlah penjualan, produk yang terjual, serta lokasi toko. Volume data yang terus meningkat memerlukan sistem pengelolaan yang mampu menyimpan, mengintegrasikan, dan menganalisis data secara efektif untuk mendukung pengambilan keputusan strategis.

Salah satu solusi yang digunakan dalam pengelolaan data skala besar adalah Data Warehouse. Data Warehouse memungkinkan integrasi data dari berbagai sumber ke dalam satu sistem terstruktur yang dirancang khusus untuk kebutuhan analisis dan pelaporan. Dengan struktur seperti star schema, data dapat diorganisasikan ke dalam tabel fakta dan tabel dimensi sehingga memudahkan proses analisis multidimensi.

Dataset Sales Forecasting (Retail) yang digunakan dalam penelitian ini berisi data historis penjualan dari beberapa toko dan item dalam rentang waktu tertentu. Dataset ini memiliki atribut utama seperti tanggal, store, item, dan jumlah penjualan (sales). Data tersebut sangat relevan untuk dianalisis guna mengetahui pola tren penjualan, performa produk, serta potensi peramalan (forecasting) di masa mendatang.

Oleh karena itu, pada proyek ini dilakukan perancangan dan implementasi Data Warehouse berbasis star schema untuk mengolah dataset penjualan retail tersebut. Hasil implementasi diharapkan dapat mendukung analisis tren penjualan dan memberikan insight yang bermanfaat bagi pengambilan keputusan bisnis.

---
</details>

<details>
<summary><h2>📁 TAHAPAN PROSES<h2></summary>

### ERD - Star Schema Data Warehouse Penjualan

<img width="1298" height="617" alt="BI KELOMPOK 21-Page-2 drawio" src="https://github.com/user-attachments/assets/261d0fee-1f6f-43e7-a01a-42d411bd7728" />

### Penjelasan Struktur Tabel pada Star Schema

Berikut adalah penjelasan masing-masing tabel pada rancangan *data warehouse* yang digunakan:

#### 1. Tabel Fakta: `fact_sales`

* Merupakan tabel utama yang menyimpan data transaksi penjualan.
* Berfungsi sebagai pusat analisis dalam data warehouse.
* Menyimpan informasi:

  * `order_id` : ID pesanan/transaksi
  * `order_date` : tanggal transaksi
  * `customer_id` : ID pelanggan
  * `product_id` : ID produk
  * `sales` : total nilai penjualan
* Digunakan untuk menghitung total penjualan, tren penjualan, dan performa bisnis.

#### 2. Tabel Dimensi Waktu: `dim_date`

* Menyimpan informasi terkait waktu transaksi.
* Berisi:

  * `order_date` : tanggal transaksi
  * `day` : hari
  * `month` : bulan
  * `year` : tahun
  * `quarter` : kuartal
* Digunakan untuk analisis penjualan berdasarkan periode waktu.

#### 3. Tabel Dimensi Produk: `dim_product`

* Menyimpan informasi detail produk.
* Berisi:

  * `product_id` : ID produk
  * `product_name` : nama produk
  * `category` : kategori produk
  * `sub_category` : subkategori produk
* Digunakan untuk mengetahui produk terlaris dan performa kategori.

#### 4. Tabel Dimensi Pelanggan: `dim_customer`

* Menyimpan data pelanggan.
* Berisi:

  * `customer_id` : ID pelanggan
  * `customer_name` : nama pelanggan
  * `segment` : segmen pelanggan
* Digunakan untuk analisis perilaku pelanggan dan segmentasi pasar.

#### 5. Tabel Dimensi Lokasi: `dim_location`

* Menyimpan informasi wilayah transaksi atau pengiriman.
* Berisi:

  * `city` : kota
  * `country` : negara
  * `state` : provinsi/wilayah
  * `region` : kawasan
* Digunakan untuk analisis distribusi penjualan berdasarkan lokasi.

### Hubungan Antar Tabel

* Tabel `fact_sales` terhubung dengan seluruh tabel dimensi.
* Relasi yang digunakan adalah *one-to-many*:

  * satu tanggal dapat memiliki banyak transaksi,
  * satu produk dapat muncul di banyak transaksi,
  * satu pelanggan dapat melakukan banyak transaksi,
  * satu lokasi dapat memiliki banyak data penjualan.
* Struktur *star schema* ini mempermudah proses analisis data, visualisasi dashboard, dan pengambilan keputusan bisnis.

---
</details>

<details>
<summary><h2>📁 ETL<h2></summary>


---
</details>

<details>
<summary><h2>📁 ANALISIS DATA<h2></summary>


---
</details>

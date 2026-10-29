# Analisis Perilaku Interaksi Pengguna E-Commerce (2022-2023)

## Latar Belakang
Toko online ingin memahami jenis produk dan periode waktu yang paling
menarik perhatian pengguna, supaya stok dan promosi bisa direncanakan
lebih baik.

## Pertanyaan Bisnis
1. Bagaimana proporsi view, like, dan purchase?
2. Subkategori produk mana yang punya porsi purchase tinggi?
3. Kapan interaksi pengguna memuncak?
4. Apakah harga berhubungan dengan jenis interaksi?

## Data
- E-commerce sales data 2024.csv: log interaksi (3.294 baris awal)
- product_details.csv: katalog produk (10.002 baris)
- customer_details.csv: tidak dipakai (lihat Keterbatasan)

## Proses
1. Cleaning: hapus 295 baris kosong dan kolom kosong, ubah tipe data,
   parse tanggal (format hari/bulan/tahun)
2. Cleaning produk: ambil kolom relevan, ubah harga ke angka, pecah kategori
3. Merge interaksi dengan produk (semua 2.999 produk cocok)
4. Analisis pada 2.871 baris yang punya jenis interaksi

## Temuan Utama
1. Like (39,9%) lebih banyak dari view (30,3%) dan purchase (29,8%).
2. Interaksi memuncak di Oktober-Desember 2023 (puncak November, sekitar
   565 interaksi), jauh di atas rata-rata Februari-September.
3. Subkategori dengan sampel besar dan porsi purchase tinggi: Dolls &
   Accessories (38,9%), Dress Up & Pretend Play (34,6%), Hobbies (34,4%).
4. Harga tidak membedakan jenis interaksi (median sekitar $15-16).

## Rekomendasi
- Tambah stok dan promosi mainan sebelum Oktober.
- Prioritaskan subkategori Dolls, Dress Up, dan Hobbies saat musim liburan.
- Selidiki penyebab lonjakan Januari (apakah promo?).

## Keterbatasan
- Setiap user hanya muncul sekali, jadi ini bukan funnel sungguhan dan
  tidak bisa dihitung conversion rate.
- Pola view/like/purchase tidak lazim, kemungkinan data sintetis.
- 128 baris tanpa jenis interaksi dan 275 produk tanpa kategori
  dikeluarkan dari analisis terkait.
- customer_details.csv tidak bisa dihubungkan karena isinya produk
  fashion AS yang berbeda dari katalog.
- Perbedaan antar subkategori kecil dan bisa jadi kebetulan.

Sumber: Kaggle, dataset "e-commerce-sales-data-2024" oleh datascientist97

# End-to-End Market Basket Recommendation System
# 🧠 End-to-End Market Basket Recommendation System

Algoritma **Apriori** digunakan untuk menemukan pola asosiasi antar item dalam data transaksi.  
Proyek ini menerapkan Apriori untuk menganalisis kebiasaan pembelian pelanggan dan menghasilkan **aturan asosiasi** yang dapat dimanfaatkan untuk **rekomendasi produk**, **penataan display toko**, atau **strategi promosi** berbasis data.

---

## 📘 Apa Itu Apriori?

**Apriori** merupakan algoritma *data mining* yang digunakan untuk menemukan hubungan antar item dalam sekumpulan transaksi.  
Hasil analisis Apriori berupa aturan seperti:

> 🛒 *Jika pelanggan membeli Tenda → maka kemungkinan besar juga membeli Sleeping Bag.*

Dengan pola seperti ini, toko dapat menata ulang produk agar lebih strategis atau membuat paket promosi berdasarkan perilaku pelanggan.

---

## ⚙️ Alur Proses Apriori

1. **Preprocessing Data**  
   - Membersihkan data dari duplikasi atau transaksi tidak relevan.  
   - Mengubah data transaksi menjadi format *itemset* (setiap baris = daftar barang yang dibeli).

2. **Pembentukan Frequent Itemset**  
   - Menentukan kombinasi item yang sering muncul bersama menggunakan ambang *minimum support*.
   - Rumus:
     \[
     Support(A) = \frac{\text{Jumlah Transaksi yang Mengandung A}}{\text{Jumlah Transaksi Keseluruhan}}
     \]

3. **Pembentukan Aturan Asosiasi**  
   - Membuat aturan “Jika A → maka B” berdasarkan nilai *confidence*.  
   - Rumus:
     \[
     Confidence(A \rightarrow B) = \frac{Support(A \cup B)}{Support(A)}
     \]

4. **Evaluasi Aturan**  
   - Menggunakan ukuran seperti **Lift Ratio** untuk menilai kekuatan hubungan antar item.  
     \[
     Lift(A \rightarrow B) = \frac{Confidence(A \rightarrow B)}{Support(B)}
     \]  
   - Lift > 1 menandakan adanya hubungan positif antara A dan B.

---

## 🧩 Contoh Dataset

| ID Transaksi | Item yang Dibeli                              |
|---------------|-----------------------------------------------|
| T001          | Tenda, Sleeping Bag, Matras                   |
| T002          | Kompor Portable, Gas Mini, Panci Lipat        |
| T003          | Sleeping Bag, Matras, Bantal Angin            |
| T004          | Tenda, Lampu Camping, Kompor Portable         |

---

## 📊 Contoh Hasil Analisis

| Aturan Asosiasi | Support | Confidence | Lift |
|------------------|----------|-------------|------|
| Tenda → Sleeping Bag | 0.40 | 0.75 | 1.50 |
| Sleeping Bag → Matras | 0.35 | 0.68 | 1.30 |
| Kompor Portable → Gas Mini | 0.25 | 0.90 | 2.10 |

Dari tabel di atas, dapat disimpulkan bahwa pelanggan yang membeli **Tenda** cenderung juga membeli **Sleeping Bag**. Pola ini dapat dimanfaatkan untuk **display toko atau promosi bundling**.

---

## 🛠️ Tools & Teknologi

- **Bahasa Pemrograman:** PHP  
- **Framework:** Laravel  
- **Database:** MySQL  
- **Metodologi Pengembangan:** Agile Development  
- **Analisis Algoritma:** Apriori

---

## 🚀 Tujuan Penelitian

Proyek ini dikembangkan untuk:
- Mengoptimalkan pengelolaan data transaksi penjualan.  
- Menghasilkan insight pola pembelian pelanggan.  
- Mendukung pengambilan keputusan berbasis data melalui *recommendation system* sederhana.

---

## 📚 Referensi

[1] Angela, “Metode Agile: Pengertian, Tujuan, dan Prinsipnya,” *Binar.co.id*, Apr. 03, 2024.  
[2] Han, J., Kamber, M., & Pei, J. (2012). *Data Mining: Concepts and Techniques*. Morgan Kaufmann Publishers.  
[3] Tan, P.-N., Steinbach, M., & Kumar, V. (2019). *Introduction to Data Mining*. Pearson Education.

---



---

> “Data tells stories — Apriori helps you listen.”



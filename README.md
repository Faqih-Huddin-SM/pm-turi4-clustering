# Praktikum - Clustering dengan K-Means
 
**Nama:** Faqih Huddin SM.
**NIM:** 2488010061
**Kelas:** Informatika / 5B
**Mata Kuliah:** Machine Learning
 
## Ringkasan
 
Praktikum ini membahas clustering dengan algoritma K-Means pada data segmentasi pelanggan buatan (200 pelanggan) yang berisi usia, pendapatan, dan skor belanja tanpa label. Kegiatan yang dilakukan meliputi scaling data, menentukan jumlah cluster dengan metode Elbow, menjalankan K-Means, menilai hasilnya dengan silhouette score, memberi nama tiap cluster berdasarkan profil rata-ratanya, serta latihan mandiri dan refleksi.
 
## Isi Repositori
 
- `PM_P9_Faqih_Huddin_SM__2488010061.ipynb` : notebook praktikum
## Temuan Utama
 
- Data di-scaling dengan StandardScaler karena K-Means bergantung pada jarak, sedangkan pendapatan angkanya jauh lebih besar daripada usia dan skor belanja.
- Pada grafik Elbow, inertia turun tajam sampai K=3 lalu melandai, jadi K=3 dipilih sebagai jumlah cluster.
- Hasil K-Means dengan K=3 membagi data menjadi 60, 70, dan 70 pelanggan, dengan silhouette score 0,774.
- Dengan K=5, silhouette score turun menjadi 0,613, sehingga K=3 lebih baik.
- Tiga cluster yang terbentuk:
| Cluster | Usia (rata-rata) | Pendapatan (rata-rata) | Skor belanja (rata-rata) | Nama |
|---|---|---|---|---|
| 0 | 59,9 | Rp4.473.333 | 19,0 | Senior Hemat |
| 1 | 25,2 | Rp5.880.000 | 79,6 | Muda Belanja Tinggi |
| 2 | 45,1 | Rp15.054.286 | 50,2 | Mapan Belanja Sedang |
 
- Tanpa scaling, kelompok Senior Hemat dan Muda Belanja Tinggi tercampur dalam satu cluster karena pendapatan mereka berdekatan. Silhouette-nya terlihat bagus (0,740) jika dihitung di data mentah, tetapi turun menjadi 0,203 jika dihitung di data yang sudah di-scaling. Jadi scaling wajib dilakukan.
- Scatter plot usia (x) vs skor belanja (y) menunjukkan tiga gerombol yang terpisah jelas beserta posisi centroid-nya.

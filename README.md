# KLASIFIKASI DATA CREDIT SCORE DENGAN IBM GRANITE
**Capstone Project - Hacktiv8 x IBM**

## Deskripsi Proyek
Proyek ini disusun untuk menyelesaikan Capstone Project yang diberikan oleh Hacktiv8 bekerja sama dengan IBM. Tujuan utama dari proyek ini adalah untuk mengklasifikasikan individu ke dalam kategori *Credit Score* berdasarkan karakteristik demografis dan finansial menggunakan algoritma Perceptron.

Fokus analisis berada pada evaluasi performa model klasifikasi linier (Perceptron) dalam memprediksi tingkat kelayakan kredit, dengan memanfaatkan fitur-fitur utama seperti usia, pendapatan, dan jumlah anak sebagai prediktor. Proyek ini juga menekankan pada proses analisis berbasis *prompt engineering* untuk menguji potensi kolaborasi antara *data science* dan kecerdasan buatan generatif.

## Data
Data yang digunakan merupakan data dummy yang diambil dari Kaggle dan menyimulasikan profil *Credit Score* dari lebih dari 100 individu di berbagai negara.

Link Dataset: [Kaggle - Credit Score Classification Dataset](https://www.kaggle.com/datasets/sujithmandala/credit-score-classification-dataset/data)

Dataset ini terdiri dari beberapa variabel berikut:
1. Age  
2. Gender  
3. Income  
4. Education  
5. Marital Status  
6. Number of Children  
7. Home Ownership  
8. Credit Score  

Untuk keperluan analisis ini, hanya 100 data pertama dari dataset yang digunakan guna menyederhanakan proses dan visualisasi.

## Temuan dan Insight
Setelah dilakukan pelatihan menggunakan model Perceptron, diperoleh akurasi sekitar **83%** pada data uji. Di antara fitur input, pendapatan (*Income*) memiliki pengaruh yang relatif lebih tinggi dibandingkan usia dan jumlah anak.

Model Perceptron secara internal menggunakan pendekatan *One-vs-Rest (OvR)* dalam menangani klasifikasi multikelas, yaitu membangun satu model untuk masing-masing kelas terhadap kelas lainnya. Meskipun termasuk model linier sederhana, Perceptron mampu memberikan hasil yang cukup baik pada dataset ini, membuktikan bahwa model dengan kompleksitas rendah tetap relevan dalam konteks data terstruktur.

## Penjelasan Dukungan AI
Dalam proyek ini, *Large Language Model* (LLM) seperti IBM Granite 3.3 8B Instruct digunakan secara aktif di dalam lingkungan Google Colab untuk mendukung berbagai tahapan analisis data dan pemodelan. Berikut adalah bentuk-bentuk dukungan yang diberikan:
1. Perhitungan Statistik Deskriptif, LLM digunakan untuk menghitung statistik deskriptif dari variabel Income berdasarkan kategori Credit Score, termasuk nilai rata-rata, maksimum, minimum, varians, dan rentang. LLM menghasilkan ringkasan hasil dalam format tabel HTML atau daftar, tanpa menunjukkan langkah-langkah perhitungannya.
2. Visualisasi Data dengan Histogram, LLM menghasilkan skrip Python untuk membuat histogram distribusi Income yang dikelompokkan berdasarkan Credit Score. Selanjutnya, agent berbasis LLM juga digunakan untuk langsung menampilkan histogram menggunakan seaborn dan matplotlib, sesuai permintaan pengguna.
3. Profil Demografis Berdasarkan Skor Kredit, LLM diminta untuk menganalisis dan menyajikan profil demografis berdasarkan kategori Credit Score, mencakup usia rata-rata, jenis kelamin paling umum, persentase individu yang sudah menikah, dan persentase kepemilikan rumah. Hasil ditampilkan dalam format tabel yang ringkas.
4. Pemodelan Klasifikasi Perceptron, LLM menghasilkan skrip klasifikasi menggunakan model Perceptron dari scikit-learn. Tahapan yang dilakukan mencakup encoding target menggunakan LabelEncoder, pembagian data secara stratified (80:20), pelatihan model dengan parameter default (termasuk class_weight='balanced'), dan evaluasi akurasi. LLM juga merangkum hasil akhir yang berupa parameter model, akurasi, koefisien (bobot), dan intersep untuk tiap kelas

Penggunaan LLM dalam proyek ini memungkinkan proses analisis menjadi lebih cepat, terstruktur, dan efisien, terutama dalam merangkum data dan mengotomatisasi interpretasi hasil model.

## Penutup
Proyek ini menunjukkan bahwa integrasi antara teknik klasik *machine learning* dan pemanfaatan LLM dapat mempercepat proses analisis data serta menghasilkan model klasifikasi yang sederhana namun efektif. Pendekatan ini memperlihatkan potensi kolaborasi manusia dan AI dalam menyelesaikan permasalahan nyata secara efisien dan akurat.

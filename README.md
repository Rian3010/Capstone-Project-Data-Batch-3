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

## Temuan dan Insight
Setelah dilakukan pelatihan menggunakan model Perceptron, diperoleh akurasi sekitar **84%** pada data uji. Di antara fitur input, pendapatan (*Income*) memiliki pengaruh yang relatif lebih tinggi dibandingkan usia dan jumlah anak.

Model Perceptron secara internal menggunakan pendekatan *One-vs-Rest (OvR)* dalam menangani klasifikasi multikelas, yaitu membangun satu model untuk masing-masing kelas terhadap kelas lainnya. Meskipun termasuk model linier sederhana, Perceptron mampu memberikan hasil yang cukup baik pada dataset ini, membuktikan bahwa model dengan kompleksitas rendah tetap relevan dalam konteks data terstruktur.

## Penjelasan Dukungan AI
Dalam proyek ini, *Large Language Model (LLM)* seperti **IBM Granite 3.3 8B Instruct** digunakan untuk mendukung berbagai proses analisis di dalam lingkungan Google Colab. Pemanfaatan LLM dilakukan secara aktif untuk:

1. Meringkas data pendapatan (*income*) berdasarkan kategori *Credit Score*, guna mendapatkan pemahaman statistik awal dari tiap kelas skor kredit.
2. Menggambarkan profil demografis (rata-rata usia, jenis kelamin dominan, persentase status pernikahan, dan persentase kepemilikan rumah) untuk masing-masing kategori *Credit Score* secara deskriptif.
3. Membangun dan mengevaluasi model klasifikasi Perceptron, termasuk proses *encoding* target, pembagian data *train-test* yang seimbang berdasarkan kategori (*stratified split*), pelatihan model, hingga pelaporan hasil seperti akurasi, bobot (koefisien), dan bias.

Penggunaan LLM dalam proyek ini memungkinkan proses analisis menjadi lebih cepat, terstruktur, dan efisien, terutama dalam merangkum data dan mengotomatisasi interpretasi hasil model.

## Penutup
Proyek ini menunjukkan bahwa integrasi antara teknik klasik *machine learning* dan pemanfaatan LLM dapat mempercepat proses analisis data serta menghasilkan model klasifikasi yang sederhana namun efektif. Pendekatan ini memperlihatkan potensi kolaborasi manusia dan AI dalam menyelesaikan permasalahan nyata secara efisien dan akurat.

# Laporan Proyek Machine Learning - Albert Ewaldo Arthur Daeli

Domain Proyek

Dari tahun ketahun tren data penjualan mobil di Indonesia selalu tidak stabil ada kenaikan dan ada penurunan, 
banyaknya faktor yang menyebabkan trend penjualan mobil di Indonesia tidak stabil mulai dari tingkat 
pendapatan yang menurun hingga ke tidak stabilan harga mobil itu sendiri.

Business Understanding

Oleh karena itu saya membuat prediksi harga mobil dengan menggunakan mechine learning yang bertujuan 
untuk memberikan harga pasti kepada para customer yang ingin membeli mobil.Dengan adanya prediksi harga mobil yang saya buat 
maka customer dapat mengetahui harga dengan spesifikasi tahun keluaran mobil, jarak tempuh dan ukuran mobil maka customer dapat mengetahui 
harga yang harus mereka persiapkan untuk membeli mobil yang mereka inginkan.

Problem Statement

1. Bagaimana membuat model machine learning yang dapat memprediksi harga mobil sesuai keinginan customer
2. Apa saja yang harus diketahui agar mendapatkan harga mobil yang akurat?

Goals

1. Menggunakan model linear regression untuk memprediksi harga mobil sesuai keinginan customer
2. Memprediksi spesifikasi mobil yang sudah ditentukan oleh customer

Data Understanding

Data yang saya gunakan pada proyek ini adalah adalah data yang bisa digunakan untuk memprediksi harga mobil 
yaitu ford dataset yang saya unduh dari website "kaggle.com". dataset ini memiliki 17966 data mobil dan 
memiliki kategori lainnya. 
berikut ini adalah link dataset yang saya pakai : https://www.kaggle.com/datasets/adhurimquku/ford-car-price-prediction

Variabel-Variabel Pada Ford Price Dataset

1. Model : Untuk menunjukan merek pada mobil.
2. Year : Untuk menunjukan tahun produksi pada mobil.
3. Price : Untuk menunjukan harga pada mobil.
4. Transmission : Untuk menunjukan model mesin pada mobil.
5. Mileage : Untuk menunjukan jarak tempuh pada mobil.
6. Fuel-Type : Untuk menunjukan jenis bahan bakar.
7. Tax : Untuk menunjukan pajak tahunan yang ada pada mobil.
8. Mpg : untuk menunjukan jarak mil untuk per galon atau tangki.
9. EngineSize : Untuk menunjukan ukuran mesin pada mobil.

Data Preparation

Tahapan yang saya pakai untuk memprediksi harga adalah sebagai berikut
1. Load Library Python = Digunakan untuk memuat beberapa library python yang digunakan dalam memprediksi harga.
2. Load Dataset = Digunakan untuk memuat dataset yang akan dipakai untuk diprediksi.
3. Handling Missing Values = Pada tahap ini digunakan untuk memeriksa atau checking data apakah terdapat missing values atau data yang kosong atau tidak. Data yang saya pakai bernilai 0 berarti data yang saya pakai tidak ada missing values.
4. Exploratory Data Analysis (EDA) = Digunakan untuk melihat data dalam bentuk diagram. data yang dilihat berupa tahun produksi, data harga pada mobil, dan data jarak tempuh pada mobil.
- ![Screenshot (633)](https://user-images.githubusercontent.com/111255438/190079114-c5a65fdf-4754-480e-b478-3f76a718cff4.png) - pada gambar ini menampilkan data tahun produksi dalam bentuk diagram 
- ![Screenshot (635)](https://user-images.githubusercontent.com/111255438/190080722-3c6bca31-c82c-45a3-b730-50ef587aaab9.png) - pada gambar ini menampilkan data harga mobil dalam bentuk diagram 
- ![Screenshot (636)](https://user-images.githubusercontent.com/111255438/190081881-0dc3f15c-5856-4c8c-a7cf-c7a541c8df22.png) - pada gambar ini menampilkan data jarak tempuh mobil dalam bentuk diagram
- ![Screenshot (637)](https://user-images.githubusercontent.com/111255438/190082258-d7a05a49-6148-4956-9263-403c57349169.png) - pada gambar ini menampilkan data spesifikasi mobil yang menentukan nilai korelasi

6. Modeling = Digunakan untuk melatih data yang akan di prediksi.
7. Prediction = Digunakan untuk memprediksi data yang sudah di modeling.


Modeling

1. Pada tahapan modeling ini, pertama saya membuat variabel x dan y.
2. Tahap Kedua, saya akan membagi dataset menjadi 2 yaitu training dataset dan test dataset dengan perbandingan 80:20, 
   80% digunakan untuk training dataset dan 20% digunakan untuk test dataset. untuk membagi data tersebut diperlukan fungsi "train_test_split" dari scikit-learn, 
   otomatis mengubah dataset dari dataframe ke dalam format array.
3. Kemudian, saya import LinearRegression dari sklearn.linear_model, kemudian saya deklarasikan LinearRegression dengan nama "lin_reg".
4. Kemudian saya fit regressor ke training dataset menggunakan "fit()" dan "predict()" untuk memprediksi nilai dari test dataset.
5. Kemudian, saya akan mencari nilai slope/koefisien dan nilai intercept menggunakan "lin_reg.coef_" dan "lin_reg.intercept_". setelah itu saya mendapatkan nilai koefisien dan intercept. nilai koefisien pada data year adalah "1145.902565" nilai pada data mileage adalah "-0.071279" dan nilai pada data enginesize adalah "5878.074518"
6. Setelah itu, saya menginput "lin_reg.score" yang berfungsi untuk mencari tahu akurasi pada model menggunakan testing dataset yang sudah di split.
   akurasi yang saya dapat adalah 70%

Evaluation

Metrik yang saya pakai adalah accuracy score, confusion matrix, dan classification report

1. Accuracy Score = merupakan rasio prediksi benar baik itu positif maupun negatif terhadap keseluruhan data. Hasil akurasi yang saya dapat adalah "1.0"
2. Confusion Matrix = Merupakan pengukuran performa untuk masalah klasifikasi machine learning dimana keluaran dapat berupa dua kelas atau lebih. 
                      Hasil confusion yang saya dapat adalah "1.0.0"
3. Classification Report = Merupakan proses memprediksi nilai pada data yang terdiri dari 3 metrik yaitu precision recall dan F1-Score

   1. Precision = Precision adalah kecocokan antara bagian data yang diambil dengan informasi yang dibutuhkan. Hasil Presisi yang saya dapat adalah 1.00
   2. Recall = merupakan tingkat keberhasilan sistem dalam menemukan kembali sebuah informasi. Hasil Recall yang saya dapat adalah 1.00
   3. F1-Score = Merupakan Data yang menggambarkan perbandingan rata-rata precision dan recall yang dibobotkan Hasil yang saya dapatkan dari data F1-Score adalah                    1.00

Kesimpulan

Dengan adanya prediksi harga mobil yang saya buat dengan menggunakan machine learning, maka customer dapat dengan mudah mengetahui 
harga yang harus mereka persiapkan untuk membeli mobil dengan spesifikasi yang mereka inginkan. Oleh karena itu menurut saya sistem 
yang saya buat ini sangat bermanfaat bagi para customer yang ingin membeli mobil.




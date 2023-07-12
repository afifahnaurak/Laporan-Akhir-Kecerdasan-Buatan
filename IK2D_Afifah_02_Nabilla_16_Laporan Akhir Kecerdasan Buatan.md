# Laporan Akhir Kecerdasan Buatan - Kelompok IK2D tes

**Anggota Kelompok :**

1. Afifah Naura Kamilia - NIM. 3.34.21.3.02
2. Nabilla Syaharani Putri S - NIM. 3.34.21.3.16

## Domain Proyek

Jam tangan merupakan alat yang berfungsi sebagai penunjuk waktu agar manusia selalu tepat waktu dalam melakukan segala sesuatu. Namun di era modern seperti sekarang ini, jam tangan tidak hanya berfungsi sebagai alat penunjuk waktu saja melainkan sudah menjadi trend fashion bagi masyarakat. Masyarakat sangat memperhatikan penampilan dan fashion yang digunakan, belum lagi aksesoris pelengkap untuk menunjang penampilan, oleh karena itu jam tangan hadir untuk memberikan sentuhan dalam menyempurnakan penampilannya dan juga sangat cocok digunakan dalam aktivitas sehari-hari, baik formal maupun informal. Masyarakat juga percaya bahwa menggunakan jam tangan bermerek dapat meningkatkan kualitas penampilan menjadi lebih elegan, menunjukkan kepribadian seseorang, dan menunjukkan kelas sosial seseorang di mata orang lain [1]. 

Harga jam tangan mewah (*luxury watch*) menjadi salah satu parameter yang paling berpengaruh terhadap kecenderungan seseorang membeli *luxury watch*. Oleh karena itu kemampuan *machine learning* dalam memprediksi harga *luxury watch* menjadi sangat penting untuk masyarakat yang ingin mencari jam tangan khususnya *luxury watch* sesuai kebutuhannya. Terdapat beberapa parameter untuk memprediksi harga *luxury watch*. Beberapa parameter tersebut adalah *brand*, *model*, *case material*, *movement type*, *power reserve*, *water resistence* dan sebagainya. 

Salah satu bidang penelitian machine learning yang didapat digunakan untuk melakukan predikasi adalah regresi. Algoritma regresi dapat memprediksi nilai dari sebuah variabel target berdasarkan nilai dari beberapa variabel input (atau fitur). Harga *luxury watch* dapat diprediksi menggunakan beberapa algoritma *machine learning* seperti Random Forest, Linear Regression, Extra Tree, Gradient Boosting, Decision Tree and SVR. Dari beberapa algoritma tersebut, algoritma Random Forest Reression memiliki akurasi paling baik.

Pada proyek ini dilakukan prediksi harga *luxury watch* menggunakan beberapa algoritma machine learning. Sebelum pelatihan model dan evaluasi, terlebih dahulu dilakukan manipulasi data, dan pembersihan data agar model *machine learning* yang dihasilkan memiliki akurasi yang tinggi. Proyek ini akan berfokus pada pembuatan sebuah sistem untuk memprediksi harga *luxury watch*.

## Business Understanding

Jam tangan mewah merupakan produk yang memiliki nilai prestise dan nilai fashion tinggi dalam industri jam tangan. Masyarakat yang tertarik pada jam tangan mewah sering kali mempertimbangkan merek, model, bahan, jenis mekanisme, daya tahan air, dan faktor-faktor lainnya sebelum melakukan pembelian. Namun, harga jam tangan mewah juga menjadi faktor penting yang mempengaruhi keputusan pembelian. Menurut data dari Statista tahun 2023 menunjukan bahwa segmen jam tangan mewah di Indonesia diproyeksikan tumbuh sebesar 3,30% (2023-2028) menghasilkan volume pasar sebesar US$32,59 juta atau setara dengan Rp 472.055 juta pada tahun 2028 [2]. Dalam konteks ini, kemampuan menggunakan *machine learning* untuk memprediksi harga jam tangan mewah menjadi penting bagi calon pembeli yang ingin memperoleh informasi tentang harga yang diharapkan sebelum melakukan pembelian.

#### Problem Statements

Berdasarkan permasalahan yang telah dijelaskan, *problem statements* dari proyek ini adalah sebagai berikut.

1. Fitur-fitur apa saja yang memiliki pengaruh signifikan terhadap penentuan harga jam tangan mewah?
2. Bagaimana melakukan proses manipulasi data dan pembersihan data agar model *machine learning* yang dihasilkan memiliki akurasi yang tinggi?
3. Bagaimana memilih atau mengembangkan model *machine learning* yang memberikan prediksi harga jam tangan mewah dengan akurasi terbaik?

#### Goals

Tujuan yang hendak dicapai dari proyek ini adalah sebagai berikut 

1. Mengidentifikasi fitur-fitur yang memiliki korelasi signifikan dengan harga jam tangan mewah (*luxury watch*).
2. Mengembangkan model *machine learning* yang dapat memprediksi harga jam tangan mewah (*luxury watch*) dengan akurasi tinggi.

3. Memilih model *machine learning* yang memberikan prediksi harga jam tangan mewah (*luxury watch*) dengan akurasi terbaik melalui proses manipulasi dan pembersihan data yang tepat.

####  Solution Statements

Solusi yang diajukan untuk menyelesaikan masalah yang telah diuraikan adalah sebagai berikut.

1. Melakukan analisis deskriptif untuk mengidentifikasi fitur-fitur yang memiliki korelasi signifikan dengan harga jam tangan mewah.
2. Melakukan manipulasi dan pembersihan data, termasuk penggabungan kolom yang berpengaruh terhadap akurasi prediksi harga jam tangan mewah.
3. Melakukan proses *preprocessing*, seperti:
   - Memeriksa keberadaan data yang hilang (*missing value*) dan duplikasi data. Jika ada, melakukan penanganan yang sesuai.
   - Menghapus kolom yang tidak berpengaruh signifikan terhadap prediksi harga jam tangan mewah.
   - Melakukan visualisasi data untuk memahami persebaran dan korelasi antar kolom.
   - Membagi data menjadi set pelatihan (*training set*) dan set pengujian (*test set*) dengan proporsi tertentu yaitu prosentase 85% banding 15%. Alasan menggunakan 15% karena jumlah data yang digunakan banyak sehingga hanya dengan 15% sudah didapatkan banyak data tes.
   - Melakukan *encoding* terhadap kolom kategorikal menggunakan metode yang sesuai, seperti *label encoding* atau *one-hot encoding*.
4. Melakukan pemilihan model *machine learning* yang memberikan performa terbaik dalam memprediksi harga jam tangan mewah menggunakan LazyPredict. 
   - Memilih 3 algoritma yang menghasilkan model *machine learning* terbaik. Pemilihan model dapat dilakukan dengan melakukan pelatihan dan evaluasi model menggunakan beberapa algoritma *machine learning* seperti Random Forest Regression, Linear Regression, Extra Trees, Gradient Boosting, Decision Tree, dan SVR. 
   - Performa model akan dievaluasi berdasarkan metrik evaluasi yang relevan, seperti Mean Squared Error (MSE), Root Mean Squared Error (RMSE), dan R-squared (R2).

## Data Understanding

Dataset yang digunakan pada proyek ini diperoleh dari Kaggle. Silahkan kunjungi tautan berikut [Luxury Watches Price](https://www.kaggle.com/datasets/rkiattisak/luxury-watches-price-dataset) untuk mengakses dataset yang dipakai. Adapun variabel-variabel yang terdapat pada dataset adalah sebagai berikut :

1. **Brand**: Merk Jam Tangan
2. **Model**: Model Jam Tangan
3. **Case Material**: Material (Bahan) yang digunakan pada Case Jam Tangan
4. **Strap Material**: Material atau bahan yang digunakan pada Pergelangan (Strap) Jam Tangan
5. **Movement Type**: Jenis Mekanisme Pada Jam Tangan
6. **Water Resistance**: kemampuan tahan jam tangan terhadap tekanan air pada kedalaman tertentu
7. **Case Diameter (mm)**: panjang Diameter Jam dalam mm (milimeter)
8. **Case Thickness (mm)**: Ketebalan case jam tangan dalam mm (milimeter)
9. **Band Width (mm)**: lebar tali jam dalam mm (milimeter)
10. **Dial Color**: Warna penanda pada jam
11. **Crystal Material**: bahan yang digunakan untuk menutupi dial
12. **Complications**: fitur atau fungsi tambahan
13. **Power Reserve**: lama jam tangan dapat berfungsi
14. **Price (USD)**: Harga jam tangan dalam USD

Pada dataset, terdapat 4 fitur numerikal dan 10 fitur kategorikal. Ringkasan statistik dari data-data numerikal dapat dilihat pada Tabel 1.

<div style="text-align:center">Tabel 1. Ringkasan Statistik Data-Data Numerikal Pada Dataset</div>

|       | Case Diameter (mm) | Case Thickness (mm) | Band Width (mm) | Price (USD) |
| ----- | ------------------ | ------------------- | --------------- | ----------- |
| count | 507.00             | 507.00              | 507.00          | 506.00      |
| mean  | 41.05              | 11.59               | 21.11           | 12082.96    |
| std   | 2.54               | 2.49                | 1.66            | 10419.82    |
| min   | 27.50              | 5.00                | 15.00           | 495.00      |
| 25%   | 40.00              | 9.80                | 20.00           | 5500.00     |
| 50%   | 41.00              | 12.00               | 20.00           | 8350.00     |
| 75%   | 42.00              | 13.30               | 22.00           | 16450.00    |
| max   | 46.50              | 17.50               | 28.00           | 70000.00    |

Pada tahap *Data Understanding* dilakukan analisis data eksploratif untuk mendapatkan wawasan tentang karakteristik data, memahami struktur data, dan mengidentifikasi potensi masalah atau kesalahan yang mungkin terjadi. Kegiatan Data Understanding yang dilakukan pada Proyek ini antara lain :

- Memberikan informasi seperti jumlah data, *missing value*, duplikasi data, korelasi antar kolom, dan sebaran data.

- Melakukan visualisasi data untuk mengetahui korelasi dan sebaran data. Visualisasi korelasi antar kolom digambarkan dalam heatmap seperti ditunjukan Gambar 1. Berdasarkan diagaram heatmap Gambar 1 diketahui bahwa terdapat beberapa kolom seperti Water Resistance, Case Diameter, Case Thickness, Band Width dan Power Reserve yang berkorelasi dengan kolom 'Price'.  Semakin mendekati nilai 1 maka korelasi semakin tinggi. Kemudian hasil visualisasi heatmap hanya menampilkan korelasi pada kolom yang memberikan data numerikal, sedangkan kolom yang memberikan hasil kategorikal tidak dapat diketahui korelasinya.

  <img  src="https://github.com/afifahnaurak/Laporan-Akhir-Kecerdasan-Buatan/assets/116862851/9647c17c-0ad3-478c-b989-5bfe83d59acd" style="zoom:67%;" />
  
  <div style="text-align:center">Gambar 1. Visualisasi Korelasi Data dengan Heatmap</div>
  
  Sedangkan contoh visualisasi dari sebaran data ditunjukan pada Gambar 2. Visualisasi yang ditunjukan pada Gambar 2 menunjukan bahwa ada ketidakseimbangan data pada kolom Case Diameter, Case Thickness, Band Width, dan Power Reserve.
  
  ![](https://github.com/afifahnaurak/Laporan-Akhir-Kecerdasan-Buatan/assets/116862851/a4e2538b-4c56-467c-b6d5-550b4e2fe983)

<div style="text-align:center">Gambar 2. Visualisasi Data pada Dataset</div>

## Data Preparation

Teknik data preparation yang dilakukan pada proyek ini adalah sebagai berikut : 

1. Feature Selection : Melakukan seleksi fitur untuk menyeleksi kolom yang berperan sebagai data fitur dan kolom yang menjadi data label.

2. Data Splitting: Membagi dataset menjadi data latih dan data uji. Pada proyek ini perbandingan data latih dan data uji adalah 85 : 15.

3. Menampilkan informasi jumlah data latih dan data uji. Jumlah data latih adalah 402, sedangkan data uji terdat 72 data. jumlah data fitur yang dipakai untuk pelatihan adalah 9.

   


## Modelling

Pada tahap ini dilakukan proses pelatihan untuk mendapatkan model dengan performa terbaik. Tahapan yang dilakukan pada proses Modelling adalah sebagai berikut.

1. Memprediksi algoritma dengan performa terbaik menggunakan Lazy Predict

   Lazy Predict adalah library Python yang membantu dalam membuat model *machine learning* dengan cepat dan mudah. Library ini dikembangkan untuk mempercepat proses eksplorasi data dan pemodelan awal. Hasil dari proses pelatihan yang dilakukan Lazy Predict ditunjukan pada Tabel 2.

   <div style="text-align:center">Tabel 2. Hasil Perbandingan model menggunakan Lazy Predict</div>

   | Model                         | Adjusted R-Squared          | R-Squared                   | RMSE            | Time Taken |
   | ----------------------------- | --------------------------- | --------------------------- | --------------- | ---------- |
   | RandomForestRegressor         | 0.78                        | 0.81                        | 0.34            | 0.31       |
   | ExtraTreeRegressor            | 0.78                        | 0.81                        | 0.34            | 0.04       |
   | GradientBoostingRegressor     | 0.76                        | 0.79                        | 0.36            | 0.13       |
   | BaggingRegressor              | 0.75                        | 0.78                        | 0.36            | 0.07       |
   | XGBRegressor                  | 0.73                        | 0.77                        | 0.37            | 0.14       |
   | HistGradientBoostingRegressor | 0.73                        | 0.76                        | 0.38            | 0.38       |
   | ExtraTreesRegressor           | 0.72                        | 0.76                        | 0.38            | 0.24       |
   | LGBMRegressor                 | 0.70                        | 0.73                        | 0.40            | 0.08       |
   | AdaBoostRegressor             | 0.58                        | 0.63                        | 0.47            | 0.19       |
   | DecisionTreeRegressor         | 0.55                        | 0.61                        | 0.48            | 0.03       |
   | KNeighborsRegressor           | 0.46                        | 0.53                        | 0.53            | 0.03       |
   | SVR                           | 0.32                        | 0.41                        | 0.59            | 0.05       |
   | NuSVR                         | 0.32                        | 0.40                        | 0.60            | 0.06       |
   | TransformedTargetRegressor    | 0.17                        | 0.27                        | 0.66            | 0.03       |
   | LinearRegression              | 0.17                        | 0.27                        | 0.66            | 0.03       |
   | RidgeCV                       | 0.17                        | 0.27                        | 0.66            | 0.03       |
   | ElasticNetCV                  | 0.16                        | 0.27                        | 0.66            | 0.18       |
   | Ridge                         | 0.16                        | 0.27                        | 0.66            | 0.03       |
   | BayesianRidge                 | 0.15                        | 0.26                        | 0.66            | 0.09       |
   | LassoCV                       | 0.15                        | 0.26                        | 0.66            | 0.13       |
   | LassoLarsIC                   | 0.15                        | 0.26                        | 0.66            | 0.04       |
   | LassoLarsCV                   | 0.14                        | 0.25                        | 0.67            | 0.08       |
   | PoissonRegressor              | 0.11                        | 0.22                        | 0.68            | 0.04       |
   | LarsCV                        | 0.09                        | 0.20                        | 0.69            | 0.08       |
   | HuberRegressor                | 0.07                        | 0.19                        | 0.69            | 0.08       |
   | LinearSVR                     | 0.06                        | 0.18                        | 0.70            | 0.03       |
   | OrthogonalMatchingPursuitCV   | -0.02                       | 0.11                        | 0.73            | 0.03       |
   | GammaRegressor                | -0.02                       | 0.11                        | 0.73            | 0.04       |
   | TweedieRegressor              | -0.02                       | 0.11                        | 0.73            | 0.02       |
   | OrthogonalMatchingPursuit     | -0.05                       | 0.08                        | 0.74            | 0.03       |
   | SGDRegressor                  | -0.06                       | 0.07                        | 0.74            | 0.03       |
   | KernelRidge                   | -0.11                       | 0.03                        | 0.76            | 0.05       |
   | QuantileRegressor             | -0.15                       | -0.00                       | 0.77            | 1.70       |
   | DummyRegressor                | -0.15                       | -0.00                       | 0.77            | 0.03       |
   | LassoLars                     | -0.15                       | -0.00                       | 0.77            | 0.03       |
   | Lasso                         | -0.15                       | -0.00                       | 0.77            | 0.03       |
   | ElasticNet                    | -0.15                       | -0.00                       | 0.77            | 0.03       |
   | PassiveAggressiveRegressor    | -0.28                       | -0.12                       | 0.82            | 0.04       |
   | MLPRegressor                  | -0.81                       | -0.58                       | 0.97            | 0.74       |
   | RANSACRegressor               | -1.79                       | -1.43                       | 1.20            | 0.15       |
   | GaussianProcessRegressor      | -10.05                      | -8.65                       | 2.39            | 0.07       |
   | Lars                          | -42988557141202895372288.00 | -37539303419078584041472.00 | 149241999378.87 | 0.03       |

   Algoritma dengan performa terbaik dilihat dari nilai R-Square dan RMSE. Semakin besar nilai R-Square (mendekati 1) maka model semakin akurat. Sedangkan pada RMSE, apabila nilai semain kecil (mendekati 0), maka akurasi model akan semakin tinggi. Berdasarkan hasil R-Square dan RMSE menggunakan Lazy Predict pada Tabel 1, disimpulkan bahwa 3 algoritma terbaik yang akan digunakan untuk mempredikasi harga adalah **RandomForestRegressor**, **ExtraTreeRegressor**, dan **GradientBoostingRegressor**.

2. Menggunakan `ColumnTransformer` untuk mengubah data kategorik menjadi numerik

   Pada proyek ini masih mempertahankan kolom kategorikal yaitu *Brand* dan *Power Reserve*. Sebab pada saat ingin mempredikasi harga *luxury brand*, calon pembeli tentunya akan memilih *Brand* dan *Power Reserve* dalam bentuk kategori bukan numerik. Oleh karena itu kita ubah data kategorik menjadi numberik menggunkan teknik OneHotEncoding. Tapi sebelum dilakukan teknik `OneHotEncoding` dilakukan harus menampilkan indeks dari masing-masing kolom menggunakan fungsi `enumerate()`. *Brand* berada di indeks 0, dan *Power Reserve* berada di index 8. Selanjutkan dilakukan proses `ColumnTransformer`.

3. Membuat pipeline untuk menggabungkan data numerik dan kategorik

   Hasil penggunakan teknik `ColumnTransformer` disimpan dalam objek feature. Selanjutnya dilakukan proses pipeline untuk menggabungkan dan meng-optimasi kolom numerikal dan kategorikan agar dapat di proses oleh algoritma machine learning. 

4. Memilih 3 (tiga) algoritma dengan performa terbaik untuk di evaluasi

   Setelah dilakukan proses pelatihan oleh Lazy Predict, diperoleh 3 algoritma dengan performa terbaik yaitu :

   - **RandomForestRegressor**

     RandomForestRegressor adalah algoritma pemodelan yang digunakan dalam pembelajaran mesin untuk memprediksi variabel target berkelanjutan. Ini adalah metode ensambel yang menggabungkan beberapa pohon keputusan acak (*random decision trees*) untuk membuat model yang lebih kuat. Pada dasarnya, algoritma RandomForestRegressor bekerja dengan menggabungkan hasil dari banyak pohon keputusan acak yang diberi bobot yang sama. Setiap pohon keputusan acak dibangun dengan menggunakan subset acak dari data pelatihan dan subset acak dari fitur (variabel independen). Proses ini dikenal sebagai bootstrap aggregating atau biasa disebut juga sebagai "bagging". Ilustrasi dari cara kerja RandomForestRegressor ditunjukan pada Gambar 3.

     <img src="https://afandistudio.net/prak_ai/RFRegression.jpg" style="zoom: 25%;" />

     <div style="text-align:center">Gambar 3. Ilustrasi RandomForestRegressor [6]</div>

   - **ExtraTreeRegressor**

     Extra Tree Regression, atau disebut juga Extreme Tree Regression, adalah sebuah algoritma pembelajaran mesin yang digunakan untuk melakukan regresi, yaitu memprediksi nilai kontinu berdasarkan fitur-fitur yang ada. Algoritma ini merupakan variasi dari algoritma ExtraTree (pohon tambahan) yang telah dijelaskan sebelumnya. Extra Tree Regression mengadopsi pendekatan ensemble learning dengan membangun sejumlah besar pohon keputusan yang tidak terkorelasi secara acak. Pada setiap simpul pemisahan pohon, algoritma menggunakan pendekatan yang acak untuk memilih fitur-fitur yang digunakan untuk membagi data. Kemudian, algoritma memilih pemisahan dengan nilai yang optimal secara acak dari subset nilai yang dipilih untuk membagi data pada simpul tersebut. Ilustrasi dari cara kerja BaggingRegressor ditunjukan pada Gambar 4.

   <img src="https://github.com/afifahnaurak/Laporan-Akhir-Kecerdasan-Buatan/assets/116862851/4b7cff84-efd7-4869-9e9d-ba8d6511d26a" style="zoom:50%;" />

   <div style="text-align:center">Gambar 4. Ilustrasi ExtraTreeRegressor [6]</div>

   Dibandingkan dengan algoritma random forest, algoritma ini memiliki efisiensi komputasi yang lebih tinggi dan akurasi yang lebih tinggi. Algoritma ExtraTree sangat mirip dengan algoritma random forest. Meskipun keduanya terdiri dari beberapa decision tree, ExtraTree dan random forest memiliki dua perbedaan. pertama, random forest menggunakan algoritma Bagging, yang berarti sampel pelatihan untuk setiap weak learner tidak semuanya, tetapi ExtraTree menggunakan semua sampel pelatihan untuk melatih setiap weak learner. Selain itu, ExtraTree mengadopsi strategi pemilihan acak untuk memilih fitur, sehingga hasilnya lebih baik daripada random forest. kedua, random forest mendapatkan atribut bifurkasi terbaik dalam subset acak, tetapi ExtraTree mendapatkan nilai bifurkasi secara sepenuhnya acak untuk melaksanakan bifurkasi pohon keputusan.

   - **GradientBoostingRegressor**

     GradientBoostingRegressor adalah algoritma pemodelan yang digunakan dalam pembelajaran mesin untuk memprediksi variabel target berkelanjutan. Ini adalah metode ensambel yang menggabungkan beberapa pohon keputusan untuk membuat model yang lebih kuat. Algoritma GradientBoostingRegressor bekerja dengan menggabungkan banyak pohon keputusan sederhana. Setiap pohon yang ditambahkan ke model berusaha untuk memperbaiki kesalahan prediksi yang dihasilkan oleh pohon sebelumnya. Algoritma ini bekerja dengan cara mengoptimalkan gradien fungsi kerugian (misalnya, *Mean Squared Error*) menggunakan proses iteratif. Ilustrasi dari cara kerja GradienBoostingRegressor ditunjukan pada Gambar 5.

     ![](https://afandistudio.net/prak_ai/GradienRegression.png)

     <div style="text-align:center">Gambar 5. Ilustrasi GradienBoostingRegressor [5]</div>

5. Menambahkan parameter tunning untuk mengingkatkan performa model

   Penambahan parameter menggunakan **Teknik Grid Search**. Sehingga diperoleh hyperparameter dari masing-masing algoritma adalah sebagai berikut.

   - Parameter RandomForestRegressor
   
     - n_estimator = 90
     - max_features = 0.4
     - max_samples = 0.6
   - Parameter ExtraTreeRegressor
   
     - criterion = mse
     - max_depth = 32
     - max_features = auto
     - max_samples_leaf = 1
     - max_samples_split = 2
     - n_estimators = 10
     - warn_start = True
   - Parameter GradienBoostingRegressor

     - n_estimator = 200
     - max_depth = 4
     - min_samples_split = 10
     - min_samples_leaf = 5
     - max_features = 3

## Evaluation

- Metrik evaluasi yang digunakan adalah *Mean Square Error* (MSE), *Root Mean Square Error* (RMSE), dan *R Square* (R2 Score)

- MSE melakukan pengurangan nilai data aktual dengan data peramalan dan hasilnya dikuadratkan (*squared*) kemudian dijumlahkan secara keseluruhan dan membaginya dengan banyaknya data yang ada. Rumus dari MSE adalah sebagai berikut 
  $$
  MSE = \frac{1}{n} \Sigma_{i=1}^n({y}-\hat{y})^2
  $$
  Diketahui:

  - n = Jumlah Data
  - yi = *Actual Value* / Nilai Sebenarnya
  - ŷi = *Predicted Value* / Nilai Prediksi

  
  
- RMSE adalah jumlah dari kesalahan kuadrat atau selisih antara nilai sebenarnya dengan nilai prediksi yang telah ditentukan. Cara menghitungnya tinggal mengakar kan mse menggunakan fungsi *np.sqrt*. Rumus dari RMSE adalah sebagai berikut.
  $$
  RMSE = \sqrt{(\frac{1}{n})\sum_{i=1}^{n}(y_{i} - x_{i})^{2}}
  $$
  Diketahui:

  - n = Jumlah Data
  - yi = *Actual Value* / Nilai Sebenarnya
  - ŷi = *Predicted Value* / Nilai Prediksi

  
  
- R2 Score dijadikan sebagai pengukuran seberapa baik garis regresi mendekati nilai data asli yang dibuat melalui model. Rumus dari R2 Score adalah sebagai berikut.
  $$
  R^2 = 1 - {SS_R \over SS_T} =  1 - {\sum_{i} (y_i - ŷ_p) ^ 2 \over \sum_{i} (y_i - ȳ) ^ 2}
  $$

  - SSR : Kuadrat dari selisih nilai Y prediksi dengan nilai rata-rata Y = ∑ (Ypred – Yrata-rata)²
  - SST : Kuadrat dari selisih nilai Y aktual dengan nilai rata-rata Y = ∑ (Yaktual – Yrata-rata)²

  
  
- Setelah melalui tahap pelatihan dan evaluasi menggunakan MSE, RMSE, dan R Square, diperoleh hasil bahwa algoritma **RandomForestRegressor** memiliki performa yang paling baik seperti ditunjukan Tabel 3. Maksud performa yang paling baik adalah memiliki nilai MSE dan RMSE yang mendekati nilai 0, serta memiliki nilai R2 Score yang mendekati nilai 1.

  <div style="text-align:center">Tabel 3. Hasil Pengujian dari 3 Algoritma Teratas</div>

  | id   | Model_Name                | MSE       | R2 Score  | RMSE      |
  | ---- | ------------------------- | --------- | --------- | --------- |
  | 0    | RandomForestRegressor     | 0.1288363 | 0.7828588 | 0.3589377 |
  | 1    | ExtraTreesRegressor       | 0.1263014 | 0.7871310 | 0.3553891 |
  | 2    | GradientBoostingRegressor | 0.2313675 | 0.6100523 | 0.4810067 |

  

- Membandingkan data sebenarnya dengan hasil prediksi. Hasil perbandingan dapat dilihat pada Tabel 4.

  <div style="text-align:center">Tabel 4. Hasil Perbandingan Data Sebenarnya dengan Hasil Prediksi</div>
  
  | Id   | y_true     | prediksi_GB | prediksi_RF | prediksi_BG |
  | :--- | :--------- | :---------- | :---------- | :---------- |
  | 79   | 12.5793451 | 12.4000000  | 12.4000000  | 12.3000000  |
  | 101  | 10.9594359 | 11.5000000  | 11.5000000  | 11.5000000  |
  | 271  | 11.5038999 | 11.5000000  | 11.5000000  | 11.5000000  |
  | 225  | 11.6393378 | 12.0000000  | 12.0000000  | 12.0000000  |
  | 466  | 13.2079537 | 13.1000000  | 13.1000000  | 13.0000000  |
  | ...  | ...        | ...         | ...         | ...         |
  | 240  | 12.6924877 | 12.4000000  | 12.4000000  | 12.3000000  |
  | 429  | 12.6301174 | 12.4000000  | 12.4000000  | 12.3000000  |
  | 169  | 11.6912976 | 12.4000000  | 12.4000000  | 12.3000000  |
  | 381  | 12.5948493 | 12.3000000  | 12.3000000  | 12.2000000  |
  | 60   | 11.8757266 | 12.4000000  | 12.4000000  | 12.3000000  |

## Conclussion

1. Berdasarkan hasil pengukuran, terdapat 9 kolom atau fitur yang mempengaruhi *Price* yaitu Brand, Model, Water Resistance, Case Diameter, Case Diameter, Band Width, Dial Color, Crystal Material, dan Crystal Material.
2. Proses preprocessing yang dilakukan adalah dengan melakukan manipulasi data seperti menghapus data yang tidak memiliki korelasi yang signifikan dengan *Price* dan mengubah format tipe data pada setiap kolom yang memiliki korelasi.
3. Berdasarkan hasil pengujian model, diperoleh hasil bahwa algoritma RandomForestRegressor memiliki performa yang paling baik yaitu memiliki nilai RMSE paling kecil dan R2 Score paling besar.
4. Meningkatkan performa model dapat dilakukan dengan menambahkan hyperparameter.  Pemilihan hyperparameter yang menghasilkan performa terbaik dapat dilakukan menggunakan teknik Grid Search.
5. Dataset yang digunakan memiliki rentang jangkauan yang berbeda (imbalace), oleh sebab itu agar performa model lebih baik maka perlu dilakukan teknik SMOTE (Synthetic Minority Over-sampling Technique). Teknik SMOTE sendiri merupakan salah satu metode oversampling yang digunakan untuk menyeimbangkan dataset yang tidak seimbang. Metode ini menghasilkan sampel sintetis baru untuk kelas minoritas dengan cara menggabungkan fitur-fitur dari data latihan yang sudah ada.

## Referensi

[1]   APJII, “Laporan Survei Internet APJII 2021 - 2021,” 2022. [Online]. Available: [https://apjii.or.id/survei](https://apjii.or.id/survei).

[2]   S. Subhiksha, S. Thota, and J. Sangeetha, “Prediction of Phone Prices Using machine learning,” 2020, doi: [10.1007/978-981-15-1097-7_65](https://doi.org/10.1007/978-981-15-1097-7_65).

[3]   M. Çetın and Y. Koç, “Mobile Phone Price Class Prediction Using Different Classification Algorithms with Feature Selection and Parameter Optimization,” 2021, doi: [10.1109/ISMSIT52890.2021.9604550](https://doi.org/10.1109/ISMSIT52890.2021.9604550).

[4]   A. Kalmaz and O. Akin, “Estimation of Mobile Phone Prices with machine learning,” 2022, doi: [10.1109/ICEET56468.2022.10007128](https://doi.org/10.1109/ICEET56468.2022.10007128).

[5]  V. Aliyev, “A hands-on explanation of Gradient Boosting Regression,” *medium.com*, 2020. https://vagifaliyev.medium.com/a-hands-on-explanation-of-gradient-boosting-regression-4cfe7cfdf9e (accessed Jun. 03, 2023).

[7]   J. H. Graw, W. T. Wood, and B. J. Phrampus, “Predicting Global Marine Sediment Density Using the Random Forest Regressor machine learning Algorithm,” *J. Geophys. Res. Solid Earth*, vol. 126, no. 1, pp. 1–14, 2021, doi: [10.1029/2020JB020135](https://doi.org/10.1029/2020JB020135).

[6]   Zheng Chu, Jiong Yu, and Askar Hamdulla, “Throughput Prediction based on ExtraTree for Stream
Processing Tasks,” 2020, doi: [10.2298/CSIS200131031C](https://doi.org/10.2298/CSIS123456789X).

**---Ini adalah bagian akhir laporan---**
# CNN untuk Klasifikasi Gambar Anjing dan Kucing  

Proyek ini merupakan implementasi **Convolutional Neural Network (CNN)** untuk mengklasifikasikan gambar anjing dan kucing. Dataset yang digunakan adalah kumpulan gambar yang telah dibagi menjadi set pelatihan (*training set*) dan set pengujian (*test set*).

## Deskripsi Kode  

### 1. Arsitektur Model CNN  
Model CNN dibangun menggunakan TensorFlow dan Keras dengan arsitektur berikut:  
- **Convolution Layer**  
  Lapisan konvolusi pertama dengan 32 filter, kernel berukuran 3x3, dan fungsi aktivasi ReLU.  
- **MaxPooling Layer**  
  Lapisan pooling dengan ukuran 2x2 untuk mengurangi dimensi data.  
- **Convolutional Layer Tambahan**  
  Lapisan konvolusi kedua dengan parameter yang sama, diikuti oleh MaxPooling.  
- **Flatten Layer**  
  Mengubah keluaran matriks menjadi vektor agar dapat digunakan di lapisan fully connected.  
- **Fully Connected Layer**  
  - Lapisan Dense dengan 128 neuron dan fungsi aktivasi ReLU.  
  - Lapisan output dengan 1 neuron dan fungsi aktivasi sigmoid untuk klasifikasi biner (anjing vs kucing).  

### 2. Kompilasi dan Pelatihan Model  
Model dikompilasi menggunakan:  
- **Optimizer:** Adam  
- **Loss Function:** *Binary Crossentropy*  
- **Metrics:** Akurasi  

Model dilatih menggunakan dataset yang telah di-*augmentasi* dengan teknik seperti *rescale*, *shear*, *zoom*, dan *horizontal flip*. Pelatihan dilakukan selama 50 *epoch*.

### 3. Evaluasi Model  
Setelah pelatihan, model diuji menggunakan data gambar baru. Kode menyediakan fungsi untuk memprediksi apakah gambar termasuk anjing atau kucing. Hasil prediksi berupa jumlah gambar anjing dan kucing yang berhasil diklasifikasikan.

### 4. Dataset  
Dataset yang digunakan dapat diunduh dari tautan berikut: [Download Dataset](https://drive.google.com/drive/folders/14WzYW03GJu4rvOdo7sXIADHdq9DVgS1o).  
Dataset terdiri dari:  
- **Training Set:** Gambar-gambar yang digunakan untuk melatih model.  
- **Test Set:** Gambar-gambar untuk menguji performa model.

## Contoh Output  
Berikut adalah contoh hasil prediksi:  
```text
count_dog: 480  
count_cat: 520  
```

### Sumber
Kode ini berasal dari: Megabagus.id
Dataset dapat diakses melalui tautan berikut: Dataset Anjing dan Kucing.

# Proyek Akhir - Klasifikasi Gambar Malaria

## Deskripsi Proyek
Proyek ini bertujuan untuk mengembangkan model klasifikasi gambar menggunakan teknik *Convolutional Neural Network (CNN)* untuk mendeteksi apakah gambar sel darah merah terinfeksi malaria atau tidak. Dataset yang digunakan berasal dari Kaggle yang berjudul **Cell Images for Detecting Malaria**.

Model ini dikembangkan menggunakan TensorFlow dan Keras. Model yang dihasilkan dapat di-export dalam beberapa format seperti **SavedModel**, **TensorFlow Lite**, dan **TensorFlow.js** agar dapat digunakan dalam berbagai platform seperti mobile, server, atau aplikasi web.

## Struktur Model
Model CNN ini terdiri dari:
- 4 layer **Conv2D** dengan **MaxPooling**
- 1 layer **Flatten**
- 2 layer **Dense** (termasuk satu dropout layer untuk regularisasi)

Model dilatih menggunakan dataset dengan dua kelas:
- **Terinfeksi** (parasite-infected cells)
- **Tidak Terinfeksi** (healthy cells)

## Dataset
Dataset yang digunakan adalah dataset gambar sel darah merah untuk deteksi malaria yang diambil dari Kaggle. Dataset ini memiliki dua kelas utama:
- **Parasitized**: Gambar yang menunjukkan sel darah merah yang terinfeksi malaria.
- **Uninfected**: Gambar yang menunjukkan sel darah merah yang sehat.

Link dataset: [Cell Images for Detecting Malaria](https://www.kaggle.com/iarunava/cell-images-for-detecting-malaria)

## Cara Menjalankan Proyek
1. **Instalasi library:**
   - Install dependensi menggunakan `pip install -r requirements.txt`.
   
2. **Menjalankan Notebook:**
   - Semua kode tersedia di notebook `notebook.ipynb`. Anda dapat menjalankan notebook di Google Colab atau secara lokal menggunakan Jupyter Notebook.

3. **Load Model dan Inference:**
   - Anda dapat melakukan prediksi menggunakan model yang sudah dilatih dalam format `SavedModel`, `TensorFlow Lite (TFLite)`, atau `TensorFlow.js` tergantung pada kebutuhan aplikasi.
   
   - Untuk model **TFLite**: gunakan `model.tflite`.
   - Untuk model **TFJS**: gunakan `model.json` dan file binari terkait.
   
4. **Contoh Prediksi:**
   - Untuk melakukan prediksi pada gambar baru, silakan mengikuti instruksi di notebook untuk memuat model dan melakukan inferensi terhadap gambar yang Anda pilih.

## Exported Models
Model ini disimpan dalam tiga format untuk kemudahan penggunaan di berbagai platform:
- **SavedModel** (TensorFlow): Disimpan di dalam folder `saved_model/`.
- **TensorFlow Lite (TFLite)**: Disimpan dalam format `.tflite` di dalam folder `tflite/`.
- **TensorFlow.js (TFJS)**: Disimpan di dalam folder `tfjs_model/`.

# Klasifikasi Gambar dengan CIFAR-10 🚀

Proyek ini adalah implementasi sistem klasifikasi gambar otomatis menggunakan dataset **CIFAR-10**. Model dibangun menggunakan **TensorFlow/Keras** dan dirancang untuk mengenali 10 kategori objek yang berbeda. Proyek ini juga mencakup alur kerja lengkap dari prapemrosesan data, augmentasi, pelatihan model, hingga ekspor model ke berbagai format (Web, Mobile, dan Edge).

## 🛠️ Tech Stack & Kegunaan

- **TensorFlow 2.x / Keras**: Framework utama yang digunakan untuk merancang arsitektur CNN, melakukan proses pelatihan (*training*), serta evaluasi model Deep Learning secara efisien.
- **TensorFlow.js (TFJS)**: Digunakan untuk mengonversi model agar dapat dijalankan langsung di sisi klien (*client-side*) melalui browser web menggunakan JavaScript.
- **TensorFlow Lite (TFLite)**: Digunakan untuk mengoptimalkan model agar ringan dan responsif saat dijalankan pada perangkat dengan sumber daya terbatas seperti smartphone (Android/iOS) atau perangkat IoT.
- **NumPy**: Library fundamental untuk komputasi sains yang digunakan untuk memanipulasi data gambar dalam bentuk array multidimensi.
- **Scikit-learn**: Digunakan untuk pembagian dataset (*train-test split*) secara sistematis dan melakukan pengacakan data agar proses validasi lebih objektif.
- **Matplotlib**: Library visualisasi yang digunakan untuk menghasilkan grafik/plot akurasi dan *loss*, sehingga progres pelatihan model dapat dipantau secara visual.
- **Python**: Bahasa pemrograman utama yang digunakan karena fleksibilitasnya dan dukungan ekosistem library AI/ML yang sangat luas.

## 📊 Dataset: CIFAR-10

Dataset CIFAR-10 terdiri dari 60.000 gambar berwarna berukuran 32x32 dalam 10 kelas, dengan 6.000 gambar per kelas. Terdapat 50.000 gambar pelatihan dan 10.000 gambar pengujian.

**Kategori Kelas:**
- ✈️ Pesawat Terbang (*Airplane*)
- 🚗 Mobil (*Automobile*)
- 🐦 Burung (*Bird*)
- 🐱 Kucing (*Cat*)
- 🦌 Rusa (*Deer*)
- 🐶 Anjing (*Dog*)
- 🐸 Katak (*Frog*)
- 🐴 Kuda (*Horse*)
- 🚢 Kapal Laut (*Ship*)
- 🚛 Truk (*Truck*)

## 🧠 Arsitektur Model

Model menggunakan struktur **Convolutional Neural Network (CNN)** dengan komponen berikut:
- **Convolutional Layers (Conv2D)**: Untuk ekstraksi fitur gambar.
- **Batch Normalization**: Untuk stabilitas dan mempercepat konvergensi pelatihan.
- **MaxPooling2D**: Untuk pengurangan dimensi spasial.
- **Dropout**: Untuk mencegah *overfitting* (menggunakan nilai antara 0.25 hingga 0.5).
- **Dense Layers**: Sebagai kepala klasifikasi akhir.
- **Data Augmentation**: Menggunakan `ImageDataGenerator` untuk meningkatkan kemampuan generalisasi model.

## 💾 Format Ekspor Model

Proyek ini secara otomatis mengekspor model yang telah dilatih ke dalam tiga format utama:
1.  **SavedModel**: Format standar TensorFlow untuk kebutuhan produksi/server.
2.  **TFLite**: Dioptimalkan untuk perangkat mobile dan IoT (sudah termasuk `label.txt`).
3.  **TFJS**: Siap untuk dijalankan langsung di browser menggunakan JavaScript.

## 🚀 Cara Menjalankan

### Prasyarat
Pastikan Anda telah menginstal Python. Pasang semua dependensi yang diperlukan dengan perintah berikut:

```bash
pip install -r requirements.txt
```

### Menjalankan Proyek
Anda dapat menjalankan pelatihan model melalui notebook atau skrip Python:

1.  Buka `notebook.ipynb` menggunakan Jupyter Notebook atau Google Colab.
2.  Atau jalankan skrip Python langsung:
    ```bash
    python notebook.py
    ```

## 📈 Hasil Pelatihan
Model ini dirancang untuk mencapai akurasi di atas **85%** pada data pengujian, memenuhi standar untuk deployment aplikasi nyata.

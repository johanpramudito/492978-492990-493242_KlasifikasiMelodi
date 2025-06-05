# Klasifikasi Atensi Teks pada Poster Film

Repositori ini berisi proyek yang mengimplementasikan pendekatan _deep learning_ menggunakan model ResNet50 yang telah dilatih sebelumnya (_pre-trained_) dengan _transfer learning_ untuk mengklasifikasikan tingkat atensi teks pada poster film. Skala klasifikasi berkisar dari 0 (tidak menarik) hingga 4 (sangat menarik).

## Kontributor

1.  Melvin Waluyo (22/492978/TK/53972)
2.  Alexander Johan Pramudito (22/492990/TK/53976)
3.  Muhammad Grandiv Lava Putra (22/493242/TK/54023)

## Gambaran Umum Proyek

Inti dari proyek ini adalah Jupyter Notebook (`492978_492990_493242_Melvin_Johan_Grandiv_Klasifikasi_Atensi_Teks_Poster_Film.ipynb`) yang melakukan klasifikasi gambar. Notebook ini menggunakan dataset gambar poster film dan file CSV (`attention.csv`) yang memetakan nama file gambar ke skor atensi masing-masing.

## Pengaturan dan Penggunaan

### Prasyarat

Pastikan Anda telah menginstal Python. Pustaka (_library_) yang diperlukan untuk proyek ini tercantum dalam file `requirements.txt`.

### Instalasi

1.  (_Clone_) repositori:

    ```bash
    git clone https://github.com/johanpramudito/492978-492990-493242_KlasifikasiMelodi.git
    cd 492978-492990-493242_KlasifikasiMelodi

    ```

2.  Instal (_library_) Python yang diperlukan:
    ```bash
    pip install -r requirements.txt
    ```
    `requirements.txt` mencakup:
    - `numpy`
    - `pandas`
    - `matplotlib`
    - `seaborn`
    - `Pillow`
    - `opencv-python`
    - `scikit-learn`
    - `tensorflow`
    - `imbalanced-learn`

### Dataset

Proyek ini mengharapkan dataset diatur secara lokal sebagai berikut:

- Direktori gambar bernama `datasets` di direktori utama (_root_) proyek. Direktori ini harus berisi gambar-gambar poster film.
- File CSV bernama `attention.csv` di direktori utama proyek. File ini berisi dua kolom: `image` (nama file poster, contoh: `1.png`) dan `attention` (skor atensi yang sesuai, contoh: 1).

### Menjalankan Kode

1.  Pastikan dataset (folder `datasets` dan file `attention.csv`) ditempatkan di direktori utama proyek.
2.  Buka dan jalankan Jupyter Notebook:
    `492978_492990_493242_Melvin_Johan_Grandiv_Klasifikasi_Atensi_Teks_Poster_Film.ipynb`
    Notebook ini menangani:
    - Pengaturan path dataset lokal.
    - Memuat dan menjelajahi data dari `attention.csv`.
    - Pra-pemrosesan gambar dan label.
    - Membangun dan melatih model berbasis ResNet50.
    - Mengevaluasi kinerja model.
    - Visualisasi hasil.

## Deskripsi File

- `492978_492990_493242_Melvin_Johan_Grandiv_Klasifikasi_Atensi_Teks_Poster_Film.ipynb`: Jupyter Notebook utama yang berisi kode Python untuk tugas klasifikasi.
- `attention.csv`: File CSV yang berisi nama file gambar dan skor atensinya.
- `requirements.txt`: File teks yang mencantumkan pustaka Python yang diperlukan untuk menjalankan proyek.
- `datasets/`: (Direktori ini diharapkan oleh notebook tetapi tidak secara eksplisit disediakan dalam daftar file). Folder ini seharusnya berisi gambar-gambar poster film.

## Model

Model klasifikasi didasarkan pada ResNet50 dengan _transfer learning_. Notebook ini juga mengeksplorasi model _pre-trained_ lain seperti VGG16 dan MobileNetV2 sebagai perbandingan. Teknik seperti SMOTE dan RandomUnderSampler digunakan untuk menangani ketidakseimbangan kelas.

## Reproduksibilitas

Notebook ini mengatur _random seed_ untuk `random`, `numpy`, dan `tensorflow` untuk memastikan reproduksibilitas hasil.

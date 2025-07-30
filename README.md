# Proyek Generative Adversarial Network (GAN) - [Kelompok 3]

## Deskripsi Singkat Tugas

Proyek ini adalah implementasi dasar dari **Generative Adversarial Network (GAN)** menggunakan pustaka PyTorch. Tujuan utama dari tugas ini adalah untuk memahami konsep inti di balik GAN, yaitu proses pembelajaran adversial antara dua jaringan saraf (Generator dan Discriminator), serta mengaplikasikannya untuk menghasilkan gambar baru yang realistis dari data pelatihan sederhana.

Dalam proyek ini, kami melatih GAN pada dataset **MNIST**, yang terdiri dari digit tulisan tangan (0-9). Generator dilatih untuk menciptakan gambar digit yang meyakinkan dari noise acak, sementara Discriminator dilatih untuk membedakan antara gambar digit asli dari dataset dan gambar palsu yang dihasilkan oleh Generator. Seiring pelatihan, Generator belajar untuk menghasilkan gambar yang semakin sulit dibedakan dari yang asli.

## Anggota Kelompok dan Pembagian Tugas

**Kelompok 3:** 
**Anggota:**

* **Firlana UmiAzzakiy** (442023618076)
    * **Tugas:** Riset Konsep GAN dan Implementasi Arsitektur Generator
* **Mutiara Afny** (442023618080)
    * **Tugas:** Persiapan Dataset (Preprocessing & DataLoader)
* **Shafiyyah Al-Khansa** (442023618075)
    * **Tugas:** Implementasi Fungsi Visualisasi Hasil & Loss
* **Andini Putri Rosyidi** (442023618079) 
    * **Tugas:** Dokumentasi (README.md, Komentar Kode)
* **Rana Rohadatul 'Aisy** (442023618081) 
    * **Tugas:** Manajemen Repositori GitHub dan Pengujian Awal Model Generator

## Struktur Direktori Proyek
```
Implementasi-Generative-Adversarial-Network/
├── gan_kelompokX.ipynb        # Notebook Jupyter berisi seluruh implementasi GAN
├── README.md                  # File dokumentasi proyek ini
├── generated_images/          # Folder untuk menyimpan contoh gambar yang dihasilkan Generator
│   ├── epoch_000.png
│   ├── epoch_010.png
│   └── ... (gambar dari setiap epoch tertentu)
└── models/                    # Folder untuk menyimpan model Generator dan Discriminator yang telah dilatih (.pth)
    ├── generator_epoch_XXX.pth
    └── discriminator_epoch_XXX.pth
```

-----
## Cara Menjalankan Kode

Untuk menjalankan proyek GAN ini, ikuti langkah-langkah berikut:

1.  **Akses Notebook di Kaggle:**
    * Buka akun Kaggle Anda.
    * Anda dapat mengunggah file `gan_kelompok3.ipynb` ke lingkungan Kaggle Anda, atau membuat Notebook baru dan menyalin seluruh kode dari file tersebut ke dalamnya.

2.  **Aktifkan GPU (Akselerator):**
    * Sangat disarankan untuk menggunakan GPU untuk pelatihan Deep Learning, karena akan mempercepat proses secara signifikan.
    * Di Notebook Kaggle, buka `Settings` (biasanya ikon roda gigi di sisi kanan atau di menu `File`).
    * Pada bagian `Accelerator`, pilih `GPU` (atau `TPU` jika tersedia dan Anda ingin menggunakannya, tetapi PyTorch lebih umum dengan GPU).

3.  **Jalankan Sel-sel Kode:**
    * Jalankan setiap sel kode dalam Notebook secara berurutan dari atas ke bawah. Anda bisa menggunakan opsi `Run All` dari menu `Run` atau menjalankan setiap sel secara manual (`Shift + Enter`).
    * Proses pelatihan GAN akan dimulai. Anda akan melihat output di konsol yang menunjukkan progres loss Generator dan Discriminator per batch dan epoch.
    * Selama pelatihan, gambar-gambar yang dihasilkan oleh Generator akan disimpan secara berkala di folder `generated_images/` dan juga akan ditampilkan langsung di output Notebook pada epoch-epoch tertentu. Model yang terlatih juga akan disimpan di folder `models/`.

4.  **Tinjau Hasil:**
    * Setelah pelatihan selesai, Anda dapat meninjau plot loss pelatihan yang menunjukkan konvergensi kedua model.
    * Perhatikan gambar-gambar yang dihasilkan di folder `generated_images/`. Bandingkan gambar dari epoch awal (yang mungkin berupa noise acak) dengan gambar dari epoch akhir (yang seharusnya menyerupai digit MNIST yang realistis).

---

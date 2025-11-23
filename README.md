<div align="center">
  <img src="https://cdn.dribbble.com/users/2234409/screenshots/11336360/media/32e790453b99992ba82033463533a272.png?resize=800x600&vertical=center" alt="Weather Prediction 3D Banner" width="100%" style="border-radius: 15px; object-fit: cover; height: 280px;">

  <br><br>

  <h1>📘 Implementasi Naive Bayes Kategorial<br>
  <span style="font-weight: 300; font-size: 20px;">Studi Kasus: Prediksi Cuaca Besok</span></h1>

  <p><strong>Panduan Resmi Notebook: <code>NB_Cuaca_NPM.ipynb</code></strong><br>
  <i>"From Scratch — No Scikit-Learn. Pure Math Logic."</i></p>

  <p>
    <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white">
    <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white">
    <img src="https://img.shields.io/badge/Algorithm-Naive%20Bayes-green?style=for-the-badge">
    <img src="https://img.shields.io/badge/Calculation-Manual-red?style=for-the-badge">
  </p>

  <br>
</div>

---

## 🌟 Pendahuluan

Dokumen ini merupakan panduan resmi untuk membuka, menjalankan, dan menguji notebook  
**`NB_Cuaca_NPM.ipynb`**, yang berisi implementasi Naive Bayes secara **manual**, tanpa bantuan modul `sklearn.naive_bayes`.

Perhitungan probabilitas dilakukan secara matematis, mulai dari:
- Prior Probability  
- Likelihood (dengan Laplace Smoothing)  
- Posterior Score  
- Output prediksi final  

Tujuan utama tugas ini adalah menunjukkan pemahaman mendalam tentang alur kerja Naive Bayes dari dasar.

---

## 🧠 Alur Logika Program

``mermaid
graph LR
    A[Start: Data Latih] --> B(Hitung Prior Probability)
    B --> C(Hitung Likelihood + Laplace Smoothing)
    C --> D{Input Data Baru}
    D --> E(Hitung Posterior Score)
    E --> F[Keputusan: Hujan / Tidak]

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style F fill:#bbf,stroke:#333,stroke-width:2px,stroke-dasharray: 5 5
1️⃣ Persyaratan Sistem
Pastikan perangkat sudah siap sebelum menjalankan notebook.

Komponen	Spesifikasi
Python	Versi 3.8 atau lebih baru
Editor	VS Code atau Jupyter Notebook
Library	pandas, numpy, openpyxl

Instalasi library:
bash
Salin kode
pip install pandas numpy openpyxl
2️⃣ Struktur Folder Tugas
Pastikan struktur file seperti berikut:

bash
Salin kode
📦 TUGAS_NAIVE_BAYES
 ┣ 📜 NB_Cuaca_NPM.ipynb                # Main Notebook (Otak Program)
 ┣ 📊 dataset_hujan_besok_kategori.xlsx # Dataset sumber
 ┗ 📝 README_NaiveBayes.md              # Dokumen panduan
3️⃣ Cara Membuka Notebook
🔵 Opsi A: Visual Studio Code (Rekomendasi)
Buka VS Code

File → Open Folder → pilih folder tugas

Klik file NB_Cuaca_NPM.ipynb

Pastikan Kernel Python aktif

Jalankan cell satu per satu (Shift + Enter)

🟠 Opsi B: Jupyter Notebook
bash
Salin kode
jupyter notebook
Browser akan terbuka → pilih file notebook → jalankan dari atas ke bawah.

4️⃣ Urutan Eksekusi Notebook (Wajib Berurutan)
Header identitas dan deskripsi

Import library

Load dataset Excel

Hitung Prior Probability (P(Yes), P(No))

Hitung Likelihood + Laplace

Implementasi fungsi prediksi

Testing 3 kasus contoh

Interpretasi hasil

✔ Indikator sukses
Notebook bisa Run All tanpa error.

5️⃣ Uji Coba Prediksi Mandiri
Masukkan data baru seperti contoh:

python
Salin kode
kasus_uji = {
    "Temp": "panas",
    "Humidity": "kering",
    "Wind": "kencang",
    "Cloud": "cerah",
    "Pressure": "tinggi",
    "RainToday": "No"
}

predict_naive_bayes(kasus_uji)
Output yang diharapkan:
markdown
Salin kode
==========================================
🔍 HASIL PREDIKSI NAIVE BAYES
==========================================
Probabilitas Hujan (Yes) : 0.0045
Probabilitas Tidak (No)  : 0.0210
------------------------------------------
🎯 KEPUTUSAN FINAL: TIDAK HUJAN (No) ☀️
==========================================
6️⃣ Catatan Penting
🧮 Perhitungan Manual
Semua probabilitas dihitung secara manual, bukan menggunakan model otomatis Scikit-Learn.

🧂 Laplace Smoothing
Digunakan agar probabilitas tidak menjadi 0 saat kategori baru muncul di data uji.

📎 Repository GitHub
Seluruh laporan dan kode lengkap dapat dilihat di:
👉 https://github.com/skimatt/Naive_Bayes

<div align="center"> <br><br> <p>Terima kasih telah meninjau tugas ini.<br> Semoga dokumen ini membantu memahami konsep Naive Bayes secara teoritis maupun praktis.</p> <img src="https://cdn-icons-png.flaticon.com/512/1163/1163661.png" width="60" alt="Sun Cloud 3D">
<sub>Dibuat dengan ❤️ dan ☕ untuk Tugas Kuliah</sub>

</div> ```

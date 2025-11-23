<div align="center">
  <img src="https://cdn.dribbble.com/users/2234409/screenshots/11336360/media/32e790453b99992ba82033463533a272.png?resize=800x600&vertical=center" alt="Weather Prediction 3D Banner" width="100%" style="border-radius: 15px; object-fit: cover; height: 280px;">

  <br><br>

  <h1>📘 Implementasi Naive Bayes Kategorial<br><span style="font-weight: 300; font-size: 20px;">Studi Kasus: Prediksi Cuaca Besok</span></h1>

  <p>
    <strong>Panduan Resmi Notebook: <code>NB_Cuaca_NPM.ipynb</code></strong><br>
    <i>"From Scratch, No Scikit-Learn, Pure Math Logic."</i>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
    <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
    <img src="https://img.shields.io/badge/Algorithm-Naive%20Bayes-green?style=for-the-badge" alt="Algorithm">
    <img src="https://img.shields.io/badge/Calculation-Manual-red?style=for-the-badge" alt="Manual Calculation">
  </p>

  <br>
</div>

---

## 🌟 Pendahuluan

Dokumen ini merupakan panduan resmi untuk membuka, menjalankan, dan menguji notebook **NB_Cuaca_NPM.ipynb**.

Sesuai ketentuan tugas, seluruh proses perhitungan Naive Bayes dilakukan **secara manual (step-by-step)** mengacu pada rumus matematika asli, **tanpa menggunakan modul `sklearn.naive_bayes`**. Notebook ini disusun untuk mendemonstrasikan pemahaman mendalam tentang alur probabilitas.

### 🧠 Alur Logika Program
```mermaid
graph LR
    A[Start: Data Latih] --> B(Hitung Prior Probability)
    B --> C(Hitung Likelihood + Laplace Smoothing)
    C --> D{Input Data Baru}
    D --> E(Hitung Posterior Score)
    E --> F[Keputusan: Hujan / Tidak]
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style F fill:#bbf,stroke:#333,stroke-width:2px,stroke-dasharray: 5 5

    1. 💻 Persyaratan SistemSebelum menjalankan notebook, pastikan perangkat Anda telah siap tempur:KomponenSpesifikasiPythonVersi 3.8 atau lebih baru 🐍EditorJupyter Notebook atau VS Code (dgn ekstensi Jupyter)Librarypandas (Manipulasi data), numpy (Numerik), openpyxl (Baca Excel)Instalasi Library:Bashpip install pandas numpy openpyxl
2. 📂 Struktur File TugasPastikan susunan file dalam folder Anda terlihat seperti ini agar script dapat membaca dataset dengan benar:Plaintext📦 TUGAS_NAIVE_BAYES
 ┣ 📜 NB_Cuaca_NPM.ipynb                # 🧠 Main Notebook (Otak Program)
 ┣ 📊 dataset_hujan_besok_kategori.xlsx # 💾 Dataset Sumber
 ┗ 📝 README_NaiveBayes.md              # 📘 Dokumen Panduan Ini
3. 🚀 Cara Membuka NotebookPilih salah satu metode yang paling nyaman bagi Anda:<img src="https://www.google.com/search?q=https://upload.wikimedia.org/wikipedia/commons/9/9a/Visual_Studio_Code_1.35_icon.svg" width="20"> Opsi A: Visual Studio Code (Recommended)Buka aplikasi VS Code.Pilih menu File → Open Folder dan arahkan ke folder tugas.Klik file NB_Cuaca_NPM.ipynb.Pastikan Kernel Python sudah terpilih di pojok kanan atas.Jalankan cell satu per satu dengan tombol ▶ Run atau shortcut Shift + Enter.<img src="https://www.google.com/search?q=https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" width="20"> Opsi B: Jupyter NotebookBuka terminal/CMD pada folder tugas.Ketik perintah:Bashjupyter notebook
Browser akan terbuka otomatis. Klik file notebook dan jalankan cell dari atas ke bawah.4. 📋 Urutan EksekusiAgar tidak terjadi error variabel, jalankan notebook secara berurutan:Identitas & Deskripsi - Header tugas.Import Library - Memuat pandas & numpy.Load Dataset - Membaca file Excel ke DataFrame.Prior Calculation - Menghitung probabilitas kelas P(Yes) dan P(No).Likelihood (Laplace) - Menghitung probabilitas bersyarat dengan smoothing.Fungsi Prediksi - Fungsi utama Naive Bayes.Testing - Pengujian 3 kasus sampel.Interpretasi - Kesimpulan hasil.✅ Indikator Sukses: Jika seluruh cell dapat dijalankan (Run All) tanpa pesan Error, maka logika matematika telah berjalan sempurna.5. 🧪 Uji Coba Prediksi MandiriDosen atau penguji dapat menguji ketangguhan model dengan memasukkan parameter cuaca baru. Gunakan format dictionary berikut pada cell baru di notebook:Python# 🌤️ Skenario: Cuaca Panas tapi Berangin
kasus_uji = {
    "Temp": "panas",      # Opsi: panas, sedang, dingin
    "Humidity": "kering", # Opsi: kering, normal, basah
    "Wind": "kencang",    # Opsi: kencang, lemah
    "Cloud": "cerah",     # Opsi: cerah, berawan, mendung
    "Pressure": "tinggi", # Opsi: tinggi, normal, rendah
    "RainToday": "No"     # Opsi: Yes, No
}

# 🔮 Panggil Fungsi Prediksi
predict_naive_bayes(kasus_uji)
Output Visual yang Diharapkan:Plaintext==========================================
🔍 HASIL PREDIKSI NAIVE BAYES
==========================================
Probabilitas Hujan (Yes) : 0.0045
Probabilitas Tidak (No)  : 0.0210
------------------------------------------
🎯 KEPUTUSAN FINAL: TIDAK HUJAN (No) ☀️
==========================================
6. ⚠️ Catatan Penting<div align="left"><table><tr><td width="60px" align="center"><img src="https://www.google.com/search?q=https://cdn-icons-png.flaticon.com/512/1067/1067357.png" width="40"><strong>Manual</strong></td><td>Semua perhitungan (Prior, Likelihood, Skor, Posterior) dihitung secara <strong>manual</strong> menggunakan rumus matematika probabilitas, bukan menggunakan library instan "black box" seperti Scikit-Learn.</td></tr><tr><td align="center"><img src="https://www.google.com/search?q=https://cdn-icons-png.flaticon.com/512/564/564619.png" width="40"><strong>Laplace</strong></td><td><strong>Laplace Smoothing</strong> diterapkan pada perhitungan Likelihood. Ini sangat penting untuk mencegah probabilitas bernilai 0 jika ada data uji yang fiturnya tidak pernah muncul di data latih.</td></tr></table></div>📎 Repository GitHubSeluruh kode sumber dan pembaruan tersedia di repositori berikut:<a href="https://github.com/skimatt/Naive_Bayes"><img src="https://www.google.com/search?q=https://img.shields.io/badge/GITHUB-Repository-181717%3Fstyle%3Dfor-the-badge%26logo%3Dgithub" alt="Github Link"></a><div align="center"><p>Terima kasih telah meninjau tugas ini.Semoga dokumen ini membantu memahami implementasi Naive Bayes secara konseptual maupun praktis.</p><img src="https://www.google.com/search?q=https://cdn-icons-png.flaticon.com/512/1163/1163661.png" width="60" alt="Sun Cloud 3D"><sub>Dibuat dengan ❤️ dan ☕ untuk Tugas Kuliah</sub></div>

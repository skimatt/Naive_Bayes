

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

# Panduan Menjalankan Notebook

## Implementasi Naive Bayes Kategorial untuk Prediksi Cuaca Besok

Dokumen ini berisi panduan lengkap untuk membuka, menjalankan, dan melakukan pengujian terhadap file **NB_Cuaca_NPM.ipynb**.  
Notebook ini menggunakan Python dan Jupyter Notebook, serta melakukan seluruh perhitungan Naive Bayes **secara manual** tanpa library _sklearn_, sesuai ketentuan tugas Bapak.

---

## 1. Persyaratan Sistem

Sebelum menjalankan notebook, pastikan perangkat sudah memiliki:

- **Python 3.8 atau lebih baru**
- **Jupyter Notebook**, atau **Visual Studio Code** dengan ekstensi:
  - _Python_
  - _Jupyter_
- Library Python berikut:
  - `pandas`
  - `numpy`
  - `openpyxl` (untuk membaca file Excel)

Jika library belum terpasang, jalankan perintah berikut:

```bash
pip install pandas numpy openpyxl
```

---

## 2. Struktur File Tugas

```
NB_Cuaca_NPM.ipynb
dataset_hujan_besok_kategori.xlsx
README_NaiveBayes.md
```

Jika dataset berada di luar folder, notebook tidak dapat membaca file Excel.

---

## 3. Cara Membuka Notebook

### A. Menggunakan Visual Studio Code

1. Buka VS Code
2. Pilih **File → Open Folder** dan arahkan ke folder tugas
3. Klik file **NB_Cuaca_NPM.ipynb**
4. Pilih kernel Python (otomatis muncul di kanan atas)
5. Jalankan setiap cell dengan:

   - Tombol **▶ Run Cell**, atau
   - Shortcut **Shift + Enter**

### B. Menggunakan Jupyter Notebook

1. Buka terminal pada folder tugas
2. Jalankan:

```bash
jupyter notebook
```

3. Notebook akan terbuka di browser
4. Klik **NB_Cuaca_NPM.ipynb**, lalu jalankan cell satu per satu

---

## 4. Menjalankan Notebook

Setelah file dibuka, jalankan cell secara berurutan mulai dari atas:

1. **Cell Identitas & Deskripsi Tugas**
2. **Import library**
3. **Pembacaan dataset**
4. **Perhitungan prior**
5. **Perhitungan likelihood (Laplace smoothing)**
6. **Fungsi prediksi Naive Bayes**
7. **Pengujian 3 kasus prediksi**
8. **Interpretasi hasil**

Jika semua cell berjalan tanpa error, notebook telah bekerja sebagaimana mestinya.

---

## 5. Menguji Prediksi Secara Manual

Bapak dapat menambahkan contoh input baru untuk menguji model.

```python
contoh = {
    "Temp": "panas",
    "Humidity": "kering",
    "Wind": "kencang",
    "Cloud": "cerah",
    "Pressure": "tinggi",
    "RainToday": "No"
}

predict_naive_bayes(contoh)
```

Output yang ditampilkan adalah:

- Prediksi: Yes / No
- Nilai probabilitas **P(Yes)** dan **P(No)**

Model akan memilih kelas dengan probabilitas terbesar.

---

## 6. Catatan

- Notebook **tidak menggunakan sklearn** dalam proses perhitungan utama, sesuai instruksi tugas.
- Semua probabilitas dihitung menggunakan rumus:

  - Prior
  - Likelihood per fitur (dengan Laplace smoothing)
  - Skor kelas
  - Posterior

- Dataset bersifat kategorial dan sudah divalidasi agar tidak menimbulkan error saat diproses

---

Terima kasih telah mengunjungi repositori ini.


🔗 **Profil Owner:**  
[![GitHub - skimatt](https://img.shields.io/badge/GitHub-skimatt-black?logo=github&style=for-the-badge)](https://github.com/skimatt)

## 🙏 Terima Kasih

Terima kasih atas perhatian dan waktunya.  
Semoga repository ini bermanfaat dan mudah dipahami.

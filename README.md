# 📘 **Panduan Menjalankan Notebook — Implementasi Naive Bayes Kategorial untuk Prediksi Cuaca Besok**

Dokumen ini merupakan panduan resmi untuk membuka, menjalankan, dan menguji notebook **NB_Cuaca_NPM.ipynb**.
Seluruh proses perhitungan Naive Bayes dilakukan **secara manual** mengacu pada ketentuan tugas, tanpa menggunakan modul `sklearn.naive_bayes`.

Notebook ini saya susun untuk mendemonstrasikan pemahaman alur lengkap Naive Bayes:
**Prior → Likelihood (Laplace smoothing) → Skor → Posterior → Prediksi**.

---

## 1. Persyaratan Sistem

Sebelum menjalankan notebook, pastikan perangkat telah memiliki:

* **Python 3.8 atau lebih baru**
* **Jupyter Notebook**, atau **Visual Studio Code** dengan ekstensi:

  * Python
  * Jupyter
* Library Python:

  * `pandas`
  * `numpy`
  * `openpyxl` (untuk membaca file Excel)

Install library dengan:

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

Pastikan file Excel berada di folder yang sama dengan notebook.

---

## 3. Cara Membuka Notebook

### A. Visual Studio Code

1. Buka VS Code
2. Pilih **File → Open Folder** dan arahkan ke folder tugas
3. Klik file **NB_Cuaca_NPM.ipynb**
4. Pilih kernel Python yang tersedia
5. Jalankan cell satu per satu dengan:

   * Tombol **▶ Run Cell**, atau
   * Shortcut **Shift + Enter**

### B. Jupyter Notebook

1. Buka terminal pada folder tugas
2. Jalankan:

```bash
jupyter notebook
```

3. Notebook akan muncul di browser
4. Klik file dan jalankan cell mulai dari atas

---

## 4. Urutan Menjalankan Notebook

Notebook terdiri dari beberapa tahap utama:

1. **Identitas & Deskripsi Tugas**
2. **Import library**
3. **Pembacaan dataset cuaca**
4. **Perhitungan prior kelas (Yes/No)**
5. **Perhitungan likelihood menggunakan Laplace smoothing**
6. **Fungsi prediksi Naive Bayes**
7. **Pengujian tiga contoh kasus prediksi**
8. **Interpretasi hasil**

Jika seluruh cell dapat dijalankan tanpa error, proses Naive Bayes berjalan dengan benar.

---

## 5. Menguji Prediksi Secara Mandiri

Dosen / penguji dapat menambahkan contoh kasus baru untuk menguji model.
Struktur input adalah dictionary dengan nilai kategorial.

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

Model akan menampilkan:

* Prediksi `Yes` atau `No`
* Probabilitas **P(Yes)** dan **P(No)** berdasarkan perhitungan posterior

---

## 6. Catatan Penting

* Semua perhitungan prior, likelihood, skor, dan posterior dihitung **manual**, bukan dari library *sklearn*.
* Likelihood menggunakan **Laplace smoothing** untuk mencegah probabilitas 0.
* Dataset sudah divalidasi dan seluruh fitur bersifat kategorial sesuai instruksi tugas.

---

## 📎 **Repository GitHub**

Seluruh kode tersedia di repositori berikut:

🔗 [https://github.com/skimatt/Naive_Bayes](https://github.com/skimatt/Naive_Bayes)

---

## 🙏 Penutup

Terima kasih atas perhatian dan waktunya.
Semoga dokumen dan notebook ini membantu memahami implementasi Naive Bayes secara konseptual maupun praktis.

Jika diperlukan, saya siap melakukan revisi tambahan sesuai arahan.

---

Kalau kamu mau, saya bisa buatkan versi README **dalam format markdown lengkap** atau **menambahkan badge lain** (Python version, project status, dsb).

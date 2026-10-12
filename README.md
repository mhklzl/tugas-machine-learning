# Klasifikasi Tingkat Kepuasan Pengguna E-Wallet Indonesia

Tugas pengolahan dataset: memprediksi `Tingkat_Kepuasan` (Kurang Puas / Cukup Puas / Puas) pengguna e-wallet dari profil dan pola transaksinya.

## Struktur
- `data/penggunaan_ewallet_indonesia_5000.csv` — dataset (5.000 baris, 11 kolom)
- `main.ipynb` — alur lengkap: EDA, preprocessing, perbandingan 6 model, tuning, evaluasi, simpan model
- `hasil_project.ipynb` — memuat model tersimpan dan menampilkan hasil evaluasi
- `model_kepuasan_rf.pkl`, `kolom_fitur.pkl` — model Random Forest hasil training
- `requirements.txt` — daftar library

## Cara menjalankan
```bash
pip install -r requirements.txt
jupyter notebook
```
Jalankan `main.ipynb` dulu, lalu `hasil_project.ipynb`.

## Ringkasan hasil
- Dataset bersih (tanpa missing value/duplikat); target tidak seimbang (Puas ≈ 60%).
- Random Forest (tuned): accuracy ≈ 45%, macro-F1 ≈ 0,34; baseline "selalu Puas": accuracy 60%, macro-F1 0,25.
- Fitur yang ada hampir tidak informatif untuk memprediksi kepuasan; hasil dilaporkan apa adanya (lihat bagian Kesimpulan di notebook).

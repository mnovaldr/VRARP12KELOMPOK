
# 🦖 AR Evolusi Burung: Deinonychus ke Kalkun

Visualisasi interaktif hubungan evolusi antara dinosaurus Deinonychus dan burung modern Kalkun menggunakan teknologi **Augmented Reality (AR)** berbasis web.

## 📌 Deskripsi Proyek

Program ini menyajikan model 3D Deinonychus dan Kalkun secara bergantian menggunakan marker AR. Pengguna dapat berinteraksi dengan objek, membaca penjelasan evolusi, serta memutar suara khas dari masing-masing hewan.

### Fitur Utama:
- Menampilkan dua model 3D: Deinonychus & Kalkun.
- Menggunakan **marker custom** dengan preset `"custom"` dan file `.patt`.
- Interaksi melalui tombol:
  - 🔄 Ganti Model
  - 📜 Tampilkan Informasi Evolusi
  - 🔊 Putar Suara sesuai model aktif
- Tampilan minimalis dan adaptif untuk perangkat mobile.

## 📁 Struktur Folder

```bash
├── index.html                  # File utama AR
├── assets/
│   ├── 3d/
│   │   ├── deinonychus.glb     # Model Deinonychus
│   │   └── turkey.glb          # Model Kalkun
│   ├── sound/
│   │   ├── Archaeopteryx.mp3   # Suara Deinonychus (representatif)
│   │   └── Pigeon.mp3          # Suara Kalkun
│   └── marker/
│       └── marker.patt         # Marker pattern custom AR.js
```

Untuk mengakses proyek ini menggunakan **Live Server** (ekstensi pada Visual Studio Code), Anda cukup mengikuti langkah berikut dan tidak perlu mengubah kode secara signifikan.

Namun, agar README lebih relevan, berikut adalah revisi bagian **Cara Menjalankan** agar menggunakan *Live Server*:


### ⚙️ Cara Menjalankan Proyek Menggunakan Live Server

1. **Buka folder proyek di Visual Studio Code**

   * Pastikan struktur folder seperti ini:

     ```
     /your-project-folder
     ├── index.html
     ├── assets/
     │   ├── 3d/
     │   ├── sound/
     │   └── marker/
     ```

2. **Pasang ekstensi Live Server**

   * Buka VS Code > Extensions (Ctrl+Shift+X)
   * Cari “Live Server” oleh *Ritwick Dey* lalu install.

3. **Jalankan dengan Live Server**

   * Klik kanan pada `index.html` > **Open with Live Server**
   * Browser akan terbuka di alamat semacam `http://127.0.0.1:5500/`

4. **Akses di Perangkat Mobile (Opsional)**

   * Hubungkan laptop dan HP ke Wi-Fi yang sama.
   * Buka alamat IP lokal (misal `http://192.168.1.x:5500`) di browser HP.
   * Gunakan kamera HP untuk pengalaman AR yang lebih baik.

5. **Pastikan Izin Kamera Aktif**

   * Saat pertama kali membuka halaman, browser akan meminta izin untuk menggunakan kamera. Klik “Izinkan”.


### 3. Scan Marker
Cetak atau tampilkan file `marker.patt` menggunakan pattern generator (misalnya Hiro Marker Generator). Pastikan pencahayaan cukup saat pemindaian.

## 💡 Penjelasan Fungsi Utama

| Fungsi JS           | Deskripsi |
|---------------------|-----------|
| `gantiModel()`      | Mengganti tampilan dari Deinonychus ↔ Kalkun |
| `togglePenjelasan()`| Menampilkan kotak info edukasi evolusi |
| `putarSuara()`      | Memainkan suara sesuai model yang aktif |
| `marker` AR.js      | Mendeteksi pola marker dan memicu tampilan objek |

## 📚 Sumber Ilmiah (Edukasi Evolusi)

- Deinonychus adalah dinosaurus berbulu dari era Cretaceous, bagian dari kelompok theropoda.
- Burung modern, seperti kalkun, merupakan keturunan langsung dari kelompok theropoda.
- Bukti evolusi mencakup kesamaan struktur tulang, kaki, paruh, dan bulu.

## 🌐 Teknologi yang Digunakan

- [A-Frame (aframe.io)](https://aframe.io)
- [AR.js (AR dengan marker)](https://github.com/AR-js-org/AR.js)
- GLB 3D Model (via [donmccurdy/aframe-extras](https://github.com/donmccurdy/aframe-extras) jika menggunakan loader tambahan)

## 📄 Lisensi

Proyek ini bersifat **edukatif** dan **non-komersial**. Semua model dan suara digunakan untuk kepentingan pembelajaran. Pastikan penggunaan aset 3D memiliki lisensi yang sesuai jika akan dipublikasikan secara luas.

## ✨ Pengembangan Selanjutnya

- Penambahan narasi audio edukasi otomatis.
- Markerless AR untuk perangkat berbasis GPS/kamera.
- Evaluasi interaktif: kuis atau fakta setelah melihat model.

# Smart Heart Pulse Monitoring Web App

**Smart Heart Monitor** adalah aplikasi web berbasis React dan Tailwind CSS yang dirancang untuk membantu tenaga medis, peneliti, maupun pengguna individu dalam memantau dan mencatat detak jantung secara real-time.

Aplikasi ini mampu:
- Membaca data pasien dari file Excel
- Menampilkan daftar pasien dalam bentuk tabel
- Menyediakan grafik detak jantung (heart rate) secara live
- Menampilkan nilai BPM (Beats Per Minute) terkini
- Memungkinkan pengguna memilih pasien tertentu dan memvisualisasikan datanya

---

## 📁 Struktur Folder

```
project-root/
├── package.json
├── vercel.json
├── public/
│   └── index.html
├── src/
│   ├── App.jsx
│   ├── index.js
│   ├── index.css
│   ├── PatientTable.jsx
│   └── components/
│       └── ui/
│           └── button.jsx
├── tailwind.config.js
├── postcss.config.js
├── jsconfig.json
└── README.md ← (file ini)
```

---

## 🔧 Teknologi yang Digunakan

| Teknologi         | Deskripsi                                                                 |
|------------------|---------------------------------------------------------------------------|
| React            | Library UI utama                                                         |
| Tailwind CSS     | Styling modern berbasis utility                                          |
| Chart.js         | Library visualisasi data grafik                                          |
| react-chartjs-2  | Wrapper React untuk Chart.js                                             |
| xlsx             | Library untuk parsing file Excel (.xlsx/.xls)                            |
| Vercel           | Platform hosting dan deployment aplikasi                                 |

---

## 📥 Cara Upload Data Pasien

1. Siapkan file Excel `.xlsx` dengan format seperti ini:

| ID   | Name       |
|------|------------|
| P001 | John Doe   |
| P002 | Jane Smith |

2. Buka aplikasi dan klik **"Choose File"**
3. Pilih file Excel dari komputer Anda
4. Data akan muncul dalam tabel

---

## 📊 Live Sensor Monitoring

Setelah memilih salah satu pasien:
- Aplikasi akan menampilkan **grafik detak jantung** dengan data dummy (simulasi)
- Angka **BPM terkini** akan muncul di atas grafik
- Grafik akan terus diperbarui setiap detik

---

## 🧪 Mode Simulasi vs Mode Nyata

Saat ini, data BPM yang ditampilkan adalah **data simulasi** untuk keperluan pengujian dan demo.

Jika Anda ingin menghubungkan sensor jantung asli (misalnya ESP32 + sensor detak):
- Backend tambahan diperlukan untuk menerima data sensor
- Anda bisa menggunakan Firebase Realtime DB, MQTT, atau REST API

Silakan hubungi pengembang untuk integrasi lebih lanjut.

---

## 📦 Build & Jalankan Lokal

```bash
# Install dependencies
npm install

# Jalankan di lokal
npm start

# Build untuk production
npm run build
```

---

## 🚀 Deployment

Aplikasi ini sudah siap deploy ke Vercel. Pastikan struktur folder sudah benar dan file `vercel.json` tersedia.

```json
// vercel.json
{
  "rewrites": [
    { "source": "/(.*)", "destination": "/" }
  ]
}
```

---

## 📈 Pengembangan Selanjutnya (Opsional)

- Integrasi sensor asli via Firebase/MQTT
- Simpan & muat riwayat pasien ke database
- Tambah export data PDF
- Fitur alert jika BPM terlalu tinggi/rendah
- Tampilan mobile responsif

---

## 👨‍💻 Kontributor

Website ini dikembangkan sebagai bagian dari proyek **IoT Kesehatan & Deteksi Dini Jantung**, dengan fokus mendukung tujuan **SDG 3 (Good Health and Well-being)** dan mendukung pelayanan medis yang **inklusif dan berkelanjutan**.

Jika Anda tertarik mengembangkan lebih lanjut, silakan fork repo dan kirim pull request.

---

Terima kasih telah menggunakan Smart Heart Monitor 💓

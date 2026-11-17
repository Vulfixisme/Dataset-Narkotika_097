# Dataset Narkotika PN Semarang

Dataset ini disusun untuk memenuhi Tugas 2 (SubCPMK-2), UTS mata kuliah Temu Kembali Informasi, Semester Ganjil 2026/2027, Universitas Muhammadiyah Malang.

Dataset berisi dokumen putusan pengadilan dalam perkara narkotika yang diperoleh melalui pengumpulan manual dan proses crawling dari Direktori Putusan Mahkamah Agung Republik Indonesia.

## Anggota Kelompok

| **Nama** | **NIM** |
|---|---|
| Hafizh Al Bukhori | 202310370311097 |

Nama repository: **Dataset-Narkotika_097_XXX**

Keterangan: `XXX` disesuaikan dengan tiga digit terakhir NIM anggota kelompok kedua apabila dikerjakan secara berkelompok. Repository pengumpulan diatur dalam bentuk **Public**.

## Cakupan Dataset

- **Pengadilan:** Pengadilan Negeri Semarang.
- **Direktori:** Pidana Khusus.
- **Klasifikasi:** Narkotika dan Psikotropika.
- **Sumber:** Direktori Putusan Mahkamah Agung Republik Indonesia.
- **Metode akuisisi:** Pengumpulan manual dan crawling.
- **Format dokumen:** PDF dan TXT.

### 1. Dataset Manual

Dokumen manual merupakan putusan pengadilan yang dikumpulkan melalui pengunduhan langsung dari Direktori Putusan Mahkamah Agung.

- Jumlah dokumen: **5 putusan**.
- Format: PDF.
- Lokasi: `Dataset/manual/`.

### 2. Hasil Crawler

Dataset juga dilengkapi dengan dokumen hasil crawling yang digunakan untuk memperluas koleksi dokumen dan mendukung proses pengolahan data.

- Jumlah dokumen PDF: **50 file**.
- Jumlah dokumen TXT: **50 file**.
- Lokasi PDF: `Dataset/pdf/`.
- Lokasi TXT: `Dataset/txt/`.

File PDF merupakan dokumen putusan pengadilan, sedangkan file TXT merupakan hasil ekstraksi teks dari dokumen PDF untuk memudahkan pengolahan dan pengambilan informasi.

Jumlah berkas tersebut merupakan hasil pengumpulan awal. Pemeriksaan kesamaan nomor perkara antara dokumen manual dan hasil crawler dilakukan untuk menghindari duplikasi data.

## Sumber dan Pengumpulan Data

Dokumen putusan diperoleh melalui [Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/direktori.html).

Pengumpulan dilakukan dengan memilih direktori **Pidana Khusus**, klasifikasi **Narkotika dan Psikotropika**, serta Pengadilan Negeri Semarang.

Proses pengumpulan data terdiri dari dua metode:

1. **Pengumpulan manual:** Dokumen putusan diunduh secara langsung melalui halaman detail putusan.
2. **Crawling:** Dokumen putusan dan hasil ekstraksi teks dikumpulkan melalui proses crawling.

Dokumen PDF digunakan sebagai sumber utama, sedangkan TXT digunakan untuk membantu proses ekstraksi dan pengolahan informasi.

## Pemeriksaan Status Putusan

Sesuai ketentuan tugas, putusan dengan status **Berkekuatan Hukum Tetap (BHT)** tidak digunakan.

Pemeriksaan status dilakukan dengan memperhatikan informasi yang tersedia pada halaman detail putusan di Direktori Putusan Mahkamah Agung.

Apabila status tidak tercantum secara jelas pada halaman sumber, informasi tersebut dicatat sebagai **Tidak tercantum** dan tidak disimpulkan sendiri.

## Struktur Repository

```text
Crawler-project/
├── Dataset/
│   ├── manual/
│   │   ├── 420_Pid.Sus_202...
│   │   ├── 436_Pid.Sus_202...
│   │   ├── 450_Pid.Sus_202...
│   │   ├── 464_Pid.Sus_202...
│   │   └── 471_Pid.Sus_202...
│   │
│   ├── pdf/
│   │   ├── Putusan_Crawler_01.pdf
│   │   ├── Putusan_Crawler_02.pdf
│   │   └── ...
│   │
│   └── txt/
│       ├── Putusan_Crawler_01.txt
│       ├── Putusan_Crawler_02.txt
│       └── ...
│
├── Overview/
│   └── Overview.xlsx
│
└── README.md
```

## Isi Overview.xlsx

File `Overview/Overview.xlsx` digunakan untuk menyajikan ringkasan informasi dari dokumen putusan pengadilan.

Overview menggunakan lima kolom utama sesuai ketentuan tugas:

| **Kolom** | **Keterangan** |
|---|---|
| No | Nomor urut data putusan |
| No Putusan | Identitas resmi nomor perkara |
| Lembaga Peradilan | Nama pengadilan yang mengeluarkan putusan |
| Barang Bukti | Rincian barang bukti berdasarkan dokumen putusan |
| Amar Putusan | Isi amar putusan pada bagian MENGADILI |

Data manual dan hasil crawler disusun dalam tabel yang sama setelah dilakukan pemeriksaan nomor perkara dan kesesuaian informasi.

## Penyusunan Ringkasan

Informasi pada Overview disusun berdasarkan isi dokumen putusan asli.

- **Nomor Putusan:** Diambil dari identitas perkara pada dokumen.
- **Lembaga Peradilan:** Diambil dari informasi pengadilan yang menangani perkara.
- **Barang Bukti:** Diambil dari bagian penetapan barang bukti dalam amar putusan.
- **Amar Putusan:** Diambil dari bagian MENGADILI pada dokumen putusan.

File TXT hasil crawler digunakan untuk membantu proses pengambilan informasi secara otomatis. Hasil ekstraksi tetap perlu diperiksa kembali menggunakan PDF asli untuk memastikan kesesuaian informasi.

Penulisan ringkasan mempertahankan substansi dokumen sumber, termasuk nama terdakwa, nomor perkara, jenis barang bukti, jumlah, berat, dan amar pidana yang dijatuhkan.

## Cara Menggunakan Dataset

1. Buka folder `Dataset/manual/` untuk melihat dokumen putusan yang dikumpulkan secara manual.
2. Buka folder `Dataset/pdf/` untuk melihat dokumen putusan hasil crawling.
3. Buka folder `Dataset/txt/` untuk mengakses hasil ekstraksi teks.
4. Buka `Overview/Overview.xlsx` untuk melihat ringkasan informasi putusan.
5. Cocokkan informasi pada Overview dengan dokumen PDF asli apabila diperlukan.

## Tujuan Penggunaan Dataset

Dataset ini digunakan sebagai bahan pembelajaran dalam domain **Temu Kembali Informasi (TKI)**, khususnya untuk memahami proses akuisisi dokumen, pengelolaan koleksi dokumen hukum, ekstraksi informasi, serta persiapan data untuk sistem pencarian informasi.

Dataset ini juga dapat dimanfaatkan sebagai bahan eksperimen dalam pengembangan sistem pencarian dokumen putusan pengadilan.

---

**Universitas Muhammadiyah Malang**

**Temu Kembali Informasi — Semester Ganjil 2026/2027**
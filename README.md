# Manajemen Proyek Kesehatan Masyarakat: Gantt Chart dengan Google Sheets

> Panduan praktis pembuatan Gantt Chart untuk perencanaan program kesehatan masyarakat

## Sasaran Pengguna
Mahasiswa S1 Kesehatan Masyarakat

## yang Akan Anda Pelajari
Membuat Gantt Chart di Google Sheets untuk memvisualisasikan jadwal proyek program kesehatan masyarakat. Panduan ini menggunakan dua contoh program yang berbeda:
1. **Program Skrining TB** di Sekolah
2. **Program Edukasi Gizi** untuk Pencegahan Stunting

---

# CONTOH 1: Program Skrining TB di Sekolah

Program skrining Tuberkulosis (TB) di lingkungan sekolah untuk deteksi dini dan penanganan kasus TB.

## Struktur Program

| Fase | Deskripsi |
|------|-----------|
| **Perencanaan** | Asesmen kebutuhan, koordinasi dengan sekolah, persiapan alat |
| **Pelaksanaan** | Skrining siswa, pemeriksaan tenaga kesehatan, rujukan kasus |
| **Evaluasi** | Analisis data, laporan hasil, perencanaan tindak lanjut |

## Data Contoh: Program Skrining TB

| | A | B | C | D |
|---|---|---|---|---|
| **1** | Nama Kegiatan | Tanggal Mulai | Tanggal Selesai | Durasi (Hari) |
| **2** | Pertemuan dengan Kepala Sekolah | 2025-04-01 | 2025-04-01 | `=C2-B2` |
| **3** | Surat Izin Orang Tua | 2025-04-02 | 2025-04-05 | `=C3-B3` |
| **4** | Rekrutmen Petugas Kesehatan | 2025-04-03 | 2025-04-08 | `=C4-B4` |
| **5** | Pelatihan Petugas Skrining | 2025-04-06 | 2025-04-10 | `=C5-B5` |
| **6** | Persiapan Alat Skrining | 2025-04-09 | 2025-04-12 | `=C6-B6` |
| **7** | Skrining TB Hari 1 - Kelas X | 2025-04-13 | 2025-04-13 | `=C7-B7` |
| **8** | Skrining TB Hari 2 - Kelas XI | 2025-04-14 | 2025-04-14 | `=C8-B8` |
| **9** | Skrining TB Hari 3 - Kelas XII | 2025-04-15 | 2025-04-15 | `=C9-B9` |
| **10** | Pemeriksaan Dokter untuk Kasus Suspek | 2025-04-16 | 2025-04-18 | `=C10-B10` |
| **11** | Konseling Siswa Positif TB | 2025-04-19 | 2025-04-20 | `=C11-B11` |
| **12** | Koordinasi dengan Puskesmas | 2025-04-21 | 2025-04-22 | `=C12-B12` |
| **13** | Entry Data & Analisis Hasil | 2025-04-23 | 2025-04-28 | `=C13-B13` |
| **14** | Laporan ke Dinas Kesehatan | 2025-04-29 | 2025-04-30 | `=C14-B14` |

---

# CONTOH 2: Program Edukasi Gizi untuk Pencegahan Stunting

Program edukasi gizi bagi orang tua siswa untuk pencegahan stunting pada anak.

## Struktur Program

| Fase | Deskripsi |
|------|-----------|
| **Perencanaan** | Survey status gizi, penyusunan materi, koordinasi dengan ahli gizi |
| **Pelaksanaan** | Edukasi orang tua, demo memasak bergizi, monitoring makanan |
| **Evaluasi** | Evaluasi pengetahuan, monitoring berat badan, laporan |

## Data Contoh: Program Edukasi Gizi

| | A | B | C | D |
|---|---|---|---|---|
| **1** | Nama Kegiatan | Tanggal Mulai | Tanggal Selesai | Durasi (Hari) |
| **2** | Survey Awal Status Gizi Siswa | 2025-05-01 | 2025-05-05 | `=C2-B2` |
| **3** | Koordinasi dengan Ahli Gizi | 2025-05-03 | 2025-05-04 | `=C3-B3` |
| **4** | Penyusunan Materi Edukasi | 2025-05-05 | 2025-05-10 | `=C4-B4` |
| **5** | Undangan Orang Tua Siswa | 2025-05-08 | 2025-05-12 | `=C5-B5` |
| **6** | Persiapan Bahan Demo Memasak | 2025-05-11 | 2025-05-14 | `=C6-B6` |
| **7** | Sesi Edukasi 1: Gizi Seimbang | 2025-05-15 | 2025-05-15 | `=C7-B7` |
| **8** | Sesi Edukasi 2: Makanan Lokal Bergizi | 2025-05-16 | 2025-05-16 | `=C8-B8` |
| **9** | Demo Memasak Sayur & Protein | 2025-05-17 | 2025-05-17 | `=C9-B9` |
| **10** | Praktek Menu Sehat di Rumah | 2025-05-18 | 2025-05-24 | `=C10-B10` |
| **11** | Pengukuran Berat Badan Siswa | 2025-05-25 | 2025-05-26 | `=C11-B11` |
| **12** | Evaluasi Pengetahuan Orang Tua | 2025-05-27 | 2025-05-27 | `=C12-B12` |
| **13** | Analisis Data Perubahan Gizi | 2025-05-28 | 2025-06-03 | `=C13-B13` |
| **14** | Laporan & Rekomendasi Program | 2025-06-04 | 2025-06-07 | `=C14-B14` |

---

# Metode 1: Stacked Bar Chart (Disarankan untuk Visualisasi)

## Langkah 1: Siapkan Data Anda

Buat Google Sheet dengan kolom persis seperti contoh di atas:

- **Kolom A**: Nama Kegiatan
- **Kolom B**: Tanggal Mulai
- **Kolom C**: Tanggal Selesai
- **Kolom D**: Durasi (Hari) dengan rumus `=C2-B2`

## Langkah 2: Buat Grafik

1. **Pilih data Anda**: Blokir kolom A, B, dan D (Nama Kegiatan, Tanggal Mulai, Durasi)
   - **Jangan sertakan** kolom Tanggal Selesai

2. **Sisipkan grafik**:
   - Klik **Insert** → **Chart**
   - Atau gunakan toolbar: Klik **ikon Chart**

3. **Atur tipe grafik**:
   - Di Chart Editor, tab **Setup**
   - Ubah **Chart type** menjadi **Stacked bar chart**

## Langkah 3: Konfigurasi Series

1. Buka tab **Customize** di Chart Editor

2. Klik dropdown **Series**

3. **Untuk series "Tanggal Mulai"** (buat tidak terlihat):
   - Pilih **Start Date** dari dropdown
   - Set **Fill color** ke **White** (atau transparan)
   - Set **Line opacity** ke **0%**

4. **Untuk series "Durasi"** (bar yang terlihat):
   - Pilih **Duration** dari dropdown
   - Set **Fill color** dengan warna terlihat (misalnya biru atau hijau)
   - Tambahkan **Border color** jika diinginkan

## Langkah 4: Balik Sumbu Vertikal

1. Di tab **Customize**, klik **Vertical axis**

2. Centang kotak: **Reverse axis order**

Ini memastikan Kegiatan 1 muncul di bagian atas (bukan bawah).

## Langkah 5: Format Sumbu Horizontal (Timeline)

1. Di tab **Customize**, klik **Horizontal axis**

2. Sesuaikan format tanggal:
   - Pilih format yang mudah dibaca (misalnya "1 Apr" atau "Apr 1")

---

# Metode 2: Conditional Formatting (Timeline Berbasis Grid)

## Langkah 1: Buat Header Timeline

1. Di sel **F1**, masukkan tanggal mulai: `2025-04-01`

2. Di sel **G1**, masukkan: `=F1+1`

3. Tarik G1 ke kanan untuk membuat tanggal harian melalui tanggal akhir proyek

## Langkah 2: Tambahkan Rumus

Untuk setiap baris kegiatan (mulai dari baris 2), gunakan rumus ini di sel F2:

```
=AND(F$1>=$B2, F$1<=$C2)
```

Lalu tarik rumus ini:
- **Ke kanan** melalui semua kolom tanggal
- **Ke bawah** untuk semua baris kegiatan

## Langkah 3: Terapkan Conditional Formatting

1. Pilih seluruh grid (dari F2 ke kolom tanggal terakhir untuk semua kegiatan)

2. Klik **Format** → **Conditional formatting**

3. Atur aturan:
   - **Format cells if**: **Is true**
   - **Value or formula**: `=AND(F$1>=$B2, F$1<=$C2)`
   - **Formatting style**: Pilih warna isi (misalnya hijau)

4. Klik **Done**

---

# Checklist Hasil Akhir

Setelah membuat Gantt Chart, verifikasi:

- [ ] Sumbu vertikal menampilkan daftar kegiatan dengan urutan benar (Kegiatan 1 di atas)
- [ ] Bar "Tanggal Mulai" tidak terlihat/putih (Metode 1)
- [ ] Durasi kegiatan akurat sesuai data
- [ ] Ketergantungan kegiatan divisualisasikan dengan benar (tumpang tindih atau berurutan)
- [ ] Grafik menunjukkan tiga fase dengan jelas: Perencanaan, Pelaksanaan, Evaluasi
- [ ] Tanggal mudah dibaca dan format benar

---

# Contoh Program Kesehatan Masyarakat Lainnya

| Jenis Program | Contoh Kegiatan |
|---------------|-----------------|
| **Imunisasi** | Persiapan lokasi, pelatihan petugas, mobilisasi masyarakat, hari imunisasi, monitoring KEI |
| **Studi Kohort** | Penyusunan protokol, persetujuan etik, rekrutmen, pengumpulan data dasar, kunjungan tindak lanjut, analisis data |
| **Seminar Kesehatan** | Pemilihan topik, undangan pembicara, booking venue, promosi, pelaksanaan acara, pengumpulan feedback |
| **Respon KLB** | Investigasi kasus, tracing kontak, tindakan karantina, edukasi masyarakat, monitoring & evaluasi |

---

# Template & Sumber Daya

### Template Siap Pakai
- [Template Google Sheets TeamGantt](https://teamgantt.com/google-sheets-gantt-chart-template)
- [Template Pelacakan Proyek Unito](https://unito.io/blog/google-sheets-gantt-chart/)

### Catatan Penting
Meskipun template membantu, pastikan Anda memahami:
- Cara kerja rumus durasi (`=Tanggal Selesai - Tanggal Mulai`)
- Cara mengatur aturan conditional formatting
- Cara menyesuaikan grafik untuk timeline proyek yang berbeda

---

# Tips untuk Mahasiswa Kesehatan Masyarakat

1. **Pecah kegiatan** menjadi tugas-tugas spesifik dan terukur
2. **Sertakan waktu buffer** untuk keterlambatan tak terduga
3. **Gunakan kode warna** untuk membedakan:
   - Fase Perencanaan (misalnya biru)
   - Fase Pelaksanaan (misalnya hijau)
   - Fase Evaluasi (misalnya oranye)
4. **Pertimbangkan ketergantungan** - tugas mana yang harus selesai sebelum tugas lain dimulai?
5. **Bagikan Gantt Chart** Anda dengan anggota tim untuk perencanaan kolaboratif

---

# File Contoh dan Template

Repository ini menyediakan file contoh untuk kedua program:

1. **`tb-screening-program.csv`** - Data lengkap Program Skrining TB
2. **`nutrition-stunting-program.csv`** - Data lengkap Program Edukasi Gizi
3. **`gantt-template.csv`** - Template kosong untuk proyek Anda sendiri

---

# Lisensi

Sumber daya edukatif ini dibuat untuk mahasiswa Kesehatan Masyarakat di Indonesia.

# Kontribusi

Ini adalah sumber daya edukasi terbuka. Silakan adaptasi contoh untuk konteks kesehatan masyarakat Anda.

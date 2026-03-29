# Manajemen Proyek Kesehatan Masyarakat: Gantt Chart dengan Google Sheets

> Panduan praktis pembuatan Gantt Chart untuk perencanaan program kesehatan masyarakat

## Sasaran Pengguna
Mahasiswa S1 Kesehatan Masyarakat

## yang Akan Anda Pelajari
Membuat Gantt Chart di Google Sheets menggunakan metode **Conditional Formatting (Grid)**. Metode ini bekerja dengan baik di Google Sheets dan mudah disesuaikan.

Panduan ini menggunakan dua contoh program yang berbeda:
1. **Program Skrining TB** di Sekolah
2. **Program Edukasi Gizi** untuk Pencegahan Stunting

---

# CONTOH 1: Program Skrining TB di Sekolah

Program skrining Tuberkulosis (TB) di lingkungan sekolah untuk deteksi dini dan penanganan kasus TB.

## Data Contoh: Program Skrining TB

| | A | B | C |
|---|---|---|---|
| **1** | Nama Kegiatan | Tanggal Mulai | Tanggal Selesai |
| **2** | Pertemuan dengan Kepala Sekolah | 2025-04-01 | 2025-04-01 |
| **3** | Surat Izin Orang Tua | 2025-04-02 | 2025-04-05 |
| **4** | Rekrutmen Petugas Kesehatan | 2025-04-03 | 2025-04-08 |
| **5** | Pelatihan Petugas Skrining | 2025-04-06 | 2025-04-10 |
| **6** | Persiapan Alat Skrining | 2025-04-09 | 2025-04-12 |
| **7** | Skrining TB Hari 1 - Kelas X | 2025-04-13 | 2025-04-13 |
| **8** | Skrining TB Hari 2 - Kelas XI | 2025-04-14 | 2025-04-14 |
| **9** | Skrining TB Hari 3 - Kelas XII | 2025-04-15 | 2025-04-15 |
| **10** | Pemeriksaan Dokter untuk Kasus Suspek | 2025-04-16 | 2025-04-18 |
| **11** | Konseling Siswa Positif TB | 2025-04-19 | 2025-04-20 |
| **12** | Koordinasi dengan Puskesmas | 2025-04-21 | 2025-04-22 |
| **13** | Entry Data & Analisis Hasil | 2025-04-23 | 2025-04-28 |
| **14** | Laporan ke Dinas Kesehatan | 2025-04-29 | 2025-04-30 |

---

# CONTOH 2: Program Edukasi Gizi untuk Pencegahan Stunting

Program edukasi gizi bagi orang tua siswa untuk pencegahan stunting pada anak.

## Data Contoh: Program Edukasi Gizi

| | A | B | C |
|---|---|---|---|
| **1** | Nama Kegiatan | Tanggal Mulai | Tanggal Selesai |
| **2** | Survey Awal Status Gizi Siswa | 2025-05-01 | 2025-05-05 |
| **3** | Koordinasi dengan Ahli Gizi | 2025-05-03 | 2025-05-04 |
| **4** | Penyusunan Materi Edukasi | 2025-05-05 | 2025-05-10 |
| **5** | Undangan Orang Tua Siswa | 2025-05-08 | 2025-05-12 |
| **6** | Persiapan Bahan Demo Memasak | 2025-05-11 | 2025-05-14 |
| **7** | Sesi Edukasi 1: Gizi Seimbang | 2025-05-15 | 2025-05-15 |
| **8** | Sesi Edukasi 2: Makanan Lokal Bergizi | 2025-05-16 | 2025-05-16 |
| **9** | Demo Memasak Sayur & Protein | 2025-05-17 | 2025-05-17 |
| **10** | Praktek Menu Sehat di Rumah | 2025-05-18 | 2025-05-24 |
| **11** | Pengukuran Berat Badan Siswa | 2025-05-25 | 2025-05-26 |
| **12** | Evaluasi Pengetahuan Orang Tua | 2025-05-27 | 2025-05-27 |
| **13** | Analisis Data Perubahan Gizi | 2025-05-28 | 2025-06-03 |
| **14** | Laporan & Rekomendasi Program | 2025-06-04 | 2025-06-07 |

---

# TUTORIAL: Membuat Gantt Chart dengan Conditional Formatting

## Langkah 1: Siapkan Data Anda

Buat Google Sheet dengan 3 kolom:

| | A | B | C |
|---|---|---|---|
| **1** | Nama Kegiatan | Tanggal Mulai | Tanggal Selesai |

**PENTING:** Format kolom B dan C sebagai tanggal:
1. Pilih sel B2 dan C2 ke bawah
2. Klik **Format** → **Number** → **Date**

## Langkah 2: Buat Header Timeline

1. Di sel **E1**, masukkan tanggal mulai proyek Anda (contoh: `2025-04-01`)

2. Di sel **F1**, masukkan rumus: `=E1+1`

3. Tarik sel F1 ke kanan sampai tanggal akhir proyek

   *Tip: Anda akan melihat tanggal berurutan (1 Apr, 2 Apr, 3 Apr, dst.)*

**Contoh hasil:**
| | E | F | G | H | I | ... |
|---|---|---|---|---|---|---|
| **1** | 01/04/2025 | 02/04/2025 | 03/04/2025 | 04/04/2025 | 05/04/2025 | ... |

## Langkah 3: Tambahkan Rumus Pengecekan

Untuk setiap baris kegiatan, kita akan menambahkan rumus yang mengecek apakah tanggal tersebut falls dalam rentang kegiatan.

1. Di sel **E2**, masukkan rumus ini:

```
=AND(E$1>=$B2, E$1<=$C2)
```

2. Tarik rumus ini:
   - **Ke kanan** ke semua kolom tanggal
   - **Ke bawah** untuk semua kegiatan

**Penjelasan Rumus:**
- `E$1` = Tanggal di header (dengan `$` untuk mengunci baris)
- `$B2` = Tanggal mulai kegiatan ini (dengan `$` untuk mengunci kolom)
- `$C2` = Tanggal selesai kegiatan ini
- `AND()` = Memeriksa apakah tanggal header ADA dalam rentang tanggal kegiatan

Hasilnya akan menampilkan **TRUE** (jika tanggal aktif) atau **FALSE** (jika tidak aktif).

## Langkah 4: Terapkan Conditional Formatting

Sekarang kita akan membuat sel berubah warna berdasarkan hasil rumus.

1. **Pilih seluruh area grid**
   - Mulai dari E2
   - Pilih sampai kolom tanggal terakhir
   - Pilih sampai baris kegiatan terakhir

2. Klik **Format** → **Conditional formatting**

3. Di panel Conditional format rules:
   - Klik **+ Add another rule**

4. Atur rule seperti ini:
   - **Format cells if**: pilih **Is true**
   - **Value or formula**: `=AND(E$1>=$B2, E$1<=$C2)`
   - **Formatting style**: Klik ikon warna isi, pilih warna (misalnya hijau atau biru)

5. Klik **Done**

## Langkah 5: Format Tampilan (Opsional tapi Disarankan)

### Menghilangkan teks TRUE/FALSE:
1. Pilih seluruh grid (E2 sampai akhir)
2. Klik **Format** → **Number** → **Custom date and time**
3. Hapus format dan biarkan kosong, atau atur warna teks sama dengan warna background

### Menambahkan garis grid:
1. Pilih seluruh area
2. Klik ikon **Borders** (garis kotak)
3. Pilih **All borders**

### Mengatur lebar kolom:
1. Pilih semua kolom tanggal
2. Klik kanan → **Resize column** → **Fit to data**

---

# HASIL AKHIR

Setelah selesai, Anda akan memiliki:

- **Kolom A-C**: Data kegiatan
- **Kolom E ke kanan**: Timeline visual dengan warna
- Setiap baris menunjukkan kapan kegiatan tersebut aktif
- Mudah melihat tumpang tindih antar kegiatan

---

# Checklist Verifikasi

Setelah membuat Gantt Chart, periksa:

- [ ] Semua kolom tanggal (B dan C) diformat sebagai **Date**
- [ ] Header timeline (baris 1) menunjukkan tanggal berurutan
- [ ] Rumus `=AND(E$1>=$B2, E$1<=$C2)` diterapkan ke seluruh grid
- [ ] Conditional formatting diatur dengan **Is true**
- [ ] Warna muncul pada tanggal yang benar
- [ ] Tidak ada teks TRUE/FALSE yang terlihat
- [ ] Garis grid memudahkan pembacaan

---

# Tips Tambahan

## Gunakan Warna Berbeda untuk Fase Berbeda

Untuk membedakan fase, Anda bisa menambahkan aturan conditional formatting tambahan:

1. Tambahkan kolom **Fase** di kolom D:
   - **Perencanaan**
   - **Pelaksanaan**
   - **Evaluasi**

2. Buat aturan conditional formatting untuk setiap fase dengan warna berbeda:
   - Perencanaan: Biru
   - Pelaksanaan: Hijau
   - Evaluasi: Oranye

## Menandai Hari Libur

1. Tambahkan baris baru di atas header (misalnya baris 1, pindahkan header ke baris 2)
2. Di baris 1, tandai hari libur dengan teks "Libur"
3. Gunakan conditional formatting untuk memberi warna merah pada hari libur

## Mencetak dalam Ukuran Kertas

1. Klik **File** → **Page setup**
2. Pilih orientasi **Landscape**
3. Atur skala ke **Fit to width**
4. Klik **File** → **Print**

---

# Contoh Program Kesehatan Masyarakat Lainnya

| Jenis Program | Contoh Kegiatan |
|---------------|-----------------|
| **Imunisasi** | Persiapan lokasi, pelatihan petugas, mobilisasi masyarakat, hari imunisasi, monitoring KEI |
| **Studi Kohort** | Penyusunan protokol, persetujuan etik, rekrutmen, pengumpulan data dasar, kunjungan tindak lanjut, analisis data |
| **Seminar Kesehatan** | Pemilihan topik, undangan pembicara, booking venue, promosi, pelaksanaan acara, pengumpulan feedback |
| **Respon KLB** | Investigasi kasus, tracing kontak, tindakan karantina, edukasi masyarakat, monitoring & evaluasi |

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

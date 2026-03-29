# Referensi Cepat: Rumus Google Sheets untuk Gantt Chart

## Rumus Durasi
```
=Sel Tanggal Selesai - Sel Tanggal Mulai
```
Contoh: `=C2-B2`

## Rumus Conditional Formatting (Metode Grid)
```
=AND(Sel Tanggal Header >= Sel Tanggal Mulai, Sel Tanggal Header <= Sel Tanggal Selesai)
```
Contoh: `=AND(F$1>=$B2, F$1<=$C2)`

### Penjelasan Rumus:
- `F$1` = Tanggal di baris header (referensi absolut untuk baris)
- `$B2` = Tanggal mulai untuk kegiatan ini (referensi absolut untuk kolom)
- `$C2` = Tanggal selesai untuk kegiatan ini (referensi absolut untuk kolom)
- `AND()` = Memeriksa apakah tanggal header berada dalam rentang tanggal kegiatan

## Rumus Kenaikan Tanggal (untuk header timeline)
```
=Sel Sebelumnya + 1
```
Contoh: Di sel G1: `=F1+1`

## Tips
- Gunakan `$` untuk mengunci baris atau kolom saat menarik rumus
- Format tanggal konsisten: Pilih sel → Format → Number → Date
- Untuk menampilkan hanya hari kerja, gunakan rumus yang lebih kompleks atau lewati akhir pekan secara manual

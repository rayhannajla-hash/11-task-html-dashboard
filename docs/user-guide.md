# Panduan Penggunaan Task.html untuk Tim

## Mulai Pakai (1 menit)

1. Copy `task.html` ke laptop kamu (boleh via flashdisk/email/chat).
2. Double-click → terbuka di browser (Chrome/Edge/Firefox).
3. Klik **➕ Tambah Task**, isi nama, PIC, prioritas, deadline, status.
4. Selesai — data otomatis tersimpan di browser (localStorage).

> Koneksi internet hanya dibutuhkan saat pertama kali buka (untuk load Alpine.js & Tailwind dari CDN). Setelah itu bisa offline selama tab/cache browser masih ada.

## Fitur Harian

| Aksi | Cara |
|------|------|
| Tandai selesai | Centang checkbox di kiri task |
| Edit task | Klik ✏️ |
| Hapus task | Klik 🗑️ (ada konfirmasi) |
| Filter | Dropdown PIC / Status / Prioritas di atas daftar |
| Urutkan | Dropdown "Urutkan": deadline terdekat, prioritas, nama |

**Arti warna:**
- 🔴 Garis merah di kiri kartu = **overdue** (lewat deadline, belum selesai)
- Badge prioritas: merah = Tinggi, kuning = Sedang, abu = Rendah
- Badge status: abu = Belum mulai, biru = Dikerjakan, ungu = Review, hijau = Selesai

## Kerja Tim: Export / Import

Data tersimpan **per browser per laptop**. Untuk berbagi antar anggota:

```
Anggota A : kerja → klik 💾 Export → kirim file task-export-YYYY-MM-DD.json
Anggota B : klik 📥 Import → pilih file → pilih GABUNG
Team Lead : import file dari semua anggota (mode GABUNG) → lihat big picture
```

**Mode import:**
- **GABUNG** (klik OK) — task baru ditambahkan, task yang sudah ada tidak diduplikasi (dicocokkan via ID).
- **TIMPA** (klik Cancel) — semua data sekarang diganti isi file.

⚠️ **Backup rutin:** localStorage bisa hilang jika browser di-clear oleh IT. Export JSON minimal seminggu sekali.

## Column Mapping (⚙️ Settings)

Sesuaikan istilah dengan tim kamu:
- "Task" → misalnya "Desain" / "Order" / "Drawing"
- "PIC" → misalnya "Operator" / "Drafter"

Label berubah di seluruh UI termasuk tombol dan KPI.

## Troubleshooting

| Masalah | Solusi |
|---------|--------|
| Data hilang setelah clear browser | Restore dari file export JSON terakhir |
| Import gagal | Pastikan file berasal dari Task.html (ada field `tasks`) |
| Halaman kosong/putih | Buka pertama kali butuh internet (CDN); cek koneksi lalu refresh |
| Tidak jalan di Internet Explorer | Gunakan Chrome, Edge, atau Firefox |

# ✅ Task.html — Team Task Dashboard

> Dashboard manajemen tugas tim berbasis Alpine.js dalam satu file HTML — dirancang khusus untuk lingkungan dengan IT restrictions ketat.

![Status](https://img.shields.io/badge/status-done-brightgreen)
![Type](https://img.shields.io/badge/type-Single%20File%20HTML-orange)
![Framework](https://img.shields.io/badge/framework-Alpine.js-8BC0D0)
![Install](https://img.shields.io/badge/install-none%20required-blue)

---

## 🎯 Latar Belakang

Tim desainer touch panel membutuhkan cara tracking task yang:
- **Tidak butuh install** — IT restrictions melarang install software baru
- **Tidak butuh server** — tidak ada akses ke internet di area produksi
- **Mudah dipakai** — tim tidak terlalu technical
- **Bisa di-share** — export/import data antar anggota tim

Solusi: satu file HTML yang bisa di-copy ke flashdisk dan dijalankan di browser mana saja.

---

## ✨ Fitur

### KPI Cards (Real-time)
- 📊 Total task
- ✅ Selesai hari ini
- 🔄 Sedang dikerjakan
- ⚠️ Overdue (lewat deadline)
- 📈 Completion rate %

### Manajemen Task
- ➕ Tambah task baru (nama, PIC, prioritas, deadline, status)
- ✏️ Edit task inline
- 🗑️ Hapus task dengan konfirmasi
- 🔍 Filter: by PIC, status, prioritas
- 🔤 Sort: by deadline, prioritas, nama

### Data Management
- 💾 **Export JSON** — backup data ke file
- 📥 **Import JSON** — restore dari backup
- 🗺️ **Column mapping** — sesuaikan kolom dengan kebutuhan tim
- 💻 localStorage — data tersimpan di browser, tidak hilang walau di-refresh

### UI/UX
- 📱 Responsive — bisa dipakai di HP
- 🎨 Color coding: prioritas dan status
- 🔔 Visual alert untuk task overdue
- 📅 Relative date display ("3 hari lagi", "Kemarin")

---

## 🚀 Cara Pakai

1. **Download** `task.html`
2. **Double-click** — langsung terbuka di browser
3. **Tambah task** pertama kamu
4. **Export** secara berkala untuk backup
5. **Share** file JSON ke anggota tim lain — mereka bisa import

### Untuk Tim
```
Anggota A: Kerja → Export task.json
Anggota B: Import task.json → Lihat progress → Export lagi
Team Lead: Import dari semua anggota untuk lihat big picture
```

---

## ⚙️ Konfigurasi Column Mapping

Task.html mendukung kustomisasi kolom sesuai kebutuhan tim. Klik ⚙️ Settings untuk mengubah:
- Label kolom (misal "PIC" → "Operator", "Task" → "Desain")
- Field yang ditampilkan / disembunyikan
- Format tanggal

---

## 🔧 Troubleshooting

| Masalah | Solusi |
|---------|--------|
| Data hilang setelah close browser | Export JSON dulu sebelum close; data di localStorage bisa terhapus jika clear browser data |
| Import gagal | Pastikan file JSON dari Task.html yang sama (format harus cocok) |
| Tidak bisa buka di Internet Explorer | Gunakan Chrome, Firefox, atau Edge |
| Filter tidak berfungsi | Refresh halaman (Ctrl+R) |

---

## 📁 Struktur Repo

```
11-task-html-dashboard/
├── README.md
├── task.html          # Aplikasi utama (single file)
└── docs/
    └── user-guide.md  # Panduan penggunaan untuk tim
```

---

## 🔗 Teknologi

- [Alpine.js](https://alpinejs.dev) — reactive UI framework ringan (di-load dari CDN)
- [Tailwind CSS](https://tailwindcss.com) — utility-first CSS (CDN)
- Web localStorage API — penyimpanan data lokal

> **Offline ready:** Setelah load pertama (perlu internet untuk Alpine.js & Tailwind CDN), app bisa dipakai offline. Untuk fully offline, bisa embed library langsung ke file HTML.

---

*Part of [Budhi's AI Engineer Portfolio](https://github.com/budhi/ai-portfolio)*

# ⚡ Neo-Brutalism Theme for SLiMS (Senayan Library Management System)

Tema OPAC modern berbasis filosofi desain **Neo-Brutalism** untuk **SLiMS 9 Bulian**. Menggabungkan tipografi tebal, kontras tinggi, palet warna *retro-cyberpunk*, bayangan tegas (*hard drop-shadow*), dan elemen interaktif yang dirancang untuk memberikan pengalaman katalog perpustakaan yang unik, dinamis, dan tidak membosankan.

---

## 🎨 Karakteristik & Filosofi Desain

- **Garis & Batas Kontras Tinggi**: Bingkai border hitam pekat (*solid black 3px - 4px*) di seluruh kartu, tombol, dan modul.
- **Hard Solid Shadows**: Efek bayangan tegas tanpa blur (`box-shadow: 5px 5px 0 #000`, `8px 8px 0 #000`) dengan animasi micro-interaction saat di-hover atau di-klik.
- **Vibrant Accent Palette**:
  - 🟡 **Cyber Yellow** (`#FFE600`)
  - 🔴 **Electric Pink** (`#FF2E93` / `#FF0055`)
  - 🔵 **Vivid Cyan** (`#00F0FF`)
  - ⚫ **Deep Jet Black** (`#0a0a0a`)
  - ⚪ **Crisp White / Off-White** (`#FFFFFF` / `#F8F9FA`)
- **Retro Badges & Stickers**: Stiker dekoratif bertema arsip digital dan keterbukaan informasi (*Open Access*).
- **Mobile Responsive & Accessible**: Layout adaptif yang tetap proporsional dan mudah dibaca di layar smartphone, tablet, maupun desktop.

---

## 🚀 Fitur Unggulan

### 1. 🔄 Infinite Running Marquee Banner
Running text bergaya retro billboard di bagian atas beranda:
- **Pause on Hover**: Animasi otomatis berhenti saat kursor mouse diarahkan, memudahkan pengunjung membaca dan mengeklik tautan.
- **Sumber Data Dinamis Terintegrasi Database**:
  - 📚 **Data Buku / Koleksi Terbaru** (`biblio_new`): Menampilkan judul koleksi buku terbaru dari database, lengkap dengan badge `BUKU BARU` dan tautan langsung ke halaman detail buku.
  - 📢 **Data Berita / Informasi Terbaru** (`news`): Menampilkan rilis berita dan pengumuman perpustakaan dari modul konten SLiMS.
  - 🔥 **Data Koleksi Terpopuler** (`biblio_popular`): Menampilkan buku yang paling sering dipinjam oleh pemustaka.
  - ★ **Slogan Brutalist & Filosofi SLiMS** (`slogan`): Slogan bawaan tema.
  - ✏️ **Teks Kustom Manual** (`custom`): Input teks manual yang dipisahkan dengan tanda pipe `|` tanpa perlu mengetik tag HTML mentah.
- **Batas Jumlah Data**: Dapat diatur jumlah data yang ingin ditampilkan (misal: 5, 8, atau 10 item).

### 2. 📢 Brutalist Hero Billboard & Stickers
- **Stiker Dinamis**: Stiker tag bergaya retro (`brutal-sticker-yellow`, `pink`, `cyan`) yang dapat dikustomisasi dengan pemisah `|`.
- **Judul Utama & Kata Sorotan**: Teks utama dengan efek sorotan garis bawah tebal (*thick yellow underline*).
- **Deskripsi Subtitle**: Pesan sambutan perpustakaan yang dapat diedit langsung dari form admin.
- **Toggle Tampilkan/Sembunyikan**: Hero billboard dapat diaktifkan atau dinonaktifkan sesuai kebutuhan.

### 3. 🔍 Search Bar & Quick Filter Brutalist
- Input pencarian berbingkai tebal dengan tombol aksi kontras tinggi.
- Filter pencarian cepat untuk mempermudah pencarian berdasarkan judul, pengarang, subjek, atau ISBN.
- Modal pencarian spesifik / lanjut (*Advanced Search*) dengan opsi filter lengkap.

### 4. 📖 Katalog & Tampilan Hasil Pencarian (Biblio List)
- Desain kartu koleksi yang rapi dengan indikator ketersediaan (*Availability Badge*) yang responsif tanpa teks terpotong (*no offside label*).
- Tombol aksi cepat:
  - 📄 **Detail Koleksi**: Membuka rincian data bibliografi lengkap.
  - 📑 **Sitasi (Citation)**: Generator kutipan otomatis format APA, Chicago, dan MLA.
  - 🏷️ **Nomor Panggil (Call Number)**: Menampilkan lokasi dan kode klasifikasi buku di rak.

### 5. 🔐 Halaman Khusus & Modul Terpadu
- **Area Anggota (Member Area)**: Dashboard login dan riwayat peminjaman pemustaka dengan sentuhan brutalist.
- **Login Pustakawan (Librarian Login)**: Halaman login pustakawan yang rapi, ringkas, dan proporsional.
- **Buku Tamu (Visitor Counter)**: Halaman presensi pengunjung perpustakaan dengan dukungan input nomor anggota dan mode tamu.

---

## 📂 Struktur Direktori Tema

```text
template/brutalism/
├── assets/
│   ├── css/
│   │   └── style.css            # Styling utama tema Neo-Brutalism
│   ├── js/                      # Script interaksi dan pendukung
│   └── images/                  # Aset gambar, ikon, dan logo
├── parts/
│   ├── _home.php                # Layout beranda (Hero, Marquee, Koleksi)
│   ├── _navbar.php              # Navigasi atas dan menu tema
│   ├── _search-form.php         # Form pencarian utama
│   ├── _result-search.php       # Layout daftar hasil pencarian OPAC
│   ├── _member.php              # Layout area anggota
│   ├── _other.php               # Layout konten statis & login librarian
│   ├── _modal_advanced.php      # Modal pencarian lanjutan
│   ├── _modal_topic.php         # Modal topik / subjek populer
│   ├── header.php               # HTML head, meta tag, dan load asset
│   └── footer.php               # Footer tema dan informasi perpustakaan
├── biblio_list_template.php     # Template tampilan kartu koleksi
├── classic.php                  # Helper functions (query biblio, berita, dll)
├── detail_template.php          # Template halaman detail buku
├── index_template.inc.php       # Router utama OPAC tema
├── news_template.php            # Template kartu berita
├── preview.png                  # Gambar thumbnail tema di panel admin
├── tinfo.inc.php                # Konfigurasi opsi tema di admin SLiMS
└── visitor_template.php         # Template modul buku tamu
```

---

## ⚙️ Cara Instalasi & Aktivasi

1. **Pastikan Folder Tema Terpasang**:
   Letakkan folder `brutalism` ke dalam direktori:
   ```text
   slims/template/brutalism
   ```

2. **Aktivasi Tema di Admin SLiMS**:
   - Buka menu **Sistem (System)** > **Tema (Theme)**.
   - Pada daftar tema publik, cari **Brutalism**.
   - Klik tombol **Aktifkan (Activate)**.

---

## 🛠️ Panduan Kustomisasi Tema

Anda dapat mengelola tampilan tema langsung tanpa mengubah file kode:

1. Masuk ke **Admin SLiMS** > **Sistem** > **Tema**.
2. Klik tombol **Kustomisasi (Customize)** pada tema **Brutalism**.
3. Beberapa pengaturan yang tersedia:
   - **Marquee Running Text**:
     - *Enable Marquee*: Tampilkan atau sembunyikan running text.
     - *Marquee Source*: Pilih antara Buku Terbaru, Berita Terbaru, Buku Terpopuler, Slogan Preset, atau Teks Kustom.
     - *Marquee Items Count*: Jumlah data yang ingin ditampilkan (misal: `10`).
     - *Custom Text*: Jika memilih teks kustom, tulis kalimat dipisahkan tanda `|`.
   - **Hero Billboard**:
     - *Tampilkan Hero Billboard*: Tampilkan atau sembunyikan hero section.
     - *Hero Stickers*: Daftar stiker dipisahkan dengan tanda `|` (contoh: `★ OPAC DIGITAL | ✦ PERPUSTAKAAN MERDEKA`).
     - *Judul Utama*: Teks judul billboard utama.
     - *Kata Sorotan*: Kata dengan aksen garis bawah kuning tebal.
     - *Deskripsi Subtitle*: Ringkasan informasi perpustakaan.
   - **Koleksi & Pustaka**:
     - Pengaturan jumlah koleksi populer, koleksi terbaru, top reader, dan peta lokasi perpustakaan.
   - **Tautan Media Sosial**:
     - Link Facebook, Twitter, Instagram, dan YouTube perpustakaan.
4. Klik **Simpan Pengaturan (Save Settings)**, lalu muat ulang (*refresh*) halaman depan OPAC.


## 📋 Kompatibilitas Sistem

- **SLiMS Version**: Tested on SLiMS 9.8 (Bulian D Roger).
- **PHP Version**: PHP 8.2+.
- **Database**: MySQL 5.7+ / MariaDB 10.3+.
- **Browser Support**: Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, Opera (Desktop & Mobile).

## Preiew Interface
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/7716ef0c-c427-453d-9f7f-2d68b56e8c5e" />
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/b3fa93d4-3f9b-4db3-b3ff-7c45943a1290" />
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/f5e66b44-ac26-42f0-921c-c56d1458cedb" />
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/8270bba4-a82c-47cf-8e28-5dc422b6c9e2" />
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/0d8ed45f-ff6d-4fba-897e-8a8acb29a11f" />
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/ac51a870-5a34-4f95-a2a5-8cc7af0cc26d" />
<img width="1908" height="952" alt="image" src="https://github.com/user-attachments/assets/142e87d4-43a6-4fba-a5d7-0e07fc12b3d7" />









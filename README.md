# Ruang Baca Kampus

Website statis sederhana untuk memperkenalkan perpustakaan komunitas mahasiswa
“Ruang Baca”. Halaman ini menyediakan informasi singkat mengenai perpustakaan,
layanan yang tersedia, galeri ruangan, dan informasi kontak.

## Fitur

- Navigasi anchor ke bagian Tentang, Layanan, Galeri, dan Kontak.
- Section informasi tentang Ruang Baca Kampus.
- Tiga kartu layanan:
  - Peminjaman Buku
  - Ruang Diskusi
  - Klub Baca
- Galeri dengan tiga gambar ruangan perpustakaan.
- Footer berisi identitas, deskripsi, alamat, email, dan jam operasional.
- Layout responsif untuk desktop dan perangkat dengan lebar layar maksimal 800px.
- Smooth scrolling saat berpindah ke section melalui navigasi.

## Teknologi

- HTML5
- Tailwind CSS v4 melalui Tailwind Play CDN
- Gambar JPG

Project ini tidak menggunakan JavaScript aplikasi, framework frontend, atau
backend. Tailwind dimuat langsung dari CDN sehingga project dapat dijalankan
tanpa proses build dan tanpa instalasi dependency lokal.

## Struktur Project

```text
Layout-web-sederhana/
├── index.html
├── style.css
├── README.md
└── img/
    ├── libarary-1.jpg
    ├── libarary-2.jpg
    └── libarary-3.jpg
```

## Cara Menjalankan

1. Clone atau download repository.
2. Buka folder project.
3. Buka file `index.html` di browser.

Alternatifnya, jalankan server lokal menggunakan extension Live Server di VS
Code, lalu buka halaman yang tersedia di browser.

Karena Tailwind digunakan melalui CDN, koneksi internet diperlukan saat halaman
pertama kali dimuat agar utility class dapat diproses oleh browser.

## Perubahan Styling ke Tailwind

Sebelumnya, styling halaman didefinisikan menggunakan selector CSS seperti
`.card`, `.photo`, `.section-inner`, dan aturan `@media` di `style.css`.

Styling kini dipindahkan ke utility class Tailwind yang ditulis langsung pada
elemen HTML di `index.html`. Perubahan utamanya meliputi:

- Layout flex dan grid menggunakan `flex`, `grid`, `grid-cols-3`, dan `gap-*`.
- Spacing menggunakan `p-*`, `px-*`, `py-*`, `m-*`, dan `gap-*`.
- Warna menggunakan utility dengan nilai warna custom, misalnya
  `bg-[#1e3a5f]` dan `text-[#f59e0b]`.
- Ukuran, border, radius, dan gambar menggunakan `size-*`, `border-*`,
  `rounded-*`, `overflow-hidden`, dan `object-cover`.
- Responsive layout menggunakan variant `max-[800px]:*`.
- Smooth scrolling menggunakan class `scroll-smooth` pada elemen `<html>`.

File `style.css` dipertahankan sebagai file pendamping, tetapi tidak lagi
menyimpan aturan styling halaman. Styling utama sekarang berada di
`index.html`.

## Catatan

- Nama file gambar mengikuti file yang tersedia di folder `img`.
- Atribut `alt` digunakan pada setiap gambar untuk membantu aksesibilitas.
- Jika desain ingin dikembangkan untuk production, Tailwind dapat dipindahkan
  dari Play CDN ke konfigurasi Tailwind lokal dengan proses build.

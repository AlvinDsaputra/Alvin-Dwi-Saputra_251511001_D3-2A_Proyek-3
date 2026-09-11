# Mini Project: Landing Page Lokakarya Web Dasar

Nama : Alvin Dwi Saputra
NIM  : 251511001
Kelas: D3 Teknik Informatika

1. RINGKASAN HALAMAN
Landing page ini dirancang untuk memfasilitasi pendaftaran Lokakarya Web Dasar D3 Teknik Informatika. Halaman dibangun memakai HTML5 semantik dan CSS3 murni dengan pendekatan mobile-first tanpa framework.

2. TIGA KEPUTUSAN TEKNIS
- Pendekatan Mobile-First: CSS dasar ditulis untuk layar HP (320px), lalu disesuaikan ke desktop menggunakan media query (@media (min-width: 768px)).
- Layout Fleksibel dengan Flexbox: Menggunakan display: flex dan flex-wrap: wrap pada kartu fitur agar tata letak menyesuaikan lebar layar secara otomatis.
- Design Tokens (:root): Variabel warna dan spacing dipusatkan pada Custom Properties di :root agar konsisten dan mudah diubah.

3. MASALAH, DIAGNOSIS, DAN PERBAIKAN
- Masalah 1: Form input melebihi lebar layar HP (overflow di 320px).
  * Diagnosis: Belum ada perhitungan box-sizing yang tepat pada elemen input.
  * Perbaikan: Menambahkan box-sizing: border-box dan max-width: 100% di CSS.

- Masalah 2: Indikator fokus tombol Tab terpotong di tepi elemen.
  * Diagnosis: Kurangnya jarak luar (offset) pada garis penanda fokus.
  * Perbaikan: Menambahkan aturan :focus-visible dengan outline-offset: 2px.

4. PENGUJIAN VIEWPORT & AKSESIBILITAS
- Layar 320px (HP Kecil)  : Layout 1 kolom, rapi, bebas overflow.
- Layar 375px (HP Sedang) : Layout 1 kolom, rapi, bebas overflow.
- Layar 768px (Tablet)    : Layout 2 kolom (Hero), bebas overflow.
- Layar 1024px (Desktop)  : Layout terpusat (max-width 1120px), bebas overflow.
- Navigasi Keyboard (Tab) : Garis fokus terlihat jelas dan tidak terpotong.

5. STRUKTUR FOLDER PROYEK
modul1_NIM_Nama/
├── index.html
├── css/
│   └── style.css
├── assets/
│   └── hero-web.jpg
├── README.md
└── evidence/
    ├── 320px.png
    ├── 375px.png
    ├── 768px.png
    ├── 1024px.png
    └── focus.png

6. REFLEKSI BELAJAR
Melalui project ini, saya memahami pentingnya tag HTML semantik (header, main, section, footer) serta penggunaan CSS Flexbox dan Box Model untuk membuat tampilan web yang responsif dan nyaman diakses.

7. LOG PENGGUNAAN AI
- Fase HTML : Diskusi pemilihan tag semantik dan struktur dokumen.
- Fase CSS  : Diskusi sintaks Flexbox untuk kartu fitur responsif.
- Fase Debug: Diskusi penanganan overflow 320px dan indikator :focus-visible.
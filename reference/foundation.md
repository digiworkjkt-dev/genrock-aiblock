# Fondasi Genrock Industrial

## DNA tetap dan adaptasi

Tetap: IBM Plex Sans, neutral hangat, hijau hutan sebagai accent utama, permukaan solid, border sebagai struktur, radius kontrol 4px, copy spesifik.

Adaptif: layout, navigasi, kepadatan, jumlah kolom, ukuran bacaan, visualisasi data, dan platform.

Jangan memakai setiap elemen signature pada setiap layar. Keunikan Genrock datang dari kualitas dan proporsi yang konsisten, bukan dekorasi berulang.

## Tipografi

Muat IBM Plex Sans weight 400, 500, 600 dari distribusi resmi dengan lisensi sesuai penggunaan. Untuk self-host, gunakan WOFF2 bila tersedia dan sertakan lisensi distribusi. `font-display: swap`; preload hanya aset kritis. Cek glyph bahasa, font fallback, dan layout shift.

Fallback: `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.
IBM Plex Mono opsional untuk kode, bukan seluruh UI. Angka tabel memakai `tabular-nums`.

| Peran | Ukuran awal | Weight | Line-height |
|---|---|---|---|
| Metadata sekunder | 0.75rem / 12px | 400 | 1.5 |
| Body UI compact | 0.875rem / 14px | 400 | 1.5 |
| Body, form, bacaan | 1rem / 16px | 400 | 1.6 |
| Label kontrol | 0.875–1rem | 500 | 1.5 |
| Subheading | 1.25rem / 20px | 600 | 1.4 |
| Section title | 1.5rem / 24px | 600 | 1.333 |
| Page title | 2rem / 32px | 600 | 1.25 |

Konversi px mengasumsikan root 16px; jangan mengunci ukuran root browser. Teks 12px hanya metadata, bukan instruksi, error, atau teks utama. Default comfortable 16px; compact 14px hanya saat volume informasi dan konteks penggunaan membenarkannya. Mockup eksplorasi dengan teks kecil bukan standar produksi.

Heading besar untuk marketing boleh fluid 32–48px, jangan membuat judul dashboard 80px. Heading semantik mengikuti struktur. Tracking body normal; heading boleh hingga -0.025em setelah inspeksi. Uppercase hanya label pendek yang relevan, bukan semua heading.

## Palette light

| Token | Nilai | Penggunaan |
|---|---|---|
| Canvas | `#f5f5f0` | Background aplikasi |
| Surface | `#ffffff` | Area kerja, dialog |
| Ink | `#212622` | Teks utama |
| Muted | `#626a63` | Teks sekunder |
| Border | `#d3d8d0` | Pemisah non-esensial |
| Control border | `#7a857b` | Batas input jika diperlukan untuk identifikasi |
| Accent | `#2c503c` | Aksi utama, selected state |
| Accent hover | `#23402f` | Hover aksi utama |
| Accent subtle | `#eaf0e7` | Selected/background penunjang |
| Danger | `#a12b2b` | Error/destructive |
| Warning ink | `#775000` | Peringatan |
| Focus | `#164a70` | Ring focus light |

Ini default brand, bukan audit otomatis semua pasangan. Ukur foreground terhadap background sebenarnya; hindari opacity pada teks penting. Accent bukan warna seluruh ikon, badge, dan heading. Semantic color boleh di luar palette brand, dengan teks/ikon selain warna.

Untuk chart, kategori dapat memerlukan warna tambahan; prioritaskan diskriminasi kategori, label, dan aksesibilitas. Tidak ada batas warna yang mengorbankan makna data.

## Permukaan dan bentuk

- Background solid. No gradient, blur, glow, noise, atau grid dekoratif sebagai default.
- Border 1px. Border pemisah halus tidak cukup untuk semua kontrol; pakai control border/fill yang dapat diidentifikasi.
- Kontrol dan panel standar 4px. Dialog besar boleh 8px. Avatar boleh lingkaran. Pil bukan default untuk tombol, input, dan cards.
- Shadow hanya elevation yang dibutuhkan, misalnya menu atau dialog; bukan pada seluruh panel.
- Spacing: 4, 8, 12, 16, 24, 32, 48, 64px. Gunakan 8–12 untuk hubungan dekat, 16–24 untuk grup, 32+ untuk bagian besar. Rhythm mengikuti hubungan konten, tidak harus jarak identik.

## Density dan komposisi

Comfortable: default untuk pengguna baru, mobile, booking, formulir, dan layanan.
Compact: pengguna rutin yang perlu scanning data cepat; jangan mengecilkan semua teks untuk memuat lebih banyak.

Utamakan ruang putih, alignment, dan heading sebelum menambah kotak. List dan tabel lebih tepat daripada card grid untuk data yang dibandingkan. Cards cocok untuk entitas yang independen atau kelompok yang jelas.

## Ikon dan motion

Gunakan satu keluarga ikon existing, umumnya ukuran 16–20px, stroke konsisten. Ikon fungsi bukan pengisi ruang; tombol icon-only perlu accessible name.

Feedback singkat sekitar 120–180ms. Jangan menerapkan reveal pada semua elemen atau membuat konten tersembunyi ketika JavaScript gagal. Hormati `prefers-reduced-motion`; hindari bounce, floating, parallax default.

## Theme

Light adalah default Genrock; jangan menambah toggle hanya karena template punya.
Dark diterapkan bila diminta atau kebutuhan produk membenarkan, lewat token semantik. Semua theme yang dikirim harus diverifikasi.

Starter dark: canvas `#171d19`, surface `#202922`, ink `#f0f3ed`, muted `#b4c0b3`, accent `#b9d6b4`, on-accent `#172b1a`, border `#455247`, control border `#839280`, focus `#b9d6b4`.

Jangan membalik warna mentah atau menggunakan accent light dengan teks putih untuk tombol dark. State hover, status, disabled, dan overlay memerlukan pasangan tersendiri serta pengujian.

## Native

Pertahankan DNA, tetapi ikuti konvensi iOS/Android, font scaling, safe area, dan target sentuh platform. Gunakan token numerik untuk React Native, bukan CSS rem/clamp. Muat Plex melalui mekanisme native existing. Jangan memaksakan desktop navbar atau tabel lebar ke layar ponsel.
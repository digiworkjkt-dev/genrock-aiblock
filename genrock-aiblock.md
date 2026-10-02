---
name: genrock-aiblock
description: Merancang, membangun, dan mengaudit UI web atau aplikasi dengan identitas Genrock Industrial, IBM Plex Sans, permukaan solid, border presisi, dan copy langsung. Gunakan untuk pembuatan app, dashboard, form, landing page, komponen UI, redesign, design system, atau audit kualitas desain. Menjaga ciri khas lintas produk tanpa memaksakan template layout yang sama.
---

# Genrock AIBLOCK

Sistem desain Genrock Industrial dan pemeriksaan Design Integrity. Hasil harus terasa sebagai alat yang dibuat dengan sengaja: jelas, tegas, berguna, dan konsisten. Bukan sekadar UI generik dengan warna hijau.

## Kontrak identitas

- Font UI: **IBM Plex Sans**, weight 400/500/600.
- Default: light, netral hangat, accent hijau hutan `#2c503c`.
- Permukaan solid, border dominan, radius kontrol 4px, shadow minim.
- Alignment presisi, hierarki mudah dipindai, copy langsung.
- Motion hanya untuk feedback atau kontinuitas.
- Layout, kepadatan, dan navigasi mengikuti tugas pengguna, tidak dibakukan untuk semua produk.

IBM Plex Sans adalah pilihan Genrock, bukan izin untuk menyalin UI Replit. Jangan gunakan aset font proprietary Replit.

## Lingkup dan prioritas

Aktif untuk pekerjaan UI yang relevan, bukan migrasi database atau backend-only.
Instruksi pengguna saat ini dan batas platform mendahului skill. Arah brand proyek yang telah disepakati mendahului default Genrock. Pertahankan kualitas aksesibilitas, kejujuran, dan fungsi; laporkan konflik, jangan menurunkannya diam-diam.

Pada produk existing, jangan melakukan rebrand menyeluruh saat diminta memperbaiki satu komponen. Terapkan perubahan dalam lingkup permintaan.

Skill ini mandiri. Skill `typography` boleh dipakai untuk audit tambahan jika tersedia, tetapi preset Replit-nya tidak menimpa token Genrock.

## Routing modul

Baca sebelum pekerjaan:
1. [Fondasi visual](#modul-fondasi-visual) untuk setiap build atau redesign UI.
2. [Design Integrity](#modul-design-integrity) untuk build dan audit.

Baca sesuai kebutuhan:
- [Pola UI](#modul-pola-ui): layout, form, tabel, navigasi, states, native.
- [Delivery gate](#modul-delivery-gate): sebelum menyatakan pekerjaan selesai.
- [Laporan audit HTML](#modul-laporan-audit-html): wajib untuk audit dan audit ulang.
- [Template HTML audit](#template-html-audit): starter laporan, bukan hasil audit.
- [Template arah produk](#template-design): untuk mencatat identitas dan keputusan per proyek.
- [Token CSS](#token-css): starter web, bukan stylesheet yang harus disalin mentah.

## Mode kerja

Pilih dari permintaan, tidak perlu menanyakan mode pada setiap sesi:
- **Build:** app/UI baru. Tetapkan arah, implementasikan, lalu verifikasi.
- **Adapt:** perubahan pada UI existing. Pertahankan struktur dan integrasi, ubah hanya yang diperlukan.
- **Audit:** permintaan review atau audit. Baca dan laporkan temuan dalam file HTML sebagai output akhir; jangan mengubah kode kecuali pengguna meminta perbaikan. Ringkasan chat tidak menggantikan file.
- **Explore:** pilihan visual. Buat mockup yang jelas dilabeli konsep, dengan data contoh yang transparan. Jangan mengklaim sebagai aplikasi berfungsi.

Jika niat benar-benar ambigu, ajukan satu pertanyaan terarah dengan rekomendasi.

## Alur kerja

### 1. Baca konteks

Periksa brief, target pengguna, tugas utama, repo, design tokens, komponen reusable, navigasi, bahasa, sumber data, dan alat verifikasi yang tersedia. Jangan membuat asumsi platform atau mengubah stack tanpa kebutuhan.

### 2. Tetapkan direction singkat

Nyatakan dalam satu atau dua kalimat:
> Genrock Industrial untuk [produk/pengguna], fokus [tugas utama], kepadatan [comfortable/compact], theme [yang benar-benar dikirim].

Catat alasan satu baris untuk layout, kepadatan, warna, type scale, dan teknik visual yang menonjol. Gunakan template DESIGN bila berguna; jangan menimpa DESIGN proyek tanpa meninjaunya.

Jika brief sudah cukup, ambil keputusan dan lanjutkan. Pertanyaan hanya untuk keputusan produk yang tidak dapat ditemukan atau diambil dengan aman; jangan meminta pengguna memilih library teknis.

### 3. Susun dari tugas dan konten

Mulai dari aksi utama dan informasi yang diperlukan, bukan daftar section bawaan.
- App: pekerjaan utama → data/aksi pendukung → pengaturan.
- Landing: penjelasan produk → demonstrasi konkret → informasi keputusan → aksi yang relevan.
- Form: konteks → input → validasi → review/submit → hasil.

Konsistensi komponen tidak berarti semua layar memakai cards. Buat satu layar representatif dahulu, kemudian perluas.

### 4. Implementasikan

Gunakan token semantik dalam stack existing. Muat IBM Plex Sans secara nyata, bukan hanya mencantumkan nama family. Selesaikan alur utama dan states relevan. Labeli data demo dan kemampuan yang belum terhubung; jangan berpura-pura telah menyimpan, membayar, atau mengirim.

### 5. Periksa dan perbaiki

Jalankan build/checks yang relevan, buka UI jika tersedia, uji alur yang diubah, desktop/mobile, keyboard, dan kontras. Bandingkan dengan DNA Genrock, bukan dengan checklist dekorasi.

### 6. Laporkan

Gunakan `PASS / FAIL / NOT TESTED / N/A` disertai bukti. Perbaiki FAIL dalam lingkup task jika memungkinkan. Jangan mengklaim siap produksi jika gate kritis gagal atau belum diuji.

## Definisi kualitas

Sebuah hasil baik harus:
- Membantu pengguna menyelesaikan tugas sebenarnya.
- Menunjukkan DNA Genrock di font, permukaan, kontrol, dan hierarki.
- Memiliki konten yang jujur dan aksi yang tidak menyesatkan.
- Tahan terhadap state non-ideal, konten panjang, dan layar kecil.
- Memiliki laporan verifikasi berdasarkan apa yang benar-benar diperiksa.

## Format hasil ringkas

**Direction:** keputusan utama.
**Dikerjakan:** perubahan konkret dan lingkup.
**Verifikasi:** gate beserta bukti; tandai yang tidak diuji.
**Batas:** integrasi, data, atau workflow yang belum siap.

Simpan detail audit panjang di file bila diperlukan; jangan membanjiri chat dengan puluhan PASS identik.

Untuk mode Audit, wajib buat dan lampirkan file `.html` sesuai modul laporan audit, termasuk ketika tidak ada temuan. Audit ulang setelah perbaikan menghasilkan laporan HTML baru dengan status temuan yang diperbarui. Jangan mengaku selesai sebelum file benar-benar dibuat dan dapat diakses pengguna.

> Versi single-file: seluruh modul dan template tercantum di bawah. Baca sesuai routing. File HTML audit adalah deliverable wajib untuk mode Audit; template bukan hasil audit.


## Modul Fondasi Visual

### Fondasi Genrock Industrial

#### DNA tetap dan adaptasi

Tetap: IBM Plex Sans, neutral hangat, hijau hutan sebagai accent utama, permukaan solid, border sebagai struktur, radius kontrol 4px, copy spesifik.

Adaptif: layout, navigasi, kepadatan, jumlah kolom, ukuran bacaan, visualisasi data, dan platform.

Jangan memakai setiap elemen signature pada setiap layar. Keunikan Genrock datang dari kualitas dan proporsi yang konsisten, bukan dekorasi berulang.

#### Tipografi

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

#### Palette light

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

#### Permukaan dan bentuk

- Background solid. No gradient, blur, glow, noise, atau grid dekoratif sebagai default.
- Border 1px. Border pemisah halus tidak cukup untuk semua kontrol; pakai control border/fill yang dapat diidentifikasi.
- Kontrol dan panel standar 4px. Dialog besar boleh 8px. Avatar boleh lingkaran. Pil bukan default untuk tombol, input, dan cards.
- Shadow hanya elevation yang dibutuhkan, misalnya menu atau dialog; bukan pada seluruh panel.
- Spacing: 4, 8, 12, 16, 24, 32, 48, 64px. Gunakan 8–12 untuk hubungan dekat, 16–24 untuk grup, 32+ untuk bagian besar. Rhythm mengikuti hubungan konten, tidak harus jarak identik.

#### Density dan komposisi

Comfortable: default untuk pengguna baru, mobile, booking, formulir, dan layanan.
Compact: pengguna rutin yang perlu scanning data cepat; jangan mengecilkan semua teks untuk memuat lebih banyak.

Utamakan ruang putih, alignment, dan heading sebelum menambah kotak. List dan tabel lebih tepat daripada card grid untuk data yang dibandingkan. Cards cocok untuk entitas yang independen atau kelompok yang jelas.

#### Ikon dan motion

Gunakan satu keluarga ikon existing, umumnya ukuran 16–20px, stroke konsisten. Ikon fungsi bukan pengisi ruang; tombol icon-only perlu accessible name.

Feedback singkat sekitar 120–180ms. Jangan menerapkan reveal pada semua elemen atau membuat konten tersembunyi ketika JavaScript gagal. Hormati `prefers-reduced-motion`; hindari bounce, floating, parallax default.

#### Theme

Light adalah default Genrock; jangan menambah toggle hanya karena template punya.
Dark diterapkan bila diminta atau kebutuhan produk membenarkan, lewat token semantik. Semua theme yang dikirim harus diverifikasi.

Starter dark: canvas `#171d19`, surface `#202922`, ink `#f0f3ed`, muted `#b4c0b3`, accent `#b9d6b4`, on-accent `#172b1a`, border `#455247`, control border `#839280`, focus `#b9d6b4`.

Jangan membalik warna mentah atau menggunakan accent light dengan teks putih untuk tombol dark. State hover, status, disabled, dan overlay memerlukan pasangan tersendiri serta pengujian.

#### Native

Pertahankan DNA, tetapi ikuti konvensi iOS/Android, font scaling, safe area, dan target sentuh platform. Gunakan token numerik untuk React Native, bukan CSS rem/clamp. Muat Plex melalui mekanisme native existing. Jangan memaksakan desktop navbar atau tabel lebar ke layar ponsel.


## Modul Design Integrity

### Design Integrity Genrock

Aturan ini bukan detector “dibuat AI”. Nilai kualitas dan alasan desain, bukan tebakan asalnya.

#### Hard gates: kejujuran, fungsi, aksesibilitas

| ID | Aturan |
|---|---|
| G-01 | Jangan mengarang statistik, testimoni, customer logos, orang, sertifikasi, atau klaim keamanan/performa. |
| G-02 | Data contoh boleh untuk demo/prototipe jika diberi label jelas; jangan tampilkan sebagai data nyata. |
| G-03 | Link memiliki tujuan nyata; kontrol aktif memiliki perilaku nyata sesuai lingkup. |
| G-04 | Jangan berpura-pura proses server selesai karena toast lokal muncul. Nyatakan mode demo atau integrasi yang belum ada. |
| G-05 | Loading, empty, error, validasi, dan success harus tersedia bila alurnya relevan. Jangan menambah state palsu ke konten statis. |
| G-06 | Semua interaksi dapat dioperasikan dengan keyboard/teknologi bantu yang relevan, focus terlihat, semantics benar. |
| G-07 | Periksa kontras teks, kontrol, dan focus. Jangan menggunakan warna sebagai satu-satunya informasi. |
| G-08 | Mobile, zoom, teks panjang, dan lokalisasi tidak boleh menghilangkan fungsi/konten penting. |
| G-09 | Hasil pengujian harus jujur. Tidak diuji tidak berarti PASS. |
| G-10 | Destructive action melindungi pengguna melalui konfirmasi atau undo yang sesuai; jangan menjalankan aksi eksternal tanpa izin yang diperlukan. |

#### Purpose gates: teknik perlu tujuan

| ID | Hindari sebagai default | Boleh ketika |
|---|---|---|
| P-01 | Gradient, glass, glow, decorative grid | Arah brand eksplisit atau makna konten membutuhkannya; jelaskan penyimpangan dari Industrial. |
| P-02 | Semua informasi dibungkus cards | Pengelompokan entitas benar-benar membantu; list/table boleh lebih baik. |
| P-03 | Sparkle/robot/bolt untuk setiap fitur | Simbol menyampaikan fungsi spesifik, bukan label “AI” generik. |
| P-04 | CTA dengan panah di mana-mana | Ada makna seperti external link atau langkah selanjutnya. |
| P-05 | Animasi setiap section | Gerak membantu pemahaman, feedback, atau konteks; reduced motion tersedia. |
| P-06 | FAQ, pricing, testimonials otomatis | Ada konten/sumber/keputusan produk yang mendukung section tersebut. |
| P-07 | Hero besar dalam semua app | Layar memang untuk discovery atau onboarding, bukan pekerjaan rutin. |
| P-08 | Layout asimetris hanya agar berbeda | Ada hirarki/narasi yang terbantu; tabel seragam tetap sah. |
| P-09 | Dark mode atau theme toggle otomatis | Diminta, ada kebutuhan penggunaan, dan dapat dipelihara serta diuji. |

Keputusan utama dicatat singkat dalam direction. Tidak perlu membuat esai untuk tiap border.

#### Quality locks: konsistensi Genrock

| ID | Pemeriksaan |
|---|---|
| Q-01 | Plex benar-benar dimuat; fallback dan weight sesuai. |
| Q-02 | Radius, spacing, warna, typography berasal dari token, bukan nilai acak per komponen. |
| Q-03 | Satu primary action dominan per konteks aksi; tidak semua tombol primary. |
| Q-04 | Page title, label, status, dan metadata punya hierarchy yang stabil. |
| Q-05 | Copy menyebut aksi/objek konkret, bukan “revolutionary”, “seamless”, atau manfaat tanpa bukti. |
| Q-06 | Struktur halaman mengikuti tugas, bukan paket hero/features/FAQ yang dipasang otomatis. |
| Q-07 | Komponen serupa berperilaku sama; jangan mengorbankan predictability untuk “keunikan”. |
| Q-08 | Identitas berasal dari keseluruhan sistem, bukan sekadar logo atau cat hijau. |

#### Copy: contoh

- “Get started” → “Buat proyek” jika memang membuat proyek.
- “Something went wrong” → “Proyek belum tersimpan. Coba lagi.” jika kondisi tersebut benar.
- “AI-powered productivity” → jelaskan fungsi nyata, misalnya “Ringkas catatan rapat menjadi daftar tugas”, hanya jika fitur ada.
- “No data” → “Belum ada proyek. Buat proyek untuk mulai mencatat pekerjaan.”

Jangan melarang kata atau tanda baca tanpa konteks. Em dash bukan bukti slop; “AI” boleh menyebut fitur nyata. Bahasa pengguna mengikuti produk, tidak harus slang percakapan.

#### Audit tanpa edit

Temuan berisi ID, severity, lokasi, alasan, rekomendasi, dan bukti.
High: kerusakan alur, informasi palsu, hambatan akses kritis.
Medium: hierarchy, responsive, state atau affordance bermasalah.
Low: konsistensi visual minor.

Severity mengikuti dampak, tidak otomatis mengikuti kategori aturan. Laporkan batas lingkup. Jika pengguna meminta audit saja, jangan otomatis memperbaiki kode.

Hasil akhir audit wajib berupa file HTML, bukan hanya daftar temuan di chat atau Markdown. Ikuti `audit-report.md` untuk struktur, keamanan, penamaan file, dan cara menyerahkan laporan. Tidak ada temuan bukan berarti semua gate lulus; laporan tetap mencatat bagian yang belum diuji.


## Modul Pola UI

### Pola UI Genrock

#### App shell dan navigasi

- Pilih sidebar untuk banyak area kerja; horizontal nav untuk sedikit area setara; bottom navigation native jika sesuai.
- Active state memakai teks/indikator selain warna. Navigasi hanya ke route/section yang tersedia.
- Mobile menu memiliki nama, state expanded, focus/keyboard yang sesuai.
- Breadcrumb hanya ketika struktur bertingkat membantu. Jangan menambahkan breadcrumb dekoratif.

#### Tombol dan aksi

Primary: fill hijau, label putih, radius 4px.
Secondary: surface solid, border kontrol, teks ink.
Tertiary: text action yang jelas; link inline bergaris bawah bila dibutuhkan untuk dikenali.
Destructive: danger + kata tindakan, bukan hanya ikon merah.

Kontrol sentuh dianjurkan setidaknya 44×44 CSS px atau mengikuti platform. WCAG 2.2 AA target size 24×24 CSS px memiliki pengecualian dan aturan spacing; jangan mengklaim rekomendasi 44px sebagai ambang universal WCAG.

State: default, hover, focus-visible, pressed, disabled, pending bila relevan. Selama submit, cegah duplikasi dan jelaskan progres. Jangan menyembunyikan label saat spinner muncul.

#### Form

- Label terlihat; placeholder bukan pengganti label.
- Instruksi dan contoh dekat input. Jelaskan required/optional secara konsisten.
- Hubungkan helper/error dengan field; tampilkan pesan penyebab dan cara memperbaiki.
- Untuk form panjang: kelompok logis dan error summary dengan tujuan ke field bermasalah.
- Pertahankan input saat gagal; fokus diarahkan dengan masuk akal, tidak mencuri focus pada setiap update.
- Jangan menampilkan sukses final sebelum backend berhasil jika memang diperlukan.
- Format uang/tanggal mengikuti locale; data disimpan dengan format yang benar, tidak hanya text display.

#### Tabel dan daftar

- Tabel untuk perbandingan kolom; list untuk browsing entitas.
- Angka rata kanan, tabular-nums, unit jelas. Kolom sortable memakai control dan state aksesibel.
- Status memakai label; dot hanya tambahan. Tanggal singkat boleh pada pengguna rutin jika tidak ambigu.
- Pagination/filter/search hanya jika berguna dan bekerja. Filter menghasilkan empty state berbeda dari dataset kosong.
- Mobile: prioritaskan kolom, detail view, atau scroll tabel lokal yang dilabeli. Jangan memotong data penting atau membiarkan seluruh halaman overflow.

#### State matrix

| State | Perilaku |
|---|---|
| First-use empty | Jelaskan objek yang belum ada dan aksi berikutnya. |
| No search result | Tampilkan query/filter dan cara reset. |
| Loading | Indikator yang proporsional; skeleton untuk loading nyata, bukan bukti produk. |
| Error | Pesan relevan dan recovery; jangan mengungkap secrets/internal traces. |
| Success | Konfirmasi hasil sebenarnya, jangan bergantung pada toast cepat saja. |
| Disabled | Jelaskan penyebab bila tidak jelas. |
| Permission denied | Jelaskan batas akses; jangan menampilkan aksi yang mustahil seolah aktif. |
| Offline/pending | Jika alurnya mendukung, jelaskan apakah perubahan lokal tersimpan atau menunggu sync. |

#### Dialog

Accessible name, focus awal, containment yang benar, Escape bila sesuai, restore focus saat ditutup. Backdrop/shadow menandai elevation, bukan tren glass. Untuk aksi berisiko gunakan label spesifik, misalnya “Hapus proyek”, bukan “OK”.

#### Landing page

Industrial tidak berarti dashboard palsu sebagai hero. Jelaskan produk dengan copy spesifik dan demonstrasi nyata atau demo yang dilabeli. Pilih struktur dari pertanyaan pembeli; jangan otomatis menambah logo bar, 3 langkah, pricing, FAQ, atau statistik.

#### Aksesibilitas

- Teks biasa 4.5:1; teks besar 3:1 (24 CSS px normal atau sekitar 18.67 CSS px bold).
- Kontrol/indikator visual esensial minimal 3:1 terhadap warna bersebelahan jika standar tersebut berlaku; divider dekoratif tidak identik dengan batas kontrol.
- Gunakan elemen native semantik. Link memakai Enter; tombol mendukung Enter/Space. Jangan memaksakan Space pada seluruh link.
- Focus harus terlihat, tidak tertutup sticky header/dialog. Outline default boleh dipertahankan.
- Zoom teks 200%, reflow ekuivalen 320 CSS px, text-spacing overrides, screen-reader checks sesuai workflow.
- `aria-live` secukupnya untuk update; jangan menjadikan semua halaman live region.
- Tidak mengklaim kepatuhan WCAG hanya berdasarkan screenshot atau satu test otomatis.

#### Native

Tokens visual dipetakan ke komponen native dan unit platform. Dukung Dynamic Type/font scaling, safe area, keyboard avoidance, label accessibility, dan target sentuh native. Material/platform behaviors dapat dipertahankan sambil memakai warna dan typography Genrock.


## Modul Delivery Gate

### Delivery Gate

Verifikasi sesuai pekerjaan yang diubah. Jangan mengejar seluruh workflow proyek saat hanya memperbaiki heading; jangan mengklaim seluruh proyek lulus karena satu layar diperiksa.

#### Status

- **PASS:** ada bukti pemeriksaan yang relevan.
- **FAIL:** ada masalah nyata, tuliskan lokasi dan dampaknya.
- **NOT TESTED:** pemeriksaan belum dilakukan/alat tidak tersedia; bukan keberhasilan.
- **N/A:** memang tidak berlaku, sebutkan alasan.

#### Matriks minimum

| Gate | Bukti yang dicatat |
|---|---|
| Direction & identity | Plex, surfaces, border, radius dan accent pada layar yang diubah; alasan layout. |
| Build & runtime | Command dan hasil build/check; console jika runtime diperiksa. |
| Task flow | Langkah alur utama yang benar-benar dijalankan dan hasil. |
| Content honesty | Sumber klaim atau label demo; tidak ada hasil server palsu. |
| States | State yang dipicu, bukan hanya komponen yang terlihat di source. |
| Responsive | Viewport aktual yang diperiksa, overflow/wrapping termasuk data panjang. |
| Keyboard & semantics | Tab/focus, aktivasi, dialog dan label yang diperiksa. |
| Contrast | Pasangan warna + rasio terukur; gradients/opacity memerlukan kondisi aktual. |
| Type & zoom | Font dirender, weight, scaling/zoom yang diperiksa. |
| Theme & motion | Theme yang dikirim dan reduced-motion jika ada motion. |

Untuk UI web baru, target sampling awal: 360/768/1280px serta cek reflow 320 CSS px. Sesuaikan dengan platform dan layout; jumlah screenshot bukan bukti semua breakpoint aman.

#### Aturan keputusan

1. Perbaiki FAIL dalam lingkup perubahan dan rerun pemeriksaan terkait.
2. Jika blocker tidak dapat diselesaikan, berikan hasil parsial dan rincian blocker. Jangan menyembunyikan FAIL untuk membuat gate “bersih”.
3. Gate kritis (fungsi, kejujuran, akses utama) FAIL atau NOT TESTED berarti jangan menyebut hasil “siap produksi”.
4. Build sukses tidak membuktikan fungsi, aksesibilitas, atau kualitas visual.
5. Audit dapat menyampaikan FAIL sebagai temuan; bukan berarti audit gagal dikerjakan.
6. Mockup statis: runtime app/backend N/A, bukan PASS. Jelaskan kontrol visual dan data contoh.

#### Format laporan

```text
Direction: Genrock Industrial, comfortable, light.
Build: PASS — [command nyata dan hasil].
Flow: PASS — [langkah yang dijalankan, outcome].
Responsive: PASS — [viewport yang diperiksa].
Keyboard: NOT TESTED — [alasan].
Contrast: PASS — [warna foreground/background dan rasio terukur].
Batas: [integrasi/state yang belum diverifikasi].
```

Contoh adalah format, bukan hasil yang boleh disalin sebagai bukti. Simpan laporan detail pada file bila panjang; ringkas temuan penting di chat.

#### Output akhir audit: HTML wajib

Untuk audit atau audit ulang, format ringkas di atas hanya ringkasan chat. Deliverable utamanya adalah file laporan `.html`, sesuai [spesifikasi laporan audit](#modul-laporan-audit-html).

Sebelum menyatakan audit selesai, periksa:
- File HTML benar-benar tersimpan dan tersedia untuk dibuka/diunduh.
- Ringkasan, scope, gate, temuan/prioritas, bukti, rekomendasi, dan batas pengujian terisi dari pemeriksaan nyata.
- Placeholder template dihapus atau diganti dengan “Tidak diuji” beserta alasan yang sesuai.
- Status tidak mengklaim PASS untuk pemeriksaan yang belum dilakukan.
- HTML tidak memuat secrets, instruksi skrip dari data sumber, atau dependensi remote wajib.

Jika pembuatan file terhalang, laporkan blocker dan hasil parsial; jangan menganggap ringkasan teks telah memenuhi output akhir audit.


## Modul Laporan Audit HTML

### Laporan Audit HTML

#### Kontrak output

Setiap audit UI/desain Genrock, termasuk audit ulang setelah perbaikan, wajib menyerahkan file HTML sebagai deliverable akhir. Berlaku juga saat tidak ditemukan masalah atau pemeriksaan hanya statis. Ringkasan chat dan Markdown boleh mendampingi, tidak menggantikan HTML.

Pembuatan skill atau template laporan bukan audit terhadap aplikasi; jangan membuat klaim hasil audit aplikasi dari task tersebut.

#### Lokasi dan penamaan

- Di proyek: `audits/genrock-audit-NNN-YYYY-MM-DD.html`.
- Di percakapan tanpa proyek: `attached_assets/genrock-audit-NNN-YYYY-MM-DD.html`.
- Cari laporan existing lebih dahulu, lalu gunakan nomor berikutnya dan tanggal lokal pengguna jika diketahui; jika tidak, gunakan tanggal lingkungan.
- Jangan menimpa laporan lama. Audit ulang punya nomor baru dan referensi ke laporan sebelumnya bila tersedia.

#### Struktur wajib

1. **Identitas:** nama produk, nomor laporan, waktu/zona waktu, reviewer agent, serta commit/branch bila benar-benar tersedia.
2. **Ringkasan:** kesimpulan dalam scope, jumlah temuan berdasarkan data laporan, high/medium/low, prioritas terpenting. Hindari skor “kualitas 95%” tanpa metodologi.
3. **Lingkup dan metode:** layar/alur/file, viewport, theme, command/test, static vs runtime; bedakan lingkup rencana dan yang dijalankan.
4. **Delivery gate:** PASS/FAIL/NOT TESTED/N/A untuk gate relevan, dengan bukti atau alasan.
5. **Temuan:** ID stabil, rule Genrock bila relevan, severity berdasarkan dampak, lokasi, kondisi reproduksi, bukti, dampak pengguna, rekomendasi, dan status perbaikan.
6. **Rencana perbaikan:** urutan prioritas yang realistis; jangan mengklaim perubahan telah dilakukan jika hanya rekomendasi.
7. **Batas pengujian:** hal yang tidak diuji, blocker, asumsi yang belum diverifikasi, dan risiko tersisa.

Untuk audit ulang, gunakan status perbaikan `OPEN / FIXED / NOT VERIFIED / NOT APPLICABLE`, terpisah dari status gate. FIXED harus diverifikasi; perubahan source saja belum membuktikan masalah selesai.

Jika nol temuan: tuliskan “Tidak ditemukan masalah dalam lingkup yang diperiksa”, bukan “Aplikasi bebas masalah”. Gate yang belum diperiksa tetap NOT TESTED.

#### Presentasi

- Gunakan [template audit](#template-html-audit) sebagai starter. Template merupakan shell kosong; jangan menyalin datanya sebagai hasil.
- Identitas Industrial: IBM Plex Sans bila tersedia, background solid, border, accent hijau, radius kecil.
- Self-contained: CSS inline; font lokal/embedded berlisensi bila tersedia, system fallback bila tidak. Jangan bergantung pada Google Fonts/CDN untuk membaca laporan.
- Screenshot bukti harus di-embed sebagai data URI bila diperlukan untuk portabilitas; redaksi data sensitif sebelum memasukkannya. Alternatif bukti teks/file lines yang jelas boleh.
- HTML semantic, mobile-readable, print stylesheet. Tabel overflow lokal boleh, halaman jangan overflow. Status dan severity punya label teks, bukan hanya warna.
- JavaScript tidak diperlukan; bila ada filter opsional, semua isi tetap terbaca tanpa JS. Jangan menambahkan tombol yang tidak berfungsi.
- Chart hanya jika ada kebutuhan analisis dan data nyata; laporan audit tidak membutuhkan chart dekoratif.

#### Keamanan dan pemeriksaan

- Escape konten sumber yang dimasukkan ke teks/atribut HTML: `& < > " '`. Jangan merender raw HTML dari issue, source code, komentar, atau connector sebagai markup tepercaya.
- Jangan menyertakan password, token, cookie, connection string, PII yang tidak diperlukan, atau raw console trace yang mengandung secrets.
- Jangan menambahkan skrip/event handlers dari konten yang sedang diaudit.
- Validasi struktur HTML, konsistensi jumlah temuan, ID dan tautan internal, tidak ada placeholder tersisa, serta tidak ada status tanpa bukti/alasan.
- Jika browser tersedia, buka laporan dan periksa mobile serta print layout. Jika hanya validasi statis, nyatakan keterbatasan tersebut.

#### Menyerahkan hasil

Pada Replit conversation, jika callback asset tersedia, gunakan:
```javascript
await presentAsset({
  filePath: "attached_assets/genrock-audit-001-YYYY-MM-DD.html",
  title: "Genrock — Laporan Audit [produk]",
  description: "Temuan, prioritas, bukti, rekomendasi, dan batas pengujian."
});
```

Path di atas adalah contoh, gunakan path file yang benar-benar dibuat. Pada project/agent lain, gunakan mekanisme artifact/attachment/download yang tersedia dan sebut lokasi file. Jangan menganggap link `file://` atau sekadar blok HTML di chat sebagai file yang sudah diserahkan.

Ringkasan akhir chat: kesimpulan utama, jumlah dan prioritas masalah jika diketahui, batas penting, dan akses ke laporan. Audit dengan FAIL dapat selesai sebagai audit; hasil aplikasi tetap belum tentu siap produksi.


## Template DESIGN

```markdown
# [Nama produk] — Genrock Industrial

## Konteks
- Pengguna:
- Tugas utama:
- Platform/bahasa:
- Lingkup perubahan:

## Identitas
- Font: IBM Plex Sans 400/500/600.
- Theme: light default; theme lain hanya jika diperlukan.
- Accent: hijau hutan #2c503c.
- Permukaan: solid, border dominan, radius kontrol 4px.
- Voice: langsung, spesifik, tidak menjanjikan tanpa bukti.

## Adaptasi produk
- Density: comfortable default / compact dengan alasan.
- Layout dan navigasi:
- Informasi utama dan primary action:
- States yang relevan:
- Sumber konten/data demo yang harus dilabeli:

## Keputusan utama
- Layout dipilih karena:
- Density dipilih karena:
- Teknik visual khusus dan alasannya:
- Penyimpangan dari default dan persetujuannya:

## Verification scope
- Layar/alur yang diuji:
- Viewport/platform:
- Checks yang tersedia:
- Blocker atau pemeriksaan yang belum dilakukan:

Template ini bukan permission untuk mengisi statistik atau fitur rekaan.
```


## Template HTML Audit

```html
<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Genrock — Template Laporan Audit</title>
<style>
/* Embed licensed IBM Plex Sans if available; otherwise use the explicit fallback.
   All audit content must be escaped before insertion into this document. */
*{box-sizing:border-box}body{margin:0;background:#f5f5f0;color:#212622;font-family:"IBM Plex Sans",system-ui,Arial,sans-serif;font-size:16px;line-height:1.6}main{max-width:1060px;margin:auto;padding:40px 28px}h1,h2,h3{line-height:1.25;font-weight:600}h1{font-size:32px;letter-spacing:-.025em;margin:12px 0}h2{font-size:24px;margin:0 0 16px}h3{font-size:20px;margin:0 0 10px}p{margin:0 0 14px}.eyebrow{font-size:12px;letter-spacing:.06em;text-transform:uppercase;color:#626a63}.muted{color:#626a63}.template{background:#fff;border:1px solid #d3d8d0;border-left:4px solid #2c503c;padding:16px;margin:24px 0}.meta{display:grid;grid-template-columns:140px minmax(0,1fr);gap:8px 20px;padding:18px 0;border-top:1px solid #d3d8d0;border-bottom:1px solid #d3d8d0}.meta dt{color:#626a63}.meta dd{margin:0;overflow-wrap:anywhere}nav{display:flex;flex-wrap:wrap;gap:12px 24px;margin:24px 0}a{color:#2c503c;text-underline-offset:3px}a:focus-visible{outline:3px solid #164a70;outline-offset:3px}section{margin:32px 0}.summary{display:grid;grid-template-columns:repeat(3,1fr);border:1px solid #d3d8d0;background:#fff;border-radius:4px}.summary div{padding:16px}.summary div+div{border-left:1px solid #d3d8d0}.summary strong{display:block;font-size:20px;font-variant-numeric:tabular-nums}.table-wrap{overflow:auto;border:1px solid #d3d8d0;border-radius:4px}table{width:100%;border-collapse:collapse;background:#fff;text-align:left}th,td{padding:12px 16px;border-bottom:1px solid #d3d8d0;vertical-align:top}th{font-weight:600;background:#eaf0e7}caption{text-align:left;padding:12px 16px;color:#626a63}tbody tr:last-child td{border-bottom:0}.status{font-size:14px;font-weight:600;white-space:nowrap}.finding{padding:20px;border:1px solid #d3d8d0;border-left:4px solid #2c503c;background:#fff;border-radius:4px;margin:16px 0}.finding dl{display:grid;grid-template-columns:125px minmax(0,1fr);gap:8px 18px}.finding dt{font-weight:500}.finding dd{margin:0;overflow-wrap:anywhere}code{font-family:ui-monospace,Consolas,monospace;font-size:.875em;overflow-wrap:anywhere}footer{margin-top:36px;padding-top:18px;border-top:1px solid #d3d8d0;font-size:14px;color:#626a63}@media(max-width:600px){main{padding:24px 16px}h1{font-size:28px}.meta,.finding dl{grid-template-columns:1fr;gap:4px}.meta dd,.finding dd{margin-bottom:12px}.summary{grid-template-columns:1fr}.summary div+div{border-left:0;border-top:1px solid #d3d8d0}th,td{padding:10px 12px;font-size:14px}}@media print{body{background:#fff;color:#000}main{max-width:none;padding:0}nav{display:none}.table-wrap{overflow:visible}.finding{break-inside:avoid}h2,h3{break-after:avoid}a{color:inherit}footer{font-size:11pt}}
</style>
</head>
<body><main>
<header>
<div class="eyebrow">Genrock / Design Integrity</div>
<h1>Template laporan audit</h1>
<p class="muted">Shell laporan, bukan hasil pemeriksaan terhadap aplikasi.</p>
</header>
<aside class="template"><strong>TEMPLATE — BELUM DIISI.</strong><br>Ganti seluruh isian dengan hasil pemeriksaan nyata. Hapus pemberitahuan ini setelah laporan terisi. Jangan menjadikan contoh struktur sebagai bukti PASS.</aside>
<dl class="meta">
<dt>Produk</dt><dd>Belum diisi</dd>
<dt>Nomor dan waktu</dt><dd>Belum diisi; sertakan zona waktu</dd>
<dt>Reviewer</dt><dd>Belum diisi</dd>
<dt>Branch / commit</dt><dd>Belum diperiksa</dd>
<dt>Jenis pemeriksaan</dt><dd>Belum diisi: statis, runtime, atau keduanya</dd>
</dl>
<nav aria-label="Bagian laporan"><a href="#summary">Ringkasan</a><a href="#scope">Lingkup</a><a href="#gates">Delivery gate</a><a href="#findings">Temuan</a><a href="#plan">Prioritas</a><a href="#limits">Batas pengujian</a></nav>
<section id="summary"><h2>Ringkasan</h2><p>Belum diisi: kesimpulan hanya berdasarkan scope yang benar-benar diperiksa.</p>
<div class="summary"><div><span>High</span><strong>Belum dihitung</strong></div><div><span>Medium</span><strong>Belum dihitung</strong></div><div><span>Low</span><strong>Belum dihitung</strong></div></div>
</section>
<section id="scope"><h2>Lingkup dan metode</h2><p>Belum diisi: layar, alur, file, perangkat/viewport, theme, command, dan pemeriksaan yang benar-benar dijalankan.</p></section>
<section id="gates"><h2>Delivery gate</h2>
<div class="table-wrap"><table><caption>Status pemeriksaan; bukan daftar klaim kelulusan.</caption><thead><tr><th scope="col">Gate</th><th scope="col">Status</th><th scope="col">Bukti / alasan</th></tr></thead>
<tbody><tr><th scope="row">Direction &amp; identity</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Build &amp; runtime</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Task flow &amp; states</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Content honesty</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Responsive, type &amp; zoom</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Keyboard &amp; semantics</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Contrast</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr>
<tr><th scope="row">Theme &amp; motion</th><td class="status">NOT TESTED</td><td>Template belum diisi.</td></tr></tbody></table></div>
</section>
<section id="findings"><h2>Temuan</h2><p>Blok di bawah adalah struktur contoh, bukan masalah yang telah ditemukan. Ganti dengan temuan nyata atau pernyataan nol temuan dalam lingkup yang diperiksa.</p>
<article class="finding"><h3>Temuan — belum diisi</h3>
<dl><dt>ID / aturan</dt><dd>Belum diisi</dd><dt>Severity</dt><dd>Belum ditentukan berdasarkan dampak</dd><dt>Status perbaikan</dt><dd>NOT VERIFIED — template belum diisi</dd><dt>Lokasi</dt><dd>Belum diisi: route, komponen, file/baris</dd><dt>Reproduksi</dt><dd>Belum diisi: langkah dan kondisi pengujian</dd><dt>Bukti</dt><dd>Belum diisi; gunakan hasil nyata, jangan menyertakan secrets</dd><dt>Dampak</dt><dd>Belum diisi: akibat bagi pengguna</dd><dt>Rekomendasi</dt><dd>Belum diisi: tindakan perbaikan yang konkret</dd></dl>
</article></section>
<section id="plan"><h2>Urutan perbaikan</h2><p>Belum diisi. Prioritaskan risiko dan hambatan alur utama; bedakan rekomendasi dengan perubahan yang telah dilakukan.</p></section>
<section id="limits"><h2>Batas pengujian dan risiko tersisa</h2><p>Belum diisi: pemeriksaan yang belum dilakukan, blocker, asumsi, dan batas klaim kesiapan produksi.</p></section>
<footer>Genrock Industrial / Design Integrity. Template ini tidak menyatakan aplikasi lulus audit atau memenuhi WCAG.</footer>
</main></body></html>
```


## Token CSS

```css
/* Genrock Industrial — starter web tokens.
   Font assets must be loaded separately from a licensed official distribution.
   Semantic mapping, not a full component stylesheet or accessibility guarantee. */
:root {
  --gr-font-ui: "IBM Plex Sans", system-ui, -apple-system,
    BlinkMacSystemFont, "Segoe UI", sans-serif;
  --gr-font-code: "IBM Plex Mono", ui-monospace, Consolas, monospace;
  --gr-canvas: #f5f5f0;
  --gr-surface: #ffffff;
  --gr-ink: #212622;
  --gr-muted: #626a63;
  --gr-border: #d3d8d0;
  --gr-control-border: #7a857b;
  --gr-accent: #2c503c;
  --gr-accent-hover: #23402f;
  --gr-on-accent: #ffffff;
  --gr-accent-subtle: #eaf0e7;
  --gr-danger: #a12b2b;
  --gr-warning: #775000;
  --gr-focus: #164a70;
  --gr-radius-control: 4px;
  --gr-radius-panel: 4px;
  --gr-radius-dialog: 8px;
  --gr-space-1: 0.25rem;
  --gr-space-2: 0.5rem;
  --gr-space-3: 0.75rem;
  --gr-space-4: 1rem;
  --gr-space-6: 1.5rem;
  --gr-space-8: 2rem;
  --gr-space-12: 3rem;
  --gr-space-16: 4rem;
  --gr-text-meta: 0.75rem;
  --gr-text-compact: 0.875rem;
  --gr-text-body: 1rem;
  --gr-text-subhead: 1.25rem;
  --gr-text-section: 1.5rem;
  --gr-text-title: 2rem;
  --gr-weight-regular: 400;
  --gr-weight-medium: 500;
  --gr-weight-semibold: 600;
  --gr-leading-body: 1.6;
  --gr-leading-title: 1.25;
  --gr-shadow-overlay: 0 8px 24px rgb(21 32 24 / 12%);
  --gr-duration-fast: 140ms;
  --gr-ease: cubic-bezier(0.2, 0, 0, 1);
}

/* Optional dark starter. Implement all component states before shipping it. */
[data-gr-theme="dark"] {
  color-scheme: dark;
  --gr-canvas: #171d19;
  --gr-surface: #202922;
  --gr-ink: #f0f3ed;
  --gr-muted: #b4c0b3;
  --gr-border: #455247;
  --gr-control-border: #839280;
  --gr-accent: #b9d6b4;
  --gr-accent-hover: #cbe4c7;
  --gr-on-accent: #172b1a;
  --gr-accent-subtle: #293c2c;
  --gr-danger: #ffb4ab;
  --gr-warning: #f0cd85;
  --gr-focus: #b9d6b4;
}

.gr-root {
  font-family: var(--gr-font-ui);
  font-size: var(--gr-text-body);
  line-height: var(--gr-leading-body);
  color: var(--gr-ink);
  background: var(--gr-canvas);
}

.gr-root :where(button, input, select, textarea) { font: inherit; }
.gr-root :where(button, a, input, select, textarea, [tabindex]):focus-visible {
  outline: 3px solid var(--gr-focus);
  outline-offset: 3px;
}
.gr-number { font-variant-numeric: tabular-nums; }
.gr-prose { max-inline-size: 65ch; overflow-wrap: break-word; }
.gr-title {
  font-size: var(--gr-text-title);
  font-weight: var(--gr-weight-semibold);
  line-height: var(--gr-leading-title);
  letter-spacing: -0.025em;
}
.gr-primary {
  min-block-size: 2.75rem;
  padding: 0.625rem 1rem;
  border: 1px solid transparent;
  border-radius: var(--gr-radius-control);
  color: var(--gr-on-accent);
  background: var(--gr-accent);
  font-weight: var(--gr-weight-medium);
}
.gr-primary:hover:not(:disabled) { background: var(--gr-accent-hover); }
.gr-primary:disabled { cursor: not-allowed; }
/* Implement pending/pressed/disabled visuals in the component system.
   Apply motion only to components with an actual transition. */
@media (prefers-reduced-motion: reduce) {
  .gr-root { --gr-duration-fast: 0ms; }
}
```

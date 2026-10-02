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
- [Template arah produk](#template-design): untuk mencatat identitas dan keputusan per proyek.
- [Token CSS](#token-css): starter web, bukan stylesheet yang harus disalin mentah.

## Mode kerja

Pilih dari permintaan, tidak perlu menanyakan mode pada setiap sesi:
- **Build:** app/UI baru. Tetapkan arah, implementasikan, lalu verifikasi.
- **Adapt:** perubahan pada UI existing. Pertahankan struktur dan integrasi, ubah hanya yang diperlukan.
- **Audit:** permintaan review atau audit. Baca dan laporkan temuan; jangan mengubah kode kecuali pengguna meminta perbaikan.
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

> Versi single-file: seluruh modul tercantum di bawah. Baca bagian sesuai routing; tidak perlu file skill Typography terpisah. Untuk dipakai di percakapan lain, tambahkan melalui workspace Knowledge → Skills.


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

# Pola UI Genrock

## App shell dan navigasi

- Pilih sidebar untuk banyak area kerja; horizontal nav untuk sedikit area setara; bottom navigation native jika sesuai.
- Active state memakai teks/indikator selain warna. Navigasi hanya ke route/section yang tersedia.
- Mobile menu memiliki nama, state expanded, focus/keyboard yang sesuai.
- Breadcrumb hanya ketika struktur bertingkat membantu. Jangan menambahkan breadcrumb dekoratif.

## Tombol dan aksi

Primary: fill hijau, label putih, radius 4px.
Secondary: surface solid, border kontrol, teks ink.
Tertiary: text action yang jelas; link inline bergaris bawah bila dibutuhkan untuk dikenali.
Destructive: danger + kata tindakan, bukan hanya ikon merah.

Kontrol sentuh dianjurkan setidaknya 44×44 CSS px atau mengikuti platform. WCAG 2.2 AA target size 24×24 CSS px memiliki pengecualian dan aturan spacing; jangan mengklaim rekomendasi 44px sebagai ambang universal WCAG.

State: default, hover, focus-visible, pressed, disabled, pending bila relevan. Selama submit, cegah duplikasi dan jelaskan progres. Jangan menyembunyikan label saat spinner muncul.

## Form

- Label terlihat; placeholder bukan pengganti label.
- Instruksi dan contoh dekat input. Jelaskan required/optional secara konsisten.
- Hubungkan helper/error dengan field; tampilkan pesan penyebab dan cara memperbaiki.
- Untuk form panjang: kelompok logis dan error summary dengan tujuan ke field bermasalah.
- Pertahankan input saat gagal; fokus diarahkan dengan masuk akal, tidak mencuri focus pada setiap update.
- Jangan menampilkan sukses final sebelum backend berhasil jika memang diperlukan.
- Format uang/tanggal mengikuti locale; data disimpan dengan format yang benar, tidak hanya text display.

## Tabel dan daftar

- Tabel untuk perbandingan kolom; list untuk browsing entitas.
- Angka rata kanan, tabular-nums, unit jelas. Kolom sortable memakai control dan state aksesibel.
- Status memakai label; dot hanya tambahan. Tanggal singkat boleh pada pengguna rutin jika tidak ambigu.
- Pagination/filter/search hanya jika berguna dan bekerja. Filter menghasilkan empty state berbeda dari dataset kosong.
- Mobile: prioritaskan kolom, detail view, atau scroll tabel lokal yang dilabeli. Jangan memotong data penting atau membiarkan seluruh halaman overflow.

## State matrix

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

## Dialog

Accessible name, focus awal, containment yang benar, Escape bila sesuai, restore focus saat ditutup. Backdrop/shadow menandai elevation, bukan tren glass. Untuk aksi berisiko gunakan label spesifik, misalnya “Hapus proyek”, bukan “OK”.

## Landing page

Industrial tidak berarti dashboard palsu sebagai hero. Jelaskan produk dengan copy spesifik dan demonstrasi nyata atau demo yang dilabeli. Pilih struktur dari pertanyaan pembeli; jangan otomatis menambah logo bar, 3 langkah, pricing, FAQ, atau statistik.

## Aksesibilitas

- Teks biasa 4.5:1; teks besar 3:1 (24 CSS px normal atau sekitar 18.67 CSS px bold).
- Kontrol/indikator visual esensial minimal 3:1 terhadap warna bersebelahan jika standar tersebut berlaku; divider dekoratif tidak identik dengan batas kontrol.
- Gunakan elemen native semantik. Link memakai Enter; tombol mendukung Enter/Space. Jangan memaksakan Space pada seluruh link.
- Focus harus terlihat, tidak tertutup sticky header/dialog. Outline default boleh dipertahankan.
- Zoom teks 200%, reflow ekuivalen 320 CSS px, text-spacing overrides, screen-reader checks sesuai workflow.
- `aria-live` secukupnya untuk update; jangan menjadikan semua halaman live region.
- Tidak mengklaim kepatuhan WCAG hanya berdasarkan screenshot atau satu test otomatis.

## Native

Tokens visual dipetakan ke komponen native dan unit platform. Dukung Dynamic Type/font scaling, safe area, keyboard avoidance, label accessibility, dan target sentuh native. Material/platform behaviors dapat dipertahankan sambil memakai warna dan typography Genrock.
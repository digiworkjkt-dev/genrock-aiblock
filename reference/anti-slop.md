# Aturan Anti-Slop Genrock

Aturan ini bukan detector “dibuat AI”. Nilai kualitas dan alasan desain, bukan tebakan asalnya.

## Hard gates: kejujuran, fungsi, aksesibilitas

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

## Purpose gates: teknik perlu tujuan

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

## Quality locks: konsistensi Genrock

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

## Copy: contoh

- “Get started” → “Buat proyek” jika memang membuat proyek.
- “Something went wrong” → “Proyek belum tersimpan. Coba lagi.” jika kondisi tersebut benar.
- “AI-powered productivity” → jelaskan fungsi nyata, misalnya “Ringkas catatan rapat menjadi daftar tugas”, hanya jika fitur ada.
- “No data” → “Belum ada proyek. Buat proyek untuk mulai mencatat pekerjaan.”

Jangan melarang kata atau tanda baca tanpa konteks. Em dash bukan bukti slop; “AI” boleh menyebut fitur nyata. Bahasa pengguna mengikuti produk, tidak harus slang percakapan.

## Audit tanpa edit

Temuan berisi ID, severity, lokasi, alasan, rekomendasi, dan bukti.
High: kerusakan alur, informasi palsu, hambatan akses kritis.
Medium: hierarchy, responsive, state atau affordance bermasalah.
Low: konsistensi visual minor.

Severity mengikuti dampak, tidak otomatis mengikuti kategori aturan. Laporkan batas lingkup. Jika pengguna meminta audit saja, jangan otomatis memperbaiki kode.
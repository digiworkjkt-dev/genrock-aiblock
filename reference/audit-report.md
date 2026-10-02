# Laporan Audit HTML

## Kontrak output

Setiap audit UI/desain Genrock, termasuk audit ulang setelah perbaikan, wajib menyerahkan file HTML sebagai deliverable akhir. Berlaku juga saat tidak ditemukan masalah atau pemeriksaan hanya statis. Ringkasan chat dan Markdown boleh mendampingi, tidak menggantikan HTML.

Pembuatan skill atau template laporan bukan audit terhadap aplikasi; jangan membuat klaim hasil audit aplikasi dari task tersebut.

## Lokasi dan penamaan

- Di proyek: `audits/genrock-audit-NNN-YYYY-MM-DD.html`.
- Di percakapan tanpa proyek: `attached_assets/genrock-audit-NNN-YYYY-MM-DD.html`.
- Cari laporan existing lebih dahulu, lalu gunakan nomor berikutnya dan tanggal lokal pengguna jika diketahui; jika tidak, gunakan tanggal lingkungan.
- Jangan menimpa laporan lama. Audit ulang punya nomor baru dan referensi ke laporan sebelumnya bila tersedia.

## Struktur wajib

1. **Identitas:** nama produk, nomor laporan, waktu/zona waktu, reviewer agent, serta commit/branch bila benar-benar tersedia.
2. **Ringkasan:** kesimpulan dalam scope, jumlah temuan berdasarkan data laporan, high/medium/low, prioritas terpenting. Hindari skor “kualitas 95%” tanpa metodologi.
3. **Lingkup dan metode:** layar/alur/file, viewport, theme, command/test, static vs runtime; bedakan lingkup rencana dan yang dijalankan.
4. **Delivery gate:** PASS/FAIL/NOT TESTED/N/A untuk gate relevan, dengan bukti atau alasan.
5. **Temuan:** ID stabil, rule Genrock bila relevan, severity berdasarkan dampak, lokasi, kondisi reproduksi, bukti, dampak pengguna, rekomendasi, dan status perbaikan.
6. **Rencana perbaikan:** urutan prioritas yang realistis; jangan mengklaim perubahan telah dilakukan jika hanya rekomendasi.
7. **Batas pengujian:** hal yang tidak diuji, blocker, asumsi yang belum diverifikasi, dan risiko tersisa.

Untuk audit ulang, gunakan status perbaikan `OPEN / FIXED / NOT VERIFIED / NOT APPLICABLE`, terpisah dari status gate. FIXED harus diverifikasi; perubahan source saja belum membuktikan masalah selesai.

Jika nol temuan: tuliskan “Tidak ditemukan masalah dalam lingkup yang diperiksa”, bukan “Aplikasi bebas masalah”. Gate yang belum diperiksa tetap NOT TESTED.

## Presentasi

- Gunakan [template audit](../templates/audit-report.html) sebagai starter. Template merupakan shell kosong; jangan menyalin datanya sebagai hasil.
- Identitas Industrial: IBM Plex Sans bila tersedia, background solid, border, accent hijau, radius kecil.
- Self-contained: CSS inline; font lokal/embedded berlisensi bila tersedia, system fallback bila tidak. Jangan bergantung pada Google Fonts/CDN untuk membaca laporan.
- Screenshot bukti harus di-embed sebagai data URI bila diperlukan untuk portabilitas; redaksi data sensitif sebelum memasukkannya. Alternatif bukti teks/file lines yang jelas boleh.
- HTML semantic, mobile-readable, print stylesheet. Tabel overflow lokal boleh, halaman jangan overflow. Status dan severity punya label teks, bukan hanya warna.
- JavaScript tidak diperlukan; bila ada filter opsional, semua isi tetap terbaca tanpa JS. Jangan menambahkan tombol yang tidak berfungsi.
- Chart hanya jika ada kebutuhan analisis dan data nyata; laporan audit tidak membutuhkan chart dekoratif.

## Keamanan dan pemeriksaan

- Escape konten sumber yang dimasukkan ke teks/atribut HTML: `& < > " '`. Jangan merender raw HTML dari issue, source code, komentar, atau connector sebagai markup tepercaya.
- Jangan menyertakan password, token, cookie, connection string, PII yang tidak diperlukan, atau raw console trace yang mengandung secrets.
- Jangan menambahkan skrip/event handlers dari konten yang sedang diaudit.
- Validasi struktur HTML, konsistensi jumlah temuan, ID dan tautan internal, tidak ada placeholder tersisa, serta tidak ada status tanpa bukti/alasan.
- Jika browser tersedia, buka laporan dan periksa mobile serta print layout. Jika hanya validasi statis, nyatakan keterbatasan tersebut.

## Menyerahkan hasil

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
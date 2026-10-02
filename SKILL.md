---
name: genrock-aiblock
description: Merancang, membangun, dan mengaudit UI web atau aplikasi dengan identitas Genrock Industrial, IBM Plex Sans, permukaan solid, border presisi, dan copy langsung. Gunakan untuk pembuatan app, dashboard, form, landing page, komponen UI, redesign, design system, atau audit anti-AI-slop. Menjaga ciri khas lintas produk tanpa memaksakan template layout yang sama.
---

# Genrock AIBLOCK

Sistem desain Genrock Industrial dan pemeriksaan anti-slop. Hasil harus terasa sebagai alat yang dibuat dengan sengaja: jelas, tegas, berguna, dan konsisten. Bukan sekadar UI generik dengan warna hijau.

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
1. [Fondasi visual](reference/foundation.md) untuk setiap build atau redesign UI.
2. [Aturan anti-slop](reference/anti-slop.md) untuk build dan audit.

Baca sesuai kebutuhan:
- [Pola UI](reference/ui-patterns.md): layout, form, tabel, navigasi, states, native.
- [Delivery gate](reference/delivery-gate.md): sebelum menyatakan pekerjaan selesai.
- [Template arah produk](templates/DESIGN.md): untuk mencatat identitas dan keputusan per proyek.
- [Token CSS](assets/genrock-tokens.css): starter web, bukan stylesheet yang harus disalin mentah.

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
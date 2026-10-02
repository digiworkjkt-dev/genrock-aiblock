# Delivery Gate

Verifikasi sesuai pekerjaan yang diubah. Jangan mengejar seluruh workflow proyek saat hanya memperbaiki heading; jangan mengklaim seluruh proyek lulus karena satu layar diperiksa.

## Status

- **PASS:** ada bukti pemeriksaan yang relevan.
- **FAIL:** ada masalah nyata, tuliskan lokasi dan dampaknya.
- **NOT TESTED:** pemeriksaan belum dilakukan/alat tidak tersedia; bukan keberhasilan.
- **N/A:** memang tidak berlaku, sebutkan alasan.

## Matriks minimum

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

## Aturan keputusan

1. Perbaiki FAIL dalam lingkup perubahan dan rerun pemeriksaan terkait.
2. Jika blocker tidak dapat diselesaikan, berikan hasil parsial dan rincian blocker. Jangan menyembunyikan FAIL untuk membuat gate “bersih”.
3. Gate kritis (fungsi, kejujuran, akses utama) FAIL atau NOT TESTED berarti jangan menyebut hasil “siap produksi”.
4. Build sukses tidak membuktikan fungsi, aksesibilitas, atau kualitas visual.
5. Audit dapat menyampaikan FAIL sebagai temuan; bukan berarti audit gagal dikerjakan.
6. Mockup statis: runtime app/backend N/A, bukan PASS. Jelaskan kontrol visual dan data contoh.

## Format laporan

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
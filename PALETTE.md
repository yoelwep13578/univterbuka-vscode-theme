# Palet & Rasional Warna

## Warna Utama untuk Dasaran/Awalan

| Nama | Hex | Turunan untuk |
|---|---|---|
| Reflex Blue | `#034694` | Light mode: keyword, UI utama <br> Dark mode: background tombol/selection |
| Yellow 109 | `#FFDE00` | Badge, find-match, accent warna |
| Hytam | `#000000` dilembutkan menjadi `#17202A` | Teks untuk light mode, teks di atas badge kuning |
| Putih | Light Mode: `#FFFFFF` <br> Dark Mode: `#EAF0F8` | Background untuk light mode <br> Teks untuk dark mode |

## Warna Harmonisasi

**Biru (analogous, hue ~212°)** 
- `#02335F` (border gelap)
- `#034694` (inti)
- `#0B5CAD` (hover/fungsi)
- `#79B8FF` (biru terang di dark mode, 9,02:1)
- `#A9D1FF` (properti di dark mode)
- Warna panel untuk light mode `#F2F6FB/#E3EBF5`.

**Kuning (hue ~52°)**
- `#FFDE00` (inti)
- `#FFE95C` (kuning terang di dark mode)
- `#7A5C00` (kuning yang agak digelapkan di light mode, 6,25:1 AA)
- `#8A6D00` (angka di light mode)
- Warna transparan `#FFDE0055` untuk seleksi/find di light mode (teks hitam tetap terbaca di atasnya).

**Netral**
- Light: teks `#17202A`, sekunder `#5A6B7F`, samar `#9AA9BC`.
- Dark: latar `#0B1220` (hitam kebiruan), panel `#0E1828`, teks `#EAF0F8`, sekunder `#7E93B0`.

**Semantik pendukung (muted)** 
- Hijau string/added `#1E7A46` (light mode) / `#4ADE80` & string kuning di dark mode
- Merah error `#B42318` / `#FF8A80`
- Teal type `#0E6E7E` / `#6ED3D8`
- Oranye angka di dark mode `#FFB86B`.

## Kaidah Penempatan Warna "Nge-jreng" (`#FFDE00` & Biru Jenuh)

Warna mencolok digunakan untuk badge berlatar kuning + teks hitam, garis atas tab aktif, highlight pencarian, kursor di dark mode, ikon Activity Bar Dark, progress bar, remote indicator.

Warna mencolok tidak dipakai untuk warna latar editor/sidebar luas, teks di atas putih, syntax massal (kecuali di darkmode untuk fungsi/string yang memang kontras AAA di latar gelap).

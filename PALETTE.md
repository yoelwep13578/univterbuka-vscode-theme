# Palet & Rasional Warna — UnivTerbuka Theme

## Warna inti (dari logo UT, GSM Universitas Terbuka)

| Nama | Hex | Turunan untuk | Dipakai sebagai teks? |
|---|---|---|---|
| UT Reflex Blue | `#034694` | Light: keyword, UI utama · Dark: latar tombol/seleksi | ✅ Light (9,10:1) · ❌ Dark (2,06:1 → diterangkan) |
| UT Yellow 109 | `#FFDE00` | Badge, find-match, aksen | ❌ Light (1,34:1) · ✅ Dark (14,0:1) |
| Hitam UT | `#000000` → dilembutkan `#17202A` | Teks utama Light, teks di atas badge kuning | ✅ |
| Putih UT | `#FFFFFF` → Dark: `#EAF0F8` | Latar Light, teks utama Dark | ✅ |

## Skala turunan (harmonisasi)

**Biru (analogous, hue ~212°):** `#02335F` (border gelap) · `#034694` (inti) · `#0B5CAD` (hover/fungsi) · `#79B8FF` (biru terang Dark, 9,02:1) · `#A9D1FF` (properti Dark) · latar panel Light `#F2F6FB/#E3EBF5`.

**Kuning (hue ~52°):** `#FFDE00` (inti) · `#FFE95C` (kuning terang Dark) · `#7A5C00` (kuning-as-text Light, 6,25:1 AA) · `#8A6D00` (angka Light) · transparan `#FFDE0055` untuk seleksi/find di Light (teks hitam tetap terbaca di atasnya).

**Netral:** Light: teks `#17202A`, sekunder `#5A6B7F`, samar `#9AA9BC`. Dark: latar `#0B1220` (hitam kebiruan — bukan `#000`, menghindari halation), panel `#0E1828`, teks `#EAF0F8`, sekunder `#7E93B0`.

**Semantik pendukung (sengaja muted, bukan neon):** hijau string/added `#1E7A46` (Light) / `#4ADE80` & string kuning di Dark · merah error `#B42318` / `#FF8A80` · teal type `#0E6E7E` / `#6ED3D8` · oranye angka Dark `#FFB86B`.

## Kaidah penempatan warna "nge-jreng" (`#FFDE00` & biru jenuh)
Boleh: badge berlatar kuning + teks hitam, garis atas tab aktif, highlight pencarian, kursor Dark, ikon Activity Bar Dark, progress bar, remote indicator.
Tidak boleh: latar editor/sidebar luas, teks di atas putih, sintaks massal (kecuali Dark untuk fungsi/string yang memang kontras AAA di latar gelap).

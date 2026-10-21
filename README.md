<h1 align="center">UnivTerbuka VS Code Color Theme</h1>

<p align="center">Color theme untuk Visual Studio Code bernuansa Universitas Terbuka (UT), yang terinspirasi dari palet warna resmi logo UT dan diharmonisasikan mengikuti prinsip HCI/IMK, keterbacaan jangka panjang, dan rasio kontras WCAG 2.1.</p>

## Sedikit Latar Belakang

Tema warna ini dibuat sebagai reaksi rasa gabut dan iseng setelah melihat seseorang memamerkan editor VS Code berwarna biru.

<div align="center">
<picture>
  <source srcset="https://github.com/user-attachments/assets/2836580e-a98f-4602-9177-18acb7dcc687" media="(prefers-color-scheme: dark)">
  <img src="https://github.com/user-attachments/assets/c002e97f-fc8f-45c4-bd23-0fcbddd4f62b" width="600">
</picture>
</div>

## Tersedia Color Theme untuk Light dan Dark

| Tema | `uiTheme` | Karakter |
|---|---|---|
| **UnivTerbuka Light** | `vs` | Putih bersih, biru sebagai warna utama teks/UI, kuning hanya sebagai aksen |
| **UnivTerbuka Dark** | `vs-dark` | Hitam kebiruan (`#0B1220`), teks putih kebiruan, kuning bersinar sebagai aksen & fungsi |

Warnanya disediakan untuk editor, syntax highlighting (TextMate + semantic tokens), Activity Bar, Side Bar, Tab, Status Bar, Panel/Terminal, notifikasi, Git decoration, bracket matching, find/replace, IntelliSense, dan minimap.

## Warna Dasar

Warna-warnanya didasari dari palet warna logo UT di [Graphic Standard Manual (GSM) Universitas Terbuka](https://www.ut.ac.id/wp-content/uploads/2026/04/Graphic-Standart-Manual_UT.pdf), dan penjelasan [makna logo](https://www.ut.ac.id/logo-ut/) di website resmi UT.

| Warna Identitas | Spesifikasi | Hex | Makna (Menurut UT) |
|---|---|---|---|
| 🔵 **Biru** | Pantone® Reflex Blue C <br> CMYK 100-80-0-10 <br> RGB 3, 70, 148 | `#034694` | Kepercayaan, kebijaksanaan, kestabilan, kematangan berpikir, nilai integritas |
| 🟡 **Kuning** | Pantone® 109 C <br> CMYK 0-10-100-0 <br> RGB 255, 222, 0 | `#FFDE00` | Imajinasi, kreativitas, kebahagiaan, kehangatan, optimisme |
| ⚫ **Hitam** | Elemen pena dan outline | turunan: `#17202A` | Ketegasan, keterbacaan teks utama |
| ⚪ **Putih** | Lembaran buku pada logo | `#FFFFFF` / `#EAF0F8` | Keterbukaan ilmu, kejernihan |

## Prinsip HCI/IMK & Kontras yang Diterapkan

Warna logo tadi dijadikan inspirasi untuk menghasilkan warna-warna yang lebih enak dilihat.

### Komposisi 60–30–10
- **60%** untuk warna netral (putih / hitam kebiruan) untuk background, agar mata bisa lebih rileks.
- **30%** biru & turunannya untuk struktur UI, keyword, fungsi.
- **10%** kuning untuk aksen. Kuning yang "nge-jreng" hanya dipakai di badge (dengan teks hitam), tab aktif (garis atas), penanda find match, kursor & nomor baris aktif (dark mode), status remote, dan progress bar.

### Variasi Warna Kuning Lain agar Jangan Bertabrakan di Background Putih
Kuning murni `#FFDE00` di atas putih rasio kontrasnya hanya 1,34:1 sehingga kurang cocok menurut WCAG (disarankan 4,5:1 untuk teks). Maka di Light Mode, kuning untuk teks digelapkan menjadi `#7A5C00` (6,25:1 AA), sedangkan kuning murni hanya dipakai sebagai latar aksen berpadu teks hitam (`#000` di atas `#FFDE00`. 15,7:1 AAA).

### Satu Warna Utama dan Dua Perilaku (Adaptasi Luminansi)
Biru murni `#034694` di atas latar gelap hanya 2,06:1 (tidak terbaca), jadi di Dark Mode akan diterangkan menjadi `#79B8FF` (9,02:1 AAA) untuk teks/keyword, sementara biru murni tetap dipakai sebagai latar tombol/seleksi dengan teks putih (9,10:1 AAA). 

Prinsip yang sama untuk warna kuning, di Dark Mode kuning murni bisa ideal (14,0:1 AAA) sehingga boleh menjadi warna string/fungsi.

### Rasio Kontras WCAG 2.1

| Pasangan warna | Mode | Rasio | Level |
|---|---|---:|---|
| `#17202A` di `#FFFFFF` (teks utama) | Light | 16,45:1 | AAA |
| `#034694` di `#FFFFFF` (keyword/link) | Light | 9,10:1 | AAA |
| `#7A5C00` di `#FFFFFF` (angka/aksen kuning-as-text) | Light | 6,25:1 | AA |
| `#000000` di `#FFDE00` (badge) | Light & Dark | 15,70:1 | AAA |
| `#FFFFFF` di `#034694` (Status/Activity Bar) | Lignt & Dark | 9,10:1 | AAA |
| `#F5F7FA`/`#EAF0F8` di `#0B1220` (teks utama) | Dark | 17,45:1 | AAA |
| `#FFDE00` di `#0B1220` (fungsi/string) | Dark | 14,00:1 | AAA |
| `#79B8FF` di `#0B1220` (keyword) | Dark | 9,02:1 | AAA |

*AAA ≥ 7:1 <br> AA ≥ 4,5:1 untuk teks normal.*

### Prinsip HCI/IMK lain
- Elemen utama diberi warna jenuh (biru/kuning), elemen pendukung diberi warna yang agak kusam (abu kebiruan), sehingga mata tahu harus melihat ke mana.
- Warna kuning selalu berarti sorotan/aksen penting, biru selalu struktur/interaksi utama.
- Warna untuk error/warning tetap dibedakan juga (garis bergelombang VS Code), ramah untuk pengguna buta warna merah–hijau. Warna semantik pendukung (hijau string, merah error, teal type) dipilih versi muted.
- Background di dark mode dibuat agak kebiruan `#0B1220`, dan warna background di light mode memakai panel `#F2F6FB` agar batas antar-area lembut.

Palet lengkapnya ada di [`PALETTE.md`](./PALETTE.md).



## Instalasi & Penggunaan

### Cara 1. Install dari File `.vsix` (Paling Mudah)

Download file `.vsix` yang siap diinstal dari Release.

**Instalasi**

- **Lewat GUI VS Code:**
  1. Buka VS Code → panel **Extensions** (`Ctrl+Shift+X` / `Cmd+Shift+X`)
  2. Klik **`...`** (Views and More Actions) di kanan atas panel
  3. Pilih **Install from VSIX...** → arahkan ke `univterbuka-vscode-theme-x.x.x.vsix`. `x.x.x` adalah nomor versi.
- **Lewat terminal:**
  ```bash
  # Windows (PowerShell/CMD), macOS, Linux perintahnya sama bila `code` ada di PATH
  code --install-extension univterbuka-vscode-theme-1.0.0.vsix
  ```

**Mengaktifkan Color Theme**

`Ctrl+K Ctrl+T` (Windows/Linux) atau `Cmd+K Cmd+T` (macOS) → pilih **UnivTerbuka Light** atau **UnivTerbuka Dark**. 

Atau lewat menu **File/Code → Preferences → Theme → Color Theme**.

### Cara 2. Copy Sendiri (Tanpa `.vsix`)

Salin folder `univterbuka-vscode-theme` ke folder extension VS Code Anda:

| OS | Folder tujuan |
|---|---|
| **Windows** | `%USERPROFILE%\.vscode\extensions\` |
| **macOS** | `~/.vscode/extensions/univterbuka-vscode-theme` |
| **Linux** | `~/.vscode/extensions/univterbuka-vscode-theme` |

Lalu **restart VS Code** dan aktifkan tema seperti di atas.

Contoh perintah:

```powershell
# Windows (PowerShell)
Copy-Item -Recurse .\univterbuka-vscode-theme "$env:USERPROFILE\.vscode\extensions\"
```
```bash
# macOS / Linux
cp -r univterbuka-vscode-theme ~/.vscode/extensions/
```

### Cara 3. Tanpa Extension

Jika hanya ingin mencoba warna editor tanpa memasang extension ini, salin isi `settings-snippet.json` (termasuk bagian `workbench.colorCustomizations` / `editor.tokenColorCustomizations` yang bisa Anda ekstrak dari file tema) ke Settings JSON Anda:
`Ctrl+Shift+P` / `Cmd+Shift+P` → **Preferences: Open User Settings (JSON)**. 

Namun **Cara A/B tetap disarankan** agar seluruh elemen UI ikut berwarna.

### Pengaturan Pendamping (Opsional)

```jsonc
// settings.json
{
  "workbench.colorTheme": "UnivTerbuka Dark",   // atau "UnivTerbuka Light"
  "editor.bracketPairColorization.enabled": true
}
```

### Membuat Theme Bisa Berganti Light & Dark Mengikuti OS (Opsional)

```jsonc
{
  "window.autoDetectColorScheme": true,
  "workbench.preferredLightColorTheme": "UnivTerbuka Light",
  "workbench.preferredDarkColorTheme": "UnivTerbuka Dark"
}
```

### Uninstall

- Buka panel **Extensions** → cari *UnivTerbuka Theme* → **Uninstall**
- Atau jalankan perintah:
  ```
  code --uninstall-extension univterbuka-theme.univterbuka-vscode-theme`
  ```
- Atau hapus foldernya dari `.vscode/extensions`.

## Struktur Repositori

```
univterbuka-vscode-theme/
├── package.json                                # manifest ekstensi VS Code
├── themes/
│   ├── univterbuka-light-color-theme.json      # UnivTerbuka Light
│   └── univterbuka-dark-color-theme.json       # UnivTerbuka Dark
├── images/icon.png                             # ikon ekstensi (buku kuning di atas biru UT)
├── settings-snippet.json                       # cuplikan setting pendamping
├── PALETTE.md                                  # dokumentasi palet & rasional warna
├── README.md                                   # dokumen ini
└── LICENSE
```

## Kustomisasi Lanjutan

Timpa warna tertentu tanpa mengedit file tema, lewat `settings.json`:

```jsonc
{
  "workbench.colorCustomizations": {
    "[UnivTerbuka Dark]": { "editor.background": "#0A0F1C" }
  },
  "editor.tokenColorCustomizations": {
    "[UnivTerbuka Light]": {
      "comments": { "foreground": "#5A6B7F", "fontStyle": "italic" }
    }
  }
}
```



## Lisensi

MIT. Bebas dipakai & dimodifikasi untuk keperluan apa saja. Logo & identitas warna UT adalah milik Universitas Terbuka. Color theme ini adalah karya komunitas/penggemar (fanmade), tidak berafiliasi dengan Universitas Terbuka.

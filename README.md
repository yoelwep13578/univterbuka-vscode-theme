# 🎓 UnivTerbuka Theme — Color Scheme Pack untuk Visual Studio Code

Tema warna (color scheme) VS Code bernuansa **Universitas Terbuka (UT)**, dibangun dari palet resmi logo UT lalu diharmonisasikan mengikuti prinsip **HCI (Human–Computer Interaction)**, keterbacaan jangka panjang, dan rasio kontras **WCAG 2.1**.

> 📝 **Catatan nama:** Anda menulis *"UnivTerbuka Lignt"* — hampir pasti typo dari *Light*. Pack ini memakai ejaan yang benar **`UnivTerbuka Light`** agar konsisten dengan konvensi penamaan tema VS Code. Jika Anda memang ingin label persis `UnivTerbuka Lignt`, ubah field `"label"` di `package.json` dan `"name"` di file tema Light.

---

## 1. Dua Tema di Dalam Pack

| Tema | `uiTheme` | Karakter |
|---|---|---|
| **UnivTerbuka Light** | `vs` | Putih bersih, biru UT sebagai warna utama teks/UI, kuning UT hanya sebagai aksen |
| **UnivTerbuka Dark** | `vs-dark` | Hitam kebiruan (`#0B1220`), teks putih kebiruan, kuning UT bersinar sebagai aksen & fungsi |

Keduanya meliputi pewarnaan lengkap: editor, syntax highlighting (TextMate + semantic tokens), Activity Bar, Side Bar, Tab, Status Bar, Panel/Terminal, notifikasi, Git decoration, bracket matching, find/replace, IntelliSense, dan minimap.

---

## 2. Warna Dasar dari Logo UT

Acuan: *Graphic Standard Manual (GSM) Universitas Terbuka* — warna identitas UT [1](https://www.ut.ac.id/wp-content/uploads/2026/04/Graphic-Standart-Manual_UT.pdf), dan penjelasan makna logo di situs resmi UT [2](https://www.ut.ac.id/logo-ut/).

| Warna identitas | Spesifikasi resmi | Hex | Makna (resmi UT) |
|---|---|---|---|
| 🔵 **Biru UT** | Pantone® Reflex Blue C · CMYK 100-80-0-10 · RGB 3, 70, 148 | `#034694` | Kepercayaan, kebijaksanaan, kestabilan, kematangan berpikir — nilai *Integrity* |
| 🟡 **Kuning UT** | Pantone® 109 C · CMYK 0-10-100-0 · RGB 255, 222, 0 | `#FFDE00` | Imajinasi, kreativitas, kebahagiaan, kehangatan, optimisme |
| ⚫ **Hitam** | Elemen pena/teks pada logo | turunan: `#17202A` | Ketegasan, keterbacaan teks utama |
| ⚪ **Putih** | Lembaran buku pada logo | `#FFFFFF` / `#EAF0F8` | Keterbukaan ilmu, kejernihan |

## 3. Prinsip HCI & Kontras yang Diterapkan

Warna logo **tidak ditempel mentah-mentah** ke editor — itu resep tema yang norak dan melelahkan mata. Pack ini menerapkan:

### 3.1 Aturan 60–30–10
- **60%** warna netral (putih / hitam kebiruan) → latar, agar mata "beristirahat".
- **30%** biru UT & turunannya → struktur UI, keyword, fungsi.
- **10%** kuning UT → aksen. Kuning *"nge-jreng"* **hanya** muncul di tempat yang memang cocok: badge (dengan teks hitam), tab aktif (garis atas), penanda *find match*, kursor & nomor baris aktif (Dark), status remote, dan progress bar. Tidak pernah jadi warna latar besar.

### 3.2 Kuning tidak pernah jadi teks di atas putih ⚠️
Kuning murni `#FFDE00` di atas putih rasio kontrasnya hanya **1,34:1** — gagal total WCAG (minimum 4,5:1 untuk teks). Maka di Light Mode, kuning untuk *teks* digelapkan menjadi **`#7A5C00`** (6,25:1 ✅ AA), sedangkan kuning murni hanya dipakai sebagai *latar* aksen berpadu teks hitam (`#000` di atas `#FFDE00` = 15,7:1 ✅ AAA).

### 3.3 Satu warna brand, dua perilaku (adaptasi luminansi)
Biru murni `#034694` di atas latar gelap hanya 2,06:1 (tidak terbaca), jadi di Dark Mode ia **diterangkan** menjadi `#79B8FF` (9,02:1 ✅ AAA) untuk teks/keyword, sementara biru murni tetap dipakai sebagai latar tombol/seleksi dengan teks putih (9,10:1 ✅ AAA). Prinsip yang sama untuk kuning: di Dark Mode kuning murni justru ideal (14,0:1 ✅ AAA) sehingga boleh menjadi warna string/fungsi.

### 3.4 Rasio kontras terukur (WCAG 2.1)

| Pasangan warna | Mode | Rasio | Level |
|---|---|---:|---|
| `#17202A` di `#FFFFFF` (teks utama) | Light | 16,45:1 | AAA |
| `#034694` di `#FFFFFF` (keyword/link) | Light | 9,10:1 | AAA |
| `#7A5C00` di `#FFFFFF` (angka/aksen kuning-as-text) | Light | 6,25:1 | AA |
| `#000000` di `#FFDE00` (badge) | Keduanya | 15,70:1 | AAA |
| `#FFFFFF` di `#034694` (Status/Activity Bar) | Keduanya | 9,10:1 | AAA |
| `#F5F7FA`/`#EAF0F8` di `#0B1220` (teks utama) | Dark | 17,45:1 | AAA |
| `#FFDE00` di `#0B1220` (fungsi/string) | Dark | 14,00:1 | AAA |
| `#79B8FF` di `#0B1220` (keyword) | Dark | 9,02:1 | AAA |

*(AAA ≥ 7:1 · AA ≥ 4,5:1 untuk teks normal.)*

### 3.5 Prinsip HCI lain
- **Hierarki visual lewat saturasi:** elemen penting = jenuh (biru/kuning), elemen pendukung = desaturasi (abu kebiruan) — mata tahu harus melihat ke mana.
- **Konsistensi semantik lintas mode:** kuning selalu berarti "sorotan/aksen penting", biru selalu "struktur/interaksi utama" — pengguna tidak belajar ulang saat ganti mode.
- **Warna bukan satu-satunya pembawa makna:** error/warning tetap dibedakan juga oleh ikon & gaya (garis bergelombang VS Code), ramah untuk pengguna buta warna merah–hijau; warna semantik pendukung (hijau string, merah error, teal type) dipilih versi *muted*, bukan neon.
- **Menghindari kelelahan mata:** latar Dark bukan hitam pekat `#000000` (kontras ekstrem menyebabkan *halation*), melainkan hitam kebiruan `#0B1220`; latar Light memakai panel `#F2F6FB` agar batas antar-area lembut.

Palet lengkap tiap elemen ada di [`PALETTE.md`](./PALETTE.md) dan pratinjau visual di [`preview/preview.html`](../preview/preview.html).

---

## 4. Instalasi & Penggunaan

### Cara A — Install dari file `.vsix` (paling mudah, semua OS)

**Prasyarat:** VS Code terinstal. Untuk membuild `.vsix` dari source (opsional, file `.vsix` siap pakai sudah disediakan di folder proyek ini):

```bash
npm install -g @vscode/vsce   # sekali saja
cd univterbuka-vscode-theme
vsce package                  # menghasilkan univterbuka-vscode-theme-1.0.0.vsix
```

**Install-nya:**

- **Lewat GUI (Windows / macOS / Linux sama):**
  1. Buka VS Code → panel **Extensions** (`Ctrl+Shift+X` / `Cmd+Shift+X` di Mac)
  2. Klik ikon **`...`** (Views and More Actions) di kanan atas panel
  3. Pilih **Install from VSIX...** → arahkan ke `univterbuka-vscode-theme-1.0.0.vsix`
- **Lewat terminal:**
  ```bash
  # Windows (PowerShell/CMD), macOS, Linux — perintahnya sama bila `code` ada di PATH
  code --install-extension univterbuka-vscode-theme-1.0.0.vsix
  ```

**Mengaktifkan tema:**
`Ctrl+K Ctrl+T` (Windows/Linux) atau `Cmd+K Cmd+T` (macOS) → pilih **UnivTerbuka Light** atau **UnivTerbuka Dark**. Atau lewat menu: *File/Code → Preferences → Theme → Color Theme*.

### Cara B — Copy manual folder ekstensi (tanpa `.vsix`)

Salin folder `univterbuka-vscode-theme` ke folder ekstensi VS Code Anda:

| OS | Folder tujuan |
|---|---|
| **Windows** | `%USERPROFILE%\.vscode\extensions\`  → contoh: `C:\Users\<nama>\.vscode\extensions\univterbuka-vscode-theme` |
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

### Cara C — Tanpa ekstensi: tempel ke `settings.json` (cepat mencoba)

Jika hanya ingin mencoba warna editor tanpa memasang ekstensi, salin isi `settings-snippet.json` (plus blok `workbench.colorCustomizations` / `editor.tokenColorCustomizations` yang bisa Anda ekstrak dari file tema) ke Settings JSON Anda:
`Ctrl+Shift+P` / `Cmd+Shift+P` → **Preferences: Open User Settings (JSON)**. Namun **Cara A/B tetap disarankan** agar seluruh elemen UI ikut berwarna.

### Pengaturan pendamping yang disarankan

```jsonc
// settings.json
{
  "workbench.colorTheme": "UnivTerbuka Dark",   // atau "UnivTerbuka Light"
  "editor.fontFamily": "'Cascadia Code', Consolas, monospace",
  "editor.bracketPairColorization.enabled": true
}
```

### Beralih Light ↔ Dark mengikuti OS (opsional)

```jsonc
{
  "window.autoDetectColorScheme": true,
  "workbench.preferredLightColorTheme": "UnivTerbuka Light",
  "workbench.preferredDarkColorTheme": "UnivTerbuka Dark"
}
```

### Uninstall
Panel **Extensions** → cari *UnivTerbuka Theme* → **Uninstall**; atau `code --uninstall-extension univterbuka-theme.univterbuka-vscode-theme`, atau hapus foldernya dari `.vscode/extensions`.

---

## 5. Struktur Pack

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
preview/
└── preview.html                                # pratinjau visual palet & contoh kode
```

## 6. Kustomisasi Lanjutan

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
MIT — bebas dipakai & dimodifikasi untuk keperluan civitas akademika UT maupun umum. Logo & identitas warna UT adalah milik Universitas Terbuka; pack ini adalah karya komunitas/penggemar non-resmi, tidak berafiliasi dengan Universitas Terbuka.

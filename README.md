# SAMAN Kemenbud — Windows Desktop App

Aplikasi desktop Windows 11 berbasis **Electron** yang membungkus situs resmi [https://saman.kemenbud.go.id](https://saman.kemenbud.go.id) sebagai aplikasi desktop.

---

## Prasyarat

- **Node.js** LTS — [https://nodejs.org](https://nodejs.org)
- **Windows 10/11** (untuk build EXE)
- Git (opsional)

---

## Cara Menjalankan Lokal

```bash
# 1. Clone repo
git clone https://github.com/galih/saman-kemenbud.git
cd saman-kemenbud

# 2. Install dependency
npm install

# 3. Jalankan aplikasi
npm start
```

---

## Build ke Windows EXE / Installer

```bash
npm run dist-win
```

Hasil build akan ada di folder `dist/`:
- `SAMAN Kemenbud Setup x.x.x.exe` — Installer Windows (NSIS)
- `SAMAN Kemenbud x.x.x.exe` — Versi portable (tidak perlu install)

---

## Struktur Project

```
saman-kemenbud/
├── main.js          # Entry point Electron, load URL utama
├── preload.js       # Script preload untuk jendela BrowserWindow
├── package.json     # Konfigurasi project & build
├── assets/
│   └── icon.ico     # Icon aplikasi Windows (ganti dengan icon Kemenbud)
└── README.md
```

---

## Catatan

- Aplikasi ini adalah **wrapper desktop** untuk website online.
- **Koneksi internet tetap dibutuhkan** agar situs dapat dimuat.
- Link eksternal yang dibuka dari situs akan diteruskan ke browser default.
- Jika ada popup atau halaman login khusus yang tidak berfungsi, tambahkan konfigurasi `webContents` di `main.js`.

---

## Lisensi

Disediakan untuk keperluan internal. Situs SAMAN adalah milik Kementerian Kebudayaan Republik Indonesia.

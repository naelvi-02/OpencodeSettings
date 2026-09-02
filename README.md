# 🚀 OpenCode Settings & Model/Router Manager

Aplikasi ringan (zero-dependency) untuk mengatur, menyesuaikan, dan mengganti model AI serta router/provider pada `opencode.json` dan `oh-my-opencode-slim.json` tanpa perlu edit manual file JSON.

---

## �( Fitur Utama

1. **One-Click Mass Router Switcher**
   - Alihkan **semua agent & main model** dari satu router (contoh: `9router`) ke router lain (contoh: `omniroute`) dalam 1 klik.

2. **Oh-My-OpenCode-Slim Agent Matrix**
   - Atur model dan variant (`high`, `medium`, `low`) untuk setiap subagent:
     - `orchestrator`
     - `oracle`
     - `council`
     - `librarian`
     - `explorer`
     - `designer`
     - `fixer`
     - `observer`

3. **Preset Manager**
   - Pilih dan aktifkan preset yang sudah ada (misal: `naelvi-grok`, `naelvi-cmc`) atau buat preset baru langsung dari UI.

4. **Router & Model Editor**
   - Kelola `baseURL`, `apiKey`, serta tambah/hapus model yang terdaftar pada provider.

5. **Auto Backup & 1-Click Restore**
   - Setiap kali menyimpan konfigurasi, snapshot otomatis disimpan di folder `.backups/`. Bisa di-restore kapanpun.

6. **Dual Interface (Web GUI & CLI)**
   - Dashboard Web modern (port 3928) + Interactive CLI untuk user terminal.

---

## 🚀 Cara Menjalankan

### 1. Melalui Web Dashboard (Recommended)
```bash
# Jalankan server (otomatis buka browser)
node server.js

# Atau klik dua kali start.bat (Windows)
start.bat
```
Buka di browser: `http://127.0.0.1:3928`

### 2. Melalui Interactive CLI
```bash
node cli.js
```

### 3. Global Shortcut (Windows)
Jika sudah terpasang di PATH, kamu bisa langsung ketik:
```cmd
opencode-manager
# atau
opencode-config
```

---

## 📁 Struktur Project
```
OpencodeSettings/
├── server.js               # Zero-dependency Node.js HTTP Server & REST API
├── cli.js                 # Interactive terminal switcher
├── start.bat               # Windows one-click launcher
├── public/
│   └── index.html         # Single-Page Tailwind Dark UI
├── README.md               # Dokumentasi utama
├── blueprint.md             # Arsitektur & design system
├── workflow.md             # Panduan workflow & operasi
└── workingagreement.md  # Convention & standard kode
```

---

## 🔒 Security & Backup Guarantee
- Aplikasi hanya berjalan lokal pada `127.0.0.1:3928`.
- Tidak ada telemetry atau koneksi ke server luar.
- Setiap perubahan file dilakukan secara atomik dengan auto-backup bertimestamp.

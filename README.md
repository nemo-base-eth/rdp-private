# 🖥️ Private RDP Server

Remote Desktop Protocol (RDP) server gratis lewat GitHub Actions. Tinggal run workflow, langsung bisa connect.

---

## 🔑 Login

| Field | Value |
|-------|-------|
| **Username** | `hkpBHMzC6u9FY` |
| **Password** | `TMq2sbT5GrXNnQ0D1OUa` |

> ⚠️ Ganti password di `.github/workflows/rdp.yml` kalau mau share repo ini.

---

## 🚀 Cara Pakai

### Langkah 1: Jalankan Workflow

1. Buka repo ini di GitHub
2. Klik tab **Actions**
3. Pilih **RDP Server**
4. Klik tombol **Run workflow**
5. Masukkan lama runtime (default: 4 jam)
6. Klik **Run workflow**

### Langkah 2: Cari Tunnel URL

1. Tunggu workflow jalan (biasanya 1-2 menit)
2. Klik workflow yang đang jalan
3. Cari step **Start RDP tunnel**
4. Cari baris `Tunnel URL: https://xxxx.trycloudflare.com`
5. Copy URL itu

### Langkah 3: Connect via RDP

Buka RDP client di device kamu:

| OS | Cara Buka |
|----|-----------|
| **Windows** | Tekan `Win + R` → ketik `mstsc` → Enter |
| **macOS** | Download "Microsoft Remote Desktop" di App Store |
| **Linux** | install `remmina` atau `xfreerdp` |

Lalu:
1. Di kolom **Computer**, paste tunnel URL (contoh: `https://abc123.trycloudflare.com`)
2. Klik **Connect**
3. Masukkan username: `hkpBHMzC6u9FY`
4. Masukkan password: `TMq2sbT5GrXNnQ0D1OUa`
5. Klik **OK**

---

## 📦 Software yang Terinstall

Semua ini otomatis terinstall saat workflow jalan:

| Software | Kegunaan |
|----------|----------|
| **VS Code** | Code editor |
| **Python** | Programming |
| **Node.js LTS** | JavaScript runtime |
| **7-Zip** |压缩/解压 file |

---

## ⚙️ Konfigurasi

### Ganti Password

Edit file `.github/workflows/rdp.yml`:

```yaml
env:
  RDP_USERNAME: username_baru kamu
  RDP_PASSWORD: password_baru kamu
```

### Ganti Durasi

Waktu default adalah 4 jam. Maksimal 6 jam (360 menit).

Untuk ganti, tinggal input **duration** waktu run workflow.

---

## 🛠️ Troubleshooting

### tunnel URL gak muncul di logs?

1. Tunggu 1-2 menit lagi
2. Scroll ke atas di logs, cari baris `Tunnel URL`
3. Kalau masih gak ada, click **Re-run all jobs**

### RDP gak bisa connect?

1. Pastikan pakai tunnel URL yang benar (bukan IP biasa)
2. Cek firewall: harusnya sudah auto-allow
3. Coba restart RDP client
4. Pastikan koneksi internet stabil

### Error "Password incorrect"?

1. Pastikan copy paste password dengan benar: `TMq2sbT5GrXNnQ0D1OUa`
2. Jangan ada spasi di awal/akhir
3. Coba ganti password di workflow, lalu run ulang

---

## 🔒 Security

- Repo ini **private** — cuma kamu yang bisa akses
- Password ada di file workflow — ganti kalau mau share
- Tunnel pakai Cloudflare — otomatis HTTPS
- User RDP punya权限Administrator

---

## 💡 Tips

1. **Simpen tunnel URL** —Expired kalau workflow stop
2. **Run berulang** —Setiap run dapet tunnel URL baru
3. **Ganti password** —Kalau mau share repo ini ke orang lain
4. **cek billing** —GitHub Actions punya limit gratis

---

## ❓ FAQ

**Q: Berapa lama bisa jalan?**
A: Maksimal 6 jam per run. Bisa run ulang kalau mau lebih lama.

**Q: Gratis?**
A: Ya, selama masih dalam limit GitHub Actions (2000 menit/bulan untuk free tier).

**Q: Bisa dari HP?**
A: Bisa, tapi harus install RDP client di HP (Microsoft Remote Desktop).

**Q: Aman?**
A: Ya, repo private + Cloudflare tunnel + cuma kamu yang tau password.

---

## 📝 Catatan

- Setiap run = fresh install (software hilang kalau run ulang)
- GitHub Actions limit: 2000 menit/bulan (free tier)
- Jangan share password kalau repo ini private
- Tunnel URL expire kalau workflow stop

---

Made with ❤️ by nemoobc

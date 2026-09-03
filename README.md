# 🖥️ Private RDP Server

Windows RDP via GitHub Actions + Tailscale.

---

## 🔑 Credentials

| Field | Value |
|-------|-------|
| **Username** | `hkpBHMzC6u9FY` (tetap) |
| **Password** | random tiap run, liat di logs blok `RDP SIAP` |

---

## 🚀 Cara Pakai

### Step 1: Run Workflow

1. Buka repo → **Actions** → **RDP Server**
2. Klik **Run workflow**
3. Set durasi (default 4 jam)

### Step 2: Login Tailscale

1. Di workflow logs, cari baris yang ada link `https://login.tailscale.com/a/...`
2. Buka link itu di browser
3. Login akun Tailscale kamu
4. Tunggu sampai connected

### Step 3: Connect RDP

1. Cari **Tailscale IP + password** di logs blok `RDP SIAP` (contoh: `100.x.x.x`)
2. Buka **Remote Desktop** (`mstsc`)
3. Masukkan IP itu
4. Login dengan username tetap + password random dari logs itu

---

## 📋 Output di Logs

```
========================================
RDP SIAP
IP       : 100.x.x.x
Username : hkpBHMzC6u9FY
Password : random-16-char
========================================
```

---

## ⚙️ Config

Username tetap di `.github/workflows/rdp.yml`:

```yaml
env:
  RDP_USERNAME: hkpBHMzC6u9FY
```

Password auto-random 16 char tiap run (huruf+angka+`!@#`).

---

## ❓ FAQ

**Q: Berapa lama?**
A: Default 4 jam, max 6 jam.

**Q: Gratis?**
A: Ya, Tailscale free tier + GitHub Actions free tier.

**Q: Bisa dari HP?**
A: Ya, install Tailscale + RDP client di HP.

---

Made with ❤️ by nemoobc

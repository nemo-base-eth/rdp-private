# 🖥️ Private RDP Server

Windows RDP via GitHub Actions + Tailscale.

---

## 🔑 Credentials

| Field | Value |
|-------|-------|
| **Username** | `hkpBHMzC6u9FY` |
| **Password** | `TMq2sbT5GrXNnQ0D1OUa` |

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

1. Cari **Tailscale IP** di logs (contoh: `100.x.x.x`)
2. Buka **Remote Desktop** (`mstsc`)
3. Masukkan IP itu
4. Login dengan credentials di atas

---

## 📋 Output di Logs

```
========================================
Tailscale IP: 100.x.x.x
Port        : 3389
Username    : hkpBHMzC6u9FY
Password    : TMq2sbT5GrXNnQ0D1OUa
========================================
```

---

## ⚙️ Config

Edit `.github/workflows/rdp.yml`:

```yaml
env:
  RDP_USERNAME: username_baru
  RDP_PASSWORD: password_baru
```

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

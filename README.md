# 🖥️ Private RDP Server

Windows RDP via GitHub Actions + Tailscale.

---

## 🔑 Credentials

| Field | Value |
|-------|-------|
| **Username** | `hkpBHMzC6u9FY` (tetap) |
| **Password** | random tiap run, lihat di logs |

---

## 🚀 Cara Pakai

### Step 1: Setup Auth Key (1x saja)

1. Buka https://login.tailscale.com/admin/settings/keys
2. Generate **pre-auth key** (Reusable + Ephemeral)
3. Buka repo → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**
4. Name: `TAILSCALE_AUTH_KEY` → paste key

### Step 2: Run Workflow

1. Buka repo → **Actions** → **RDP Server**
2. Klik **Run workflow**
3. Set durasi (default 4 jam)

### Step 3: Connect RDP

1. Lihat IP + password di logs blok output
2. Buka **Remote Desktop** (`mstsc`)
3. Masukkan IP:3389
4. Login dengan username + password dari logs

---

## ⚙️ Config

Username tetap di `.github/workflows/rdp.yml`:

```yaml
env:
  RDP_USERNAME: hkpBHMzC6u9FY
```

Password auto-random 16 char tiap run.

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

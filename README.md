# 🖥️ Private RDP Server

Remote Desktop via GitHub Actions + Chrome Remote Desktop.

---

## 🔑 Login

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

### Step 2: Setup Chrome Remote Desktop

1. Buka https://remotedesktop.google.com/access
2. Login Google account kamu
3. Klik **Set up remote access**
4. Download & install host (kalau belum)
5. Set PIN: `TMq2sbT5GrXNnQ0D1OUa`
6. Computer name: sesuai nama machine di logs

### Step 3: Connect

1. Buka https://remotedesktop.google.com/access
2. Login Google account
3. Klik computer yang sudah di-setup
4. Masukkan PIN

---

## 📋 Credentials

```
Username: hkpBHMzC6u9FY
Password: TMq2sbT5GrXNnQ0D1OUa
```

---

## ⚙️ Config

Edit `.github/workflows/rdp.yml` untuk ganti:

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
A: Ya, selama masih dalam GitHub Actions limit.

**Q: Bisa dari HP?**
A: Ya, bisa via Chrome Remote Desktop app.

---

Made with ❤️ by nemoobc

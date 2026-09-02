# Private RDP + Tailscale

Remote Desktop server via GitHub Actions with Tailscale VPN.

## Credentials

| Field | Value |
|-------|-------|
| **Username** | `hkpBHMzC6u9FY` |
| **Password** | `TMq2sbT5GrXNnQ0D1OUa` |

> ⚠️ Change this password in `.github/workflows/rdp.yml` if needed.

## Setup

### 1. Get Tailscale Auth Key

1. Login to [Tailscale](https://login.tailscale.com/)
2. Go to **Settings** → **Keys**
3. Generate an **Auth Key** (one-time use recommended)

### 2. Run the Workflow

1. Go to **Actions** tab
2. Select **RDP Server**
3. Click **Run workflow**
4. Enter your Tailscale Auth Key
5. Set duration (default: 4 hours)

### 3. Connect via RDP

Once the workflow is running:

1. Check the workflow logs for the Tailscale IP
2. Open your RDP client:
   - **Windows**: `mstsc` or Remote Desktop Connection
   - **macOS**: Microsoft Remote Desktop (App Store)
   - **Linux**: `remmina` or `xfreerdp`
3. Connect to: `<TAILSCALE_IP>:3389`
4. Login with credentials above

## What's Installed

- Google Chrome
- VS Code
- Python
- Node.js LTS
- 7-Zip

## Notes

- Session runs for the specified duration (default 4 hours)
- RDP is only accessible via Tailscale network
- Your GitHub Actions minutes will be consumed
- Windows Server latest is used as the runner

## Security

- Password is in `rdp.yml` — change it if sharing repo access
- Tailscale ensures only your devices can connect
- Consider using Tailscale ACLs for additional restrictions

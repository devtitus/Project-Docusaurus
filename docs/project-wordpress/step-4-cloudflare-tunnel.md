---
sidebar_position: 6
---

## ☁️ 3. Expose Localhost Using Cloudflare Tunnel

### ✅ Step 1: Install Cloudflared CLI

Download from:
🔗 [https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/installation/](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/installation/)

Place `cloudflared.exe` in:

```
C:\Program Files (x86)\cloudflared
```

### ✅ Step 2: Authenticate Tunnel

Run CMD or PowerShell:

```bash
cloudflared tunnel login
```

Follow browser steps to authenticate and select your domain.

### ✅ Step 3: Create Tunnel

```bash
cloudflared tunnel create blogs-tunnel
```

This creates a tunnel ID and credentials JSON file.

### ✅ Step 4: Configure Tunnel

Create file:

```
C:\Program Files (x86)\cloudflared\config.yml
```

Content:

```yaml
tunnel: blogs-tunnel
credentials-file: C:\Users\<YourUser>\.cloudflared\blogs-tunnel.json

ingress:
  - hostname: blogs.portwork.site
    service: http://localhost:80
  - service: http_status:404
```

Replace `<YourUser>` with your Windows username.

### ✅ Step 5: Add DNS Record in Cloudflare

Go to:
🔗 [https://dash.cloudflare.com](https://dash.cloudflare.com)

DNS > Add record:

- Type: `CNAME`
- Name: `blogs`
- Target: `<your-tunnel-id>.cfargotunnel.com`
- Proxy status: Orange cloud (on)

---

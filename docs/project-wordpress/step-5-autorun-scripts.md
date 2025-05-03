---
sidebar_position: 7
title: Step 5 - Autorun Scripts
---

## 📦 4. Run Tunnel Automatically at Startup

### ✅ Option A: Silent Background Script (VBScript)

#### 📄 File: `start-cloudflared-silent.vbs`

```vbscript
Set oShell = CreateObject("WScript.Shell")
oShell.Run """C:\Program Files (x86)\cloudflared\start-cloudflared.bat""", 0, False
```

Save to:

```
C:\Users\<YourUser>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
```

#### 📄 File: `start-cloudflared.bat`

```bat
@echo off
cd /d "C:\Program Files (x86)\cloudflared"
cloudflared.exe tunnel run blogs-tunnel
```

This will start the tunnel silently every time your PC boots.

### ✅ Option B: Manual Console Mode (For Debugging)

Create shortcut:

```bat
@echo off
cd "C:\Program Files (x86)\cloudflared"
cloudflared.exe tunnel run blogs-tunnel
```

Save as:

```
C:\Users\<YourUser>\Desktop\Run Cloudflare Tunnel (Show Console).bat
```

Double-click to run manually with logs visible.

---

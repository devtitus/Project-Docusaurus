---
sidebar_position: 9
title: Checklist and Tips
---

## 📌 6. Final Checklist

| Task                                     | Status |
| ---------------------------------------- | ------ |
| Installed XAMPP                          | ✅     |
| Installed WordPress                      | ✅     |
| Set dynamic URLs in wp-config.php        | ✅     |
| Created Cloudflare Tunnel                | ✅     |
| Configured DNS in Cloudflare             | ✅     |
| Created silent startup script (.vbs)     | ✅     |
| Tested access via `blogs.portwork.site`  | ✅     |
| Optional: Fixed redirects and permalinks | ✅     |

---

## 🧠 Tips

- Use `hosts` file to test locally with domain:
  ```
  127.0.0.1 blogs.portwork.site
  ```
- Always keep `cloudflared.exe` updated.
- Monitor logs by running tunnel manually.

---

## 🚀 You're Done!

Your WordPress site is now:

- Fully accessible locally
- Live online via `https://blogs.portwork.site`
- Auto-starting on boot
- Easy to maintain and develop

---
sidebar_position: 8
title: Optional Fixes
---

## 🧰 5. Optional: Fix Redirect Issues

If you're seeing redirect loops:

### ✅ Reset Site URLs via Database

In phpMyAdmin → `wp_options` table:

| option_name | value                         |
| ----------- | ----------------------------- |
| `siteurl`   | `https://blogs.portwork.site` |
| `home`      | `https://blogs.portwork.site` |

Or reset permalinks:
Dashboard > Settings > Permalinks → Choose "Post name" → Save

---

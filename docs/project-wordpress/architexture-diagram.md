---
sidebar_position: 2
title: Architecture Diagram
---

## 📐 Hosting Architecture Diagram

```
+------------------+       +---------------------+
|                  | HTTPS |                     |
|  Public Internet <-------> Cloudflare Tunnel   |
|                  |       | Tunnel: blogs-tunnel|
+--------+---------+       +----------+----------+
         |                            |
         |                            |
         |                            |
+--------v---------+       +----------v----------+
|                  | HTTP  |                     |
|  Your Laptop     <------->  Local WordPress    |
|  (XAMPP Server)  |       |  (Apache + MySQL)   |
|                  |       |  Running on Port 80 |
+------------------+       +---------------------+
```

---

---
sidebar_position: 5
---

## 🔁 2. Configure Dynamic URLs in WordPress

Edit file:

```
C:\xampp\htdocs\wordpress\wp-config.php
```

Add just before `/* That's all, stop editing! */`:

```php
if (!defined('WP_HOME') && !defined('WP_SITEURL')) {
    if ($_SERVER['HTTP_HOST'] == 'localhost' || $_SERVER['HTTP_HOST'] == '127.0.0.1') {
        define('WP_HOME', 'http://localhost/wordpress');
        define('WP_SITEURL', 'http://localhost/wordpress');
    } else {
        $protocol = (!empty($_SERVER['HTTPS']) && $_SERVER['HTTPS'] !== 'off') ? "https://" : "http://";
        define('WP_HOME', $protocol . $_SERVER['HTTP_HOST']);
        define('WP_SITEURL', $protocol . $_SERVER['HTTP_HOST']);
    }
}
```

This ensures WordPress works both locally and via domain.

---

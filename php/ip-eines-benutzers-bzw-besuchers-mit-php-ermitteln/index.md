---
title: IP eines Benutzers/Besuchers mit PHP ermitteln
---

## IP eines Benutzers/Besuchers mit PHP ermitteln

Das folgende Beispiel zeigt, wie man mit PHP die IP eines Benutzers/Besuchers ermittelt:

```php
<?php
  $ip = '';

  if (empty($_SERVER['HTTP_CLIENT_IP']) === false) {
    $ip = $_SERVER['HTTP_CLIENT_IP'];
  } elseif (empty($_SERVER['HTTP_X_FORWARDED_FOR']) === false) {
    $ip = $_SERVER['HTTP_X_FORWARDED_FOR'];
  } elseif (empty($_SERVER['REMOTE_ADDR']) === false) {
    $ip = $_SERVER['REMOTE_ADDR'];
  }
?>
```

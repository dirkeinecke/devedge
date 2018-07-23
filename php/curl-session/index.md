---
title: cURL-Session
---

# cURL-Session

Beispiel #1

```php
<?php
  // cURL-Session initialisieren
  $res_ch = curl_init('http://www.google.de/');

  // cURL-Session ausführen
  curl_exec($res_ch);

  // Gibt die letzte Fehlernummer zurück
  if ( !curl_errno($res_ch) ) {
    // Informationen zu einem bestimmten Transfer abfragen
    $info = curl_getinfo($res_ch);
    echo 'Took ' . $info['total_time'] . ' seconds to send a request to ' . $info['url'];
  }

  // cURL-Session beenden
  curl_close($res_ch);
?>
```

### Weiterführende Informationen

- [PHP-Dokumentation: curl_init](http://de2.php.net/curl_init){:target="_blank"}
- [PHP-Dokumentation: curl_exec](http://de2.php.net/curl_exec){:target="_blank"}
- [PHP-Dokumentation: curl_errno](http://de2.php.net/curl_errno){:target="_blank"}
- [PHP-Dokumentation: curl_getinfo](http://de2.php.net/curl_getinfo){:target="_blank"}
- [PHP-Dokumentation: curl_close](http://de2.php.net/curl_close){:target="_blank"}

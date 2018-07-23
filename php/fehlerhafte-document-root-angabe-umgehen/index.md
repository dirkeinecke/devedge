---
title: Fehlerhafte DOCUMENT_ROOT-Angabe umgehen
---

## Fehlerhafte DOCUMENT_ROOT-Angabe umgehen

Wenn die superglobale Server-Variable $_SERVER['DOCUMENT_ROOT'] keinen oder einen falschen Wert beinhaltet, dann kann man den richtigen Wert wie folgt setzen:

```php
<?php
  preg_match_all("/\/{1,}/", $_SERVER['SCRIPT_NAME'], $arr_matches); // doppelte (oder mehr) Slashes finden
  rsort($arr_matches[0]);
  if (is_array($arr_matches) && 0 < count($arr_matches)) {
    $_SERVER['SCRIPT_NAME'] = str_replace($arr_matches[0], '/', $_SERVER['SCRIPT_NAME']); // doppelte (oder mehr) Slashes ersetzen
  }
  $_SERVER['DOCUMENT_ROOT'] = (string) substr($_SERVER["SCRIPT_FILENAME"], 0, -(strlen($_SERVER['SCRIPT_NAME'])));
?>
```

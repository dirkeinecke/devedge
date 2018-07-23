---
title: Dateiname bereinigen
---

## Dateiname bereinigen

Hinweis: Es werden alle Dateinamen in Kleinbuchstaben umgewandelt, da es Betriebssysteme gibt, die im Dateisystem nicht zwischen Groß- und Kleinschreibung unterscheiden. 

```php
<?php
  function cleanup_filename ($str_filename) {
    $arr_before = array('ü', 'ö', 'ä', 'ß');
    $arr_after = array('ue', 'oe', 'ae', 'ss');
    $str_filename = str_replace($arr_before, $arr_after, $str_filename);
    $str_filename = preg_replace("/[^a-z0-9-.]/", '-', strtolower ($str_filename));
    return $str_filename;
  }
?>
```

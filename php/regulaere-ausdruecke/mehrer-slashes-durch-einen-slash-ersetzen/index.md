---
title: Mehrer Slashes durch einen Slash ersetzen
---

## Mehrer Slashes durch einen Slash ersetzen

```php
<?php
  $str_subject = (string) 'Das ist // ein ///// Text.';

  preg_match_all("/\/{1,}/", $str_subject, $arr_matches);
  rsort($arr_matches[0]);

  if (is_array($arr_matches) && 0 < count($arr_matches)) {
    $str_subject = str_replace($arr_matches[0], '/', $str_subject);
  }

  echo $str_subject; // Ausgabe: Das ist / ein / Text.
?>
```

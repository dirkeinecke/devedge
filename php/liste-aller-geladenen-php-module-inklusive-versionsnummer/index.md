---
title: Liste aller geladenen PHP-Module inklusive Versionsnummer
---

## Liste aller geladenen PHP-Module inklusive Versionsnummer

Das folgende Beispiel zeigt, wie man sich eine Liste aller geladenen PHP-Module inklusive deren Versionsnummer ausgeben lassen kann.

```php
<?php
  $loaded_extensions = get_loaded_extensions();

  natcasesort($loaded_extensions);

  echo '<ul>';
  foreach ($loaded_extensions as $loaded_extension) {
    echo '<li>', (phpversion($loaded_extension) !== false ? $loaded_extension.' ('.phpversion($loaded_extension).')' : $loaded_extension), '</li>';
  }
  echo '</ul>';
?>
```

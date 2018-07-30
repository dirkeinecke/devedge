---
title: Komfortabler Helper für die Funktion print_r()
---

## Komfortabler Helper für die Funktion print_r()

Der folgende Helper stellt eine neue Funktion `p_r()` zur Verfügung. Diese Funktion setzt um die Ausgabe der Funktion `print_r()` zusätzlich noch das `<pre>`-Tag. Dies erleichtert die das Lesen der Ausgabe.

Erstellen Sie im Verzeichnis "application/helpers" eine neue Datei mit dem Namen "MY_array_helper.php" mit dem unten gezeigten Quellcode. Den Helper laden Sie dann mittels `$this->load->helper('array');`. Danach kann man anstelle der Funktion `print_r()` die neue Funktion `p_r()` verwenden.

```php
<?php if ( ! defined('BASEPATH')) exit('No direct script access allowed');

  if (function_exists('element') === FALSE) {
    function p_r($array) {
      echo '<pre>';
      print_r($array);
      echo '</pre>';
    }
  }

/* End of file MY_array_helper.php */
/* Location: ./application/helpers/MY_array_helper.php */
```

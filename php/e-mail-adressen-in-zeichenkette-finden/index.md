---
title: E-Mail-Adressen in Zeichenkette (String) finden
---

## E-Mail-Adressen in Zeichenkette (String) finden

Mit Hilfe der folgenden PHP-Funktion können Sie E-Mail-Adressen innerhalb einer Zeichenkette finden.

```php
<?php
  function extract_email_addresses($string) {
    $string = strip_tags($string);
    $email_addresses = array();

    foreach (preg_split('/\s/', $string) as $token) {
      $email_address = filter_var(filter_var($token, FILTER_SANITIZE_EMAIL), FILTER_VALIDATE_EMAIL);
      if ($email_address !== FALSE) {
        $email_addresses[] = $email_address;
      }
    }

    return $email_addresses;
  }
?>
```

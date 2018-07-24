---
title: Syntax einer E-Mail-Adresse mit PHP prüfen
---

## Syntax einer E-Mail-Adresse mit PHP prüfen

```php
<?php
  function check_email_address($email_address) {
    if ($email_address !== '') {
      $result = filter_var($email_address, FILTER_VALIDATE_EMAIL);

      if ($result === false) {
        return false;
      } else {
        return true;
      }
    } else {
      return true;
    }
  }

  if (check_email_address($email_address) === false) {
    // E-Mail-Adresse ist syntaktisch falsch
  }

?>
```

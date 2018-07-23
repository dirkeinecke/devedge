---
title: Testen ob ImageMagick installiert ist
---

## Testen ob ImageMagick installiert ist

Das folgende Beispiel zeigt, wie man testen kann, ob ImageMagick installiert ist.

```php
<?php
  if (function_exists('NewMagickWand') === true) {
    echo 'ImageMagick is running.';
  } else {
    echo 'ImageMagick is NOT running.';
  }
?>

### Weiterführende Informationen

- [Website von ImageMagick](http://www.imagemagick.org/){:target="_blank"}

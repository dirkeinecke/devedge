---
title: Scrollen beim Mobile Webkit verhindern
---

## Scrollen beim Mobile Webkit verhindern

Das folgende Beispiel zeigt, wie man das Schollen beim Mobile Webkit verhindern kann.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0">
    <title></title>
    <script>
      document.addEventListener('touchmove', function (e) { e.preventDefault(); }, false);
    </script>
  </head>
  <body>
  </body>
</html>
```

---
title: iPhone und iPod touch Detection mit JavaScript
---

## iPhone und iPod touch Detection mit JavaScript

```html
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8">
    <title>iPhone and iPod touch detection with JavaScript</title>
    <style type="text/css">
      * {
        font-size: 30px;
      }
    </style>

    <script>
      function detect_iPhone() {
        var return_value = false;
        if (navigator.userAgent.match(/iPhone/i) || navigator.userAgent.match(/iPod/i)) {
          return_value = true;
        }
      }
    </script>
  </head>
  <body>
    <script>
      if (detect_iPad() == true) {
        document.write('This is an iPhone or iPod touch.');
      } else {
        document.write('This is not an iPhone or iPod touch.');
      }
    </script>
  </body>
</html>
```

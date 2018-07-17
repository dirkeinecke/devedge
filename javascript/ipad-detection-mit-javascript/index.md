## iPad Detection mit JavaScript

```html
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
    <title>iPad detection with JavaScript</title>
    <style type="text/css">
      * {
        font-size: 30px;
      }
    </style>

    <script>
      function detect_iPad() {
        var return_value = false;
        if (navigator.userAgent.match(/iPad/i)) {
          return_value = true;
        }
      }
    </script>
  </head>
  <body>
    <script>
      if (detect_iPad() == true) {
        document.write('This is an iPad.');
      } else {
        document.write('This is not an iPad.');
      }
    </script>
  </body>
</html>
```

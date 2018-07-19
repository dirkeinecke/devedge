---
title: Dateiname bereinigen
---

## Dateiname bereinigen

```javascript
function cleanUpFilename(filename) {
  var newFileName = filename;
  newFileName = newFileName.replace(new RegExp('[^A-Za-z0-9\\-_.ÄäÖöÜüß ]', 'g'), '');
  newFileName = newFileName.replace(new RegExp('Ä', 'g'), 'Ae');
  newFileName = newFileName.replace(new RegExp('ä', 'g'), 'ae');
  newFileName = newFileName.replace(new RegExp('Ö', 'g'), 'Oe');
  newFileName = newFileName.replace(new RegExp('ö', 'g'), 'oe');
  newFileName = newFileName.replace(new RegExp('Ü', 'g'), 'Ue');
  newFileName = newFileName.replace(new RegExp('ü', 'g'), 'ue');
  newFileName = newFileName.replace(new RegExp('ß', 'g'), 'ss');
  newFileName = newFileName.replace(new RegExp(' ', 'g'), '-');

  return newFileName;
}
```

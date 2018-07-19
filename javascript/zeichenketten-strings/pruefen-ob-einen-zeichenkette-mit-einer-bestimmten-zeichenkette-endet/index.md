---
title: Prüfen ob einen Zeichenkette mit einer bestimmten Zeichenkette endet
---

## Prüfen ob einen Zeichenkette mit einer bestimmten Zeichenkette endet

Das folgende Beispiel zeigt wie man prüfen kann, ob eine Zeichenkette (String) mit einer bestimmten Zeichenkette (String) endet.

```javascript
String.prototype.endsWith = function(suffix) {
  return this.match(suffix+"$") == suffix;
};

if ('www.google.de'.endsWith('.de') == true) {
  //
}
```

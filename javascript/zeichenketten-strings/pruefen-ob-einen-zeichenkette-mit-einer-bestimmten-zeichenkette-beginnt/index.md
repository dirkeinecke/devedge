---
title: Prüfen ob einen Zeichenkette mit einer bestimmten Zeichenkette beginnt
---

## Prüfen ob einen Zeichenkette mit einer bestimmten Zeichenkette beginnt

Das folgende Beispiel zeigt wie man prüfen kann, ob eine Zeichenkette (String) mit einer bestimmten Zeichenkette (String) beginnt.

```javascript
String.prototype.startsWith = function(prefix) {
  return this.indexOf(prefix) === 0;
}

if ('www.google.de'.startsWith('www') == true) {
  //
}
```

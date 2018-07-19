---
title: Gepunktete Linie bei Input-Buttons entfernen
---

## Gepunktete Linie bei Input-Buttons entfernen

```css
button::-moz-focus-inner,
input[type="reset"]::-moz-focus-inner,
input[type="button"]::-moz-focus-inner,
input[type="submit"]::-moz-focus-inner,
input[type="file"] > input[type="button"]::-moz-focus-inner {
  border: none;
}
```

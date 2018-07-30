---
title: Darstellungsoptionen für den Schreibtisch ermitteln
---

## Darstellungsoptionen für den Schreibtisch ermitteln

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man die Darstellungsoptionen für den Schreibtisch ermitteln möchte, dann kann man dies so tun, wie es die folgenden Beispiele exemplarisch zeigen.

### Am Raster ausrichten

```applescript
set iconSize to (get word 3 of ¬
  (do shell script "defaults read com.apple.finder DesktopViewOptions | grep ArrangeBy"))
display dialog iconSize buttons ("OK") default button 1
```

### Textgröße

```applescript
set iconSize to (get word 3 of ¬
  (do shell script "defaults read com.apple.finder DesktopViewOptions | grep FontSize"))
display dialog iconSize buttons ("OK") default button 1
```

### Symbolgröße

```applescript
set iconSize to (get word 3 of ¬
  (do shell script "defaults read com.apple.finder DesktopViewOptions | grep IconSize"))
display dialog iconSize buttons ("OK") default button 1
```

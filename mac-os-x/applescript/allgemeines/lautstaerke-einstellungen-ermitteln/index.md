---
title: Lautstärke-Einstellungen ermitteln
---

## Lautstärke-Einstellungen ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Einstellungen für die Lautstärke ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
get volume settings
-- Ergebnis z.B.: {output volume:26, input volume:53, alert volume:50, output muted:true}
```

Die einzelnen Werte der Einstellungen für die Lautstärke kann man wie folgt ermitteln:

### Gesamtlautstärk (output volume)

```applescript
get output volume of (get volume settings)
-- Ergebnis z.B.: 26
```

### Eingangslautstärke (input volume)

```applescript
get input volume of (get volume settings)
-- Ergebnis z.B.: 53
```

### Warton-Lautstärke (alert volume)

```applescript
get alert volume of (get volume settings)
-- Ergebnis z.B.: 50
```

### Ton aus (output muted)

```applescript
get output muted of (get volume settings)
-- Ergebnis z.B.: true
```

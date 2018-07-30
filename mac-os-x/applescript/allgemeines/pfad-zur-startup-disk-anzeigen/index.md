---
title: Pfad zur startup disk anzeigen
---

## Pfad zur startup disk anzeigen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man den Pfad zur startup disk benötigt und diesen nicht fest in den Quellcode schreiben möchte (wenn der User diesen zum Beispiel geändert hat und er also nicht mehr "Macintosh HD" ist), dann kann man dies wie folgt machen:

```applescript
set myPath to path to startup disk as text
display dialog myPath buttons {"OK"} default button 1
```

Die Konvertierung "`as text`" in der ersten Zeile ist nur dann notwendig, wenn man sich den Pfad zum Beispiel mit "`display dialog`" ausgeben lassen möchte. 

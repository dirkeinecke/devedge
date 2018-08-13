---
title: Den Betreff einer neuen E-Mail in Apple Mail setzen
---

## Den Betreff einer neuen E-Mail in Apple Mail setzen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn Sie den Betreff einer neuen E-Mail im Programm "Mail" setzen möchten, dann können Sie dies wie folgt tun:

```applescript
tell application "Mail"
  set subject of outgoing message ¬
    1 to "Hier steht der Betreff"
end tell
```

Beachten Sie, dass das Fenster für eine neue E-Mail bereits offen sein muss. 

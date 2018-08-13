---
title: JavaScript ausführen
---

## JavaScript ausführen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man aus AppleScript heraus ein JavaScript im Browser Safari ausführen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Safari"
  activate
  do JavaScript "document.title = 'Mac DevEdge'" in document 1
end tell
```applescript

Das Ergebnis könnte dann zum Beispiel so aussehen:


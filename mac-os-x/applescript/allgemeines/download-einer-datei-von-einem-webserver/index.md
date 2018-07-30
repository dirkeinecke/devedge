---
title: Download einer Datei von einem Webserver
---

## Download einer Datei von einem Webserver

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Um eine Datei von einem Webserver auf Ihre lokale Festplatte herunterzuladen können Sie folgendes Script verwenden:

```applescript
tell application "URL Access Scripting"
  download "http://www.server.de/Datei.pdf" to ¬
    file "Macintosh HD:Datei.pdf" replacing yes ¬
    with progress and unpacking
end tell
```

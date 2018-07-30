---
title: Upload einer Datei auf einen Webserver
---

## Upload einer Datei auf einen Webserver

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Um eine Datei auf einen Webserver hochzuladen können Sie folgendes Script verwenden:

```applescript
tell application "URL Access Scripting"
  upload file "Macintosh HD:Datei.pdf" to ¬
    "ftp://username:password@ftp.server.de" replacing yes ¬
    with progress without binhexing
end tell
```

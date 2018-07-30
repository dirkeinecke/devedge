---
title: Inhalt einer Textdatei lesen
---

## Inhalt einer Textdatei lesen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wie man den Inhalt einer Textdatei auslesen kann zeigt folgendes Script:

```applescript
set file_path to path to desktop folder as string
set file_path to file_path & "datei.txt"
read file file_path
set file_contents to result
display dialog file_contents buttons ¬
  {"OK"} default button 1
```

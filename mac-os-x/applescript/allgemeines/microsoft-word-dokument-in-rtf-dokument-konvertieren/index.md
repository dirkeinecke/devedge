---
title: Microsoft Word-Dokument in RTF-Dokument konvertieren
---

## Microsoft Word-Dokument in RTF-Dokument konvertieren

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man ein Microsoft Word-Dokument in RTF-Dokument konvertieren möchte, dann kann man dies wie folgt tun:

```applescript
set the_file to choose file
if name extension of (info for the_file) is "doc" then
  set the_path to quoted form of (POSIX path of the_file)
  do shell script "textutil -convert rtf " & the_path
else
  display dialog "Kein Word-Dokument!" buttons {"OK"} default button 1
end if
```

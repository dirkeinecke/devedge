---
title: Inhalt einer RTF-Datei lesen
---

## Inhalt einer RTF-Datei lesen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man den Inhalt einer RTF-Datei lesen möchte, dann könnte man dies einfach mit "`read file`" machen. So würde man aber auch den Header und alle Steuerzeichen der RTF-Datei bekommen. Möchte man allerdings nur den echten Text-Inhalt haben, dann kann man dies mit einen Umweg über das Programm "TextEdit" realisieren. Dies zeigt das folgende Script:

```applescript
tell application "TextEdit"
  set file_path to path to desktop folder as string
  set file_path to file_path & "datei.rtf"
  open file file_path
  set file_contents to text of document 1
  close document 1
  display dialog file_contents buttons ¬
    {"OK"} default button 1
end tell
```

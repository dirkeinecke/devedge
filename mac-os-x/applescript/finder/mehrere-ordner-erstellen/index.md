---
title: Mehrere Ordner erstellen
---

## Mehrere Ordner erstellen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn Sie mehrere Ordner anlegen möchten und dabei bereits existierende Ordner mit dem gleichen Namen nicht überschreiben möchten, dann können Sie das wie folgt tun:

```applescript
set new_folder_names to {"Ordner 1", "Ordner 2", "Ordner 3"}
set target_folder to path to desktop as Unicode text

tell application "Finder"
  repeat with name_ in new_folder_names
    try
      alias (target_folder & name_)
      display dialog ¬
        "Es existiert bereits ein Ordner " & ¬
        "mit dem Namen '" & name_ & "'." buttons ¬
        {"OK"} default button 1
      on error
        make new folder ¬
          at folder target_folder ¬
          with properties {name:name_}
      end try
  end repeat
end tell
```

In diesem Beispil werden die Ordner "Ordner 1", "Ordner 2" und "Ordner 3" auf dem Schreibtisch (`desktop`) angelegt. Wenn bereits ein Ordner mit einem dieser Namen existiert, dann wird mittels "`display dialog`" ein entsprechender Hinweis angezeigt.

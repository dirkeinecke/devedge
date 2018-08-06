---
title: Ordner erstellen
---

## Ordner erstellen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn Sie einen Ordner neu erstellen möchten, dann können Sie dies wie folgt realisieren:

```applescript
-- Es soll auf dem "Schreibtisch" (desktop) ein Ordner
-- mit dem Namen "Ordnername" angelegt werden.
tell application "Finder" to make new folder ¬
  at desktop with properties {name:"Ordnername"}
```

Sollte es allerdings bereits einen Ordner mit dem gewählten Namen geben, dann würde das Script einen Fehler verursachen. Wie man dies umgehen kann zeigt folgendes Script:

```applescript
try
  -- Es soll auf dem "Schreibtisch" (desktop) ein Ordner
  -- mit dem Namen "Ordnername" angelegt werden.
  tell application "Finder" to make new folder ¬
    at desktop with properties {name:"Ordnername"}
end try
```

Für den Fall, dass es nicht möglich ist den Ordner anzulegen, kann man auch eine eigene "Fehlermeldung" ausgeben. Wie man dies machen kann zeigt das folgende Script:

```applescript
try
  -- Es soll auf dem "Schreibtisch" (desktop) ein Ordner
  -- mit dem Namen "Ordnername" angelegt werden.
  tell application "Finder" to make new folder ¬
    at desktop with properties {name:"Ordnername"}
on error
  -- Wenn es bereits einen Ordner mit diesem Namen gibt,
  -- dann wird hier eine Fehlermeldung ausgegeben.
  display dialog "Es existiert bereits ein Ordner mit diesem Namen."
end try
```

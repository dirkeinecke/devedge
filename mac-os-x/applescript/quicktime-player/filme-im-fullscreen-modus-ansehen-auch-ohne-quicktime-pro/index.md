---
title: Filme im Fullscreen-Modus ansehen ... auch ohne QuickTime PRO
---

## Filme im Fullscreen-Modus ansehen ... auch ohne QuickTime PRO

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Möchte man mit der kostenlosen Standardversion vom QuickTime Player auch in den Genuss des QuickTime PRO Features "Gesamter Bildschirm" - also Fullscreen-Modus - kommen, so kann man dies sehr einfach mit Hilfe von nur drei Zeilen AppleScript erreichen. Dazu muss man nur das folgende Script in den Scripteditor eingeben und als Programm abspeichern (Menü: Ablage -> Speichern unter... -> hier bei der Selektbox für das Dateiformat "Programm" auswählen). Danach einfach den gewünschten Film ganz normal im QuickTime Player öffnen und danach durch einen Doppelklick das eben erstellte Programm starten. Und schon wechselt der QuickTime Player in den Fullscreen-Modus.

```applescript
tell application "QuickTime Player"
  present front movie scale screen
end tell
```

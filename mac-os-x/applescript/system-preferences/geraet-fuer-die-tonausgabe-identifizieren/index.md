---
title: Gerät für die Tonausgabe identifizieren
---

## Gerät für die Tonausgabe identifizieren

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man herausfinden möchte, welches Gerät für die Tonausgabe ausgewählt ist, dann kann man dies wie folgt tun:

```applescript
tell application "System Preferences"
  reveal anchor "output" of pane id ¬
    "com.apple.preference.sound"
end tell

tell application "System Events"
  set soundOutputDevice to value of text field 1 of row 1 of table 1 of ¬
    scroll area 1 of tab group 1 of window "Ton" of ¬
    application process "System Preferences"
end tell

quit application "System Preferences"
display dialog soundOutputDevice buttons ("OK") default button 1
```

Dabei muss man beachten, dass der Wert "`Ton`" abhängig von der aktuell eingestellten Sprache für das Betriebssystem ist. Wenn man zum Beispiel Englisch als Systemsprache eingestellt hat, dann muss man den Wert "`Ton`" durch "`Sound`" ersetzen.

---
title: Pfad zum Preferences-Ordner des aktuellen Benutzers
---

## Pfad zum Preferences-Ordner des aktuellen Benutzers

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man den Pfad zum Preferences-Ordner des aktuellen Benutzers herausbekommen möchte, dann fällt dies ganz klar unter die Rubrik "Viele Wege führen nach Rom." Hier eine Auswahl der verschiedenen Möglichkeiten:

### Möglichkeit 1

```applescript
set the_path to path to preferences as text
display dialog the_path
```

### Möglichkeit 1a

```applescript
set the_path to (path to preferences from user domain) as text
display dialog the_path
```

### Möglichkeit 1b

```applescript
tell application "System Events"
  set the_path to the path to preferences as text
end tell
display dialog the_path
```

Man kann sich den Pfad natürlich auch selber zusammensetzen:

### Möglichkeit 2

```applescript
set the_path to (do shell script "printenv HOME") & "/Library/Preferences/"
display dialog the_path
```

### Möglichkeit 3

```applescript
set current_user to do shell script "whoami"
set the_path to "/Users/" & current_user & "/Library/Preferences/"
display dialog the_path
```

---
title: Papierkorb in Apple Mail leeren
---

## Papierkorb in Apple Mail leeren

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man den Papierkorb in Apple Mail leeren ("E-Mails entgültig löschen") möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Mail"
  delete messages of the trash mailbox
end tell
```

---
title: Neue E-Mail erstellen
---

## Neue E-Mail erstellen

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript eine neue E-Mail in Apple Mail erstellen:

```applescript
tell application "Mail"
  set myMessage to make new outgoing message
  set visible of myMessage to true
  activate
end tell
```

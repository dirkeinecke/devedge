---
title: Anzeigen des aktuellen Titels aus iTunes
---

## Anzeigen des aktuellen Titels aus iTunes

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man sich den aktuellen Titel aus iTunes anzeigen lassen möchte, dann kann man das wie folgt machen:

```applescript
tell application "iTunes"
  set theIndex to index of current track
  set thisTrack to track (theIndex) of current playlist
  set trackName to name of thisTrack
  display dialog trackName
end tell
```

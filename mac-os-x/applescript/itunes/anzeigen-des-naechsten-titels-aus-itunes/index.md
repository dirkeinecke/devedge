---
title: Anzeigen des nächsten Titels aus iTunes
---

## Anzeigen des nächsten Titels aus iTunes

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man sich den nächsten Titel aus iTunes anzeigen lassen möchte, dann kann man das wie folgt machen:

```applescript
tell application "iTunes"
  set theIndex to index of current track
  set nextTrack to track (theIndex + 1) of current playlist
  set trackName to name of nextTrack
  display dialog trackName
end tell
```

---
title: Lautstärke von iTunes einfaden
---

## Lautstärke von iTunes einfaden

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man die Lautstärke von iTunes einfaden möchte, dann kann man das wie folgt tun:

```applescript
on iTunesFadeVolumeUp()
  tell application "iTunes"
    if (player state is playing) then
      set iTunesIsActive to true
    else
      set iTunesIsActive to false
    end if
    if iTunesIsActive then
      play
      set iTunesTargetVolume to 100
      repeat with i from 1 to iTunesTargetVolume
        if sound volume is less than iTunesTargetVolume then
          -- In der nächsten Zeile wird nicht 1 sondern 2
          -- hinzuaddiert, da es in älteren iTunes-Versionen
          -- einen Bug gab, der das Hinzuaddieren von 1 verhinderte.
          set the sound volume to (sound volume + 2)
        end if
        if sound volume ≥ iTunesTargetVolume then exit repeat
      end repeat
    end if
  end tell
end iTunesFadeVolumeUp

iTunesFadeVolumeUp()
```

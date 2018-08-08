---
title: Lautstärke von iTunes ausfaden
---

## Lautstärke von iTunes ausfaden

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man die Lautstärk von iTunes ausfaden möchte, dann kann man das wie folgt tun:

```applescript
on iTunesFadeVolumeDown()
  tell application "iTunes"
    if (player state is playing) then
      set iTunesIsActive to true
    else
      set iTunesIsActive to false
    end if
    if iTunesIsActive then
      set iTunesPrevVolume to sound volume
      repeat with i from 1 to iTunesPrevVolume
        if sound volume is greater than 0 then
          set the sound volume to (sound volume - 1)
        end if
        if sound volume is 0 then exit repeat
      end repeat
      pause
    end if
  end tell
end iTunesFadeVolumeDown

iTunesFadeVolumeDown()
```

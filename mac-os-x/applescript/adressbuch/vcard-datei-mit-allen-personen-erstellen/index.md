---
title: vCard-Datei mit allen Personen erstellen
---

## vCard-Datei mit allen Personen erstellen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man eine vCard-Datei mit allen Personen erstellen möchte, dann kann man dies wie folgt tun:

```applescript
set the_file to "vcards.vcf"
tell application "Address Book" to set vcard_data to vcard of the people
tell application "Finder"
  make new file with properties {name:the_file} at (choose folder)
  set the_destination to the result as alias
end tell
set file_reference to open for access the_destination with write permission
set eof file_reference to 0
write (vcard_data as text) to file_reference
close access file_reference
```

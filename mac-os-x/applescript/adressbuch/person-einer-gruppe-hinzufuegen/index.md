---
title: Person einer Gruppe hinzufügen
---

## Person einer Gruppe hinzufügen

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn Sie die aktuell ausgewählte Person zu einer Gruppe hinzuzufügen möchten und Ihnen der Name der Gruppe bekannt ist, dann können Sie dies wie folgt tun.

```applescript
tell application "Address Book"
  try
    set the_person to item 1 of (get selection)
    add the_person to group "Name der Gruppe"
  end try
  save addressbook
end tell
```

Wenn Sie hingegen die aktuell ausgewählte Person einer beliebigen Gruppe hinzufügen möchten, dann können Sie dies wie folgt tun. Sie erhalten dabei eine Liste aller zur Verfügung stehenden Gruppen und können aus dieser Liste wählen.

```applescript
tell application "Address Book"
  try
    set the_person to item 1 of (get the selection)
    set the_group to item 1 of (choose from list ((name of groups) as list))
    add the_person to group the_group
  end try
  save addressbook
end tell
```

Wenn Sie eine bestimmte Person (oder mehrere) einer bestimmten Gruppe (oder mehreren) hinzufügen möchten, dann können Sie dies wie folgt tun. Sie erhalten dabei eine Liste aller zur Verfügung stehenden Personen und können aus dieser eine oder mehrere Person(en) auswählen. Danach erhalten Sie eine Liste aller zur Verfügung stehenden Gruppen und können hier ebenfalls eine oder mehrere Gruppe(en) auswähen.

```applescript
tell application "Address Book"
  set the the_persons to (choose from list (get the name of the people) with multiple selections allowed)
  set the the_groups to (choose from list (get the name of the groups) with multiple selections allowed)
  repeat with this_person in the the_persons
    repeat with this_group in the the_groups
      add person this_person to group this_group
    end repeat
  end repeat
  save addressbook
end tell
```

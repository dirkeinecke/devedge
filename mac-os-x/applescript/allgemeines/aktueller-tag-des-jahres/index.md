---
title: Aktueller Tag des Jahres
---

## Aktueller Tag des Jahres

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man Nummer des Tages im aktuellen Jahr herausbekommen möchte, dann kann man dies wie folgt tun:

```applescript
set current_date to (current date)
copy current_date to jan_1_date
set month of jan_1_date to January
set day of jan_1_date to 1
set day_num to (1 + (current_date - jan_1_date) / days)
display dialog day_num buttons ("OK") default button 1
```

Eine andere - und vor allem kürzere - Variante wäre, wenn man dies mit Hilfe von "shell script" realisiert:

```applescript
set day_num to do shell script "date +%j"
display dialog day_num buttons ("OK") default button 1
```

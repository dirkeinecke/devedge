---
title: Längsten Eintrag einer Spalte ermitteln
---

## Längsten Eintrag einer Spalte ermitteln

Das folgende Beispiel zeigt, wie man den den längsten Eintrag einer Spalte (column) einer Tabelle (table) ermittelt.

```sql
SELECT MAX( LENGTH( `column` ) ) AS `max_len` FROM `table`
```

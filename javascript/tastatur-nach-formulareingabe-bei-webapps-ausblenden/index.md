## Tastatur nach Formulareingabe bei WebApps ausblenden

Wenn man in einer WebApp für das iPhone beziehungsweise für den iPod touch ein Formular hat und man möchte, dass nach der Formulareingabe mit einem Klick auf einen Button in der WebApp die Tastatur wieder ausgeblendet wird (ohne das der Benutzer auf den "Fertig"-Button auf der Tastatur klicken muss), kann man dies realisieren, in dem man beim Klick auf den Button in der WebApp folgendes JavaScript ausführt:

```javscript
document.getElementById('ID_DES_FORMULARFELDES').blur();
```

Hat man mehrere Eingabefelder im Formular, muss man die o. g. Zeile für alle Eingabefelder wiederholen.

---
title: Google Analytics in phpBB einbinden
---

## Google Analytics in phpBB einbinden


### Voraussetzungen

- Google Analytics Account
- Google Analytics Tracking-Code
- Sie haben bei Ihrer phpBB-Installation der Berechtigung Templates zu bearbeiten

### Hinweis #1

Die hier genannte Vorgehensweise bezieht sich auf die Version 3 der phpBB-Software.

### Hinweis #2

Nach einem Update der phpBB-Software müssen Sie prüfen, ob der Google Analytics Code noch in der Vorlage enthalten ist, da durch ein Update auch die Vorlage durch eine neuere Version ersetzt werden könnte.

### Um Google Analytics einzubinden, gehen Sie wie folgt vor:

1. Loggen Sie sich in den Administrations-Bereich Ihrer phpBB-Installtion ein.
2. Klicken Sie auf die Registerkarte "Styles".
3. Klicken Sie in der linken Navigation "Style-Komponenten" auf "Templates".
4. Klicken Sie in der Tabelle im rechten Bereich auf den "Ändern"-Link des von Ihnen verwendeten Styles.
5. Wählen Sie aus dem Drop-Down-Menü "Template-Datei" den Eintrag "overall_footer.html" aus.
6. Klicken Sie auf den Button "Template-Datei auswählen".
7. Scrollen Sie im Bereich "HTML-Template-Editor" den Inhalt der Textarea ganz nach unten.
8. Fügen Sie vor "`</body>`" den Google Analytics Code ein.
9. Klicken Sie auf den Button "Absenden".
10. Klicken Sie in der linken Navigation "Style-Komponenten" auf "Templates".
11. Klicken Sie in der Tabelle im rechten Bereich auf den "Cache"-Link des von Ihnen verwendeten Styles.
12. Klicken Sie am Ende der Tabelle "Template-Cache" auf den Link " Alle markieren ".
13. Klicken Sie auf den Button "Markierte löschen".

## Weiterführende Informationen

- [Google Analytics Website](https://marketingplatform.google.com/about/){:target="_blank"}

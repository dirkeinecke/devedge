---
title: URL-Kodierung einer Zeichenkette nach RFC 1738
---

## URL-Kodierung einer Zeichenkette nach RFC 1738

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Wie Sie eine URL-Kodierung einer Zeichenkette nach RFC 1738 vornehmen können, zeigt Ihnen das folgende Script:

```applescript
on urlEncode(myString)
  set myQuotedString to quoted form of myString
  set myCmd to "php -r \"echo rawurlencode(" & myQuotedString & ");\""
  set myResult to do shell script myCmd
  return myResult
end urlEncode

set myText to "Das ist ein Beispieltext."
set urlEncodedText to urlEncode(myText)
-- Ergebnis: "Das%20ist%20ein%20Beispieltext."
```

---
title: Einfaches Kontaktformular mit Perl
---

## Einfaches Kontaktformular mit Perl

### HTML-Seite

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8"/>
    <title>Kontaktformular</title>
    <style type="text/css">
      label {
        display: block;
      }
    </style>
  </head>
  <body>
    <form method="post" action="Kontaktformular.pl">
      <p>
        <label for="Anrede">Anrede</label>
        <select name="Anrede" id="Anrede">
            <option></option>
            <option>Herr</option>
            <option>Frau</option>
          </select>
      </p>
      <p>
        <label for="Vorname">Vorname</label>
        <input type="text" name="Vorname" id="Vorname"/>
      </p>
      <p>
        <label for="Nachname">Nachname</label>
        <input type="text" name="Nachname" id="Nachname"/>
      </p>
      <p>
        <label for="EMailAdresse">E-Mail-Adresse</label>
        <input type="text" name="EMailAdresse" id="EMailAdresse"/>
      </p>
      <p>
        <label for="Text">Text</label>
        <textarea name="Text" id="Text" rows="10" cols="30"></textarea>
      </p>
      <p>
        <input type="submit" value="Absenden"/>
      </p>
    </form>
  </body>
</html>
```

### Perl-Script

```perl
#!/usr/local/bin/perl

use CGI::Carp 'fatalsToBrowser';

# Konfiguration
$sendmail   = '/usr/lib/sendmail';
$empfaenger = 'info@domain.de';
$absender   = 'info@domain.de';
$site_name  = 'Meine Site';
$site_url   = '/';

use CGI qw(:standard);

$email_body = '';

foreach $feld (param) {
  foreach $wert (param($feld)) {
    $email_body .= "$feld: $wert\n";
  }
}

if ($email = param('EMailAdresse')) {
  $email =~ s/\n/ /g;
  $absender = $email;
}

open MAIL, "|$sendmail -oi -t" or die "Kann keine Pipe zu $sendmail oeffnen: $!\n";

print MAIL <<"EOF";
To: $empfaenger
From: $absender
Subject: Kontaktformular

$email_body
EOF

close MAIL or die "Kann Pipe zu $sendmail nicht schliessen: $!\n";

charset('utf-8');
print header;
print <<"EOF";
<html>
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8"/>
    <title>Kontaktformular versendet</title>
  </head>
  <body>
    <p>
      Vielen Dank für Ihre Anfrage.
    </p>
    <p>
      <a href="$site_url">zurück zu $site_name</a>
    </p>
  </body>
</html>
EOF
```

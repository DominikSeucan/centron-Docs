---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 18. April 2024
---

# Exchange-Konto-Verwaltung

Exchange Postfächer ermöglichen das Sammeln, Organisieren und Teilen von Informationen mit anderen Mitgliedern Ihrer Organisation.

### Exchange-Konto hinzufügen <a href="#exchange-konto_hinzufuegen" id="exchange-konto_hinzufuegen"></a>

Um ein Exchange-Konto einzurichten wird ein Konto auf einem unserer Mailserver benötigt, welches die Mails an unseren Exchange Server zu Ihrem Postfach weiterleitet. Alternativ kann auch ein Alias erstellt werden, der zum Exchange-Konto weiterleitet. Folgend finden Sie eine Schritt-für-Schritt-Anleitung, wie Sie in Ihrem Paket ein weiteres Exchange Konto einrichten können.

**Wichtig:** Bitte beachten Sie, dass Sie über unsere Webseite oder per Mail erst ein weiteres Exchange-Konto bestellen müssen, damit Ihnen das Kontingent zur Verfügung steht, dieses einrichten zu können. Gerne richten wir auch für Sie das Konto ein. Senden Sie uns dazu bei der Bestellung einfach die gewünschte E-Mail-Adresse mit.

Um ein Exchange-Konto zu benutzen wird eine Weiterleitung an unseren Exchange Server benötigt. Wenn Sie bereits ein IMAP/POP3 Postfach besitzen, richten Sie wie beschrieben eine Weiterleitung ein. Ist noch kein Postfach vorhanden, genügt es einen Alias anzulegen.

#### Weiterleitung bei bestehendem Postfach einrichten <a href="#weiterleitung_bei_bestehendem_postfach_einrichten" id="weiterleitung_bei_bestehendem_postfach_einrichten"></a>

1. Klicken Sie auf der Startseite auf „E-Mail-Konten“
2. Wählen Sie das gewünschte E-Mail-Konto aus
3. Unter „E-Mail-Weiterleitung“ muss der Haken bei „Weiterleiten aktiviert“ gesetzt werden
4. Unter „E-Mail weiterleiten an Adresse:“ geben Sie folgendes an: EMAIL@DOMÄNE.TLD.exch14.internet1.de [![](https://wiki.centron.de/_media/webhosting/interfaces/webpanel/exchange_weiterleitung_postfach.png?w=400\&tok=041910)](https://wiki.centron.de/_media/webhosting/interfaces/webpanel/exchange_weiterleitung_postfach.png)
5. Bestätigen Sie Ihre Angaben mit einem Klick auf „Speichern“

#### oder Alias anlegen <a href="#oder_alias_anlegen" id="oder_alias_anlegen"></a>

1. Wählen Sie auf der Startseite „E-Mail-Aliasse“ aus
2. Klicken Sie oben rechts auf „E-Mail-Alias erstellen“
3. Geben Sie den gewünschten Namen ein
4. Wählen Sie mit Hilfe des Drop-Down-Menüs die Domäne aus
5. Unter „Weiterleiten an E-Mail“ geben Sie folgendes an: EMAIL@DOMÄNE.TLD.exch14.internet1.de
6. Erstellen Sie Ihren Alias mit einem Klick auf „Speichern“

#### Exchange-Konto anlegen <a href="#exchange-konto_anlegen" id="exchange-konto_anlegen"></a>

1. Wählen Sie Ihr gewünschtes Paket im Drop-Down-Menü aus
2. Klicken Sie unter „Gehostete Organisation – Exchange“ auf „Postfächer“
3. Rechts oben finden Sie den Button „Neues Postfach“
   1. Geben Sie Ihren gewünschten Vor- und Nachnamen an
   2. Geben Sie Ihre E-Mail-Adresse an
   3. Legen Sie ein sicheres Passwort fest
   4. Wählen Sie unter „Mailboxplan Name“ „Default“ aus
4. Bestätigen Sie Ihre Angaben mit einem Klick auf „Postfach erstellen“
5. Nachdem das Postfach erstellt wurde, klicken Sie auf den Reiter „E-Mail Adressen“
6. Geben Sie Ihre E-Mail Adresse an und wählen im Drop-Down-Menü @DOMÄNE.TLD.exch14.internet1.de aus und fügen mit einem Klick auf „E-Mail-Adresse hinzufügen“ die Weiterleitungsadresse hinzu
7. EMAIL@DOMÄNE.TLD muss als „Primäre E-Mail-Adresse“ mit einem grünen Haken markiert sein

[![](https://wiki.centron.de/_media/webhosting/interfaces/webpanel/exchange_e-mail-adresse_hinzufuegen.png?w=800\&tok=cace5c)](https://wiki.centron.de/_media/webhosting/interfaces/webpanel/exchange_e-mail-adresse_hinzufuegen.png)

#### Akzeptierte Domäne hinzufügen <a href="#akzeptierte_domane_hinzufuegen" id="akzeptierte_domane_hinzufuegen"></a>

Eine akzeptierte Domäne ist mit einem Alias zu vergleichen. Diese wird benötigt um die Weiterleitungsadresse am Exchange Server zu autorisieren.

1. Klicken Sie unter „Gehostete Organisation – Exchange“ auf „Akzeptierte Domänen“
2. Oben rechts finden Sie „+ Neue Domäne hinzufügen“
   1. Wählen Sie Ihre Domäne im Drop-Down-Menü aus
   2. Bestätigen Sie Ihre Auswahl mit einem Klick auf „Domäne hinzufügen“
3. Lege Sie die Domaintypen folgendermaßen fest:
   1. DOMÄNE.TLD → InternalRelay
   2. DOMÄNE.TLD.exch14.internet1.de → Authoritative
   3. Standard-Domäne → DOMÄNE.TLD

[![](https://wiki.centron.de/_media/webhosting/interfaces/webpanel/exchange_akzeptierte_domain.png?w=800\&tok=a74625)](https://wiki.centron.de/_media/webhosting/interfaces/webpanel/exchange_akzeptierte_domain.png)

### Exchange-Konto entfernen <a href="#exchange-konto_entfernen" id="exchange-konto_entfernen"></a>

Wenn Sie ein Exchange-Konto nicht mehr benötigen, muss das Postfach und der Benutzer gelöscht werden. Es ist darauf zu achten, dass die Weiterleitung beim POP3/IMAP Konto entfernt wird bzw. der Alias gelöscht wird. Benötigen Sie Ihr POP3/IMAP Konto nicht mehr, können Sie dies ebenfalls löschen.

**Wichtig:** Wenn Sie Ihr Exchange-Konto gelöscht haben, geben Sie uns unbedingt Bescheid, damit Sie nicht weiterhin die Lizenz für das Postfach bezahlen müssen.

#### Postfach, Weiterleitung und Benutzer löschen <a href="#postfach_weiterleitung_und_benutzer_loschen" id="postfach_weiterleitung_und_benutzer_loschen"></a>

1. Wählen Sie unter „Gehostete Organisation – Exchange“ „Postfächer“ aus
2. Klicken Sie auf der rechten Seite bei dem Postfach, das Sie löschen möchten, auf den roten „Löschen-Button“
3. Unter „Gehostete Organisation“ finden Sie unter „Benutzer“ den dazugehören Benutzer, welchen Sie ebenfalls auf der rechten Seite mit dem „Löschen-Button“ entfernen
4. Entfernen Sie als Nächstes die Weiterleitung:
   1. Löschen Sie unter „E-Mail-Aliasse“ Ihren Alias
   2. Löschen Sie unter „E-Mail-Konten“ bei Ihrem gewünschten Postfach die Weiterleitung und nehmen den Haken bei „Weiterleiten aktiviert“ heraus

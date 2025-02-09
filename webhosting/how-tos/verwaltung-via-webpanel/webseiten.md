---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 18. April 2024
---

# Webseiten

### Webseite anlegen <a href="#webseite_anlegen" id="webseite_anlegen"></a>

1. Melden Sie sich im [Webpanel](https://webpanel.internet1.de/) an
2. Wählen Sie Ihr gewünschtes Paket im Drop-down Menü aus
3. Klicken Sie auf „Webseiten“
4. Unter „Webseite erstellen“ wählen Sie Ihre Domäne aus und erstellen die Webseite mit einem Klick auf „+ Webseite erstellen“\


{% embed url="https://wiki.centron.de/_media/webhosting/interfaces/webpanel/webseiteanlegen.mp4" %}

### Webseiten verwalten <a href="#webseiten_verwalten" id="webseiten_verwalten"></a>

### Webseite löschen <a href="#webseite_loschen" id="webseite_loschen"></a>

Ihre Webseite können Sie über den roten Button „Löschen“ entfernen. Hierbei werden allerdings nicht die Webdaten gelöscht. Möchten Sie auch die dazu gehörigen Daten löschen, setzen Sie den Haken bei „Löschen des Webseiten-Verzeichnisses erzwingen?“.

### Webseite weiterleiten <a href="#webseite_weiterleiten" id="webseite_weiterleiten"></a>

#### Externe Domain <a href="#externe_domain" id="externe_domain"></a>

Möchten Sie Ihre Domain auf eine andere URL weiterleiten? Diese Einstellung können Sie im [Webpanel](https://webpanel.internet1.de/) festlegen:

1. Wählen Sie unter Webseiten die gewünschte Webseite, die weitergeleitet werden soll aus
2. Klicken Sie auf „Weiterleitung zur URL“
   1. Fügen Sie die Ziel-URL ein
   2. Nun haben Sie noch die Möglichkeit verschiedene Umleitungstypen auszuwählen
      * **„Alle Anfragen zum genauem Ziel weiterleiten (anstatt relativ zum Ziel)“**
        * Gibt einen 302-Statuscode (Moved Permanently) zurück, der den Client anweist, eine neue Anforderung an die die Ziel-URL zu senden, da der Inhalt dauerhaft verschoben wurde. Diese Information darf im Cache gespeichert werden. Hier erscheint die genaue Zieladresse nach der Umleitung in der Adresszeile des Browsers.
      * **„Nur Anfragen zu Inhalten in diesem Verzeichnis weiterleiten (keine Unterverzeichnisse)“**
        * Gibt einen 302-Statuscode (Moved Permanently) zurück, der den Client anweist, eine neue Anforderung an die die Ziel-URL zu senden, da der Inhalt dauerhaft verschoben wurde. Dies wird nicht gecached, da hier davon auszugehen ist, dass in absehbarer Zeit die alte URL wieder verfügbar ist. Auch hier erscheint die Zieladresse nach der Umleitung in der Adresszeile des Browsers. Etwaige Eingaben nach dem / werden in diesem Fall übernommen und ergänzt.
      * **„Permanente Weiterleitung aktivieren“**
        * Gibt einen 301-Statuscode (Found) zurück, der den Client darüber informiert, dass sich der Standort für die angeforderte Ressource dauerhaft geändert hat. Hier erscheint die Zieladresse nach der Umleitung in der Adresszeile des Browsers. Etwaige Eingaben nach dem / werden in diesem Fall übernommen und ergänzt.
   3. Bestätigen Sie Ihre Angaben mit einem Klick auf „Änderungen speichern“ rechts unten

#### https:// <a href="#https" id="https"></a>

Sie haben im Webpanel ein Zertifikat für Ihre Webseite eingebunden, allerdings erscheint die Webseite nach Aufrufen im Internetbrowser immer noch mit http und wird als unsicher angezeigt? In den folgenden Schritten wird erklärt, wie eine https-Weiterleitung in der web.config eingerichtet wird, damit Ihre Webseite als „sicher“ angezeigt wird:



1. Klicken Sie links im „Main Menu“ auf den Reiter „Hosting-Bereich Menü“ → „Dateimanager“
2. Wählen Sie den Ordner Ihrer Webseite aus
3. Klicken Sie auf „web“
4. Bearbeiten Sie die „web.config“ mit einem Klick auf das Symbol mit „Stift und Papier“
5. Fügen Sie anschließend unten stehende Regel ein
6. Bestätigen Sie Ihre Angaben danach mit einem Klick auf „Speichern“ rechts unten

```
<rewrite>
<rules>
</rule>
<rule name="http to https" stopProcessing="true">
    <match url="(.*)" />
    <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
          <add input="{HTTPS}" pattern="^OFF$" />
    </conditions>
    <action type="Redirect" url="https://€{HTTP_HOST}/{R:1}" />
</rule>
</rules>
</rewrite>
```

**Sie haben ein Linux-Hosting gebucht und möchten Ihre Webseite verwalten?**

Eine entsprechende Anleitung finden Sie [hier](broken-reference).

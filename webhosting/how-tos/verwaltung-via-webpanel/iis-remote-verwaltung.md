---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 18. April 2024
---

# IIS Remote Verwaltung

Der IIS (**I**nternet **I**nformation **S**erver) ist ein Teil des Windows Betriebssystems, welches die Möglichkeit bietet, Webserver zu realisieren und Daten und Dokumente online zugänglich zu machen.\
Unterstützte Protokolle sind z. B. HTTP, HTTPS, FTP, SMTP, POP3 und WebDAV.

### Ihre Möglichkeiten mit der IIS Remote Verwaltung <a href="#ihre_moglichkeiten_mit_der_iis_remote_verwaltung" id="ihre_moglichkeiten_mit_der_iis_remote_verwaltung"></a>

* Verwalten einer IIS-Webseite per remote

### IIS Remote Administrator Einrichtung <a href="#iis_remote_administrator_einrichtung" id="iis_remote_administrator_einrichtung"></a>

1. Webpanel Zugang anlegen
2. IIS Modul installieren
3. IIS Modul verbinden

#### 1. Webpanel Zugang anlegen <a href="#webpanel_zugang_anlegen" id="webpanel_zugang_anlegen"></a>

1. Wählen Sie unter „Webseiten“ Ihre gewünschte Webseite aus
2. Klicken Sie auf den Reiter „Verwaltung“
3. Geben Sie ein Passwort an, mit dem Sie sich in Zukunft mit dem IIS verbinden möchten
4. Nun werden die Verbindungsinformationen zum IIS-Server, sowie der IIS interne Name für die Webseite angezeigt. Diese benötigen Sie zur Einrichtung der Webseite im IIS.\


#### 2. IIS Modul installieren <a href="#iis_modul_installieren" id="iis_modul_installieren"></a>

Als Nächstes müssen Sie die Verwaltungskonsole installieren, welche sich mit dem Server verbindet und mit welcher Sie die Seite verwalten können. Hierzu muss ein zusätzliches Windows Feature installiert werden.

1. Klicken Sie mit einem Rechtsklick auf das Startmenü und wählen „Programme und Features“ aus (siehe Bild)
2. Klicken Sie dort auf „Windows-Features aktivieren oder deaktivieren“
3. Wählen Sie das Modul IIS-Verwaltungskonsole in Internetinformationsdienste > Webverwaltungstools > IIS-Verwaltungskonsole
4. Anschließend die Installation mit „OK“ starten
5. Installieren Sie den IIS Manager for Remote Administration von der Microsoft Webseite

#### 3. IIS Modul verbinden <a href="#iis_modul_verbinden" id="iis_modul_verbinden"></a>

1. Öffnen Sie IIS
2. Wählen Sie unter „Datei“ „Mit einer Site verbinden“ aus
3. Geben Sie die Verbindungsdetails an, welche Sie aus dem Webpanel (Schritt 1.5) entnehmen können. Bestätigen Sie mit „Weiter“
4. Geben Sie nun den Benutzernamen und das Passwort an, welches Sie im Webpanel für diese Webseite festgelegt haben (Schritt 1.4)
5. Nach erfolgreicher Installation können Sie noch einen benutzerdefinierten Namen für Ihre Seite festlegen und anschließend mit „Fertig“ die Einrichtung abschließen

Wichtig! Es kann sein, dass Sie bei der Einrichtung gefragt werden, ob Sie dem Server vertrauen, oder einige zusätzliche Module installieren und ausführen wollen. Installieren Sie hier alle angebotenen Module und lassen die Ausführung zu, um die Verwaltung vollständig durchführen zu können.

Ihr IIS Manager für entfernte Administration ist nun vollständig eingerichtet. Sie können Ihre Webseite nun darüber steuern.

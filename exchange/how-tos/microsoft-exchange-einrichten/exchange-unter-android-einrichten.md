---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Exchange unter Android einrichten

In diesem Artikel erfahren Sie, wie Sie Ihr neues Microsoft Exchange 2019-Konto in der Gmail App auf einem Android-Gerät einrichten. Dies wird am Beispiel des Samsung GALAXY S10 mit Android 11 erläutert. Beachten Sie, dass die Menüpunkte auf anderen Android-Modellen abweichen können.

**Automatische Konfiguration:**

1. Öffnen Sie die Gmail App.
2. Tippen Sie links oben auf das Symbol mit den drei waagerechten Strichen.
3. Wählen Sie „Einstellungen“.
4. Tippen Sie auf „Konto hinzufügen“.
5. Wählen Sie „Exchange und Office 365“.
6. Geben Sie Ihre E-Mail-Adresse ein und tippen Sie auf „Weiter“.
7. Geben Sie Ihr Passwort ein und tippen Sie erneut auf „Weiter“.
8. Warten Sie, bis die Kontoinformationen abgerufen werden.
9. Tippen Sie auf „Fertig“.

**Manuelle Konfiguration:** Falls die automatische Einrichtung fehlschlägt, richten Sie das Konto manuell ein:

1. Befolgen Sie die Schritte 1 bis 6 der automatischen Konfiguration.
2. Wählen Sie „Manuell Einrichten“.
3. Geben Sie Ihr Passwort ein.
4. Stellen Sie sicher, dass im Feld „Domain\Nutzername“ Ihre E-Mail-Adresse steht.
5. Tragen Sie im Feld „Server“ den Server „exchange2019.centron.eu“ ein.
6. Stellen Sie sicher, dass im Feld „Port“ der Port 443 und als Sicherheitstyp „SSL“ eingetragen sind.
7. Tippen Sie auf „Weiter“.
8. Warten Sie, bis die Kontoinformationen abgerufen werden.
9. Tippen Sie auf „Fertig“.

Hilfe bei Problemen: Sollte auch die manuelle Einrichtung fehlschlagen, überprüfen Sie, ob in den DNS-Einstellungen Ihrer Domain ein Autodiscover-Eintrag vorhanden ist. Beachten Sie, dass nach dem Anlegen einer neuen Domain oder Änderungen an den DNS-Einstellungen eine gewisse Zeit für die Aktualisierung benötigt wird. Weitere Informationen finden Sie im Artikel „Autodiscover-Einstellungen Ihrer Domain prüfen“.

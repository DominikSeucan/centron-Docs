---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Migrieren von E-Mails von centron Mail Accounts zu Microsoft 365

Für Kunden mit centron Mail Basic und centron Mail Business Postfächern:

In diesem Artikel erfahren Sie mehr über die Migration von E-Mails aus centron Mail Basic und centron Mail Business Postfächern (IMAP) zu Microsoft 365.

#### Bitte Beachten

Um zu erfahren, wie Sie sich auf die Migration vorbereiten, lesen Sie den Artikel „Vorbereitung von centron E-Mail-Konten für die Migration zu Microsoft 365“. Beachten Sie, dass alle Vorbereitungsschritte zuerst abgeschlossen sein müssen.

#### Einschränkungen bezüglich des Imports

* Die maximale Größe einer E-Mail darf 35 Megabyte nicht überschreiten.
* Pro Benutzerpostfach können maximal 500.000 Elemente übertragen werden.
* Es werden nur E-Mails migriert, keine Kontakte, Aufgaben usw.

#### Vorbereitung auf die Migration

Um die Benutzerdaten der centron Postfächer zu Microsoft 365 zu übertragen:

1. Öffnen Sie ein Programm, das es Ihnen ermöglicht, kommagetrennte CSV-Dateien zu erstellen, z.B. Microsoft Excel.
2. Geben Sie in der ersten Zeile folgende Überschriften pro Spalte ein: E-Mail Adresse, Benutzername, Passwort.
3. Fügen Sie eine Zeile mit den Benutzerdaten für jedes Benutzerpostfach hinzu.
4. Speichern Sie die Datei im CSV-Format (Trennzeichen: Komma).

#### Durchführung der Migration

**Hinweise**

* Die zu importierenden Benutzer müssen bereits in Microsoft 365 erstellt sein.
* Seit Anfang 2022 hat Microsoft das Design des Exchange Admin Centers geändert. Die folgenden schrittweisen Anweisungen beziehen sich auf die Menüstrukturen und Optionen der klassischen Anzeige.

1. Melden Sie sich bei Ihrem Microsoft 365-Administrator-Konto an.
2. Wählen Sie das Admin-Symbol im linken Menü. Das Microsoft 365 Admin Center öffnet sich.
3. Wählen Sie Exchange im linken Menü. Beachten Sie, dass Sie möglicherweise das Menü mit „Alle anzeigen“ komplett anzeigen müssen.
4. Klicken Sie auf den Button „Klassisches Exchange Admin Center“, um die korrekten Menüstrukturen und Optionen für die folgenden Schritte zu finden.
5. Unter „Empfänger“ klicken Sie auf „Migration“.
6. Klicken Sie auf den ...-Button und wählen Sie „Migrationsendpunkte“. Das Fenster „Migrationsendpunkte“ öffnet sich.
7. Klicken Sie auf das Pluszeichen, um einen neuen Migrationsendpunkt zu erstellen. Das Fenster des Migrationsendpunkt-Assistenten öffnet sich.
8. Wählen Sie den Migrationsendpunkt IMAP und klicken Sie auf „Weiter“.
9. Geben Sie im Feld „IMAP-Server“ **imap.centron.com** ein und bestätigen Sie den Eintrag mit „Weiter“.
10. Geben Sie im Feld „Name des Migrationsendpunkts“ den gewünschten Namen des Migrationsendpunkts ein und klicken Sie auf „Neu“.
11. Schließen Sie das Fenster „Migrationsendpunkte“.
12. Klicken Sie auf das Pluszeichen und wählen Sie „Migration zu Exchange Online“. Das Fenster „Neuer Migrationsbatch“ öffnet sich.
13. Wählen Sie den Punkt „IMAP-Migration“ und laden Sie Ihre vorbereitete CSV-Datei hoch.
14. Vervollständigen Sie Ihren Eintrag mit „Weiter“.
15. Geben Sie im Feld „Name des neuen Migrationsbatches“ einen Namen Ihrer Wahl ein und klicken Sie auf „Weiter“.
16. Um die Migration zu starten, klicken Sie auf „Neu“. Sie können jetzt das Exchange Admin Center schließen. Der Migrationsprozess läuft im Hintergrund weiter.

Sie haben Ihre E-Mails von centron Mail Basic bzw. centron Mail Business zu Microsoft 365 migriert.

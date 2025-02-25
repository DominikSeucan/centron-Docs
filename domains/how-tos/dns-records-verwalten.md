---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# DNS Records verwalten

**Erstellen, Aktualisieren und Löschen von Einträgen über das Kontrollpanel**

Sie können DNS-Einträge für eine Domain auf der Netzwerkseite hinzufügen, ändern und löschen. Klicken Sie im Kontrollpanel auf "Netzwerk" im Hauptmenü und dann auf die Domain, die Sie verwalten möchten.

Um einen Eintrag zu erstellen, wählen Sie den Eintragstyp unter der Überschrift aus, füllen Sie die erforderlichen Felder für diesen Eintragstyp aus und klicken Sie auf "Eintrag erstellen". Die unten aufgeführten Abschnitte zu unterstützten Eintragstypen enthalten detaillierte Anleitungen für jeden Eintragstyp.

Um einen Eintrag zu ändern oder zu löschen, öffnen Sie das Menü "Mehr" des Eintrags.

Klicken Sie auf "Eintrag bearbeiten", um die Werte für diesen Eintrag zu ändern. Um den Eintrag dauerhaft zu löschen, klicken Sie auf "Löschen" und dann im Bestätigungsfenster auf "Eintrag löschen".

Diese Einträge werden erst wirksam, nachdem Sie Ihre Nameserver bei Ihrem Domain-Registrar aktualisiert haben und diese Änderungen verbreitet wurden, was bis zu 48 Stunden dauern kann.

**Unterstützte Eintragstypen:**

* **A-Einträge**: Verbinden eine IPv4-Adresse mit einem Domainnamen.
* **AAAA-Einträge**: Verbinden eine IPv6-Adresse mit einem Domainnamen.
* **CNAME-Einträge**: Definieren einen Alias für einen A-Eintrag.
* **MX-Einträge**: Spezifizieren die Mailserver, die für Ihre Domain zuständig sind.
* **TXT-Einträge**: Werden verwendet, um eine Zeichenkette mit einem Hostnamen zu verknüpfen.
* **SPF-Einträge**: Enthalten Listen von E-Mail-Servern, die autorisiert sind, E-Mails im Namen Ihrer Domain zu senden.
* **DKIM-Einträge**: Enthalten öffentliche Schlüssel, die zur Authentifizierung von E-Mails verwendet werden.
* **NS-Einträge**: Spezifizieren die Nameserver für eine Domain oder Subdomain.
* **SRV-Einträge**: Spezifizieren einen Hostnamen und Portnummer für einen spezifischen Dienst.
* **CAA-Einträge**: Spezifizieren, welche Zertifizierungsstellen Zertifikate für eine Domain ausstellen dürfen.
* **PTR (rDNS)-Einträge**: Verbinden einen Domainnamen mit einer IP-Adresse.

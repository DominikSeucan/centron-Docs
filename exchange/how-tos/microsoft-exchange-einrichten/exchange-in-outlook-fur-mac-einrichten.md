---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Exchange in Outlook für Mac einrichten

In diesem Artikel erfahren Sie, wie Sie auf Ihrem Apple Mac ein neues Microsoft Exchange 2019-Konto in Outlook 2019 oder Outlook 2016 einrichten.

**Wichtiger Hinweis**: Die Version von Outlook für Mac, die mit Microsoft 365 geliefert wird, unterstützt noch nicht die Einrichtung von Microsoft Exchange 2019-Konten. Verwenden Sie daher eine andere Programmversion von Outlook für Mac.

**Voraussetzungen**:

* Sie haben ein Microsoft Exchange 2019-Konto.
* Sie haben eine E-Mail-Adresse in Ihrem Microsoft Exchange 2019-Konto erstellt.
* Ein Autodiscover-Eintrag wurde in den DNS-Einstellungen Ihrer Domain angelegt.

**Outlook 2019:**

* Beachten Sie, dass MacOS 13.1 kein On-Premise Exchange mit Outlook 2019 unterstützt. On-Premise Exchange bezieht sich hier auf Exchange 2019, das nicht bei Microsoft Exchange Online, sondern bei centron gehostet wird.
* Für die Nutzung von Exchange 2019 mit Outlook 2019 ist ein Workaround erforderlich. Installieren Sie zuerst Outlook 2019 auf Ihrem Mac und führen Sie dann die Wiederherstellung der Outlook-Legacyversion durch.

**Einrichtung eines Kontos in Outlook 2019:**

1. Starten Sie Outlook 2019 für Mac.
2. Gehen Sie zu „Extras“ > „Konten“.
3. Wählen Sie „E-Mail-Konto hinzufügen“.
4. Geben Sie Ihre Microsoft Exchange 2019-E-Mail-Adresse ein und wählen Sie „Exchange“.
5. Geben Sie Ihre Exchange-Kontoinformationen ein, einschließlich Serveradresse „exchange2019.centron.de“ und schließen Sie die Einrichtung ab.
6. Autorisieren Sie Autodiscover für den Server „autodiscover.1and1.info“, falls gefragt.

**Outlook 2016:**

* Installieren Sie Outlook 2016 auf Ihrem Mac.
* Starten Sie Outlook 2016 und gehen Sie zu „Extras“ > „Konten“.
* Fügen Sie Ihr Microsoft Exchange 2019-Konto wie oben beschrieben hinzu.

Sollten Probleme bei der Einrichtung auftreten, überprüfen Sie den Autodiscover-Eintrag in den DNS-Einstellungen Ihrer Domain und berücksichtigen Sie, dass DNS-Änderungen Zeit zur Aktualisierung benötigen.

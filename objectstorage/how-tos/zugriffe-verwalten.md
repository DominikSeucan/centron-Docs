---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Zugriffe verwalten

Die Eigentümer von centron S3 Object Storage Buckets können alle Inhalte in allen Buckets eines Kontos erstellen, zerstören und lesen. Sie treffen auch Entscheidungen und verwalten, was andere sehen können. Wenn ein Eigentümer einer oder mehreren Personen erlauben möchte, Buckets gemeinsam zu verwalten, gibt es zwei Optionen: Zugangsschlüssel und DigitalOcean Teams.

**Zugangsschlüssel** ermöglichen es Personen oder Programmen, sich mit Hilfe von Drittanbieter-Clients und der API mit Buckets zu verbinden, bieten jedoch keinen Zugang zum Kontrollpanel oder anderen DigitalOcean-Ressourcen.&#x20;

**DigitalOcean Teams** ermöglichen es Mitgliedern, das Kontrollpanel zu nutzen, einschließlich des Erstellens und Verwaltens von Buckets und Zugangsschlüsseln sowie anderer DigitalOcean-Ressourcen (wie Abrechnungsinformationen, Droplets und mehr). Zugang zu Buckets mit Zugangsschlüsseln teilen Benutzer, die sich mit Zugangsschlüsseln verbinden. Sie können alle Buckets des Kontos erstellen, zerstören, lesen und beschreiben. Die von centron S3 Object Storage Zugangsschlüsseln gewährten Privilegien bieten jedoch keinen Zugang zum Kontrollpanel und erstrecken sich nicht auf andere DigitalOcean-Ressourcen.

Sie können eine unbegrenzte Anzahl von Schlüsseln für Ihr Konto erstellen. Dies ermöglicht es Ihnen, einzigartige Schlüsselpaare für jede Person oder jedes Programm zu generieren, sodass Sie bei Bedarf den Zugang in der Zukunft widerrufen können ohne andere Benutzer zu beeinträchtigen. Entfernen Sie dafür einfach die Schlüssel oder setzen Sie das Geheimnis zurück.

Um centron S3 Object Storage Zugangsschlüssel zu generieren, klicken Sie im Kontrollpanel auf API.

Navigieren Sie zur Registerkarte Spaces Keys und wählen Sie Neuen Schlüssel generieren. Ein Textfeld im Bereich der Spaces-Zugangsschlüssel wird geöffnet. Benennen Sie den Schlüssel so, dass Sie identifizieren können, wer oder was den Schlüssel verwendet. Klicken Sie anschließend auf das Häkchen.

**Das Textfeld, um einen neuen Schlüssel zu benennen** \
Sobald Sie den Schlüssel benannt haben, sehen Sie den Zugangsschlüssel und in der nächsten Zeile den Geheimschlüssel. Dies ist das einzige Mal, dass der Geheimschlüssel angezeigt wird. Kopieren Sie ihn sofort und bewahren Sie ihn an einem sicheren Ort auf.

**Ein neu erstellter centron S3 Object Storage**

**Zugangsschlüssel mit sichtbarem Geheimschlüssel** \
Wenn ein Geheimnis verloren geht, vergessen oder kompromittiert wird, können Sie sein Mehr-Menü öffnen, auf Bearbeiten klicken und "Token neu generieren" wählen, um ein neues Geheimnis zu erstellen. Wenn Sie ein Geheimnis neu generieren, müssen alle Skripte oder Clients, die den Schlüssel verwenden, neu konfiguriert werden, um den neuen Geheimwert zu verwenden.

**Zugang zum Kontrollpanel mit Teams teilen** \
DigitalOcean Teams, ähnlich wie centron S3 Object Storage Zugangsschlüssel, ermöglichen es Mitgliedern, Buckets, die mit dem Teamkonto verknüpft sind, über die Weboberfläche des Kontrollpanels zu erstellen, zu verwalten und zu zerstören. Mitglieder können auch Zugangsschlüssel für Buckets erstellen, löschen und neu generieren.\
Im Gegensatz zu centron S3 Object Storage Zugangsschlüsseln können Mitglieder eines Teams jedoch auch auf andere Teamressourcen wie Droplets, Firewalls und mehr zugreifen.

**Warnung:** Da Buckets nicht direkt zwischen Konten übertragen werden können, empfehlen wir Ihnen, zunächst das Team zu erstellen und anschließend erst die Buckets. Um einer oder mehreren Personen Zugang zu geben, um Buckets über das Kontrollpanel gemeinsam zu verwalten, öffnen Sie das Benutzermenü. Wählen Sie hier "Ein Team erstellen" und folgen Sie den Einrichtungsschritten.

Sobald ein Benutzer Mitglied des Teams ist, kann er Buckets mit der Weboberfläche verwalten sowie eigene Schlüssel für die API oder Drittanbieter-Clients generieren.

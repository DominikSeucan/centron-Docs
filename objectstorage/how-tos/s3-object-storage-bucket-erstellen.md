---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Januar 2025
---

# S3 Object Storage Bucket erstellen

centron S3 Object Storage bietet Ihnen die Möglichkeit, große Mengen an Daten zu speichern und bereitzustellen. Jeder Bucket, den Sie innerhalb eines Kontos erstellen, hat seine eigene URL und kann als logische Einheit zur Segmentierung von Inhalten verwendet werden.

Das URL-Namensschema für centron S3 Object Storage lautet bucketname.s3.internet1.de.



### Einen Bucket erstellen

Sie können jederzeit über das Menü "Create" einen Bucket erstellen, indem Sie "S3" auswählen. Dies führt Sie zur Seite "Create a S3 Bucket".



### **Vorgehensweise**

1. **Dateilistenbeschränkung wählen**: Wählen Sie, ob die Dateiliste des Buckets eingeschränkt oder sichtbar sein soll. Die Sichtbarkeit der Dateiliste eines Buckets hat keinen Einfluss auf die Sichtbarkeit der Dateien selbst. Sie können die Sichtbarkeit der Dateiliste jederzeit nach der Erstellung ändern.
2. **Einen eindeutigen Namen für Ihren Bucket wählen**: Der Name des Buckets ist Teil seiner Endpoint-URL und kann nach der Erstellung nicht geändert werden. Namen müssen:
   * Einzigartig unter allen Benutzern in allen Regionen sein.
   * Zwischen 3 und 63 Zeichen lang sein.
   * Nur Kleinbuchstaben, Zahlen und Bindestriche enthalten.
   * Mit einem Buchstaben oder einer Zahl beginnen.

{% hint style="danger" %}
Vermeiden Sie die Verwendung von persönlich identifizierbaren Daten oder anderen privaten Informationen in Bucket-Namen, da diese in clientseitigen Designs typischerweise nicht verschlüsselt sind.
{% endhint %}

3. **Bucket erstellen**: Nachdem Sie Ihre Einstellungen gewählt haben, klicken Sie auf "Create a S3 Bucket". Dies führt Sie zum "Files"-Tab des neu erstellten Buckets, der die Dateien und Ordner in seinem Root-Verzeichnis anzeigt.

Nach der Erstellung zeigt die "Settings"-Seite eines Buckets seinen Endpoint-Wert an, der zur Konfiguration von Drittanbieter-Clients verwendet wird. Die Index-Seite zeigt seinen Namen, seine Größe und sein Erstellungsdatum an.

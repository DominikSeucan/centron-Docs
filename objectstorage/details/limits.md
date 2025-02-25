---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Januar 2025
---

# Limits

#### **Buckets**

* Bis zu 100 Buckets pro Konto. Für eine Erhöhung des Limits kontaktieren Sie bitte den Support.
* Keine Unterstützung für centron-Tags oder Bucket-Tags.
* Der Name eines Buckets, der zur Löschung ansteht, kann während des Löschvorgangs (1 Woche oder länger) nicht wiederverwendet werden.

#### **SSL-Zertifikate**

* Kann nicht mit einem benutzerdefinierten Wildcard-SSL-Zertifikat gesichert werden, das bereits anderswo im Konto verwendet wird.
* Wildcard-SSL-Zertifikate stimmen nicht mit Buckets überein, wenn der Name des Buckets einen Punkt enthält.

#### **Automatische Löschung**

* Unvollständige Multi-Part-Uploads, die älter als 90 Tage sind, werden automatisch gelöscht.

#### **Anfragelimits**

* 1500 Anfragen (jede Operation) pro IP-Adresse pro Sekunde für alle Buckets auf einem Konto.
* 10 gleichzeitige PUT- oder COPY-Anfragen für jedes einzelne Objekt in einem Bucket.

#### **Objekt- und Dateigrößenlimits**

* PUT-Anfragen dürfen maximal 5 GB groß sein.
* Jeder Teil eines Multi-Part-Uploads darf maximal 5 GB groß sein.
* Der maximale Gesamtumfang eines Multi-Part-Uploads beträgt 5 TB.
* Maximale Nutzdatengröße für PUT-Anfragen und Einzelteile von Multi-Part-Uploads über CDN: 8100 KiB.
* Es sind maximal 10 Millionen Objekte pro Bucket zugelassen.

#### **Dateilöschung**

* Bis zu 9999 Dateien können gleichzeitig über das Control Panel gelöscht werden.



### **Bekannte Probleme**

**Sicherheitshistorie**

Löschaktionen in Buckets enthalten nicht die korrekte IP-Adresse, die die Aktion durchgeführt hat.

#### **Hochladen von Dateien**

Hochladen von Hunderten oder Tausenden von Dateien über die Cloud-Plattform kann unzuverlässig sein. Für diesen Anwendungsfall sollten Sie Tools wie s3cmd verwenden.

#### **API-Unterstützung**

Die S3-API unterstützt keine list-objects-v2-Paginierung.

#### **CDN-Subdomänenzertifikate**

Stilles Fehlschlagen des Hochladens von Zertifikaten zum CDN bei der Erneuerung. Dies kann dazu führen, dass das CDN aufhört, Assets mit SSL zu bedienen, sobald das ursprüngliche Zertifikat abläuft.


---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Best Practices

Zur Optimierung der Leistung von centron S3 Object Storage, basierend auf Ihrem Anwendungsfall und Ihrer Architektur, sollten Sie folgende Empfehlungen beachten:



### **Einsatz eines Content Delivery Networks (CDN):**

**Wann:** Besonders nützlich, wenn hauptsächlich GET-Anfragen aus dem Internet bedient werden, insbesondere bei häufigen Anfragen nach kleinen Dateien.

**Vorteile:** Verteilung von Inhalten mit geringer Latenz und höherer Datenübertragungsrate. Senkung der Latenz und Reduzierung der GET-Anfragen an centron S3 Object Storage.

**Umsetzung:** Nutzung des kostenlosen centron S3 Object Storage CDN, welches Teil Ihres Abonnements ist, oder anderer CDNs, die minimale Konfiguration benötigen.



### **Optimale Benennung von Objekten:**

**Wann:** Empfohlen, wenn Sie erwarten, den ListObject-API-Aufruf zu verwenden und eine erhebliche Anzahl von Objekten in Ihrem Bucket zu speichern.

**Vorteile:** Beschleunigung der ListObject-API bei unterschiedlichen Objektschlüsselanfängen.

**Umsetzung:** Präfix für jeden Objektschlüsselnamen im Bucket verwenden, z.B. Zufallszeichen oder aktuelles Datum.



### **Vermeidung kleiner Dateien und Nutzung von Multi-Part-Uploads für große Dateien:**

**Wann:** Bei der Handhabung von Dateien unter 1 MB oder dem Hochladen von Dateien über 500 MB.

**Vorteile:** Reduzierung der Gesamtanzahl von Anfragen an Ihren Space.

**Umsetzung:** Multi-Part-Uploads für Dateien über 500 MB nutzen und kleinere Dateien in einer größeren Datei zusammenführen



### **Wahl des richtigen Rechenzentrums für Ihre Ressourcen:**

**Wann:** Abhängig von der Herkunft der Verbindungen zu Ihren Buckets.

**Vorteile:** Minimale Latenz und stabile Verbindung über das centron-Backbone.

**Umsetzung:** Regionen für Ihre Ressourcen bei der Erstellung wählen oder bestehende Infrastruktur migrieren.



### **Korrekte Handhabung von 50x-Fehlern:**

**Wann:** Bei jedem Datei-Upload zu centron S3 Object Storage.

**Vorteile:** Schnellere Uploads und weniger manueller Eingriff.

**Umsetzung:** Verwendung von S3-kompatiblen Clients oder Bibliotheken mit Wiederholungslogik.



### **Optimierung Ihrer Anfragerate:**

**Wann:** Bei mehr als 150 Anfragen pro Sekunde oder bei Häufigkeit von 503 Slow Down-Antworten.

**Vorteile:** Vermeidung unerwarteter Drosselungen.

**Umsetzung:** Kombinieren kleiner Dateien oder Öffnen eines Support-Tickets bei hohem Anfrageaufkommen.



### **Einsatz lokaler oder Blockspeicher statt Object Storage:**

**Wann:** Für dynamische oder strukturierte Daten, die traditionellen Dateisystemzugriff erfordern.

**Vorteile:** Bessere Leistung für bestimmte Anwendungsfälle durch hardwarenahe, latenzarme I/O.

**Umsetzung:** Start mit Volumes oder Einsatz von Datenbanklösungen wie Redis oder Cassandra.

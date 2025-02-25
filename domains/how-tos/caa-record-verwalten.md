---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# CAA Record verwalten

### **Hintergrundinformationen zu CAA-Einträgen**

CAA (Certificate Authority Authorization) ist ein Standard, der darauf abzielt, die Erstellung unbefugter SSL/TLS-Zertifikate durch böswillige Akteure zu verhindern. CAA-Einträge legen fest, welche Zertifizierungsstellen (CAs) Zertifikate ausstellen dürfen.

Wie bei anderen Arten von DNS-Einträgen können CAA-Einträge für eine gesamte Domain (wie example.com) oder für bestimmte Subdomains (wie assets.example.com) gelten. Ebenso kann die Lebensdauer des Eintrags mit einem Time To Live (TTL)-Wert in Sekunden festgelegt werden.

CAA-Einträge haben drei zusätzliche Felder: Tags, Werte und Flags.

* **Tags** sind ASCII-Strings. Drei Tags sind durch den CAA-Standard definiert. Zusätzlich dazu erlaubt der CAA-Standard CAs, eigene Tags zu definieren. Jeder CAA-Eintrag ist auf ein einzelnes Tag beschränkt. Die definierten Tags sind:
  * `issue` autorisiert eine einzelne CA, jegliche Art von Zertifikat für einen bestimmten Hostnamen auszustellen.
  * `issuewild` autorisiert eine einzelne CA, ausschließlich ein Wildcard-Zertifikat für einen Hostnamen auszustellen.
  * `iodef` definiert eine URL, an die eine CA Verstöße gegen die Richtlinie melden kann.
* **Werte** sind Strings, die mit Tags verbunden sind.
  * Für die Tags `issue` und `issuewild` setzen Sie in der Regel den Wert auf den Domainnamen der CA, die durch den Eintrag die Erlaubnis erhält, wie z.B. letsencrypt.org.
  * Für `iodef` geben Sie eine URL an, an die Verstöße gegen die Richtlinien gemeldet werden sollen.
* **Flags** sind vorzeichenlose Ganzzahlen zwischen 0 und 255. Derzeit wird dieses Feld verwendet, um ein Issuer Critical-Flag zu setzen, das festlegt, wie eine CA sich verhalten soll, wenn sie auf ein ihr unbekanntes Tag stößt.

Der Standardflag ist 0. Fordert eine CA den DNS-Eintrag zur Ausstellung eines Zertifikats an und es gibt ein Tag, das sie nicht versteht, und das Flag ist auf 0 gesetzt, ignoriert sie diesen speziellen Eintrag und verarbeitet weitere Einträge.

Wenn jedoch irgendein Eintrag in der Antwort das Issuer Critical-Flag, 128, gesetzt hat und die CA das Tag in diesem Eintrag nicht versteht, muss eine standardkonforme CA die Ausstellung eines Zertifikats verweigern.

### **Erstellen von CAA-Einträgen**

Sie können einen neuen CAA-Eintrag auf der Netzwerkseite erstellen. Öffnen Sie im Kontrollpanel entweder das Menü "Erstellen" und klicken Sie auf "Domains/DNS" oder klicken Sie auf "Netzwerk" in der linken Navigationsleiste.

Auf der Netzwerkseite klicken Sie auf die Domain. Wählen Sie innerhalb der Domain unter der Überschrift "Neuen Eintrag erstellen" CAA aus. Der CAA-Tab enthält die Felder, die Sie benötigen, um CAA-Einträge hinzuzufügen.

---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Dateien hinzufügen und entfernen

### Dateien hochladen

**Größenbeschränkungen**: Aufgrund von Browserbeschränkungen funktionieren Uploads über das Control Panel am besten mit Dateien, die kleiner als 2 GB sind, und in Batches von weniger als 100 Dateien gruppiert sind. Für größere Dateien und Batches können Sie einen Drittanbieter-Client oder die DigitalOcean API verwenden.



### **Dateien hochladen**

Auf der Hauptseite Ihres Buckets können Sie Dateien auf zwei Arten hochladen:

**Drag-and-Drop**: Erlaubt das Hinzufügen von Dateien, Ordnern und Elementen in Ordnern.

**Upload Files auswählen**: Öffnet ein Fenster, um Dateien von Ihrem lokalen Computer hinzuzufügen, unterstützt jedoch nicht das Hinzufügen von Ordnern.

**Upload-Fenster**: Im Upload-Fenster können Sie die Dateiberechtigungen für alle gestagten Dateien festlegen. Mit dem "X"-Button neben jedem Element können Sie Dateien oder Ordner wieder entfernen. Ordner und ihr Inhalt werden als Einheit behandelt, daher entfernt das Entfernen eines Ordners hier den Ordner sowie alle darin enthaltenen Dateien und Ordner.

**Upload starten**: Klicken Sie auf "Upload Files", um die gestagten Elemente mit den ausgewählten Berechtigungen hochzuladen.



### Dateien herunterladen

**Download starten**: Um eine Datei von einem Bucket auf Ihren lokalen Computer herunterzuladen, öffnen Sie das "More"-Menü der Datei und wählen Sie "Download". Abhängig von den Einstellungen Ihres Browsers kann der Download automatisch starten oder Sie werden aufgefordert, die Datei zuerst zu speichern. Die Datei kann auch in Ihrem Browser geöffnet werden, abhängig vom Dateityp und Ihrem Browser.



### Dateien löschen

* **Datei löschen**: Um eine Datei aus einem Bucket zu löschen, öffnen Sie das "More"-Menü der Datei und wählen Sie "Delete". Löschungen sind endgültig, daher müssen Sie die Löschung in dem sich öffnenden Fenster bestätigen, bevor das Element tatsächlich gelöscht wird.
* **Mehrere Dateien löschen**: Sie können mehrere Dateien gleichzeitig löschen, indem Sie das "Actions"-Menü öffnen und auf "Delete" klicken. Hier werden Sie ebenfalls aufgefordert, die Löschung zu bestätigen.



### Dateien suchen

**Suchfunktion**: Um einen Bucket nach einer bestimmten Datei zu durchsuchen, gehen Sie zum "Files"-Tab des Buckets und geben Sie den Dateinamen in die Suchleiste ein. Dies zeigt alle Dateien an, die mit einer passenden Zeichenfolge im aktuellen Verzeichnis beginnen.

**Sucheinschränkungen**: Die Suchfunktion unterstützt nur Präfixsuche, d.h. es werden nur Dateien mit Namen zurückgegeben, die mit der gesuchten Zeichenfolge beginnen. Es gibt keinen Platzhalter für Wildcard-Suchen. Außerdem werden nur Dateien im aktuellen Verzeichnis zurückgegeben, d.h. es kann nicht in Ordnern gesucht werden.

---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Juni 2024
---

# Partitionen vergrößern

Bei centron angepasste Anleitung für die Erweiterung eines partitionierten Volumes:



### **Überprüfen der Partitionierung**

Wenn Sie nicht sicher sind, ob Ihr Volume partitioniert ist, können Sie dies mit `lsblk --fs` überprüfen:

```bash

sudo lsblk --fs /dev/disk/by-id/use_your_volume_identifier
```

Die Spalte `FSTYPE` listet ein Dateisystem wie `ext4` für unpartitionierte Volumes und eine Variante wie `sda1` für partitionierte Volumes auf.



### **Erweiterung eines partitionierten Volumes**

Zur Erweiterung eines partitionierten Volumes müssen Sie nach der Vergrößerung des Volumes selbst die letzte Partition erweitern, um den neuen Speicherplatz zu nutzen. Dies beinhaltet das Neuschreiben der Partitionstabelle und das Erweitern des Dateisystems der letzten Partition.



### **Neuschreiben der Partitionstabelle**

Wir empfehlen `gdisk` zum Neuschreiben von Partitionstabellen. Zuerst hängen Sie alle Partitionen aus. Dies ist der gleiche Prozess wie beim Aushängen eines unpartitionierten Volumes, wiederholt für jede der Partitionen auf dem Volume.

Wechseln Sie in ein schreibbares Verzeichnis und starten Sie `gdisk` mit dem Volume-Identifikator:

```bash
cd ~
sudo gdisk /dev/disk/by-id/use_your_volume_identifier
```

Für Sicherheit, verwenden Sie den `b` Befehl, um die aktuelle Partition zu sichern und geben Sie einen Dateinamen für das Backup ein, wenn Sie dazu aufgefordert werden.



### **Erweitern der letzten Partition**

Um den neuen Speicherplatz auf dem Volume zu nutzen, erweitern Sie die letzte Partition in den freien Bereich, indem Sie die bestehende Partition entfernen und neu erstellen.

Verwenden Sie `p`, um die aktuelle Partitionstabelle anzuzeigen, notieren Sie die Werte von Number, Start (Sektor), Code und Name der letzten Partition. Verwenden Sie diese, um die korrekten Werte bei der Erstellung der neuen Partition zu überprüfen.

Verwenden Sie `d`, um die Partition zu entfernen. Verwenden Sie `n`, um eine neue Partition zu erstellen. Die vorgeschlagenen Werte sind normalerweise korrekt, überprüfen Sie sie jedoch mit den Werten der gelöschten Partition. Akzeptieren Sie für die Eingabeaufforderung "Letzter Sektor" den Standardwert, um die Partition bis zum Ende der Festplatte zu erweitern.



### **Erweitern des Dateisystems der letzten Partition**

Als Nächstes müssen Sie das Dateisystem auf der letzten Partition erweitern, um den zusätzlichen verfügbaren Speicherplatz zu nutzen.

Zuerst hängen Sie die Festplatte aus:

```bash
sudo umount /mnt/use_your_mount_point
```

Das Verfahren zur Erweiterung des Dateisystems der letzten Partition hängt vom Dateisystemtyp ab.

Verwenden Sie `lsblk --fs`, um die Dateisysteme auf Ihren Partitionen zu überprüfen. Erweitern Sie ext4-Partitionen und überprüfen Sie sie mit `e2fsck` auf Inkonsistenzen, bevor Sie sie mit `resize2fs` erweitern:

```bash
sudo e2fsck -f /dev/disk/by-id/scsi-0DO_Volume_volume-nyc1-01-part1
sudo resize2fs /dev/disk/by-id/scsi-0DO_Volume_volume-nyc1-01-part1
```

Nach der Überprüfung und Erweiterung des Dateisystems können Sie das neue Dateisystem einbinden und den erweiterten Speicherplatz im Volume nutzen. Verwenden Sie `df -h -x tmpfs -x devtmpfs`, um die verfügbaren Speicherinformationen zu überprüfen.

Diese Anleitung passt zu den Funktionen und Diensten von centron, einschließlich der Verwaltung und Erweiterung von Speicherlösungen.

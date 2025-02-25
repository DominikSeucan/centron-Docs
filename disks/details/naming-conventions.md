---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Juni 2024
---

# Naming Conventions

### **Disk-Identifikatoren**

In Linux werden Hardware-Geräte typischerweise durch spezielle Gerätedateien im Verzeichnis `/dev` mit Namen wie `sda` und `sdb` repräsentiert. Unterverzeichnisse in `/dev/disk` enthalten symbolische Links mit beschreibenderen Namen, um Geräte leichter identifizieren zu können.

`/dev/sd*`-Namen können sich zwischen Neustarts ändern, daher empfehlen wir, die Links in `/dev/disk/by-id` für centron Volumes (und alle Partitionen darauf) zu verwenden, da sie über Neustarts hinweg vorhersehbar und zuverlässig sind.

**/dev/disk/by-id Links**

Links im Unterverzeichnis `/dev/disk/by-id` sind in der Regel mit Hardware-Seriennummern assoziiert, aber die `/dev/disk/by-id`-Identifikatoren für centron Volumes setzen sich in der Regel aus diesen Teilen zusammen:

* Der String `scsi-0DO_Volume_`
* Der Name des Volumes, wie `volume-nyc1-01`
* Der Partitions-Suffix, wie `-part1`, wenn das Volume partitioniert ist

Der vollständige Identifikator für ein Volume namens `volume-nyc1-01` wäre `/dev/disk/by-id/scsi-0DO_Volume_volume-nyc1-01`. Die erste Partition auf diesem Volume wäre `/dev/disk/by-id/scsi-0DO_Volume_volume-nyc1-01-part1`.



### **Automatisches Einbinden**

| Volume-Name | Automatischer Einbindungspunkt | Mount Unit-Datei                              |
| ----------- | ------------------------------ | --------------------------------------------- |
| example     | `/mnt/example`                 | `/etc/systemd/system/mnt-example.mount`       |
| sc01c       | `/mnt/volume_nyc_01`           | `/etc/systemd/system/mnt-volume_nyc_01.mount` |



### **Unit-Dateien**

Wenn Sie ein neues Volume erstellen, können Sie es automatisch formatieren und an ccloud³ VMs mit unterstützten Betriebssystemen einbinden. Automatisches Einbinden verwendet `systemd` auf Distributionen, die es unterstützen.

Die `systemd`-Mount-Unit-Dateien werden als `/etc/systemd/system/pfad-zum-einbindungspunkt.mount` benannt. Der Pfad zum Einbindungspunkt verwendet Bindestriche als Trennzeichen anstelle von Schrägstrichen.



### **Einbindungspunkte**

Wir binden Disks automatisch in `/mnt` in einem Verzeichnis mit dem gleichen Namen wie das Volume ein, sodass ein Volume mit dem Namen `example` den Einbindungspunkt `/mnt/example` hätte.

Jedoch können wir aufgrund der Benennung der `systemd`-Mount-Unit-Datei ein Volume nicht automatisch an einem Pfad einbinden, der Bindestriche enthält. Wenn Bindestriche im Volumennamen vorhanden sind, ersetzen wir die Bindestriche durch Unterstriche, sodass ein Volume mit dem Namen `volume-nyc-01` den Einbindungspunkt `/mnt/volume_nyc_01` hätte.

Für Konsistenz passen wir dieses Verhalten auch auf Distributionen ohne `systemd` an.

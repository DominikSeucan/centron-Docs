---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Quickstart

### Das Hinzufügen neuer Disks zu ccloud³ VMs&#x20;

Sie können ein neues Volume zu einer bestehenden ccloud³ VM hinzufügen oder dies während der Erstellung einer neuen ccloud³ VM tun.

Alternativ können Sie auf der Seite zur Erstellung von ccloud³ VMs im Abschnitt "Blockspeicher hinzufügen" auf "Volume hinzufügen" klicken.

Wählen Sie die Größe Ihres Disks aus, die zwischen 1 GB und 5 TB liegen kann.



### Formatieren und mounten Sie die Disk

Dies geschieht automatisch für unterstützte Betriebssysteme. Anleitungen zur manuellen Formatierung und zum Mounten finden Sie im Menü "Mehr" des Disks unter "Konfigurationsanweisungen".

Sowohl die automatische als auch die manuelle Einrichtung formatieren das Volume mit "ext4, mounten" es in "/mnt" mit den Optionen defaults, nofail, discard, noatime und aktualisieren /etc/fstab für ein dauerhaftes Mounten nach Neustarts.



### Die Größe von Disks erhöhen&#x20;

Wenn Sie mehr Speicherplatz benötigen, können Sie die Größe eines Disks erhöhen.

Vergrößern Sie das Volume selbst. Im "Mehr"-Menü des Disks wählen Sie "Größe erhöhen". Im Fenster "Disk-Größe erhöhen" geben Sie eine neue Größe in GB an (mindestens 1 GB größer als die aktuelle Größe) und klicken auf "Disk vergrößern". Erweitern Sie das Dateisystem, um den zusätzlichen Platz zu nutzen. Für ext4 verwenden Sie resize2fs. Für XFS verwenden Sie xfs\_growfs. Disks sind standardmäßig unpartitioniert, aber wenn Sie Ihr Volume bei der Erstellung manuell partitioniert haben, müssen Sie die letzte Partition erweitern, bevor Sie das Dateisystem erweitern.

Sie können die Größe eines Disks nicht verringern, da dies ein Risiko für Datenverlust und Dateisystemkorruption darstellt.



### Disks löschen&#x20;

Das Löschen einer Disk zerstört das Volume und seinen Inhalt dauerhaft und unwiderruflich.

Öffnen Sie das Menü "Mehr" der Disk und wählen Sie "Löschen". Im sich öffnenden Fenster "Volume löschen" bestätigen Sie die Löschung.

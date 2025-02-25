---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Juni 2024
---

# Disks mounten

#### **Formatieren einer Disk**

Wenn Sie ein neues Volume erstellen, müssen Sie es formatieren. Das Formatieren eines Volumes erstellt ein Dateisystem auf dem Volume und löscht alle vorhandenen Daten. Ein Volume muss nur einmal formatiert werden, wenn es zum ersten Mal erstellt wird, da neue Disks kein Dateisystem haben.

#### **Einbinden einer formatierten Disk**

Jedes Mal, wenn Sie ein Volume an eine ccloud³ VM anhängen, einschließlich des ersten Males, müssen Sie es einbinden. Das Einbinden eines formatierten Volumes fügt das Dateisystem des Volumes der bestehenden Dateihierarchie der ccloud³ VM hinzu. Sie müssen ein Volume jedes Mal einbinden, wenn Sie es an eine ccloud³ VM anhängen, um es für das Betriebssystem der VM zugänglich zu machen.

Um ein formatiertes Volume einzubinden, wählen Sie zuerst einen Einbindungspunkt, also das Verzeichnis, an dem das Dateisystem der Disk angehängt werden soll. Dort greifen Sie auf die Dateien der Disk zu, nachdem sie eingebunden ist.

Wir empfehlen ein neues Verzeichnis in "/mnt" als Einbindungspunkt zu erstellen:

```bash
sudo mkdir /mnt/example_mount_point
```

Verwenden Sie anschließend `mount`, um das Dateisystem des Volumes am Einbindungspunkt einzubinden. Wir empfehlen die gleichen Optionen wie beim automatischen Einbinden, die sind `defaults,nofail,discard,noatime`:

```bash
sudo mount -o defaults,nofail,discard,noatime /dev/disk/by-id/scsi-example /mnt/example_mount_point
```

**Einrichten des persistenten Einbindens**

Die Datei `/etc/fstab` enthält statische Informationen über Dateisysteme, die das Betriebssystem einbinden kann, einschließlich derer, die beim Booten automatisch eingebunden werden sollen. Sie können eine Zeile für das Dateisystem der Disk hinzufügen, um es beim Booten der ccloud³ VM automatisch einzubinden. Dies hält das Dateisystem der Disk auch nach Neustarts beständig.

Jede Zeile in `/etc/fstab` repräsentiert ein Dateisystem und besteht aus sechs durch Leerzeichen getrennten Feldern:

* `fs_spec`, das Blockgerät zum Einbinden. Verwenden Sie den `/dev/disk/by-id`-Identifikator für das Volume oder die Partition.
* `fs_file`, der Einbindungspunkt für das Dateisystem.
* `fs_vfstype`, der Typ des Dateisystems in Kleinbuchstaben, wie ext4 oder xfs.
* `fs_mntops`, die Einbindungsoptionen. Wir empfehlen die gleichen Optionen wie beim automatischen Einbinden: `defaults,nofail,discard,noatime`.

Letztendlich sollte die Zeile, die Sie zu `/etc/fstab` hinzufügen, mit dem Identifikator Ihres Volumes und dem Einbindungspunkt so aussehen:

```bash
/dev/disk/by-id/scsi-example /mnt/example-mount-point ext4 defaults,nofail,discard,noatime 0 2
```

Nachdem Sie die Datei bearbeitet haben, überprüfen Sie, ob `/etc/fstab` parsbar und nutzbar ist:

```bash
findmnt --verify --verbose
```

Dies listet alle Pars-, Ausführungsfehler und Warnungen auf. Sobald Sie alle Fehler behoben haben, können Sie `mount -a` verwenden, um das Volume einzubinden.

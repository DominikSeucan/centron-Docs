---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Disks partitionieren

**Partitionierung**

Partitionierung ermöglicht es Ihnen, ein einzelnes Speichergerät in kleinere Einheiten aufzuteilen, die Sie unabhängig verwalten können. Sie können mehrere Dateisysteme auf einem Gerät schreiben, um den Speicherplatz nach funktionalen Gesichtspunkten zu segmentieren.

Um Partitionen mit einem Volume zu verwenden, müssen Sie zuerst die Partition(en) erstellen und dann jede Partition formatieren.

**Partitionen erstellen**

Die beiden gängigsten Partitionierungssysteme sind das traditionelle Master Boot Record (MBR) Format und die modernere GUID Partitionstabelle (GPT). Das MBR-Format hat einige inhärente Einschränkungen, insbesondere bezüglich der Anzahl und Größe der Partitionen, die Sie erstellen können.

Wenn Sie keine speziellen Anforderungen haben, empfehlen wir die Verwendung von GPT-Partitionen. Für die Arbeit mit GPT-Partitionen empfehlen wir `parted` für nicht-interaktive Partitionierung und `gdisk` für interaktive Partitionierung.

**Nicht-interaktive Partitionierung mit `parted`**

Zuerst schreiben Sie eine leere GPT-Partitionstabelle auf Ihr Volume, indem Sie das Gerät mit dem `parted`-Befehl und dem Unterbefehl `mklabel gpt` übergeben:

```bash
sudo parted /dev/disk/by-id/scsi-0DO_Volume_volume-nyc1-01 mklabel gpt
```

**Partitionen erstellen**

Als Beispiel, dieser Befehl erstellt eine einzelne Partition, die das gesamte Volume umfasst:

```bash
sudo parted -a opt /dev/disk/by-id/scsi-example mkpart primary 0% 100%
```

**Partitionen formatieren**

Nach der Partitionierung müssen Sie die Partitionen formatieren, indem Sie ein Dateisystem auf jede schreiben.

**Formatieren mit ext4**

Um eine Partition mit einem ext4-Dateisystem zu formatieren, verwenden Sie `mkfs.ext4`:

```bash
bashCopy codesudo mkfs.ext4 /dev/disk/by-id/scsi-0DO_Volume_volume-nyc1-01-part1
```

Nachdem Sie jede Partition formatiert haben, sind Sie bereit, das Volume einzubinden und zu verwenden.

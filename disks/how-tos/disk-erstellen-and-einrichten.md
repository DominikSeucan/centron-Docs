---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Disk erstellen & einrichten

#### **Disks erstellen**

Um ein Volume über das Kontrollpanel von centron zu erstellen, öffnen Sie das Erstellungs-Menü und wählen Sie Volumes. Im Abschnitt "Blockspeicher hinzufügen" der ccloud³ VM-Erstellungsseite können Sie auch ein neues Volume erstellen und anhängen, während Sie eine neue ccloud³ VM erstellen.

#### **Disk-Größe auswählen**

Wählen Sie im Abschnitt "Volume-Größe auswählen" die Größe des Volumes, entweder durch Auswahl einer voreingestellten Größe oder durch Eingabe einer Größe in Gigabyte.

#### **ccloud³ VM auswählen und Volume benennen**

Wählen Sie im nächsten Abschnitt die ccloud³ VM, an die Sie das Volume anhängen möchten, und geben Sie einen Namen für das Volume ein. Disks befinden sich im gleichen Rechenzentrum und Projekt wie ihre zugeordneten ccloud³ VMs.

#### **Konfigurationsoptionen wählen**

In diesem Abschnitt wählen Sie, wie Sie das neue Volume formatieren und einbinden möchten.

#### **Automatisches Formatieren & Einbinden**

Wenn Sie ein Volume automatisch formatieren und einbinden, wählen Sie auch ein Dateisystem (ext4 ist standardmäßig ausgewählt). Sie können auch XFS wählen, das sich auf Leistung bei großen Datendateien spezialisiert hat.

#### **Manuelles Formatieren & Einbinden**

Wenn Sie sich für das manuelle Formatieren und Einbinden Ihres Volumes entscheiden, können Sie die VM-spezifischen Anweisungen im Menüpunkt "Mehr" unter Konfigurationsanweisungen des Volumes nutzen.

#### **Disk erstellen**

Nachdem Sie alle notwendigen Einstellungen gewählt haben, klicken Sie auf "Volume erstellen", um das Volume zu erstellen. Sobald das Volume formatiert und eingebunden ist, ist es einsatzbereit.

#### **Dateien hinzufügen, verschieben oder löschen**

Nachdem das Volume eingebunden wurde, ist es auf Ihrer ccloud³ VM unter "/mnt/ihrem-volume-name" zugänglich. Sie können diesen Pfad nutzen, um alle Dateioperationen durchzuführen, die Sie auch mit einem nativen Volume durchführen würden, einschließlich Erstellen, Verschieben oder Löschen von Dateien.

---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Features

#### Anwendungsfälle

Disks sind besonders nützlich, wenn Sie mehr Speicherplatz benötigen, aber nicht die zusätzliche Rechenleistung oder den zusätzlichen Speicher, den eine größere ccloud³ VM bieten würde, wie zum Beispiel:

* Als Dokumentenwurzel oder Verzeichnis für Medien-Uploads auf einem Webserver.
* Zum Speichern von Datenbankdateien für einen Datenbankserver.
* Als Zielort für Backups.
* Als erweiterter Speicher für persönliche Datei-Hosting-Plattformen wie ownCloud.
* Als Speicher für bestimmte verteilte Webanwendungen und Workflows in den Bereichen künstliche Intelligenz und maschinelles Lernen.

#### Benutzerfreundlichkeit

Disks funktionieren als generische Blockgeräte, sodass Sie angehängte Disks wie lokal angeschlossene Speicherlaufwerke behandeln können. Dies ermöglicht es Ihnen, Disks mit bekannten Tools und Techniken zu partitionieren, formatieren und verwalten.

Sie können wählen, ob Sie ein Volume für die erstmalige Verwendung aufWindows, Ubuntu, Fedora, Debian 8+, CentOS und Fedora Atomic formatieren und einbinden möchten.

#### Flexibilität

Disks sind unabhängige Ressourcen, sodass Sie sie zwischen ccloud³ VMs im gleichen Rechenzentrum verschieben können, und Sie können die Größe eines Disks erhöhen, ohne die zugehörige ccloud³ VM herunterzufahren.

Volume-Snapshots sind vollständige Festplattenabbilder, die Sie auf Abruf erstellen können. Erstellen Sie einen Snapshot, um den Inhalt des Disks zu speichern, und erstellen Sie Disks basierend auf Snapshots, um ein neues Volume mit dem gleichen Inhalt zu erstellen.

#### Leistung

Wie ccloud³ VMs sind Disks durch SSDs unterstützt.

Disks verfügen auch über Burst-Unterstützung. Die Burst-Unterstützung erhöht automatisch die IOPS- und Bandbreitenraten der Disks für kurze Zeiträume (60 Sekunden), bevor sie zur Basisleistung zurückkehren, um Spitzen in der Arbeitslast zu unterstützen.

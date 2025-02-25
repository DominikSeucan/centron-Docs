---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# Features

#### **Wie funktionieren centron ccloud³ VM Backups?**

Backups sind ein automatischer Prozess, der innerhalb eines vordefinierten Zeitfensters erfolgt und im Hintergrund ausgeführt wird, während die ccloud³ VM läuft. Dies ermöglicht systemweite Backups Ihres Servers, ohne diesen herunterzufahren.

#### **Prozess während eines Backups:**

1. Es wird ein Snapshot des laufenden Systems erstellt, wodurch ein Crash-konsistentes, zeitpunktbezogenes Image entsteht.
2. Der Snapshot wird außerhalb der Disk gesichert.
3. Der Snapshot wird gelöscht, sobald das Backup abgeschlossen ist.

#### **Crash-Konsistenz Backup:**

* Ein Crash-konsistentes Backup ermöglicht es, alle Daten auf der Festplatte genau so zu erfassen, wie sie zu einem bestimmten Zeitpunkt waren. Das bedeutet, dass die Daten in einem konsistenten Zustand gesichert werden.

#### **Backup-Zeitplan:**

* Sobald Sie Backups aktiviert haben, werden sie wöchentlich innerhalb eines spezifischen Zeitfensters geplant, das automatisch von centron zugewiesen wird. Um das Zeitfenster, in dem Ihre Backups beginnen, einzusehen, navigieren Sie zu Ihrer ccloud³ VM im centron Control Panel und klicken Sie auf den Link "Backups".
* Im "Backups"-Block finden Sie eine Angabe wie diese: "Backups sind derzeit aktiviert. Sie sind geplant, wöchentlich von Sonntag 15 Uhr bis Montag 14 Uhr zu beginnen."
* Backups für Ihre ccloud³ VM beginnen irgendwann während des angegebenen Zeitfensters. Abhängig davon, wann das Backup gestartet wird und wie groß die zu sichernde Disk ist, kann es sein, dass es nicht bis zum Ende des aufgeführten Fensters abgeschlossen wird.

#### **Bitte beachten Sie:**

* Backups eignen sich möglicherweise nicht ideal für ccloud³ VMs mit intensiven I/O-Workloads wie Datenbankserver, da die Disk-Leistung während der Erstellung des Backups beeinträchtigt werden kann.
* centron-automatisierte Backups könnten ähnlich wie bei DigitalOcean keine Volumes beinhalten, aber Sie können manuelle Backups mit Volume-Snapshots durchführen.

Diese Informationen sind an die ccloud³ VMs von centron angepasst und basieren auf den Funktionen und Prozessen von DigitalOcean Backups.

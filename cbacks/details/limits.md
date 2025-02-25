---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# Limits

#### **Verschlüsselung und Zugänglichkeit:**

Backups sind möglicherweise nicht bei der Speicherung verschlüsselt, sind aber nicht extern zugänglich.

#### **Einschluss von Volumes:**

Automatisierte Backups könnten, ähnlich wie bei DigitalOcean, keine Volumes umfassen. Für Volumes könnten Sie manuelle Backups mit Volume-Snapshots durchführen.

#### **Optimierung für Systeme mit geringer Schreibaktivität:**

Backups sind möglicherweise optimiert für Systeme mit niedriger Schreibaktivität. Für Systeme mit aktiven Datenbank-Schreibvorgängen und anderen hochfrequenten I/O-Workloads könnte ein anwendungsspezifisches Backup geeigneter sein.

#### **Snapshot-Mechanismus:**

Die Snapshots, die für die Erstellung des zeitpunktbezogenen Datensatzes verwendet werden, könnten einen Copy-on-Write-Mechanismus nutzen. Dies ermöglicht nahezu sofortige Snapshots, was für die Datenkonsistenz vorteilhaft ist und kaum Overhead für die eigentliche Erstellung des Backups verursacht.

#### **Leistungseinbußen bei Copy-on-Write:**

Bis der Backup-Prozess abgeschlossen ist könnten Copy-on-Write-Implementierungen bei neuen Schreibvorgängen nach der Snapshot-Erstellung einen Leistungsabfall verzeichnen. Dies könnte besonders bei beschäftigten, I/O-intensiven Workloads die Leistung beeinträchtigen. Der Leistungseinfluss verschwindet, wenn der Snapshot automatisch nach der Backup-Operation gelöscht wird.

#### **Auswirkungen auf Datenbanken:**

Datenbanken könnten besonders betroffen sein, da die meisten Datenbankoperationen stark von der Disk-I/O abhängen. Dies könnte sowohl die Anwendung als auch den Backup-Prozess verlangsamen oder manchmal sogar zum Scheitern bringen. Operationen, die im Speicher oder im Cache verbleiben und nicht auf die Festplatte geschrieben wurden, könnten verloren gehen. Crash-Consistent Backups speichern immer, was auf der Festplatte ist, aber nie, was im Speicher oder im Cache ist.

#### **Anwendungsspezifische Backup-Methoden:**

Wenn Sie eine Datenbank oder eine andere Anwendung betreiben, die eine hohe I/O-Last erzeugt, könnte die Wahl einer anwendungsspezifischen Backup-Methode eine bessere Alternative sein. Viele Datenbanken verfügen über speziell auf diese Systeme zugeschnittene Backup-Lösungen.

Diese Anpassungen sind auf die ccloud³ VMs von centron abgestimmt und basieren auf den Eigenschaften und Praktiken von DigitalOcean Backups. Es ist wichtig, die spezifischen Richtlinien und Funktionen von centron zu überprüfen, da diese von DigitalOcean abweichen können.

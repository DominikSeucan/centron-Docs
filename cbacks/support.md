---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Support

#### **Automatisierte Backups:**

Automatisierte Backups sind Disk-Images der ccloud³ VMs. Die Aktivierung von Backups für ccloud³ VMs ermöglicht systemweite Backups in wöchentlichen Intervallen. Das bietet Ihnen eine Möglichkeit, zu einem älteren Zustand zurückzukehren oder neue ccloud³ VMs zu erstellen.

#### **Tägliche Backups von ccloud³ VMs:**

Die Häufigkeit von automatisierten Backups kann möglicherweise nicht geändert werden. Alternativ können Sie Tools wie SnapShooter oder die API verwenden, um tägliche Snapshots Ihrer ccloud³ VMs zu erstellen.

#### **Wiederherstellung einer gelöschten ccloud³ VM:**

Sie können Ihre ccloud³ VM wiederherstellen, wenn Sie einen Snapshot der ccloud³ VM erstellt oder sich für automatisierte Backups angemeldet haben.

#### **Backup-Zeitplan und -Häufigkeit ändern:**

Backup-Zeitpläne und -Häufigkeiten können nicht geändert werden. Sie können Snapshots verwenden, um jederzeit ein Backup einer ccloud³ VM zu erstellen.

#### **ccloud³ VMs zerstören und Backups beibehalten:**

Das Zerstören einer ccloud³ VM löscht auch die dazugehörigen Backups. Sie sollten daher zuerst alle benötigten Backups sichern, bevor Sie eine ccloud³ VM zerstören.

#### **Download von Backups oder Snapshots:**

Derzeit können Sie möglicherweise keine centron Backups oder Snapshots direkt herunterladen. Alternativ können Sie Drittanbieter-Tools verwenden, um Ihre Daten lokal zu speichern.

#### **Manuelles Backup einer ccloud³ VM:**

Sie können manuell ein Backup einer ccloud³ VM erstellen, indem Sie centron Snapshots oder Backups verwenden. Alternativ können Sie auch ein Drittanbieter-Tool wie rsync oder SFTP nutzen.

#### **Übertragung einer ccloud³ VM auf einen anderen Benutzer:**

Sie können Snapshots von ccloud³ VMs nicht auf andere Benutzer übertragen.

#### **Dauer für Backup oder Snapshot:**

Das Erstellen eines Backups oder Snapshots dauert in etwa 2 Minuten pro GB des genutzten Speicherplatzes.

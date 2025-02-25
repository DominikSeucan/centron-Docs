---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# Support

#### **Warum kann ich keine ccloud³ VM aus einem Snapshot erstellen?**&#x20;

Sie können in bestimmten Rechenzentren aufgrund begrenzter Kapazität keine ccloud³ VMs erstellen. Wenn Sie Snapshots in einem Rechenzentrum mit begrenzter Kapazität haben, übertragen Sie diese in ein anderes Rechenzentrum, um dort ccloud³ VMs daraus zu erstellen.

#### **Kann ich eine ccloud³ VM mit einem Snapshot verkleinern?**&#x20;

Sie können eine ccloud³ VM nicht aus einem Snapshot verkleinern. Daten werden nicht immer sequentiell im Speicher gespeichert, sodass die Verkleinerung einer Festplatte zu Datenverlust oder -korruption führen kann.

#### **Warum unterscheidet sich die Größe meines Snapshots von der gemeldeten Festplattennutzung?**&#x20;

Snapshots von ccloud³ VMs sind eine bestmögliche Schätzung basierend auf der Festplattennutzung. Snapshots von Volumes arbeiten auf Blockspeicherebene, daher kann die Snapshot-Größe von dem abweichen, was das Dateisystem meldet.

#### **Beim Versuch, einen Snapshot wiederherzustellen, erhalte ich einen Fehler, dass die Ressource nicht gefunden werden konnte.**&#x20;

Erstellen Sie eine neue ccloud³ VM aus Ihrem Snapshot-Image.

#### **Wie klone ich oder erstelle ich eine Kopie einer ccloud³ VM?**&#x20;

Erstellen Sie einen Snapshot der ccloud³ VM und erstellen Sie dann eine neue ccloud³ VM aus diesem Snapshot. Snapshot-Übertragungen an andere Benutzer sind vorübergehend für einige neue Konten nicht verfügbar.  Als vorübergehende Lösung können neue centron-Benutzer, die mit einem Teamkonto beginnen, Snapshots über Teams an andere Benutzer übertragen statt direkt über die E-Mail-Adresse.

#### **Wie kann ich eine gelöschte ccloud³ VM wiederherstellen?**&#x20;

Sie können Ihre ccloud³ VM wiederherstellen, wenn Sie zuvor manuell einen Snapshot der ccloud³ VM erstellt haben oder sich für automatisierte Backups angemeldet haben.

#### **Behalten Snapshots die IP-Adresse der ccloud³ VM, von der sie erstellt wurden?**&#x20;

Nein, Snapshots behalten nicht die IP-Adresse der ccloud³ VM, von der sie erstellt wurden. Sie können jedoch reservierte IP-Adressen verwenden, um dieselbe Adresse neuen oder neu bereitgestellten ccloud³ VMs zuzuweisen.

#### **Wie kann ich meine ccloud³ VMs zerstören, während ich meine Backups beibehalte?**&#x20;

Wenn Sie eine ccloud³ VM zerstören, werden auch die dazugehörigen Backups gelöscht. Sie sollten daher zunächst Ihre Backups sichern, bevor Sie die ccloud³ VM zerstören.

#### **Kann ich ein Backup oder einen Snapshot herunterladen?**&#x20;

Derzeit können Sie centron Backups oder Snapshots nicht direkt herunterladen. Sie können jedoch Drittanbieter-Tools verwenden, um Ihre Daten lokal zu speichern.

#### **Wie führe ich manuell ein Backup meiner ccloud³ VM durch?**&#x20;

Sie können manuell ein Backup einer ccloud³ VM durchführen, indem Sie centron Snapshots oder Backups verwenden. Alternativ können Sie auch ein Drittanbieter-Tool wie rsync oder SFTP nutzen.

#### **Wie übertrage ich eine ccloud³ VM auf einen anderen Benutzer?**&#x20;

Sie können Snapshots von ccloud³ VMs nicht auf andere Benutzer übertragen.

#### **Wie lange dauert es, bis mein Backup oder Snapshot abgeschlossen ist?**

Das Erstellen eines Backups oder Snapshots dauert in etwa 2 Minuten pro GB des genutzten Speicherplatzes.

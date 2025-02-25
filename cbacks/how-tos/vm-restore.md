---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# VM Restore

Um neue centron ccloud³ VMs aus Backups zu erstellen und bestehende ccloud³ VMs aus Backups wiederherzustellen, können Sie die folgenden Schritte ausführen:

### **Neue ccloud³ VMs aus Backups erstellen**

#### **Über das Control Panel:**

Klicken Sie im Control Panel auf den Namen der ccloud³ VM mit dem Backup, das Sie verwenden möchten. Klicken Sie nun auf "Backups".

Im Abschnitt "Backups der ccloud³ VM" öffnen Sie das "Mehr"-Menü des Backups, welches Sie verwenden möchten. Wählen Sie "ccloud³ VM erstellen".

Dies führt Sie zum Erstellungsbildschirm der ccloud³ VM mit dem ausgewählten Backup als Image. Legen Sie die restlichen Optionen der ccloud³ VM fest.

Beachten Sie: Um die Datenintegrität zu bewahren, müssen Sie eine Festplattengröße wählen, die gleich oder größer als die der ursprünglichen ccloud³ VM ist, von der das Backup erstellt wurde.

Klicken Sie abschließend auf "Erstellen", um eine ccloud³ VM basierend auf dem ausgewählten Backup zu erstellen.

#### **Datenübertragung:**

Sobald die neue ccloud³ VM erstellt wurde, können Sie Dateien zwischen der ursprünglichen und der neuen ccloud³ VM mit Dateiübertragungstools wie scp oder rsync kopieren.



### **ccloud³ VMs aus Backups wiederherstellen**

#### **Über Automation:**

Sie können eine ccloud³ VM aus einem Backup wiederherstellen, indem Sie einen entsprechenden Befehl verwenden oder eine Anfrage an den ccloud³ VM-Aktions-Endpunkt senden und das Feld `restore` auf die ID des Backup-Images setzen.

#### **Über das Control Panel:**

* Um eine ccloud³ VM auf eines ihrer Backups wiederherzustellen, klicken Sie im Control Panel auf den Namen der ccloud³ VM und dann auf "Backups". Im Abschnitt "Backups der ccloud³ VM" öffnen Sie das "Mehr"-Menü des Backups, aus welchem Sie wiederherstellen möchten. Wählen Sie hier "ccloud³ VM wiederherstellen".
* Da die Wiederherstellung eines Backups auf Ihrer ccloud³ VM bestehende Daten auf dieser ccloud³ VM löscht, ist eine Bestätigung erforderlich, um den Vorgang abzuschließen. Bestätigen Sie die Wiederherstellung im Fenster "ccloud³ VM wiederherstellen".
* Die Wiederherstellung aus einem Backup schaltet Ihre ccloud³ VM während des Wiederherstellungsprozesses aus. Sobald die Wiederherstellung abgeschlossen ist, erfolgt eine automatische Wiedereinschaltun&#x67;_._

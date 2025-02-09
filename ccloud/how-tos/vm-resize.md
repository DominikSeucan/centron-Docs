---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# VM Resize

Das Ändern der Größe eines Servers beeinflusst die Ressourcen (CPU, RAM und Festplatte), die ihm zur Verfügung stehen. Für ccloud³ VMs gibt es zwei Optionen zur Größenänderung:

1. **Nur CPU und RAM**: Diese Option ermöglicht es Ihnen, die Menge an CPU und RAM, die einer ccloud³ VM zur Verfügung stehen, zu ändern.
2. **Festplatte, CPU und RAM**: Mit dieser Option können Sie die Menge an CPU und RAM, die einer ccloud³ VM zur Verfügung stehen, ändern und die Größe der Festplatte der ccloud³ VM dauerhaft erhöhen.

Das Erhöhen des Arbeitsspeichers und der CPU einer ccloud³ VM verbessert deren Leistung. Das Vergrößern der Festplatte erhöht die Menge an Daten, die Sie speichern können.

Sie können auf jeden ccloud³ VM-Tarif umsteigen, der gleich viel oder mehr Festplattenspeicher als die ursprüngliche ccloud³ VM hat. Das bedeutet, dass Sie die Menge an CPU und RAM erhöhen oder verringern und die Menge des Festplattenspeichers erhöhen können.



### Überlegungen vor der Größenänderung

* Planen Sie etwa eine Minute Ausfallzeit pro GB genutzten Festplattenspeicher ein, obwohl die tatsächlich benötigte Zeit normalerweise kürzer ist. Sie können den Festplattenspeicher im Dateisystem mit `df / -h` überprüfen.
* Die geschätzte Ausfallzeit hängt von der Festplattennutzung ab - auch bei Größenänderungen, die die Festplattengröße nicht verändern. Dies liegt daran, dass die ccloud³ VM möglicherweise auf einen neuen Hypervisor umzieht, wodurch Festplattendaten über das Netzwerk übertragen werden.
* Wir empfehlen Ihnen dringend, vor der Größenänderung einen Snapshot der ccloud³ VM zu erstellen.
* ccloud³ VMs können während einer Größenänderung Hypervisors wechseln. Änderungen am Dateisystem können bei Problemen zu Datenverlust führen. Wir empfehlen dringend, die Daten der ccloud³ VM vor der Größenänderung zu sichern. Wenn Sie Snapshots verwenden, können Sie den Snapshot nach Bestätigung des erfolgreichen Umzugs löschen.
* Sie können die Größe der Festplatte einer ccloud³ VM nicht verringern.



### ccloud³ VMs über das Control Panel oder die API ändern

* Sie können ccloud³ VMs über das Control Panel oder die API von centron ändern.
* Bevor Sie eine ccloud³ VM im Control Panel ändern können, müssen Sie sie ausschalten. Wir empfehlen, dies über die Befehlszeile zu tun, um Datenkorruption zu vermeiden. Fügen Sie SSH zu Ihrer ccloud³ VM hinzu und führen Sie den Befehl `sudo shutdown -h now` aus.
* Gehen Sie dann zum centron Control Panel. Klicken Sie auf der Seite ccloud³ VMs auf den Namen der ccloud³ VM, die Sie ändern möchten, und anschießend auf die Option "Größe ändern" im ccloud³ VM-spezifischen Menü.
* Wählen Sie CPU & RAM oder Festplatte, CPU & RAM zur Größenänderung aus und wählen Sie dann die gewünschte ccloud³ VM-Größe. Sobald die ccloud³ VM heruntergefahren ist und Sie ihren neuen Plan ausgewählt haben, klicken Sie auf "Größe ändern". Ein Fortschrittsbalken zeigt den Fortschritt der Größenänderung an.
* Wenn die Größenänderung abgeschlossen ist, klicken Sie auf die Ein-/Aus-Taste, um die ccloud³ VM wieder einzuschalten.

### Überprüfen von Festplattengrößenänderungen

* In bestimmten Fällen schlägt eine Festplattengrößenänderung fehl, um die Partition oder das Dateisystem der ccloud³ VM zu ändern. Wenn Sie `df -h` nach einer Festplattengrößenänderung erneut ausführen und die Ausgabe unverändert ist, deutet dies normalerweise auf ein Problem hin. Verwenden Sie `gdisk`, um weitere Informationen zu erhalten.
* Um die Partition zu ändern, verwenden Sie den Befehl `growpart`.
* Der Befehl zum Ändern des Dateisystems hängt vom Dateisystemtyp ab. Verwenden Sie `resize2fs` für ext3/4-Dateisysteme oder `xfs_growfs` für XFS-Dateisysteme.

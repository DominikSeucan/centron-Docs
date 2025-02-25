---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Juni 2024
---

# Support

#### **Kann ich ein Volume an mehrere ccloud³ VMs anhängen?**

Nein, jedoch können Sie Ihrem ccloud³ VM mit einem angehängten Volume eine zusätzliche Schicht hinzufügen.

#### **Warum zeigt meine ccloud³ VM fast 100% Festplattenauslastung, auch nachdem ich ein neues Volume hinzugefügt habe?**

Das Hinzufügen eines Volumes zu Ihrer ccloud³ VM erhöht nicht die Größe ihrer Hauptfestplatte. Sie müssen die ccloud³ VM vergrößern, um deren Hauptfestplattengröße zu erhöhen.

#### **Warum ist mein vergrößertes Volume kleiner als erwartet?**

Dateisystem-Tools berichten oft nicht über die Kapazität, die für Metadaten und den Root-Benutzer reserviert ist, und manche berichten Größe in unterschiedlichen Einheiten.

#### **Warum unterscheidet sich die Größe meines Snapshots von der gemeldeten Festplattennutzung?**

Snapshots von ccloud³ VMs sind eine bestmögliche Schätzung, basierend auf der Festplattennutzung. Snapshots von Volumes operieren auf der Ebene des Blockspeichers, sodass die Snapshot-Größe nicht mit dem übereinstimmen muss, was das Dateisystem berichtet.

#### **Kann ich ein Backup oder einen Snapshot herunterladen?**

Derzeit können Sie keine Backups oder Snapshots von centron herunterladen, aber Sie können Drittanbieter-Tools verwenden, um Ihre Daten lokal zu speichern.

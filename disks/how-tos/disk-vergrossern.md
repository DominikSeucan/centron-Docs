---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Juni 2024
---

# Disk vergrößern

Wenn Sie mehr Speicherplatz benötigen als Ihr aktuelles Volume bietet, können Sie zusätzliche Volumes an die gleiche ccloud³ VM anhängen oder die Größe eines aktuellen Volumes erweitern.

**Überlegungen vor der Größenänderung**

* Sie können die Größe eines Volumes nicht verringern. Volume-Änderungen sind also irreversibel.
* Zur Verringerung des Speicherplatzes eines Volumes erstellen Sie ein kleineres Volume und übertragen die Inhalte des bestehenden Volumes mit einem Tool wie SnapShooter oder rsync.
* Wir empfehlen dringend, vor der Größenänderung ein Snapshot der Disk zu erstellen.

**Disk-Größe über das Kontrollpanel ändern**

* Nachdem Sie ein Backup der Disk erstellt haben, können Sie dessen Größe im Kontrollpanel erhöhen. Wählen Sie im Menü "Mehr" des Volumes die Option "Größe erhöhen".
* Wählen Sie im sich öffnenden Fenster eine neue Größe für das Volume aus.

**Dateisystem erweitern**

* Um den zusätzlichen Speicherplatz zu nutzen, müssen Sie das Dateisystem des Volumes erweitern.
* Für nicht partitionierte Volumes mit ext4-Dateisystem geben Sie den Volume-Identifikator `/dev/disk/by-id` an `resize2fs` weiter.
* Stellen Sie sicher, dass das Volume eingehängt ist, bevor Sie den Befehl ausführen.
* Überprüfen Sie die Verfügbarkeit des erweiterten Dateisystems mit `df`.

{% hint style="info" %}
Einige Betriebssysteme benötigen einen Neustart, um die neue Größe der Disk zu erkennen. Starten Sie Ihre ccloud³ VM neu, falls erforderlich.
{% endhint %}

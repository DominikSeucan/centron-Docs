---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# VM Snapshot

Sie können Snapshots von einer bestehenden ccloud³ VM erstellen, um alle aktuellen Inhalte von der Festplatte der ccloud³ VM zu sichern.

Abhängig von den Diensten, die auf der ccloud³ VM laufen, möchten Sie möglicherweise die ccloud³ VM vor der Erstellung eines Snapshots ausschalten, um sicherzustellen, dass alle Anwendungen ihre Daten auf die Festplatte geschrieben haben. Beispielsweise garantieren viele Datenbanken keine Datenkonsistenz auf der Festplatte, es sei denn, der Datenbankdienst wird gestoppt oder die gesamte ccloud³ VM wird zuerst ausgeschaltet.

### Ausschalten und Snapshot (empfohlen)&#x20;

**Live Snapshot**&#x20;

Sie können eine ccloud³ VM über das Control Panel oder mit der Befehlszeile mit poweroff oder shutdown ausschalten. Wir empfehlen die Verwendung der Befehlszeile, da sie sicherstellt, dass alle Dienste gestoppt sind, bevor die ccloud³ VM ausgeschaltet wird:

```arduino
sudo shutdown -h now
```

Wenn Sie jedoch eine ccloud³ VM über das Control Panel ausschalten möchten, klicken Sie auf den Namen der ccloud³ VM, um auf ihre Detailseite zu gelangen. Klicken Sie in der oberen rechten Ecke auf den ON-Schalter und dann im Popup-Warnfenster auf "Turn off".

### Snapshot einer ccloud³ VM mit Automatisierung

Sobald die ccloud³ VM ausgeschaltet ist, können Sie einen Snapshot der ccloud³ VM erstellen, indem Sie den folgenden doctl-Befehl verwenden oder eine Anfrage an den VM Actions-Endpunkt senden und das type-Feld auf "snapshot" setzen.

**Wie man einen Snapshot einer ccloud³ VM mit der centron API macht**&#x20;

{% embed url="https://doku.ccloud.de/#ccloud-customer-api-snapshots" %}

**Snapshot einer ccloud³ VM über das Control Panel** \
Sobald die ccloud³ VM ausgeschaltet ist, können Sie aus dem Snapshots-Menü der ccloud³ VM im Abschnitt "Take snapshot" einen Snapshot erstellen.

### Take snapshot button&#x20;

Das Feld "Enter snapshot name" wird standardmäßig mit dem Namen der ccloud³ VM gefüllt, gefolgt vom aktuellen Unix-Zeitstempel, um Ihnen später die Identifizierung des Snapshots zu erleichtern. Alternativ können Sie den Namen allerdings auch vor oder nach der Erstellung manuell anpassen.&#x20;

Klicken Sie nun auf die Schaltfläche "Take Snapshot" oder "Take Live Snapshot", um einen (Live) Snapshot zu erstellen.

Eine Fortschrittsleiste zeigt den Fortschritt der Snapshot-Erstellung an. Nach Fertigstellung wird der Snapshot zusammen mit allen früheren Snapshots aufgelistet. Um die ccloud³ VM wieder einzuschalten, klicken Sie auf den OFF-Schalter.

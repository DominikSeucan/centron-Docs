---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Firewall erstellen

Beim Erstellen einer neuen Cloud-Firewall über das centron Control Panel wählen Sie zunächst einen Namen für Ihre Firewall im Feld "Name" und definieren dann mindestens eine Regel.

### **Standard-Eingehende Regel:**&#x20;

#### **SSH**&#x20;

Da der Kompromiss eines Servers typischerweise über eine eingehende Verbindung beginnt, bleiben die standardmäßigen eingehenden Verbindungen, mit einer Ausnahme, vollständig eingeschränkt. Die vorgeschlagene Regel erlaubt SSH-Verbindungen auf Port 22 von überall, sodass Benutzer den Server von einem Terminal aus administrieren können.

### **Standard-Ausgehende Regeln:**&#x20;

#### **Erlauben aller Verkehrsarten**&#x20;

Viele grundlegende Dienste sind auf ausgehende Kommunikation angewiesen. Dienste wie Ping benötigen ausgehendes ICMP. DNS-Abfragen, VoIP und NTP sind auf ausgehende UDP-Verbindungen angewiesen. Aufgaben wie Datensynchronisation, Paketlisten-Updates, Webanfragen und E-Mail erfordern ausgehende TCP-Verbindungen.

Daher erlauben die vorgeschlagenen ausgehenden Regeln allen Verkehr zu jedem Ziel auf jedem Port. Diese Standardeinstellungen erleichtern die Einrichtung eines neuen Servers, ohne Einschränkungen einzuführen, die die erwartete Funktionalität blockieren könnten.

#### **Anwenden auf ccloud³ VMs**&#x20;

Nachdem Sie die Regeln der Firewall konfiguriert haben, wenden Sie die Firewall auf die ccloud³ VMs an, die Sie sichern möchten, indem Sie das Feld "Anwenden auf ccloud³ VMs" verwenden. Sie können dieses Feld auch leer lassen und später ccloud³ VMs zuweisen.

Geben Sie im Feld "Anwenden auf ccloud³ VMs" den Namen einer ccloud³ VM oder eines Ressourcen-Tags ein. Ein Dropdown-Menü mit entsprechenden Ressourcen wird angezeigt. Wählen Sie ccloud³ VMs nach Namen, Tag oder einer Kombination aus beidem. Sie können auch nach IP-Adresse nach ccloud³ VMs suchen.

#### **Grenzen**&#x20;

Es gibt Grenzen für die Anzahl der ccloud³ VMs und Tags, die einer Firewall hinzugefügt werden können, aber keine Grenzen für die Anzahl der ccloud³ VMs, die mit einem Tag verknüpft werden können. Die Verwendung von Tags ermöglicht es Ihnen, das individuelle Limit für ccloud³ VMs bei Firewalls zu überschreiten. Sie können auch eine ccloud³ VM beim Erstellen taggen, was bedeutet, dass Sie Firewall-Regeln sofort anwenden können.

Eine ccloud³ VM kann durch mehr als eine Cloud-Firewall geschützt werden. In diesem Fall wird eine Vereinigung der Regeln angewendet. Zum Beispiel, wenn eine Regel TCP von jeder Quelle erlaubt und eine andere TCP von einem eingeschränkten Bereich erlaubt, bedeutet die Vereinigung der beiden, dass TCP-Verkehr von überall erlaubt ist.

#### **Firewall erstellen**&#x20;

Nachdem Sie die Regeln der Firewall definiert und ccloud³ VMs hinzugefügt haben, klicken Sie auf "Firewall erstellen".

Nachdem Sie eine Firewall erstellt haben, können Sie deren Regeln und die Ressourcen, die sie schützt, über den Reiter "Firewalls" im Abschnitt "Networking" des Control Panels verwalten.

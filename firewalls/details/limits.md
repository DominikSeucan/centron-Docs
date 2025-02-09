---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Limits

Bei centron können Sie maximal 10 ccloud³ VMs pro Firewall haben und bis zu 5 Tags pro Firewall verwenden. Wenn Sie mehr als 10 ccloud³ VMs haben, die dieselbe Firewall benötigen, versehen Sie die ccloud³ VMs mit Tags und fügen diesen Tag dann zur Firewall hinzu.

Jede Firewall kann bis zu 50 eingehende und ausgehende Regeln haben.

Cloud-Firewalls können nicht auf Load-Balancer angewendet werden.

Firewalls beeinflussen sowohl den öffentlichen als auch den VPC-Netzwerkverkehr. Regeln, die spezifisch für eines davon sind, müssen den öffentlichen oder privaten IP-Bereich angeben.

Firewalls unterstützen nur ICMP, TCP und UDP.

Firewalls blockieren den Verkehr auf Netzwerkebene, bevor dieser Ihre Ressourcen erreicht. Aus diesem Grund sind Verkehrslogs nicht verfügbar.

Das Hinzufügen neuer Regeln zu einer Firewall führt nicht zur Beendigung bestehender Verbindungen.

Firewall-Regeln sind auf 1000 Einträge im Quellen- oder Zielbereich beschränkt. Um mehr als 1000 IPs zu filtern, verwenden Sie Tags oder Netzwerkbereiche anstelle der Auflistung einzelner IPs. Weitere Informationen finden Sie in der Anleitung zum Konfigurieren von Firewall-Regeln.

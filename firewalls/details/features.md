---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Features

Firewalls dienen als Barriere zwischen Ihren Servern und anderen Maschinen im Netzwerk, um sie vor externen Angriffen zu schützen. Firewalls können hostbasiert sein, was bedeutet, dass sie auf Basis einzelner Server konfiguriert werden, unter Verwendung von Diensten wie IPTables oder UFW. Andere, wie die Cloud-Firewalls von Centron, sind netzwerkbasiert und stoppen den Datenverkehr auf Netzwerkebene, bevor er den Server erreicht.

Sie können Cloud-Firewall-Regeln auf einzelne ccloud³ VMs anwenden, aber eine leistungsfähigere Option ist die Verwendung von Tags. Tags sind benutzerdefinierte Labels, die Sie ccloud³ VMs und anderen Centron-Ressourcen zuweisen können. Wenn Sie einem Firewall ein Tag hinzufügen, werden alle ccloud³ VMs mit diesem Tag automatisch in die Firewall-Konfiguration einbezogen.

Diese Methode ermöglicht eine flexible und effiziente Verwaltung von Sicherheitsregeln, insbesondere in dynamischen Umgebungen, in denen ccloud³ VMs häufig hinzugefügt, entfernt oder geändert werden. So können Sie beispielsweise ein Tag "Webserver" für alle VMs erstellen, die als Webserver fungieren und ein anderes Tag "Datenbank" für diejenigen, die Datenbankdienste bereitstellen. Durch die Anwendung von Firewall-Regeln auf diese Tags, statt auf einzelne VMs, vereinfachen Sie die Wartung und sorgen für Konsistenz in der Sicherheitsrichtlinie Ihrer Infrastruktur.

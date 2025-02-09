---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Firewall konfigurieren

Eingehende Firewall-Regeln bei centron definieren den erlaubten Verkehr zum Server, einschließlich der Ports und der Quellen. Wenn keine eingehenden Regeln konfiguriert sind, wird kein eingehender Verkehr zugelassen.

Ausgehende Firewall-Regeln definieren den erlaubten Verkehr, der den Server verlassen darf, einschließlich der Ports und der Ziele. Wenn keine ausgehenden Regeln konfiguriert sind, wird kein ausgehender Verkehr zugelassen.

Hinweis: Der centron Cloud-Firewall-Service ist eine separate Firewall von jeder Firewall-Software, die auf einer ccloud³ VM läuft, wie z.B. UFW oder IPFire. Alle Regeln, die mit dem Cloud-Firewall-Service erstellt werden, spiegeln sich nicht in der Firewall-Software der ccloud³ VMs wider, die sie schützen. Wenn Sie außerdem sowohl den Cloud-Firewall-Service als auch eine Firewall-Software auf ccloud³ VM-Basis verwenden, stellen Sie sicher, dass die Regeln zwischen den beiden Firewalls nicht in Konflikt stehen.



**Regeln einer Firewall über das Control Panel hinzufügen oder entfernen**

* Um die Regeln einer Firewall zu verwalten, navigieren Sie im Control Panel von "Networking" zu "Firewalls". Klicken Sie auf den Namen der Firewall, um zu deren Regeln-Tab zu gelangen. Hier können Sie neue Regeln erstellen und vorhandene bearbeiten oder löschen.

Hinweis: Wenn mehr als eine Firewall auf eine ccloud³ VM angewendet wird, sind die Regeln additiv und können nicht durch andere Regeln wieder eingeschränkt werden.

**Neue Regeln erstellen**

* Sie können neue eingehende und ausgehende Regeln erstellen, indem Sie die Liste "Neue Regel" unter "Eingehende Regeln" oder "Ausgehende Regeln" öffnen. Sie können eine voreingestellte Protokollregel verwenden oder eine benutzerdefinierte Regel erstellen.

Hinweis: Sie können Firewall-Regeln nur definieren, um den Verkehr zu und von Ports, basierend auf Verbindungstypen, Quellen und Zielen, zu beschränken. Sie können keine Regel definieren, um den Verkehr, basierend auf HTTP-Headern wie X-Forwarded-For, Content-Type oder User-Agent, einzuschränken.

* Für benutzerdefinierte Regeln geben Sie das Protokoll, den Portbereich und die Quelle oder das Ziel an.
* Sie können die Quellen/Ziele auf ccloud³ VMs, centron Load Balancer, centron Kubernetes-Cluster oder auf Nicht-centron-Server durch IP-Adressen, Subnetze oder CIDR-Bereiche beschränken.

**Regeln bearbeiten oder löschen**

* Um eine Regel zu bearbeiten oder zu löschen, öffnen Sie das "Mehr"-Menü der Regel und wählen Sie "Regel bearbeiten" oder "Regel löschen". Beim Löschen einer Regel wird sie sofort ohne zusätzliche Bestätigung gelöscht.

---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Quickstart

Bei centron können Sie eine neue Cloud-Firewall über das Control Panel, die API oder die CLI erstellen.

**Erstellen einer Firewall über das Control Panel:** Nutzen Sie dafür die Firewall-Erstellungsseite im Control Panel.

**Erstellen einer Firewall über die API:** Verwenden Sie dafür den Endpunkt `/v2/firewalls`.

Beim Erstellen einer Firewall müssen Sie deren Namen, die eingehenden und ausgehenden Regeln sowie die ccloud³ VMs, auf die sich die Firewall-Regeln beziehen, festlegen.

**Eingehende Regeln (Inbound Rules):** Eingehende Firewall-Regeln definieren, welcher Verkehr zum Server zugelassen wird, auf welchen Ports und von welchen Quellen. Wenn Sie keine eingehenden Regeln konfigurieren, erlaubt der Server keinen eingehenden Datenverkehr.

Die im Control Panel vorgeschlagene eingehende Regel erlaubt SSH-Verbindungen auf Port 22 von überall, sodass Sie alle ccloud³ VMs hinter dieser Firewall über ein Terminal administrieren können.

**Ausgehende Regeln (Outbound Rules):** Ausgehende Firewall-Regeln definieren, welcher Verkehr den Server verlassen darf, auf welchen Ports und zu welchen Zielen. Wenn Sie keine ausgehenden Regeln konfigurieren, erlaubt der Server keinen ausgehenden Datenverkehr.

Die im Control Panel vorgeschlagenen ausgehenden Regeln erlauben jeden Verkehr zu jedem Ziel auf jedem Port. Dies erleichtert das Einrichten eines neuen Servers, da viele grundlegende Dienste auf ausgehende Verbindungen angewiesen sind.

**Anwendung auf ccloud³ VMs:** Sie können wählen, ob Sie die Firewall-Regeln auf einzelne ccloud³ VMs anwenden, entweder nach Name oder nach Tag. Die Verwendung von Tags ermöglicht es Ihnen, Firewall-Regeln auf ccloud³ VMs anzuwenden, sobald Sie diese erstellen, und vereinfacht das Verwalten Ihrer ccloud³ VMs im Allgemeinen.

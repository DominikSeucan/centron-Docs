---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# Limits

Einige Arten von Netzwerkverkehr bei ccloud³ VMs sind eingeschränkt, um böswillige Aktionen wie reflektierte DDoS-Angriffe zu verhindern. Diese Einschränkungen verhindern auch Funktionen wie die Konfiguration von Direct Server Return und die Nutzung von ccloud³ VMs als Router und Site-to-Site-VPN-Gateways. Zukünftige Änderungen an unserem Netzwerk werden diese Funktionalität unterstützen. Bis dahin beinhalten einige Workarounds die Verwendung eines VPN-Mesh-Netzwerks oder Overlay-Netzwerks.

Die folgenden Arten von Verkehr sind eingeschränkt:

* TCP- und UDP-Verkehr auf Port 11211 von externen Netzwerken eingehend (aufgrund der Memcached-Amplifikationsangriffe im März 2018)
* Multicast-Verkehr
* Verkehr, der nicht mit der IP-Adresse/MAC-Adresse einer ccloud³ VM übereinstimmt
* SMTP über zusätzliche IPs und IPv6

Alle ccloud³ VMs  haben eine Netzwerk-Durchsatzbeschränkung von 1 Gbps.&#x20;

Sie können nicht mehr als 10 ccloud³ VMs gleichzeitig über das Control Panel oder die API erstellen.

Der SMTP-Port 25 ist bei allen ccloud³ VMs für neue Konten blockiert. Als Alternative empfehlen wir die Verwendung einer dedizierten E-Mail-Zustellplattform wie Cleverreach. Wir raten Ihnen generell davon ab, Ihren eigenen Mailserver zu betreiben.

Root-Passwort-Resets sind für Betriebssysteme mit intern verwalteten Passwörtern, einschließlich Fedora, nicht verfügbar.

ccloud³ VMs kann nicht mehr als eine reservierte IP-Adresse gleichzeitig zugewiesen werden.

### VM Ressourcen

Ihre VM kann mindestens und höchstens folgende Ressourcen besitzen:

| Ressource | Minimum | Maximum |
| --------- | ------- | ------- |
| vCPU      | 1       | 24      |
| RAM (GB)  | 1       | 64      |
| SSD (GB)  | 5       | 3000    |

### Nested Virtualization

Im Rahmen von ccloud³ VMs inkl. allen zusätzlichen Funktionen wird Nested Virtualization nicht unterstützt.

### Bekannte Probleme

Aufgrund unseres Netzwerkdesigns können Traceroute-Diagnosen zwischen ccloud³ VMs während der letzten zwei Hops 100% Paketverlust anzeigen. Der Paketverlust ist zu erwarten und hat keinen Einfluss auf die Konnektivität zwischen ccloud³ VMs.

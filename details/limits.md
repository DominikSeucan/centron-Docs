---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Limits

#### Einschränkungen

Einige Arten von Netzwerkverkehr bei ccloud³ VMs sind eingeschränkt, um böswillige Aktionen wie reflektierte DDoS-Angriffe zu verhindern. Diese Einschränkungen verhindern auch Funktionen wie die Konfiguration von Direct Server Return und die Nutzung von ccloud³ VMs als Router und Site-to-Site-VPN-Gateways. Zukünftige Änderungen an unserem Netzwerk werden diese Funktionalität unterstützen. Bis dahin beinhalten einige Workarounds die Verwendung eines VPN-Mesh-Netzwerks oder Overlay-Netzwerks.

Die folgenden Arten von Verkehr sind eingeschränkt:

* TCP- und UDP-Verkehr auf Port 11211 von externen Netzwerken eingehend (aufgrund der Memcached-Amplifikationsangriffe im März 2018).
* Multicast-Verkehr.
* Verkehr, der nicht mit der IP-Adresse/MAC-Adresse einer ccloud³ VM übereinstimmt.
* SMTP über reservierte IPs und IPv6.

CPU-optimierte ccloud³ VMs mit Premium-CPUs haben eine Netzwerk-Durchsatzbeschränkung von 10 Gbps. Alle anderen ccloud³ VMs haben eine maximale Netzwerk-Durchsatzgrenze von 2 Gbps.

Sie können nicht mehr als 10 ccloud³ VMs gleichzeitig über das Control Panel oder die API erstellen.

Der SMTP-Port 25 ist bei allen ccloud³ VMs für neue Konten blockiert. Als Alternative empfehlen wir die Verwendung einer dedizierten E-Mail-Zustellplattform, wie SendGrid, und raten generell davon ab, Ihren eigenen Mailserver zu betreiben.

/proc/cpuinfo zeigt Ihren ccloud³ VM-Plan an, entweder DO-Premium oder DO-Regular. Sie können sehen, welche Prozessoren jeder Plan in der Auswahl des richtigen ccloud³ VM-Plans verwendet.

Root-Passwort-Resets sind für Betriebssysteme mit intern verwalteten Passwörtern, einschließlich Fedora, nicht verfügbar.

ccloud³ VMs können nicht mehr als eine reservierte IP-Adresse gleichzeitig zugewiesen haben.

#### Bekannte Probleme

Aufgrund unseres Netzwerkdesigns können Traceroute-Diagnosen zwischen ccloud³ VMs während der letzten zwei Hops 100% Paketverlust anzeigen. Der Paketverlust ist zu erwarten und hat keinen Einfluss auf die Konnektivität zwischen ccloud³ VMs.

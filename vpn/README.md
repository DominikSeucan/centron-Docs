---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Quickstart

## Virtual Private Network <a href="#virtual_private_network" id="virtual_private_network"></a>

In dieser Kategorie erhalten Sie Informationen zu Virtual Private Networks.

### Was ist ein Virtual Private Network (VPN) ? <a href="#was_ist_ein_virtual_private_network_vpn" id="was_ist_ein_virtual_private_network_vpn"></a>

Ein Virtual Private Network (VPN) stellt eine verschlüsselte, zielgerichtete Übertragung von Daten über öffentliche Netzwerke, wie das Internet, bereit. Damit ein sicherer Betrieb mit Datenschutz möglich ist, muss folgendes sichergestellt werden:

* _Authentizität_, welche erreicht wird durch:
  * Identifizierung autorisierter Benutzer
  * Überprüfung der Daten, dass sie auch nur aus der autorisierten Quelle stammen
* _Vertraulichkeit_ (wird erreicht durch Verschlüsselung)
* _Integrität_ (Daten können nicht von Dritten verändert werden)

Einsatzmöglichkeiten:

* Anbindung mehrerer Standorte. (Site-to-Site-VPN)
* Anbindung von Kunden oder sonstiger externer Unternehmen an das Unternehmensnetzwerk. (z.B.: externe IT-Dienstleistungsunternehmen)
* Anbindung von Außendienstmitarbeitern oder Homeoffice Usern. (End-to-Site-VPN)

### Welche Arten gibt es ? <a href="#welche_arten_gibt_es" id="welche_arten_gibt_es"></a>

#### End-to-Site-VPN / Remote-Access-VPN <a href="#end-to-site-vpnremote-access-vpn" id="end-to-site-vpnremote-access-vpn"></a>

![](https://wiki8.centron.de/_media/server/end_to_site.png?w=600\&tok=b0908f)

* Clients werden in Unternehmensnetzwerke eingebunden.

z. B. externe Mitarbeiter mit Heimarbeitsplatz oder mobile Benutzer.

#### Site-to-Site-VPN / LAN-to-LAN-VPN / Branch-Office-VPN <a href="#site-to-site-vpnlan-to-lan-vpnbranch-office-vpn" id="site-to-site-vpnlan-to-lan-vpnbranch-office-vpn"></a>

![](https://wiki8.centron.de/_media/server/site_to_site.png?w=600\&tok=c9ccae)

* mehrere lokale Netzwerke werden über öffentliches Netz zu einem virtuellen Netzwerk zusammengeschalten.
* virtuell: Site-to-Site-VPN; physikalisch: Standleitung.

#### End-to-End-VPN / Host-to-Host-VPN / Remote-Desktop-VPN <a href="#end-to-end-vpnhost-to-host-vpnremote-desktop-vpn" id="end-to-end-vpnhost-to-host-vpnremote-desktop-vpn"></a>

![](https://wiki8.centron.de/_media/server/end_to_end.png?w=600\&tok=08eea7)

* Client greift auf einen anderen Client in entferntem Netzwerk zu.
* VPN deckt gesamte Verbindung zwischen zwei Clients/Hosts ab.
* auf beiden Seiten ist eine VPN-Software nötig.
* keine direkte Verbindung, sondern jeweils Verbindung zu Gateway, welche beide Verbindungen zusammenschaltet.
* meist proprietäre und kommerzielle Software wie z.B. Teamviewer und GoToMyPC. (RDP und VNC nur lokal, da Verschlüsselung fehlt)

#### IPSec <a href="#ipsec" id="ipsec"></a>

Bei IPSec handelt es sich um eine Erweiterung des Internet-Protokolls (IP) um Verschlüsselungs- und Authentifizierungsmechanismen.

* Verbindungsmodus: Tunnelmodus.
* geeignet für Gateway-to-Gateway-Szenarien. (Verbindung zwischen Netzen über drittes (unsicheres) Netz)

Sicherheitsmechanismen:

* Zugriffskontrolle
* Datenintegrität
* Verschlüsselung
* Authentifizierung
* kryptografischer Schutz der übertragenen Daten.
* Interoperabilität
* Verwaltung von Schlüsseln

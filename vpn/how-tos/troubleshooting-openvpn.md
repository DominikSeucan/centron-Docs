---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Troubleshooting OpenVPN

In diesen Artikel erfahren Sie, wie Sie Log–Dateien einsehen können, die Version Ihres Clients nachprüfen und VPN-Konfigurationsdateien exportieren. Am Ende finden Sie noch eine kleine Auflistung der häufigsten Fehler.

### Client Bedienung <a href="#client_bedienung" id="client_bedienung"></a>

Hier zeigen wir Ihnen, wie Sie die Log-Dateien auslesen, die Version nachprüfen und ihre Konfiguration exportieren.

#### Log-Dateien einsehen <a href="#log-dateien_einsehen" id="log-dateien_einsehen"></a>

* Bereits beim Start sehen Sie den Log des Clients im Hintergrund des Anmeldefensters.

![](https://wiki8.centron.de/_media/server/vpn/openvpn_01.png)

* Kopieren Sie diesen einfach in die Mail an unsere Techniker.

#### Version des Clients nachprüfen <a href="#version_des_clients_nachpruefen" id="version_des_clients_nachpruefen"></a>

* Machen Sie einen Rechtsklick auf das Icon des OpenVPN-Client in der Symbolleiste. Dort wählen Sie „Einstellungen…“. Nun öffnet sich ein weiteres Fenster, dort wählen Sie im Reiter den Punkt „Über“.

![](https://wiki8.centron.de/_media/server/vpn/openvpn_03.png)

#### VPN-Konfigurationsdateien <a href="#vpn-konfigurationsdateien" id="vpn-konfigurationsdateien"></a>

* Machen Sie einen Rechtsklick auf das Icon des OpenVPN-Client in der Symbolleiste. Dort wählen Sie „Einstellungen…“. Nun öffnet sich ein weiteres Fenster, dort wählen Sie im Reiter den Punkt „Erweitert“.

![](https://wiki8.centron.de/_media/server/vpn/openvpn_04.png)

* Nun kopieren Sie den Pfad der Konfigurationsdatei und geben diesen im Windows-Explorer ein. Nun sehen Sie den Ordner mit der Datei.

![](https://wiki8.centron.de/_media/server/vpn/openvpn_05.png)

### Häufige Probleme <a href="#haufige_probleme" id="haufige_probleme"></a>

#### Benutzer oder Passwort falsch <a href="#benutzer_oder_passwort_falsch" id="benutzer_oder_passwort_falsch"></a>

* Häufig kommt es vor, dass die VPN Verbindung nicht hergestellt werden kann, da ein falsches Passwort oder ein falscher Benutzer eingegeben wurde. Überprüfen Sie den Log und sollten Sie folgende Fehlermeldung sehen, stimmt das Passwort, oder der Benutzername nicht.

![](https://wiki8.centron.de/_media/server/vpn/openvpn_error_01.png)

* Bitte überprüfen Sie Ihre Eingaben. Sollte der Login weiterhin fehlschlagen, wenden Sie sich bitte an unseren Support.

### Weitere Fehler <a href="#weitere_fehler" id="weitere_fehler"></a>

* Noch mehr Fehlerbeschreibungen und Problemlösungen finden Sie auf der Herstellerwebseite:\
  [OpenVPN FAQ](https://www.ovpn.com/de/faq/fehlerbehebung)

\

---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Troubleshooting Securepoint

In diesen Artikel erfahren Sie, wie Sie Log–Dateien einsehen können, die Version Ihres Clients nachprüfen und VPN-Konfigurationsdateien exportieren. Am Ende finden Sie noch eine kleine Auflistung der häufigsten Fehler.

### Client Bedienung <a href="#client_bedienung" id="client_bedienung"></a>

Hier zeigen wir Ihnen, wie Sie die Log-Dateien auslesen, die Version nachprüfen und ihre Konfiguration exportieren.

#### Log-Dateien einsehen <a href="#log-dateien_einsehen" id="log-dateien_einsehen"></a>

* Machen Sie einen Rechtsklick auf die fehlschlagende Verbindung und wählen Sie die Punk „Log“ aus.

![](https://wiki8.centron.de/_media/server/vpn/securepoint_01.png)

* Nun wird Ihnen der aktuelle Log Ihres Client angezeigt. Klicken Sie auf „Speichern“ um den Log als gesonderte TXT-Datei abzuspeichern. Gerne können Sie die Log-Datei auch heraus kopieren und Ihn uns direkt in der Mail zukommen zu lassen.

![](https://wiki8.centron.de/_media/server/vpn/securepoint_02.png)

#### Version des Clients nachprüfen <a href="#version_des_clients_nachpruefen" id="version_des_clients_nachpruefen"></a>

* Klicken Sie auf das Zahnrad-Symbol am unteren rechten Eck des Interfaces und wählen Sie „Information“.

![](https://wiki8.centron.de/_media/server/vpn/securepoint_05.png)

* Nun sehen Sie Ihre Client-Version. Bitte teilen Sie diese unseren Technikern mit.

![](https://wiki8.centron.de/_media/server/vpn/securepoint_04.png)

#### Konfigurationsdateien exportieren <a href="#konfigurationsdateien_exportieren" id="konfigurationsdateien_exportieren"></a>

* Machen Sie einen Rechtsklick auf die Verbindung, bei der Sie die Konfigurationsdatei exportieren möchten. Wählen Sie den Punkt „Exportieren“.

![](https://wiki8.centron.de/_media/server/vpn/securepoint_03.png)

* Nun wählen Sie einen Speicherort für die exportierte Datei.

### Häufige Probleme <a href="#haufige_probleme" id="haufige_probleme"></a>

#### Benutzer oder Passwort falsch <a href="#benutzer_oder_passwort_falsch" id="benutzer_oder_passwort_falsch"></a>

* Häufig kommt es vor, dass die VPN Verbindung nicht hergestellt werden kann, da ein falsches Passwort oder ein falscher Benutzer eingegeben wurde. Überprüfen Sie den Log, sollten Sie folgende Fehlermeldung sehen, stimmt das Passwort, oder der Benutzername nicht.

![](https://wiki8.centron.de/_media/server/vpn/securepoint_error_01.png)

* Bitte überprüfen Sie Ihre Eingaben. Sollte der Login weiterhin fehlschlagen, wenden Sie sich bitte an unseren Support.

#### TAP Adapter nicht gefunden <a href="#tap_adapter_nicht_gefunden" id="tap_adapter_nicht_gefunden"></a>

* Bei Starten des Client kann es zu folgender Fehlermeldung kommen:

![](https://wiki8.centron.de/_media/server/vpn/securepoint_error_02.jpg)

* Dies ist ein Problem, welches bei älteren Versionen von securepoint vorkommen kann, bitte installieren Sie die neuste Client-Version.

### Weitere Fehler <a href="#weitere_fehler" id="weitere_fehler"></a>

* Noch mehr Fehlerbeschreibungen und Problemlösungen finden Sie auf der Herstellerwebseite:\
  [Securepoint VPN Client FAQ](https://wiki.securepoint.de/VPN/faq/fehlerbehebung)

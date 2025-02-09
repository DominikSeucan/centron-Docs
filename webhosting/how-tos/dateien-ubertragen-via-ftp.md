---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Dateien übertragen via FTP

### Verwendung <a href="#verwendung" id="verwendung"></a>

Sie können das FTP-Protokoll zusammen mit einem FTP-Client nutzen, um Daten wie Bilder, HTML-Dateien oder Scriptdateien zwischen Ihrem Computer und Ihrem Server zu übertragen.

### FTP-Server <a href="#ftp-server" id="ftp-server"></a>

In Ihrem Webhosting-Paket sind normalerweise ein oder mehrere FTP-Zugänge freigeschaltet.

Sie können für jeden FTP-Benutzer einen eigenen Benutzernamen und ein zugehöriges sicheres Kennwort festlegen.\
Dem FTP-Benutzer wird auch der Dokumentenpfad mitgegeben, auf welchen er Zugriff hat. Möchten Sie beispielsweise einen Benutzer für einen Dienstleister erstellen, welcher nur auf den Ordner unter dem Pfad `/web/entwicklung/` Zugriff haben soll, dann können Sie den Zugang des FTP-Benutzers auf diesen Ordner (und untergeordnete) beschränken.

Als weitere Option können Sie für jeden FTP-Benutzer festlegen, ob er Dateien lesen, schreiben oder beides darf. Im Normalfall benötigt Ihr FTP-Benutzer beide Berechtigungen für den gewählten Dokumentenpfad.

#### Konfiguration <a href="#konfiguration" id="konfiguration"></a>

Die Konfiguration eines FTP-Nutzers ist von Hostsystem und Bedienoberfläche abhängig.

### FTP-Clients <a href="#ftp-clients" id="ftp-clients"></a>

Ein FTP-Client ist die Anwendung, welche auf Ihrem Computer installiert werden kann. Diese wird zum Herstellen einer Verbindung mit einem FTP-Server verwendet. Es stehen zahlreiche kostenlose und kostenpflichtige FTP-Clients im Internet zur Auswahl. Wir stellen Ihnen hier einige beliebte Programme vor:

* [FileZilla](https://filezilla-project.org/download.php?type=client) (kostenlos) - Erhältlich für Windows, Mac & Linux
* [WinSCP](https://winscp.net/eng/docs/lang:de) (kostenlos) - Erhältlich für Windows

#### Konfiguration <a href="#konfiguration1" id="konfiguration1"></a>

Die Konfiguration aller FTP-Clients oder von Anwendungen mit FTP-Funktion funktioniert grundlegend gleich.\
Suchen Sie in Ihrem FTP-Client das Menü zum Verbinden mit Netzwerkgeräten / FTP-Servern, bzw. den Verbindungsmanager auf und geben Sie die benötigten Daten ein.

Welche Informationen Sie für die Eingabe verwenden müssen, hängt von Ihrem Hosting-Paket ab. Grundlegend benötigt der FTP-Client folgende Daten für eine erfolgreiche Verbindung:

* FTP-Server/-Hostname - Hier muss die Adresse des FTP-Servers eingegeben werden. Das ist meist die Domain Ihrer Webseite.
* FTP-Benutzername - Der Benutzernamen für Ihren erstellten FTP-Benutzer.
* FTP-Passwort - Das Kennwort für Ihren FTP-Benutzer.
* FTP-Port - Wenn nicht anders angegeben, kann der FTP-Standardport 21 verwendet werden.

Beispiel FileZilla:

<figure><img src="https://wiki8.centron.de/_media/webhosting/filezillaverbinden02.png" alt=""><figcaption></figcaption></figure>

\

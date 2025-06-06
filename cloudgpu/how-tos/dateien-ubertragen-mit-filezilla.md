---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Januar 2025
---

# Dateien übertragen mit Filezilla

Mithilfe verschiedener Protokolle und Datenübertragungstools können Sie  Dateien von einem lokalen Computer zu einer ccloud³ VM bei centron übertragen. Wir empfehlen die Verwendung von SFTP (SSH File Transfer Protocol) mit FileZilla, da es ein kostenloses, Open-Source- und plattformübergreifendes Tool mit einer benutzerfreundlichen Oberfläche ist, die auch für Anfänger geeignet ist. Wenn Sie sich mit der Kommandozeile wohlfühlen, können Sie auch Tools wie "rsync" sowie "OpenSSHs sftp" und "scp" verwenden. Diese Anleitung führt Sie durch die Erstinstallation von FileZilla und zeigt Ihnen, wie Sie Dateien mittels einer SSH-Verbindung zu Ihrer ccloud³ VM übertragen.

Aus Sicherheitsgründen empfehlen wir die Verwendung von SSH-Schlüsseln mit SFTP. Wenn Sie noch keine SSH-Schlüssel zur Verbindung mit Ihrer ccloud³ VM verwenden, richten Sie diese ein.

#### FileZilla installieren

Auf dem Computer, von dem aus Sie Dateien übertragen möchten, laden Sie FileZilla herunter und installieren es. Wählen Sie nun die Version für Ihr Betriebssystem aus.

Unter Debian-basierten Linux-Distributionen, wie Ubuntu, können Sie FileZilla alternativ mit dem APT-Paketmanager installieren:

```bash
sudo apt-get update
sudo apt-get install filezilla
```

#### FileZilla konfigurieren

Nachdem Sie FileZilla installiert haben, müssen Sie es konfigurieren, um eine Verbindung zu Ihrer ccloud³ VM herzustellen.

* Öffnen Sie FileZilla und klicken Sie dann im Dropdown-Menü "Bearbeiten" auf "Einstellungen".
* Im Abschnitt "Verbindung" klicken Sie auf "SFTP". Hier fügen Sie den privaten SSH-Schlüssel Ihrer ccloud³ VM hinzu. Klicken Sie auf "Schlüsseldatei hinzufügen...", und suchen Sie dann den privaten SSH-Schlüssel Ihrer ccloud³ VM auf Ihrem lokalen Computer. Wenn FileZilla Sie auffordert die Datei in ein unterstütztes Format zu konvertieren, klicken Sie auf "Ja".
* Nachdem Sie den SSH-Schlüssel hinzugefügt haben, öffnen Sie das Dropdown-Menü "Datei" und klicken Sie auf "Serververwaltung". Die Serververwaltung ermöglicht es Ihnen, Server und Geräte, zu denen Sie sich mit FileZilla verbinden möchten, hinzuzufügen, zu entfernen und zu verwalten.
* Klicken Sie auf "Neuer Server" und geben Sie den Namen Ihrer ccloud³ VM ein. Wählen Sie im Feld "Protokoll" "SFTP" aus dem Dropdown-Menü. Geben Sie Informationen für die folgenden Felder ein:
  * Host: Die IP-Adresse Ihrer ccloud³ VM.
  * Port: Geben Sie den Port ein, über den Sie sich mit der ccloud³ VM verbinden möchten (Port 22 ist der Standard).
  * Anmeldeart: Wählen Sie "Interaktiv".
  * Benutzer: Geben Sie den Benutzernamen ein, mit dem Sie sich bei der ccloud³ VM anmelden (root ist standardmäßig der Benutzer auf den meisten VMs).
* Nachdem Sie Ihre Einstellungen eingegeben haben, klicken Sie auf "Verbinden". Das Statusfeld im oberen Fenster zeigt den Status der Verbindung an.

#### Dateien mit FileZilla übertragen

Sobald Sie mit der ccloud³ VM verbunden sind, verwenden Sie die Fenster "Lokale Seite", um die Verzeichnisse Ihres lokalen Computers zu durchsuchen und die Dateien zu finden, die Sie hochladen möchten. Klicken Sie mit der rechten Maustaste auf die Datei, die Sie auf die ccloud³ VM übertragen möchten, und klicken Sie dann auf "Hochladen".

Um Dateien von der ccloud³ VM auf Ihren lokalen Computer zu übertragen, verwenden Sie die Fenster "Remote-Seite", um die Verzeichnisse Ihrer ccloud³ VM zu durchsuchen und die Dateien zu finden, die Sie auf Ihren lokalen Computer herunterladen möchten. Klicken Sie mit der rechten Maustaste auf die Datei, die Sie von der ccloud³ VM übertragen möchten, und klicken Sie dann auf "Herunterladen".

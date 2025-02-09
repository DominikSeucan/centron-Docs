---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023.
---

# Keys zu VMs hinzufügen

Aus Sicherheitsgründen können Sie nach der Erstellung einer ccloud³ VM bei centron keine SSH-Schlüssel über das Kontrollpanel hinzufügen oder ändern. Sie haben jedoch mehrere Möglichkeiten, dies über die Kommandozeile zu tun. Wenn Sie derzeit über SSH-Zugriff auf Ihre ccloud³ VM verfügen, können Sie Schlüssel auf mehrere Arten hochladen:

* **Von Ihrem lokalen Computer mit `ssh-copy-id`**: Diese Methode wird in vielen Linux-Distributionen, die OpenSSH-Pakete enthalten, unterstützt. Sie ist für die Benutzerfreundlichkeit zu empfehlen.
* **Von Ihrem lokalen Computer durch Pipen des Schlüssels in die Datei `~/.ssh/authorized_keys` auf der ccloud³ VM**: Diese Methode ist eine gute Wahl, wenn Sie `ssh-copy-id` nicht zur Verfügung haben.
* **Durch direktes Verbinden mit Ihrer ccloud³ VM über SSH und manuelles Hinzufügen des öffentlichen Schlüssels**: Dies ist notwendig, wenn Sie keinen passwortbasierten SSH-Zugriff haben.

Wenn Sie derzeit überhaupt keine Verbindung zu Ihrer ccloud³ VM herstellen können, verwenden Sie die Recovery-Konsole, um das Root-Benutzerpasswort zurückzusetzen. Nachdem Sie sich über die Konsole angemeldet haben, können Sie Ihren Schlüssel manuell von der Konsole hinzufügen oder die passwortbasierte Authentifizierung vorübergehend aktivieren, um den Schlüssel über SSH hinzuzufügen.

#### Lokal mit `ssh-copy-id` und passwortbasiertem Zugang

Wenn Sie passwortbasierten Zugriff auf Ihre ccloud³ VM haben, können Sie Ihren SSH-Schlüssel von Ihrem lokalen Computer auf Ihre ccloud³ VM mit `ssh-copy-id` kopieren.

*   **Befehl**: `ssh-copy-id use_your_username@203.0.113.0`

    Um einen anderen Schlüssel anzugeben, verwenden Sie die `-i`-Flag: `ssh-copy-id -i ~/path/to/key.pub use_your_username@203.0.113.0`.
* **Bestätigung der Authentizität und Eingabe des Passworts**, gefolgt von einer Bestätigung der Schlüsselhinzufügung.

#### Lokal durch Pipen in SSH mit passwortbasiertem Zugang

Wenn Sie `ssh-copy-id` nicht haben, aber passwortbasierten SSH-Zugriff auf Ihre ccloud³ VM haben, können Sie einen SSH-Schlüssel zu Ihrer ccloud³ VM hinzufügen, indem Sie den Inhalt des Schlüssels in den SSH-Befehl pipen:

* **Befehl**: `cat ~/.ssh/id_rsa.pub | ssh username@203.0.113.0 "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"`

#### Manuell von der ccloud³ VM

Wenn Sie keinen passwortbasierten SSH-Zugriff haben, müssen Sie Ihren öffentlichen Schlüssel manuell auf dem Remote-Server hinzufügen.

* **Anzeigen des Schlüsselinhalts auf dem lokalen Computer**: `cat ~/.ssh/id_rsa.pub`
*   **Kopieren und Einfügen des Schlüssels auf der ccloud³ VM**.

    Befehl: `echo "ssh-rsa EXAMPLEzaC1yc2E...GvaQ== username@203.0.113.0" >> ~/.ssh/authorized_keys`

Stellen Sie sicher, dass das `~/.ssh`-Verzeichnis und die `authorized_keys`-Datei die richtigen eingeschränkten Berechtigungen haben (700 für `~/.ssh` und 600 für `authorized_keys`), um sich ohne Passwort anmelden zu können.

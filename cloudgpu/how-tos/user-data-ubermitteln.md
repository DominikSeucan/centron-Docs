---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# User Data übermitteln

Metadata ist ein Dienst, der es einer ccloud³ VM ermöglicht, Daten über sich selbst abzurufen. Zusätzlich können Sie Metadata verwenden, um Benutzerdaten bei der Erstellung einer ccloud³ VM bereitzustellen und die Einrichtung zu vereinfachen oder zu automatisieren.

#### Über Benutzerdaten

Benutzerdaten sind beliebige Daten, meist ein Skript, die Sie während der Erstellung einer ccloud³ VM bereitstellen können. Wenn CloudInit auf der ccloud³ VM verfügbar ist, verarbeitet es die Benutzerdaten, die es nutzen kann, um Aufgaben als Root-Benutzer während des ersten Starts der ccloud³ VM durchzuführen.

CloudInit akzeptiert Cloud-Config-Dateien oder jedes Skript, das von der neuen ccloud³ VM interpretiert werden kann, wie ein Bash-Skript. CloudInit ist auf den neuesten Ubuntu- und CentOS-Images von centron verfügbar. Sie können Benutzerdaten für Images definieren, die CloudInit nicht unterstützen, aber diese werden nicht automatisch beim ersten Start verarbeitet.

#### Bereitstellung von Benutzerdaten

Sie können Benutzerdaten bei der Erstellung einer ccloud³ VM über das centron Control Panel, die API oder doctl, den CLI-Client, bereitstellen.

* **Über das centron Control Panel**: Auf der Seite zur Erstellung der ccloud³ VM klicken Sie oberhalb des Abschnitts "Abschließende Details" auf "+ Erweiterte Optionen". Im sich öffnenden Abschnitt aktivieren Sie das Kontrollkästchen neben "Initialisierungsskripte hinzufügen". Fügen Sie Ihre Benutzerdaten in das erscheinende Feld ein.
* **Über die centron API**: Verwenden Sie das Feld `user_data` im POST-Request zur Erstellung der ccloud³ VM.
* **Über doctl**: Verwenden Sie die Flags `--user-data` oder `--user-data-file`, wenn Sie `doctl compute droplet create` aufrufen.

Benutzerdaten können nach der Erstellung einer ccloud³ VM nicht mehr geändert werden.

#### Debugging von Benutzerdaten

Um zu sehen, wie eine CloudInit-Datei die bereitgestellten Benutzerdaten verwendet, betrachten Sie die Datei `/var/log/cloud-init-output.log`:

* **Befehl**: `cat /var/log/cloud-init-output.log | grep userdata`

Diese Datei protokolliert die Ausgabe von CloudInits, sodass Sie Warnungen, Fehlermeldungen oder Debug-Informationen einsehen können.

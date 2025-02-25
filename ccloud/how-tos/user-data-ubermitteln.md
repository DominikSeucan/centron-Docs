---
description: Validiert am 19.09.2024 • Zuletzt bearbeitet am 21. September 2024
---

# User Data übermitteln

Metadata ist ein Dienst, der es einer ccloud³ VM ermöglicht, Daten über sich selbst abzurufen. Zusätzlich können Sie Metadata verwenden, um Benutzerdaten bei der Erstellung einer ccloud³ VM bereitzustellen, um die Einrichtung zu vereinfachen oder zu automatisieren.

### Über User Data

Benutzerdaten sind beliebige Daten, meist ein Skript, die Sie während der Erstellung einer ccloud³ VM bereitstellen können. Wenn CloudInit auf der ccloud³ VM verfügbar ist, verarbeitet es die Benutzerdaten, die es nutzen kann, um während des ersten Starts der ccloud³ VM Aufgaben als Root-Benutzer durchzuführen.

CloudInit akzeptiert Cloud-Config-Dateien oder jedes Skript, das von der neuen ccloud³ VM interpretiert werden kann, wie ein Bash-Skript. CloudInit ist auf den neuesten Ubuntu- und CentOS-Images von centron verfügbar. Sie können Benutzerdaten für Images definieren, die CloudInit nicht unterstützen, diese werden allerdings nicht automatisch beim ersten Start verarbeitet.



### Bereitstellung von Benutzerdaten

Sie können Benutzerdaten bei der Erstellung einer ccloud³ VM über das centron Control Panel oder die API bereitstellen.

* **Über das centron Control Panel**: Auf der Seite zur Erstellung der ccloud³ VM klicken Sie oberhalb des Abschnitts "Abschließende Details" auf "+ Erweiterte Optionen". Im sich öffnenden Abschnitt aktivieren Sie das Kontrollkästchen neben "Initialisierungsskripte hinzufügen". Geben Sie Ihre Benutzerdaten in das erscheinende Feld ein.
* **Über die centron API**: Verwenden Sie das Feld `user_data` im POST-Request zur Erstellung der ccloud³ VM.

Benutzerdaten können nach der Erstellung einer ccloud³ VM nicht mehr geändert werden.



### Debugging von Benutzerdaten

Um zu sehen, wie eine CloudInit-Datei die bereitgestellten Benutzerdaten verwendet, betrachten Sie die Datei `/var/log/cloud-init-output.log`:

**Befehl**: `cat /var/log/cloud-init-output.log | grep userdata`

Diese Datei protokolliert die Ausgabe von CloudInits, sodass Sie Warnungen, Fehlermeldungen oder Debug-Informationen einsehen können.

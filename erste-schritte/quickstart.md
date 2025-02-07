---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Quickstart

Centron ccloud³ VMs sind virtuelle Maschinen (VMs), die auf virtualisierter Hardware laufen. Jede ccloud³ VM, die Sie erstellen, ist ein neuer Server, den Sie entweder eigenständig oder als Teil einer größeren, cloud-basierten Infrastruktur verwenden können.



### Erstellen von ccloud³ VMs&#x20;

1. Über das Create-Menü oben rechts im ccenter klicken Sie auf "ccloud³ VMs".
2. Wählen Sie ein Image, das eine Linux-Distribution oder eine Windows-Distribution sein kann.
3. Wählen Sie einen Pool und eine Größe für Ihre ccloud³ VM, die deren RAM, Speicherplatz und vCPUs sowie den Preis bestimmt. Erfahren Sie mehr darüber, [wie Sie den richtigen ccloud³ VM-Plan wählen.](../konzepte/vm-grosse-pool-and-gpu-wahlen.md)

Das Erstellungsformular für ccloud³ VMs bietet eine Reihe von Optionen, die Sie jetzt oder nach der Erstellung anpassen können. Um die Standardeinstellungen zu akzeptieren, scrollen Sie nach unten und klicken Sie auf Erstellen. Andernfalls:

4. Optional, fügen Sie [Disks ](https://app.gitbook.com/o/qZfyhEIOoMD2Tm025WII/s/RJxFPLhOBZQT2DPxjzdO/)hinzu.
5. Wählen Sie ein VPC-Netzwerk für die ccloud³ VM.
6. Wählen Sie einen SSH-Schlüssel, falls Sie einen hinzugefügt haben, oder erstellen Sie ein Root-Passwort für die ccloud³ VM.
7. Geben Sie einen Namen ein und klicken Sie auf "Erstellen".

Von hier aus können Sie unserer[ detaillierten Anleitung zum Verbinden mit ccloud³ VMs über SSH](../how-tos/mit-ssh-verbinden.md) folgen oder die unten stehenden Anweisungen befolgen.



### Verbindung zu ccloud³ VMs

Um über ein Terminal unter Linux, macOS oder Windows-Subsystem für Linux zu verbinden:

1. Öffnen Sie Ihr Terminal und geben Sie den Befehl "ssh benutzername@203.0.113.0" ein.
2. Ersetzen Sie den Teil nach dem @ durch die IP-Adresse Ihrer ccloud³ VM. Der Benutzername ist bei den meisten Distributionen root.
3. Drücken Sie ENTER und antworten Sie mit ja auf die Aufforderung, die Verbindung zu bestätigen.
4. Wenn Sie keine SSH-Schlüssel verwenden, geben Sie bei Aufforderung Ihr Passwort ein.

Windows-Benutzer können alternativ mit PuTTY eine Verbindung herstellen.

Wenn Sie eingeloggt sind, ändert sich Ihr Befehlsprompt und Sie sehen einen Willkommensbildschirm.



### Zerstören von ccloud³ VMs

Das Zerstören einer ccloud³ VM zerstört dauerhaft und unwiderruflich die VM, ihren Inhalt, automatische Backups und alle damit verbundenen Ressourcen, die Sie zum Zerstören ausgewählt haben.

1. Klicken Sie im Kontrollpanel auf das Mehr-Menü der ccloud³ VM und wählen Sie "Zerstören".
2. (Optional) Auf der Zerstören-Seite der ccloud³ VM, unter ccloud³ VM und Backups zerstören, klicken Sie auf "verbundene Ressourcen anzeigen" und wählen Sie alle verbundenen Ressourcen der ccloud³ VM aus, die Sie ebenfalls zerstören möchten.
3. Klicken Sie auf "Diese ccloud³ VM und Backups zerstören" (oder "diese ccloud³ VM und X ausgewählte Ressourcen zerstören", wenn Sie auch mit der ccloud³ VM verbundene Ressourcen zerstören).
4. Bestätigen Sie die Zerstörung im Bestätigungsfenster, das sich öffnet, indem Sie auf "Bestätigen" (oder "Zerstören", wenn Sie auch mit der ccloud³ VM verbundene Ressourcen zerstören) klicken. Wenn Sie auch verbundene Ressourcen zerstören, werden Sie aufgefordert, den Namen der ccloud³ VM in das Bestätigungsfenster einzugeben, bevor Sie die ccloud³ VM zerstören.

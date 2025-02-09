---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# SSH Keys zu VMs hinzufügen

Für das Verwalten Ihrer ccloud³ VMs bei centron empfehlen wir ebenfalls die Verwendung von SSH-Schlüsselpaaren anstelle von passwortbasierten Logins. SSH-Schlüssel sind sicherer als Passwörter und erleichtern außerdem das Einloggen im Vergleich zu komplexen Passwörtern.

Um SSH-Schlüssel mit Ihren ccloud³ VMs zu verwenden, sollten Sie die folgenden Schritte durchführen:



## SSH-Schlüssel erstellen

{% content-ref url="keys-mit-openssh-erstellen.md" %}
[keys-mit-openssh-erstellen.md](keys-mit-openssh-erstellen.md)
{% endcontent-ref %}

OpenSSH ist in Linux, MacOS und im Windows-Subsystem für Linux enthalten. Verwenden Sie OpenSSH, um neue SSH-Schlüssel zu erstellen.

{% content-ref url="keys-mit-putty-erstellen.md" %}
[keys-mit-putty-erstellen.md](keys-mit-putty-erstellen.md)
{% endcontent-ref %}

Für Windows-Nutzer ohne Bash ist PuTTY eine gute Alternative zur Erstellung von SSH-Schlüsseln.



## SSH-Schlüssel zu Ihren ccloud³ VMs hinzufügen

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

Bei der Erstellung Ihrer ccloud³ VMs können Sie Ihren öffentlichen SSH-Schlüssel hinzufügen, was das Einloggen ohne Passwort ermöglicht und gleichzeitig sicher bleibt.



## Verbindung mit ccloud³ VMs über SSH

{% content-ref url="../mit-ssh-verbinden.md" %}
[mit-ssh-verbinden.md](../mit-ssh-verbinden.md)
{% endcontent-ref %}

---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# Limits

* Benutzerdefinierte Images müssen kleiner als 100 GB sein, wenn sie unkomprimiert sind.&#x20;
* ISO-Images werden momentan nicht unterstützt. centron zieht die Unterstützung von ISO für die Zukunft in Betracht. Alternativ können Sie in der Zwischenzeit ein neues Image mit Ihrer bevorzugten VM-Software erstellen und es erneut in einem unterstützten Format speichern. Für eine detaillierte Anleitung siehe 'Wie man eine ccloud³ VM aus einem Ubuntu ISO-Format Image erstellt'.
* Anders als Standard-Images, die von centron bereitgestellt werden, verwenden ccloud³ VMs, die aus benutzerdefinierten Images erstellt wurden, DHCP, um eine IP-Adresse von der centron-Plattform zu erhalten. Die Netzwerkkonfiguration des benutzerdefinierten Images erfordert keine zusätzliche Einrichtung um DHCP zu verwenden.
* IPv6 wird bei ccloud³ VMs, die aus benutzerdefinierten Images erstellt wurden, nicht unterstützt.
* Automatisches Monitoring kann während der Erstellung einer ccloud³ VM mit einem benutzerdefinierten Image nicht aktiviert werden. Stattdessen muss das Monitoring manuell eingerichtet werden.
* Sie müssen einen SSH-Schlüssel hinzufügen, wenn Sie ccloud³ VMs aus einem benutzerdefinierten Image erstellen. Diese VMs haben die Passwortauthentifizierung standardmäßig deaktiviert - Sie können das Kontrollpanel nicht verwenden, um das Root-Passwort zurückzusetzen.
* Das Importieren eines benutzerdefinierten Images über eine URL schlägt fehl, wenn das Image von einem CDN bereitgestellt wird, das HEAD-Anfragen nicht unterstützt. Wenn Sie Probleme beim Importieren eines Images über eine URL haben, versuchen Sie, die Datei herunterzuladen und direkt hochzuladen.
* ccloud³ VMs, die aus einem benutzerdefinierten Image erstellt wurden, erhalten keine Anker-IP-Adresse und benötigen diese auch nicht, um eine reservierte IP zu verwenden. Wenn Sie einer ccloud³ VM, die aus einem benutzerdefinierten Image erstellt wurde, eine reservierte IP-Adresse zuweisen, wird die reservierte IP automatisch der öffentlichen IPv4-Adresse der VM zugeordnet anstatt einer Anker-IP.

### Bekannte Probleme:

* Der Gesamtspeicher, der von benutzerdefinierten Images genutzt wird, kann nicht eingesehen werden.
* Das Fenster zum Hochladen von Images zeigt die Größe des Images nicht korrekt an.

\

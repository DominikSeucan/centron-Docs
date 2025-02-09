---
description: Erstellt am 29. November 2023
---

# Empfohlenes VM Setup

centron ccloud³ VMs sind virtuelle Maschinen (VMs), die auf virtualisierter Hardware laufen. Jede ccloud³ VM, die Sie erstellen, ist ein neuer Server, den Sie entweder eigenständig oder als Teil einer größeren, cloud-basierten Infrastruktur verwenden können.

Wenn Sie eine ccloud³ VM zum ersten Mal erstellen, empfehlen wir Ihnen, sie hinsichtlich Sicherheit und Benutzerfreundlichkeit so zu konfigurieren, dass eine spätere Skalierung und Integration mit anderen Produkten vereinfacht wird. Unsere empfohlene Einrichtung für eine ccloud³ VM mit Ubuntu 18.04 umfasst Folgendes:

### Verbesserte Sicherheit

SSH-Schlüsselauthentifizierung für einen sudo Nicht-Root-Benutzer, kein passwortbasierter Zugriff auf Root und eine Cloud-Firewall, um den Zugriff auf SSH zu beschränken.



### Zuverlässigkeit und Benutzerfreundlichkeit

Automatische Backups zur Verhinderung von Datenverlust in Notfällen und Netzwerkfunktionen wie VPC und IPv6-Unterstützung ohne manuelle Konfiguration.

Kapazitäts- und Skalierungsinformationen: Der centron-Metrics-Agent, um Ihre Ressourcennutzung zu verstehen und fundiertere Entscheidungen darüber zu treffen, wann und wie Sie skalieren sollten.

Nachdem Sie eine ccloud³ VM mit unserer empfohlenen Einrichtung konfiguriert haben, erfordert das Konfigurieren nachfolgender ccloud³ VMs mit derselben Einrichtung nur die Auswahl von Optionen auf der Erstellungsseite der ccloud³ VM.

Sie können ccloud³ VMs mit dieser Einrichtung nutzen, um eine Website zu hosten, von einer einzelnen ccloud³ VM zu mehreren ccloud³ VMs mit einem Load Balancer zu skalieren oder Objektspeicher hinzuzufügen, um Assets bereitzustellen.

Um einen sicheren Zugang zu Ihren ccloud³ VMs bei centron zu gewährleisten, ist die Verwendung von SSH-Schlüsseln anstelle einer passwortbasierten Authentifizierung zu empfehlen. Hier ist eine Schritt-für-Schritt-Anleitung, wie Sie SSH-Schlüssel erstellen und diese zu Ihrem centron-Konto hinzufügen können:



## **SSH-Schlüsselpaar erstellen**

1. **Erstellen eines SSH-Schlüsselpaares:** Falls Sie noch kein SSH-Schlüsselpaar haben, erstellen Sie eines mit OpenSSH, welches in Linux, macOS und dem Windows-Subsystem für Linux enthalten ist. Verwenden Sie hierfür diesen Befehl in Ihrer Kommandozeile:

```
ssh-keygen
```

2. **Speicherort des Schlüsselpaares:** Das Schlüsselpaar wird standardmäßig in `~/.ssh/` unter Linux und `/Users/Ihr_Benutzername/.ssh` unter Windows und macOS gespeichert. Kopieren Sie den Inhalt Ihres öffentlichen Schlüssels, der standardmäßig `id_rsa.pub` heißt.
3. **Kopieren des öffentlichen Schlüssels:** Unter macOS können Sie den Schlüssel direkt in Ihre Zwischenablage kopieren, indem Sie den Befehl&#x20;

```
pbcopy < ~/.ssh/id_rsa.pub
```

verwenden. Für Windows und Linux variiert der Befehl je nach spezifischer Distribution, Subsystem oder Kommandozeile.

<details>

<summary>Mehr Details zum Erstellen von SSH Keys.</summary>

1. [How to Create SSH Keys with OpenSSH on MacOS or Linux](../how-tos/ssh-keys-zu-vms-hinzufugen/keys-mit-openssh-erstellen.md)
2. [How to Create SSH Keys with PuTTY on Windows](../how-tos/mit-ssh-verbinden.md#ssh-key-generieren)

</details>

Durch die Nutzung von SSH-Schlüsseln erhöhen Sie die Sicherheit Ihrer ccloud³ VMs erheblich und vermeiden das manuelle Hinzufügen oder Konfigurieren von Schlüsseln für jede VM.



## Konfiguration Ihrer ccloud³ VM

Beim Erstellen und Konfigurieren Ihrer ccloud³ VMs bei centron sollten Sie folgende empfohlene Einstellungen berücksichtigen:

1. **VPC (Virtual Private Cloud):**
   * Erstellt eine private Netzwerkschnittstelle, die nur von Ressourcen innerhalb desselben Kontos oder Teams zugänglich ist.
   * Bietet erhöhte Sicherheit und reduzierte Bandbreitenkosten für die interne Kommunikation.
   * Eine nachträgliche Aktivierung erfordert manuelle Netzwerkkonfiguration und Neustart der VM.
2. **IPv6:**
   * Aktivieren Sie IPv6.
   * Diese Option ist kostenlos; eine spätere Aktivierung erfordert ebenfalls manuelle Netzwerkkonfiguration und einen Neustart der VM.
3. **Advanced Monitoring:**
   * Ein Metrik-Visualisierungsdienst, der zusätzliche Diagramme in einem separaten Interface anzeigt.
   * Ermöglicht das Einrichten von Alarmrichtlinien.
4. **Backups:**
   * Automatische, systemweite Backups Ihrer VMs, die täglich erstellt werden.
   * Ermöglichen es Ihnen, eine VM auf einen neuesten Zustand zurückzusetzen.
   * Fügen 0,03 € / GB verbrauchtem Backup - Speicher hinzu.
5. **User Data:**
   * Daten, die CloudInit während des ersten Boot-Vorgangs der VM verarbeitet, um Aufgaben auszuführen oder Skripte zu starten.
   * Das im Tutorial verwendete User data-Skript implementiert zwei Sicherheitsmaßnahmen:&#x20;
     * Deaktiviert das passwortbasierte Login, sodass der Zugriff nur über SSH-Schlüssel möglich ist.
     * Erstellt einen sudo Nicht-Root-Benutzer für den alltäglichen Gebrauch, um das Risiko versehentlicher destruktiver Änderungen zu verringern und dennoch bei Bedarf eine Eskalation der Berechtigungen zu ermöglichen.

## Wie erstelle ich eine ccloud³ VM?

Die folgenden Schritte stellen sicher, dass Ihre ccloud³ VMs bei centron optimal konfiguriert sind, um Sicherheit, Effizienz und Skalierbarkeit zu gewährleisten:

1. **Öffnen Sie das Erstellungs-Menü:**
   * Loggen Sie sich in das centron-Kontrollpanel ein.
   * Klicken Sie oben rechts auf "Erstellen", um das Erstellungs-Menü zu öffnen.
2. **Wählen Sie 'ccloud³ VMs' aus:**
   * Klicken Sie im Erstellungs-Menü auf "ccloud³ VMs", um zur Erstellungsseite für ccloud³ VMs zu gelangen.
3.  **Konfigurieren Sie Ihre ccloud³ VM:**

    * **Wählen Sie ein Image:** Unter dem Reiter 'OS' wählen Sie die neueste Version von Ubuntu 18.04.
    * **VPC-Netzwerk:** Wählen Sie das Standard-VPC.
    * **Empfohlene und erweiterte Optionen:** Aktivieren Sie die Optionen für IPv6 und Monitoring.
    * **Erweiterte Optionen - Nutzerdaten:** Aktivieren Sie das Kontrollkästchen für Nutzerdaten und fügen Sie das bereitgestellte Cloud-Config-Skript in das Textfeld ein. Passen Sie die hervorgehobene Zeile an, um den Benutzernamen zu setzen.

    Hier ist das Skript, das Sie verwenden sollten (ersetzen Sie `USERNAME=cadmin`durch Ihren gewünschten Benutzernamen):

```bash
set -euo pipefail

USERNAME=IhrBenutzername # TODO: Passen Sie den sudo Nicht-Root-Benutzernamen hier an

# Benutzer erstellen und sofortiges Passwortablaufen erzwingen
useradd --create-home --shell "/bin/bash" --groups sudo "${USERNAME}"
passwd --delete "${USERNAME}"
chage --lastday 0 "${USERNAME}"

# SSH-Verzeichnis für sudo-Benutzer erstellen und Schlüssel übertragen
home_directory="$(eval echo ~${USERNAME})"
mkdir --parents "${home_directory}/.ssh"
cp /root/.ssh/authorized_keys "${home_directory}/.ssh"
chmod 0700 "${home_directory}/.ssh"
chmod 0600 "${home_directory}/.ssh/authorized_keys"
chown --recursive "${USERNAME}":"${USERNAME}" "${home_directory}/.ssh"

# SSH-Login als root mit Passwort deaktivieren
sed --in-place 's/^PermitRootLogin.*/PermitRootLogin prohibit-password/g' /etc/ssh/sshd_config
if sshd -t -q; then systemctl restart sshd; fi 
```



4. **Authentifizierung:**

* Wählen Sie 'SSH-Schlüssel' für die Authentifizierung und wählen Sie einen oder mehrere Schlüssel aus. Diese Schlüssel geben Ihnen Zugriff auf den Root-Benutzer. Das Nutzerdaten-Skript wird diese Schlüssel dem sudo Nicht-Root-Benutzer hinzufügen und die Passwortauthentifizierung deaktivieren.

5. **Tags:**

* Erstellen Sie ein Tag, das Ihrem Verwendungszweck der ccloud³ VM entspricht, wie z.B. 'webserver'. Sie können dieses Tag verwenden, um Cloud-Firewalls im nächsten Schritt anzuwenden.

6. **Empfohlene Optionen:**

* Aktivieren Sie die Option für 'Backups' durch Premium Full Managing.

7. **Erstellung der ccloud³ VM:**

* Nachdem Sie alle Optionen ausgewählt haben, klicken Sie auf "ccloud³ VM erstellen".

## Cloud Firewall erstellen

Bei centron können Sie Firewall-Regeln ähnlich den DigitalOcean Cloud Firewalls einrichten, um Ihre ccloud³ VMs vor externen Angriffen zu schützen. Diese Firewalls fungieren als Barriere und blockieren jeglichen Verkehr, der nicht explizit durch eine Regel erlaubt wird. Hier ist eine Anleitung, wie Sie eine Firewall für Ihre ccloud³ VMs konfigurieren können:

1. **Erstellen der Firewall:**
   * Loggen Sie sich in Ihr centron-Kontrollpanel ein.
   * Klicken Sie oben rechts auf "ccloud³ VM erstellen", um das Erstellungsmenü zu öffnen, und wählen Sie dann "PFSense", um eine Firewall zu erstellen.
2. **Firewall benennen:**
   * Geben Sie im Feld "Name" beispielsweise "inbound-ssh-only" ein.
3. **Eingehende Regeln konfigurieren:**
   * Belassen Sie die Standardregel für SSH. Diese Regel ermöglicht eingehende SSH-Verbindungen zum Droplet über Port 22.
4. **Ausgehende Regeln konfigurieren:**
   * Behalten Sie die Standardregeln bei, die allen Verkehr zu jedem Ziel auf jedem Port erlauben. Dies ist wichtig, da viele grundlegende Dienste auf ausgehende Kommunikation angewiesen sind.
5. **Firewall auf ccloud³ VMs anwenden:**
   * Fügen Sie das Tag hinzu, das Sie bei der Erstellung der neuen ccloud³ VM verwendet haben. Wenn Sie zusätzliche ccloud³ VMs erstellen und dasselbe Tag hinzufügen, werden diese automatisch in diese Cloud-Firewall aufgenommen. Dies vereinfacht Ihnen das Skalieren in der Zukunft.
6. **Firewall erstellen:**
   * Nachdem Sie alle Optionen ausgewählt haben, klicken Sie auf "Firewall erstellen".

## Zusammenfassung

Nachdem Sie eine ccloud³ VM bei centron mit der empfohlenen Konfiguration eingerichtet haben, ist die Einrichtung zukünftiger VMs noch einfacher, da Sie die meisten Schritte nicht wiederholen müssen. Die einmaligen Schritte umfassen:

* Das Erstellen eines SSH-Schlüsselpaares.
* Das Hochladen Ihres öffentlichen SSH-Schlüssels zu Ihrem centron-Konto.
* Das Erstellen der Cloud-Firewall.

Um zusätzliche ccloud³ VMs mit derselben Konfiguration zu erstellen, müssen Sie lediglich die Konfigurationsoptionen auf der ccloud³ VM-Erstellungsseite auswählen:

* Aktivieren Sie dieselben Funktionen (VPC, IPv6, Monitoring und Backups).
* Wählen Sie Ihren SSH-Schlüssel.
* Fügen Sie das Cloud-Config-Skript in den Nutzerdaten ein.
* Fügen Sie das Tag für die Cloud-Firewall hinzu.

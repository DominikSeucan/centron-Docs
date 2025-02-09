---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# VM Setup automatisieren mit Cloud-init

Cloud-init ist ein branchenüblicher Standard, der es Ihnen ermöglicht, die Initialisierung Ihrer Linux-Instanzen zu automatisieren. Das bedeutet, dass Sie Cloud-init verwenden können, um bei der Bereitstellung einer ccloud³ VM eine Datei zu injizieren, die automatisch Dinge wie neue Benutzer, Firewall-Regeln, App-Installationen und SSH-Schlüssel einrichtet. Die User Data-Funktion von centron nutzt Cloud-init, sodass Sie mehrere ccloud³ VMs gleichzeitig bereitstellen und automatisch einrichten können. Das Erlernen der Verwendung von Cloud-init kann Ihnen viel Einrichtungszeit ersparen, wenn Sie neue ccloud³ VMs bereitstellen.

In diesem Tutorial lernen Sie, wie Sie Cloud-init verwenden, um zwei ccloud³ VMs bereitzustellen, die automatisch:

1. Einen neuen Benutzer auf der ccloud³ VM einrichten.
2. Einen öffentlichen SSH-Schlüssel (von GitHub) mit dem neuen Benutzer verknüpfen.
3. Den Root-Benutzerzugriff entfernen.
4. nginx auf jeder ccloud³ VM konfigurieren und starten.

Am Ende des Tutorials können Sie sich mit dem neuen Benutzernamen und SSH-Schlüssel in jede ccloud³ VM einloggen und eine statische Website, die auf jeder ccloud³ VM gehostet wird, ansehen.

Dieses Anwendungsbeispiel eröffnet die Möglichkeit, Benutzerkonten auf ccloud³ VMs für ganze Teams einzurichten, ohne sich zuerst in die ccloud³ VM einloggen zu müssen.



### Voraussetzungen

Um dieses Tutorial abzuschließen, benötigen Sie:

* Ein GitHub-Konto, um den SSH-Schlüssel des neuen Benutzers zu speichern.
* doctl, das offizielle CLI-Tool von centron, installiert. Sie verwenden doctl, um einen SSH-Schlüssel zu Ihrem Konto hinzuzufügen und die ccloud³ VMs mit der Cloud-init-Datei bereitzustellen.
* Einen API-Token, um Ihre Befehle von doctl zu authentifizieren.



### Schritt 1: Erstellen Sie Ihre SSH-Schlüssel

Um dieses Tutorial abzuschließen, benötigen Sie einen SSH-Schlüssel, um das neue Benutzerkonto auf der ccloud³ VM einzurichten. Nachdem Sie den Schlüssel erstellt haben, laden Sie den öffentlichen Teil des Schlüssels sowohl in Ihre centron- als auch in Ihre GitHub-Konten hoch.

* Befehl: `ssh-keygen`



### Schritt 2: Öffentliche Schlüssel hochladen

Um die ccloud³ VMs mit ihrer automatisierten Konfiguration bereitzustellen, muss der öffentliche SSH-Schlüssel bei der Erstellung der ccloud³ VMs zugänglich sein.

Befehl zum Hochladen des öffentlichen Schlüssels auf Ihr centron-Konto:

`compute ssh-key import git-user --public-key-file /Users/example-user/.ssh/git-user.pub`



### Schritt 3: Konfigurieren Sie die Cloud-init-Datei

Nachdem Sie den öffentlichen SSH-Schlüssel auf Ihre centron- und GitHub-Konten hochgeladen haben, können Sie beginnen, die Cloud-init.yaml-Datei zu konfigurieren, welche die ccloud³ VM verwendet, um sich selbst zu konfigurieren.

**Beispielkonfiguration:**

```yaml
yamlCopy code#cloud-config
users:
  - name: example-user
    shell: /bin/bash
    sudo: ['ALL=(ALL) NOPASSWD:ALL']
    ssh_import_id:
      - gh:<your-GitHub-username>
disable_root: true
packages:
  - nginx
runcmd:
  - 'export PUBLIC_IPV4=$(curl -s http://169.254.169.254/metadata/v1/interfaces/public/0/ipv4/address)'
  - 'echo Droplet: $(hostname), IP Address: $PUBLIC_IPV4 > /var/www/html/index.html'
```



### Schritt 4: Bereitstellen der ccloud³ VMs

Sobald Sie die Cloud-config.yaml-Datei konfiguriert haben, können Sie die ccloud³ VMs auf Ihrem centron-Konto bereitstellen.



### Schritt 5: Überprüfen Sie die Einrichtung

Sobald Sie die ccloud³ VMs erfolgreich bereitgestellt haben, können Sie überprüfen, ob die Cloud-init-Konfiguration erfolgreich war, indem Sie sich bei einer der ccloud³ VMs mit dem Benutzernamen aus der Cloud-config.yaml-Datei anmelden.

`ssh example-user@<your-vm-ip-address>`



### Zusammenfassung

In diesem Tutorial haben Sie:

1. Ein SSH-Schlüsselpaar erstellt und den öffentlichen Schlüssel auf Ihre centron- und GitHub-Konten hochgeladen.
2. Eine Cloud-init YAML-Datei konfiguriert.
3. Zwei ccloud³ VMs bereitgestellt, die eine Cloud-init-Datei verwenden, um automatisch einen neuen Benutzer und eine nginx-Website zu konfigurieren.

Sie können jetzt diese ccloud³ VMs wie gewohnt verwenden oder bei Bedarf löschen.

---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Custom Image hochladen

## **Anforderungen an benutzerdefinierte Images bei centron**&#x20;

Benutzerdefinierte Images, die Sie zu centron hochladen, müssen folgende Anforderungen erfüllen:

* **Betriebssystem**: Die Images müssen ein Unix-ähnliches Betriebssystem enthalten.
* **Dateiformat**: Images müssen in einem der folgenden Formate vorliegen:
  * Raw (.img) mit MBR- oder GPT-Partitionstabelle
  * qcow2
  * VHDX
  * VDI
  * VMDK
* **Größe**: Images dürfen nicht größer als 100 GB im unkomprimierten Zustand sein, inklusive des Dateisystems.
* **Dateisystem**: Images müssen die Dateisysteme ext3 oder ext4 unterstützen.
* **cloud-init**: Images müssen cloud-init 0.7.7 oder höher, cloudbase-init, coreos-cloudinit, ignition oder bsd-cloudinit korrekt installiert und konfiguriert haben. Ist die Standardkonfiguration von cloud-init so eingestellt, dass die NoCloud-Datenquelle vor der ConfigDrive-Datenquelle aufgeführt ist, funktionieren ccloud³ VMs, die aus Ihrem Image erstellt wurden, möglicherweise nicht korrekt.
* **SSH-Konfiguration**: Images müssen sshd installiert haben und so konfiguriert sein, dass es beim Booten ausgeführt wird. Ohne eingerichtetes sshd haben Sie keinen SSH-Zugang zu ccloud³ VMs, die aus diesem Image erstellt wurden, es sei denn, Sie stellen den Zugang über die Wiederherstellungskonsole wieder her.

Benutzerdefinierte Images, die diesen Kriterien entsprechen, können auch als komprimierte gzip- oder bzip2-Datei hochgeladen werden.

**Warnung:** Sie müssen beim Erstellen von ccloud³ VMs aus einem benutzerdefinierten Image einen SSH-Schlüssel hinzufügen. Diese ccloud³ VMs haben standardmäßig die Passwortauthentifizierung deaktiviert. Sie können das Root-Passwort nicht über das Kontrollpanel zurücksetzen. Offizielle Unix-ähnliche OS-Images, die cloud-freundlich sind, finden Sie auf OpenStack.

## **Benutzerdefinierte Images mit Automation hochladen**&#x20;

Um Ihre Images in der centron ccloud³ verwenden zu können, senden Sie uns Ihr Image bitte an [technik@centron.de](mailto:technik@centron.de). Wir werden Ihr Image prüfen und Ihnen innerhalb von 24 Stunden zur Verfügung stellen.&#x20;

## **Ein benutzerdefiniertes Image über das Kontrollpanel hochladen**

Um ein Image über das Kontrollpanel hochzuladen, klicken Sie auf "Images" in der Hauptnavigation und dann auf den Tab für benutzerdefinierte Images.

Hier können Sie auf zwei Arten ein benutzerdefiniertes Image hochladen:

1. Laden Sie eine Bilddatei direkt hoch, indem Sie auf den Button "Image hochladen" klicken, der einen Dateiauswähler öffnet, oder indem Sie die Bilddatei in das Fenster ziehen und ablegen.

**Hinweis:** Einige Browser haben Dateigrößenbeschränkungen. Wenn Sie eine große Datei nicht über Ihren Browser hochladen können, können Sie die Datei irgendwo hosten und sie per URL hochladen. Laden Sie beispielsweise Ihr Image in den centron S3 Object Storage hoch und machen Sie die Datei öffentlich oder verwenden Sie ein Dateifreigabetool wie Dropbox. Achten Sie darauf, dass die URL mit der Dateierweiterung endet (z. B. beispiel.com/datei.raw statt beispiel.com/datei.raw?dl=0).

2. Geben Sie die URL einer Bilddatei ein, indem Sie auf den Button "Import via URL" klicken. Geben Sie im sich öffnenden Fenster "Ein Image hochladen" die URL des gewünschten Images in das Textfeld ein und klicken Sie auf Weiter. Das Kontrollpanel unterstützt Uploads von HTTP-, HTTPS- und FTP-URLs.

**Hinweis:** Das Importieren eines benutzerdefinierten Images per URL schlägt fehl, wenn das Image von einem CDN bereitgestellt wird, das HEAD-Anfragen nicht unterstützt. Wenn Sie Probleme beim Importieren eines Images über eine URL haben, versuchen Sie, die Datei herunterzuladen und direkt hochzuladen.

Nachdem Sie Ihre Auswahl getroffen haben, öffnet sich ein Fenster, in dem Sie Details zu Ihrem Image eingeben.

## **Ein Image hochladen**

* **Image-Name bearbeiten**: Dieses Feld wird automatisch mit dem Namen der hochgeladenen Datei ausgefüllt, kann aber manuell angepasst werden.
* **Distribution**: Sie können zwischen Arch Linux, Fedora, Ubuntu, CentOS, Debian oder Unbekannt wählen.
* **Wählen Sie eine Rechenzentrumregion**: Ihr Image befindet sich zunächst in einem einzelnen Rechenzentrum Ihrer Wahl, und Sie können benutzerdefinierte Images nach dem Hochladen in verschiedene Rechenzentren übertragen.
* **Tags (optional)**: Benutzerdefinierte Images unterstützen das Tagging. Sie können hier Tags zu Ihrem benutzerdefinierten Image hinzufügen oder dies jederzeit nach dem Hochladen tun.
* **Notizen (optional)**: Dies ist ein Textfeld, in dem Sie zusätzliche Anmerkungen zu Ihrem benutzerdefinierten Image für Ihre Verwendung eingeben können.

Nachdem Sie diese Details eingegeben haben, klicken Sie auf "Image hochladen". Eine Fortschrittsanzeige erscheint im Kontrollpanel neben dem Button "Image hochladen". Wenn Sie auf den Button "Details" über dieser Fortschrittsanzeige klicken, öffnet sich ein Fenster, das alle Ihre aktuellen Uploads auflistet.

Sie können jeden laufenden Upload mit einem Klick auf das nebenstehende X abbrechen oder auf "Uploads abbrechen" klicken, um alle aktuell laufenden Uploads zu beenden.

Sobald Sie mindestens ein benutzerdefiniertes Image zu Ihrem Konto hinzugefügt haben, können Sie eine ccloud³ VM aus einem benutzerdefinierten Image erstellen.

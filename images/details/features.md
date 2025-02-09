---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Features

Nachdem Sie ein benutzerdefiniertes Image auf Ihr centron-Konto hochgeladen haben, können Sie ccloud³ VMs basierend auf diesem Image erstellen. Wenn Sie ein benutzerdefiniertes Image hochladen, wählen Sie eine Region aus, in der es verfügbar sein soll. Sie können ccloud³ VMs basierend auf einem benutzerdefinierten Image in dieser Region erstellen und Ihr benutzerdefiniertes Image jederzeit in zusätzlichen Regionen verfügbar machen.

Sie finden cloud-freundliche offizielle Unix-ähnliche OS-Images auf OpenStack oder erstellen Ihr eigenes mit Ihrer bevorzugten VM-Software.

**Anforderungen an Images:** Die Images, die Sie zu centron hochladen, müssen die folgenden Anforderungen erfüllen:

* **Betriebssystem:** Die Images müssen ein Unix-ähnliches Betriebssystem haben.
* **Dateiformat:** Die Images müssen in einem der folgenden Dateiformate vorliegen:
  * Raw (.img) mit einer MBR- oder GPT-Partitionstabelle
  * qcow2
  * VHDX
  * VDI
  * VMDK
* **Größe:** Die Images dürfen nicht größer als 100 GB sein (unkomprimiert, einschließlich Dateisystems).
* **Dateisystem:** Die Images müssen die Dateisysteme ext3 oder ext4 unterstützen.
* **cloud-init:** Die Images müssen cloud-init 0.7.7 oder höher, cloudbase-init, coreos-cloudinit, Zündung oder bsd-cloudinit installiert und korrekt konfiguriert haben. Wenn die Standardkonfiguration von cloud-init Ihres Images die NoCloud-Datenquelle vor der ConfigDrive-Datenquelle auflistet, funktionieren ccloud³ VMs, die aus Ihrem Image erstellt wurden, möglicherweise nicht ordnungsgemäß.
* **SSH-Konfiguration:** Die Images müssen sshd installiert haben und so konfiguriert sein, dass es beim Booten ausgeführt wird. Wenn Ihr Image sshd nicht eingerichtet hat, haben Sie keinen SSH-Zugang zu ccloud³ VMs, die aus diesem Image erstellt wurden, es sei denn, Sie stellen den Zugang über die Wiederherstellungskonsole wieder her.

**Sie können auch ein benutzerdefiniertes Image, das die oben genannten Kriterien erfüllt, als komprimierte gzip- oder bzip2-Datei hochladen.**

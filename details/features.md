---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Features

centron unterstützt die folgenden Linux- und Windows-Distributionen:

* **Windows**
  * 2022 (de-DE)
  * 2022 (en-US)
  * 2019 (de-DE)
  * 2019 (en-US)
* **Ubuntu**:
  * 23.10 x64
  * 23.04 x64
  * 22.04 (LTS) x64
  * 20.04 (LTS) x64
* **Debian**:
  * 12.0 x64
  * 11.0 x64
  * 10.3 x64
* **CentOS**:
  * 9 Stream x64
  * 8 Stream x64
  * 7.6 Linux x64
* **Alma Linux**:
  * 8.6
  * 9
* **Rocky Linux**:
  * 8 x64
  * 9 x64
* **Fedora**:
  * 39 x64
  * 38 x64
  * 37 x64

#### Tags

Tags sind benutzerdefinierte Etiketten, die Sie ccloud³ VMs zuweisen können und die mehrere Verwendungszwecke haben:

* **Filterung**: Mehrere ccloud³ VMs mit demselben Label zu taggen, ermöglicht es Ihnen, Ihre Ressourcen zu organisieren und eine gefilterte Liste von ccloud³ VMs anzuzeigen, die diesen bestimmten Tag teilen.
* **Automatische Einbeziehung in Firewall-Regeln und Load Balancer-Backend-Pools**: Schließen Sie ccloud³ VMs automatisch in einer Firewall oder Load Balancer-Konfiguration ein, indem Sie Tags verwenden, um den Verwaltungsaufwand beim Hinzufügen neuer ccloud³ VMs zu Ihrer Infrastruktur zu minimieren.
* **Ausführung von API-Aufrufen auf mehreren ccloud³ VMs gleichzeitig**: Initiieren Sie eine Aktion über alle ccloud³ VMs mit demselben Tag mithilfe der centron-API. Das Identifizieren von Gruppen von ccloud³ VMs und deren gleichzeitige Verwaltung reduziert die Zeit, die benötigt wird, um Ressourcen zu managen.

#### Zusätzliche IPs

centron IPs sind öffentlich zugängliche statische IP-Adressen, die Sie ccloud³ VMs zuweisen können. Eine reservierte IP bietet eine zusätzliche statische Adresse, die Sie verwenden können, um auf eine ccloud³ VM zuzugreifen, ohne die ursprüngliche öffentliche IP-Adresse der ccloud³ VM zu ersetzen oder zu ändern.

#### Premium Full Managing

Premium Full Managing übernimmt die Grundaufgaben Ihrer Infrastruktur: Backup, Monitoring und Patch Management. Da centron Premium Full Managing pro VM als Add-on ausgewählt werden kann, können Sie frei entscheiden, welcher Teil Ihrer Infrastruktur von centron übernommen wird.&#x20;

#### Firewalls

Die centron Cloud-Firewalls sind ein zustandsbehafteter Firewall-Dienst für Ihre ccloud³ VMs. Sie blockieren allen Verkehr, der nicht ausdrücklich durch eine Regel erlaubt ist. Sie können die von einer Firewall geschützten ccloud³ VMs individuell oder mithilfe von Tags definieren.

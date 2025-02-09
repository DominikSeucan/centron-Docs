---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Features

#### OS

centron unterstützt die folgenden Linux- und Windows-Distributionen:

**Windows**

* 2022 (de-DE)
* 2022 (en-US)
* 2019 (de-DE)
* 2019 (en-US)

**Ubuntu**:

* 23.10 x64
* 23.04 x64
* 22.04 (LTS) x64
* 20.04 (LTS) x64

**Debian**:

* 12.0 x64
* 11.0 x64
* 10.3 x64

#### Tags

Tags sind benutzerdefinierte Etiketten, die Sie ccloud³ VMs zuweisen können und die mehrere Verwendungszwecke haben:

* **Filterung**: Mehrere ccloud³ VMs mit demselben Label zu taggen, ermöglicht es Ihnen, Ihre Ressourcen zu organisieren und eine gefilterte Liste von ccloud³ VMs anzuzeigen, die diesen bestimmten Tag teilen.
* **Automatische Einbeziehung in Firewall-Regeln und Load Balancer-Backend-Pools**: Schließen Sie ccloud³ VMs automatisch in einer Firewall oder Load Balancer-Konfiguration ein, indem Sie Tags verwenden, um den Verwaltungsaufwand beim Hinzufügen neuer ccloud³ VMs zu Ihrer Infrastruktur zu minimieren.
* **Ausführung von API-Aufrufen auf mehreren ccloud³ VMs gleichzeitig**: Initiieren Sie eine Aktion über alle ccloud³ VMs mit demselben Tag mithilfe der centron-API. Das Identifizieren von Gruppen von ccloud³ VMs und deren gleichzeitige Verwaltung reduziert die Zeit, die benötigt wird, um Ressourcen zu managen.

#### Reservierte IPs

centron Reservierte IPs sind öffentlich zugängliche statische IP-Adressen, welche Sie ccloud³ VMs zuweisen können. Eine reservierte IP bietet eine zusätzliche statische Adresse, die Sie verwenden können, um auf eine ccloud³ VM zuzugreifen, ohne die ursprüngliche öffentliche IP-Adresse der ccloud³ VM zu ersetzen oder zu ändern.

#### Volumes Blockspeicher

Der centron Volumes Blockspeicher ist eine flexible und bequeme Möglichkeit, zusätzlichen Speicher (in Einheiten, die als Volumes bezeichnet werden) für Ihre ccloud³ VMs zu verwalten. Volumes sind unabhängige Ressourcen, die Sie zwischen ccloud³ VMs innerhalb derselben Region verschieben können. Sie können die Größe eines Volumes erhöhen, ohne die ccloud³ VM herunterzufahren, an die es angeschlossen ist. Sie sind besonders nützlich, wenn Sie mehr Speicherplatz benötigen, aber nicht die zusätzliche Verarbeitungsleistung oder den zusätzlichen Speicher, den eine größere ccloud³ VM bieten würde.

#### Firewalls

Die centron Cloud-Firewalls sind ein kostenloser, netzwerkbasierter, zustandsbehafteter Firewall-Dienst für Ihre ccloud³ VMs. Sie blockieren allen Verkehr, der nicht ausdrücklich durch eine Regel erlaubt ist. Sie können die von einer Firewall geschützten ccloud³ VMs individuell oder mithilfe von Tags definieren.

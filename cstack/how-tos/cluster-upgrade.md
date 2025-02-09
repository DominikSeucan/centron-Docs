---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# Cluster Upgrade

Bei centron können Sie Ihre Apache Cloudstack-basierten Kubernetes-Cluster sowohl auf neue Patch-Versionen (z.B. von 1.20.1 auf 1.20.2) als auch auf neue kleinere Versionen (z.B. von 1.19.1 auf 1.20.1) aktualisieren. Dies kann über das cStack Webinterface erfolgen.

Dazu navigieren Sie bitte wie folgt:

1. Klicken Sie im cStack Webinterface auf den linken Navigationspunkt "Berechnen" - "Instanzen"
2. Wählen Sie Ihr Kubernetes Cluster aus, welches Sie upgraden möchten
3. Anschließend können Sie oben Rechts auf den Button "Kubernetes Cluster upgraden" klicken und eine neuere Version auswählen

<figure><img src="../.gitbook/assets/Kubernetes Cluster Upgraden ®.png" alt=""><figcaption></figcaption></figure>

**Upgrade-Optionen**

1. **Manuelles Upgrade**: Wenn ein Upgrade für Ihr Kubernetes-Cluster verfügbar wird, können Sie den Upgrade-Prozess manuell auslösen. Sie können auf eine neue kleinere Version upgraden, sofern zuerst alle verfügbaren Patch-Updates für Ihre aktuelle kleinere Version durchgeführt wurden.
2. **Automatisches Upgrade**: Sie können automatische Upgrades für Ihr Cluster aktivieren, die innerhalb eines von Ihnen festgelegten Wartungsfensters stattfinden. Automatische Updates werden bei neuen Patch-Versionen von Kubernetes und bei neuen Punktversionen von Apache Cloudstack mit nicht-brechenden Updates ausgelöst. Upgrades auf neue kleinere Kubernetes-Versionen erfolgen jedoch nicht automatisch.

**Hinweis**: centron unterstützt die neuesten drei kleineren Versionen von Kubernetes. Wenn Ihr Cluster eine ältere Version ausführt, wird ein Upgrade erzwungen, selbst wenn automatische Upgrades deaktiviert sind.



**Notwendige Upgrades**&#x20;

Erforderliche Upgrades werden im Control Panel angezeigt. Sie können den Wochentag und die Zeit für erforderliche Upgrades im Einstellungsbereich Ihres Clusters konfigurieren.



**Der Upgrade-Prozess**&#x20;

Während eines Upgrades wird die Kontrollebene (Kubernetes-Hauptteil) durch eine neue Kontrollebene mit der neuen Kubernetes-Version ersetzt. Arbeiterknoten werden dann schrittweise ersetzt.

**Warnung**: Daten auf den lokalen Disks der Arbeiterknoten gehen beim Upgrade verloren. Wir empfehlen, persistente Volumes für die Datenspeicherung zu verwenden.



**Surge-Upgrades**&#x20;

Surge-Upgrades erstellen duplizierte aktualisierte Knoten und verschieben die Workloads von den alten zu den neuen Knoten. Sie sind standardmäßig aktiviert und verfügbar, um ein schnelleres und stabileres Upgrade zu ermöglichen.



**Upgrades über das cStack Webinterface**&#x20;

Für manuelle Upgrades besuchen Sie den Überblicks-Tab Ihres Clusters im cStack Webinterface. Für automatische Upgrades aktivieren Sie die entsprechende Option im Einstellungsbereich.



**Minimierung von Unterbrechungen während Upgrades**&#x20;

Konfigurieren Sie ein PodDisruptionBudget und implementieren Sie Graceful Shutdowns in Ihren Workloads, um die Verfügbarkeit der Dienste während des Upgrades zu verbessern.

Diese angepasste Version stellt sicher, dass das ursprüngliche Konzept der Kubernetes-Cluster-Upgrades bei DigitalOcean in den Kontext von centron und Apache Cloudstack übertragen wird, wobei die spezifischen Merkmale und Vorteile des centron-Angebots berücksichtigt werden.

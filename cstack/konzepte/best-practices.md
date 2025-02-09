---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# Best Practices

Bei der Erstellung und Verwaltung von Kubernetes-Clustern gibt es eine Reihe von Best Practices, die dazu beitragen können, eine hohe Verfügbarkeit und Skalierbarkeit zu gewährleisten und gängige Störungen zu vermeiden. Hier sind einige dieser Best Practices zusammengefasst:

#### Verwendung von Replikas anstelle von Bare Pods

* **Einsatz von Replikas**: Stellen Sie Ihre Anwendungen immer in hochverfügbarer Form bereit, indem Sie mehrere stabile Replikas Ihrer Anwendungen verwenden und keine Bare Pods einsetzen.
* **Anwendungsspezifikation**: Verwenden Sie das `replicas`-Feld in Ihrer Anwendungsspezifikation, um mindestens drei Replikas zu definieren.

#### Knotengröße angemessen wählen

* **Knotengröße für Produktionsumgebungen**: Für Produktionscluster sollten Knoten groß genug sein (2,5 GB oder mehr), um die Arbeitslast eines ausgefallenen Knotens aufzufangen.
* **Knotenplan**: Wählen Sie während der Clustererstellung einen Knotenplan, der den Anforderungen Ihres Projekts entspricht.

#### Knotenpools für hohe Verfügbarkeit dimensionieren

* **Mindestanzahl von Knoten**: Node Pools mit Produktionsworkloads sollten mindestens drei Knoten umfassen.
* **Autoskalierung**: Konfigurieren Sie die Autoskalierungsfunktion, um eine Mindestclustergröße von drei Knoten sicherzustellen.

#### Anfragen und Limits festlegen

* **Effiziente Ressourcennutzung**: Definieren Sie die `requests`- und `limits`-Objekte in Ihrer Anwendungsspezifikation für alle Deployments, um die Ressourcennutzung zu optimieren.

#### Pod Disruption Budgets einrichten

* **Vermeidung von Störungen**: Richten Sie ein Pod Disruption Budget (PDB) ein, das die Anzahl der replizierten Pods begrenzt, die gleichzeitig ausfallen können.
* **PDB-Spezifikation**: Erstellen Sie eine PodDisruptionBudget-Policy-Spezifikation, um das Minimum an verfügbaren Pods für eine Anwendung festzulegen.

#### Automatische Upgrades aktivieren

* **Aktuellste Features und Sicherheitspatches**: Aktivieren Sie automatische Upgrades, um sicherzustellen, dass Ihr Cluster mit den neuesten Funktionen, Sicherheitspatches und Stabilitätsverbesserungen läuft.

#### Surge Upgrades aktivieren

* **Reduzierung der Upgrade-Auswirkungen**: Aktivieren Sie Surge Upgrades, um die Gesamtausfallzeit und den Einfluss auf Anwendungen während eines Upgrades zu reduzieren.

#### Cluster Linter-Nachrichten überprüfen

* **Frühzeitige Identifizierung von Problemen**: Verwenden Sie regelmäßig Clusterlint, um Probleme in Ihrem Cluster zu identifizieren, die sonst möglicherweise nicht sofort erkennbar sind.

Diese Best Practices helfen dabei, die Stabilität, Skalierbarkeit und Verfügbarkeit von Kubernetes-Clustern zu maximieren und gleichzeitig potenzielle Probleme und Ausfallzeiten zu minimieren.

---
description: Überprüft am 12. April 2023 • Zuletzt bearbeitet am 4. April 2024
---

# VM Größe & Pool wählen

Die Auswahl des richtigen cStack-Plans hängt stark von Ihrer Arbeitslast ab. Ein zu groß dimensioniertes Kubernetes Cluster nutzt seine Ressourcen nicht vollständig aus und verursacht höhere Kosten, während ein zu klein dimensioniertes Kubernetes Cluster, welches bei voller CPU- oder Speicherauslastung läuft, eine verschlechterte Leistung oder Fehler aufweisen kann. Diese Anleitung umfasst die folgenden Themen:

#### Auswahl von Knotengröße und -anzahl

* **Knotengröße**: Bestimmt die maximale Menge an Speicher, die Pods zugewiesen werden kann. Für Produktionscluster wird empfohlen, Knoten mit mindestens 2,5 GB oder mehr Speicher zu verwenden.
* **Knotenanzahl**: Bestimmt die gesamte CPU, den RAM und den Speicher Ihres Clusters. Mehr Knoten bedeuten mehr Flexibilität bei der Lastverteilung.

#### Datenbasierte Entscheidung treffen

* **Benchmarking und Lasttests**: Nach der Erstellung eines Clusters sollten Sie Ihre Arbeitslast benchmarken und Lasttests durchführen, um zu sehen, wie sie unter simulierter Last abschneidet.
* **Ressourcennutzung analysieren**: Überwachen Sie die CPU- und Speichernutzung Ihres Clusters und passen Sie die Knotengröße entsprechend den Anforderungen Ihrer Arbeitslast an.

#### Zusätzlicher Speicher

* **Attached Block Storage**: Wenn zusätzlicher Speicher benötigt wird, können Sie netzwerkgebundene Blockspeicher verwenden, um zusätzliche Volumes an einen Cluster anzuhängen.

#### Wichtig zu beachten

* **CPU- und RAM-Spitzen**: Da die CPU-Auslastung eines Kubernetes-Clusters dazu neigt, mit hohen Spitzen an Aktivität zu schwanken, während der RAM tendenziell konstant bleibt, wird empfohlen, Ihre CPU so zu dimensionieren, dass sie diese Spitzen in Ihrer Arbeitslast bewältigen kann.
* **Änderungen nach der Erstellung**: Nach der Erstellung können Sie ein Kubernetes-Cluster jederzeit auf einen anderen Plan umstellen. Für eine vollständige Liste der Pläne und Preise siehe die Preisseite für Cluster.

Diese Punkte sollen Ihnen ein ungefähres Gefühl dafür geben welche Punkte für die Auswahl des richtigen cStack Plans ausschlaggebend sein können.

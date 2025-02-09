---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# Cluster zerstören

Sofern Sie ein erstelltes Kubernetes Cluster nicht mehr benötigen so können Sie dieses über unser cStack Webinterface wieder löschen. Dazu wählen Sie das gewünschte Kubernetes Cluster aus und klicken auf den roten Papierkorb. Die Auflistung der vorhandenen Kubernetes Cluster erreichen Sie wie folgt:

1. Öffnen Sie das cStack Webinterface über unser ccenter
2. Klicken Sie links in der Navigation auf "Berechnen" - "Kubernetes"

<figure><img src="../.gitbook/assets/Pasted Graphic 25.png" alt=""><figcaption></figcaption></figure>

Sie können das Kubernetes Cluster auch löschen, wenn Sie dieses über den Namen im cStack Webinterface ausgewählt haben.

<figure><img src="../.gitbook/assets/Pasted Graphic 26.png" alt=""><figcaption></figcaption></figure>

Beim Löschvorgang eines Kubernetes Clusters werden Sie gefragt, ob dieses bereinigt und/oder unwiederbringlich gelöscht werden soll. Weitere Informationen zu den beiden Optionen erhalten Sie über dem Info-Button „i“.

<figure><img src="../.gitbook/assets/Kubernetes Cluster löschen ©.png" alt=""><figcaption></figcaption></figure>

#### Manuelle Löschung von zugehörigen Ressourcen

* **Nach dem Zerstören des Clusters**: Sie können auch die zugehörigen Load Balancer und Volumes manuell über das cStack Webinterface löschen, nachdem das Kubernetes Cluster zerstört wurde. Sie werden weiterhin für diese Ressourcen belastet, bis sie zerstört werden.

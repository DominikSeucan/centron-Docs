---
description: Überprüft am 12. April 2023 • Zuletzt bearbeitet am 4. April 2024
---

# Persistent Volume Claims

Diese Anleitung beschreibt die Schritte, wie man mit centron cStack einem Kubernetes Cluster Persistent Volumes (PVs) mittels Persistent Volume Claims (PVCs) hinzufügt. Dies basiert auf dem Einsatz des [CloudStack CSI Drivers](https://github.com/apalia/cloudstack-csi-driver) und einem Beispielkonfigurationscode für die PVC-Definition.

### Voraussetzungen

* Zugang zu einem centron cStack Kubernetes Cluster
* Funktionierende Installation und Konfiguration des CloudStack CSI Drivers
* Administratorrechte für das Kubernetes Cluster

### Schritte zur Erstellung eines Persistent Volume Claims

1. **Installieren der .yaml files**

Laden Sie die Files `install.yaml` & `0-storageclass.yaml` herunter. Installieren Sie als erstes die Storage Class, um Ihrem Kubernetes Cluster Volumes hinzuzufügen:

{% file src="../.gitbook/assets/install.yaml" %}

{% file src="../.gitbook/assets/0-storageclass.yaml" %}

Führen Sie anschließend folgende Befehle aus:

```
kubectl apply -f install.yaml
```

```
kubectl apply -f 0-storageclass.yaml
```

#### 2. Erstellen einer Persistent Volume Claim YAML-Datei

Erstellen Sie eine YAML-Datei (z.B. `pvc.yaml`) mit folgendem Inhalt:

```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: wp-pv-claim
  labels:
    app: wordpress
spec:
  storageClassName: cloudstack-custom
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 20Gi
```

In dieser Definition:

* **metadata.name**: Der Name des Persistent Volume Claims (`wp-pv-claim`).
* **labels**: Labels zur einfacheren Identifikation, hier auf die Anwendung "wordpress" abgestimmt.
* **spec.storageClassName**: Gibt die zu verwendende StorageClass an (`cloudstack-custom`), die auf die Konfiguration Ihres CloudStack-Clusters abgestimmt ist.
* **spec.accessModes**: Gibt die Zugriffsmethode für das Volume an. In diesem Fall ist `ReadWriteOnce` angegeben, d.h. das Volume kann von einem einzelnen Node gelesen und beschrieben werden.
* **spec.resources.requests.storage**: Gibt die gewünschte Größe des Volumes an (hier 20Gi).

#### 3.. Anwenden der Persistent Volume Claim Definition

Um den Persistent Volume Claim im Kubernetes Cluster zu erstellen, verwenden Sie den `kubectl`-Befehl:

```
kubectl apply -f pvc.yaml
```

Nach erfolgreicher Anwendung sehen Sie eine Ausgabe ähnlich wie:

```
persistentvolumeclaim/wp-pv-claim created
```

#### 4.. Überprüfen des Persistent Volume Claims

Sie können den Status des Persistent Volume Claims überprüfen, indem Sie den folgenden Befehl ausführen:

```
kubectl get pvc
```

Dies zeigt die Liste der PVCs und deren aktuellen Status. Die Ausgabe könnte so aussehen:

```
NAME          STATUS   VOLUME                                     CAPACITY   ACCESS MODES   STORAGECLASS      AGE
wp-pv-claim   Bound    pvc-12345678-1234-5678-1234-567812345678   20Gi       RWO            cloudstack-custom 5m
```

Ein `STATUS` von `Bound` zeigt an, dass das Volume erfolgreich gebunden wurde und zur Verwendung bereitsteht.

#### 5. Integration in Ihre Anwendung

Verwenden Sie die Persistent Volume Claim in Ihren Deployments oder StatefulSets, um Speicher für Ihre Anwendungen bereitzustellen. Ein Beispiel für die Nutzung in einem Deployment sieht wie folgt aus:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: wordpress
spec:
  replicas: 1
  selector:
    matchLabels:
      app: wordpress
  template:
    metadata:
      labels:
        app: wordpress
    spec:
      containers:
      - name: wordpress
        image: wordpress:latest
        ports:
        - containerPort: 80
        volumeMounts:
        - mountPath: /var/www/html
          name: wp-volume
      volumes:
      - name: wp-volume
        persistentVolumeClaim:
          claimName: wp-pv-claim

```

#### 6. Wichtige Hinweise

* Stellen Sie sicher, dass Ihre `StorageClass`-Konfiguration kompatibel mit dem CloudStack CSI Driver ist.
* Der `storageClassName` in der PVC-Definition sollte mit einer vorhandenen StorageClass übereinstimmen, die für den Cluster konfiguriert ist.
* Der `accessModes`-Wert kann angepasst werden, je nach den Anforderungen der Anwendung (z.B. `ReadOnlyMany` oder `ReadWriteMany`).

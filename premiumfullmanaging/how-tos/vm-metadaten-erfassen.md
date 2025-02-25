---
description: Validiert am 28.05.2024 • Zuletzt bearbeitet am 17. September 2024
---

# VM Metadaten erfassen

Der Metadata-Service ermöglicht es einer VM, Daten über sich selbst abzurufen. Neben der grundlegenden Abfrage von VM-Metadaten erlaubt der Service den Benutzern, beliebige Nutzerdaten bei der Erstellung der VM bereitzustellen, welche dann von CloudInit verwendet werden können, um die Bereitstellung von Cloud-Servern zu erleichtern und zu beschleunigen.

Obwohl die spezifischen Details und Endpunkte des Metadata-Services bei centron variieren können, ist das grundlegende Konzept ähnlich. Hier ist eine allgemeine Anleitung, wie Sie Metadaten für eine VM abrufen können:

#### Metadata Service IP

VMs können auf den Metadata-Service über eine spezielle statische IP-Adresse zugreifen, was zum Beispiel die 169.254.169.254 ist. Dies ermöglicht die Verwendung ähnlicher Skripte auf verschiedenen VMs, ohne die Ziel-IP-Adresse ändern zu müssen.

#### Metadaten einer VM abrufen

Sie können Metadaten von einer VM abfragen, indem Sie eine HTTP-GET-Anfrage an eine Link-Local-Adresse senden, die ähnlich der folgenden sein könnte:

```ruby
http://169.254.169.254/metadata/v1/
```

#### Top-Level-Index

Hier ein Beispiel, wie Sie den Befehl `curl` verwenden können, um eine HTTP-GET-Anfrage an die oberste Ebene des Metadata-Endpunkts zu senden:

```bash
curl http://169.254.169.254/metadata/v1/
```

Dies gibt einen Index der verfügbaren VM-Metadaten zurück und kann wie ein Verzeichnislisting angesehen werden. Sie können weitere `curl`-Befehle in die Indizes senden, um mehr Einträge zu sehen.

#### Nutzerdaten

Hier ein Beispiel, wie Sie `curl` verwenden können, um die Nutzerdaten einer VM abzurufen:

```bash
curl http://169.254.169.254/metadata/v1/user-data
```

#### Öffentliche Netzwerkschnittstelle

Hier ein Beispiel, wie Sie `curl` verwenden können, um die öffentliche IP-Adresse einer VM abzurufen:

```bash
curl http://169.254.169.254/metadata/v1/interfaces/public/0/ipv4/address
```

#### Fazit

Durch Aufrufen der speziellen IP (z.B. 169.254.169.254) von einer VM aus können Sie Metadaten über diese VM abrufen. Vollständige Details der zugänglichen Metadaten sind normalerweise auf dem Entwicklerportal des jeweiligen Cloud-Anbieters verfügbar.

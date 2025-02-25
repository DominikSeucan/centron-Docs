---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Features

Im Kontext von centron und dessen ccloud³ VMs lässt sich das Konzept der Reserved IPs (reservierten IP-Adressen) folgendermaßen adaptieren und anwenden:

**Verwendung von Reserved IPs**: Reserved IPs ermöglichen es Ihnen, den Netzwerkverkehr zwischen Ihren ccloud³ VMs innerhalb desselben Rechenzentrums umzuleiten. Das Zuweisen einer Reserved IP zu einer ccloud³ VM ersetzt oder ändert deren ursprüngliche öffentliche IP-Adresse nicht.

**Aufbau Serverinfrastrukturen ohne einzelne Ausfallpunkte**: Mithilfe von Reserved IPs können Sie Serverinfrastrukturen ohne einzelne Ausfallpunkte erstellen. Dies erhöht die Zuverlässigkeit und Ausfallsicherheit Ihrer Anwendungen.

**High Availability (Hohe Verfügbarkeit)**: Eine Reserved IP allein bietet jedoch keine automatische Hochverfügbarkeit. Für eine hochverfügbare Einrichtung müssen Sie einen Failover-Mechanismus implementieren, der Ausfälle des aktiven Servers automatisch erkennt und die Reserved IP einem passiven Server zuweist.

**Aktive/Passive-Setup**: Dies beinhaltet typischerweise ein aktives/passives Setup, bei dem ein aktiver Server den Großteil der Last trägt, während ein oder mehrere passive Server bereitstehen, um im Falle eines Ausfalls des aktiven Servers einzuspringen.

**Verwaltung über API**: Reserved IPs können über eine API verwaltet werden, was eine automatische Neuverteilung im Falle eines Serverausfalls ermöglicht. Dies ist besonders nützlich für die Implementierung von automatisierten Failover-Prozessen.

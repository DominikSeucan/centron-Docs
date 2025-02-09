---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# VM Größe & Pool wählen

Die Wahl des richtigen ccloud³ VM-Plans hängt von Ihrer Arbeitslast ab. Eine überdimensionierte ccloud³ VM würde ihre Ressourcen unterausnutzen und mehr kosten, während eine unterdimensionierte ccloud³ VM bei voller CPU- oder Speicherauslastung eine verschlechterte Leistung oder Fehler erleiden könnte.

Um Ihnen bei der Auswahl des besten ccloud³ VM-Plans für Ihren Anwendungsfall zu helfen, erklärt dieser Artikel die Unterschiede zwischen gemeinsam genutzten und dedizierten CPUs, geht detailliert auf jeden ccloud³ VM-Plan ein und schließt mit Empfehlungen für eine datengesteuerte Entscheidung ab.

Sie können auch nach der Erstellung eine ccloud³ VM auf einen größeren Plan umstellen, einschließlich der Umstellung auf einen größeren ccloud³ VM-Plan eines anderen Typs. Beispielsweise können Sie von einem Basic ccloud³ VM-Plan auf einen größeren CPU-optimierten ccloud³ VM-Plan umstellen. Die Preisliste für ccloud³ VMs finden Sie auf der Preisübersichtsseite.



### Shared CPU vs. Dedicated CPU

Eine ccloud³ VM ist eine virtuelle Maschine (VM), die Ressourcen wie CPU, RAM und Festplattenspeicher von einem physischen Host zugewiesen bekommt.

Ein Hypervisor, auch bekannt als virtueller Maschinenmonitor, stellt sicher, dass die auf einem physischen Host laufenden ccloud³ VMs jeweils ihre virtuellen Ressourcen, wie vCPU erhalten.

Eine vCPU ist eine Einheit der Verarbeitungsleistung, die einem einzelnen Hyper-Thread auf einem Prozessorkern entspricht. Ein moderner, mehrkerniger Prozessor hat mehrere vCPUs.

Der von Ihnen gewählte ccloud³ VM-Plan bestimmt die Menge der Ressourcen, die der ccloud³ VM zugewiesen werden. Ressourcen wie RAM, Festplattenspeicher und Netzwerkbandbreite sind immer dediziert, aber Sie können zwischen Plänen mit gemeinsam genutzten CPUs und dedizierten CPUs für dedizierte vCPUs wählen.

Dedizierte CPU-ccloud³ VMs haben garantierten Zugriff auf den vollen Hyper-Thread zu jeder Zeit. Bei gemeinsam genutzten CPU-ccloud³ VMs kann der dem ccloud³ VM zugewiesene Hyper-Thread zwischen mehreren anderen ccloud³ VMs geteilt werden. Wenn eine gemeinsam genutzte CPU-ccloud³ VM eine höhere Last erfährt, weist der Hypervisor dynamisch mehr Hyper-Thread(s) zu.

Die Menge der für den Hypervisor verfügbaren CPU-Zyklen hängt jedoch von der Arbeitslast der anderen ccloud³ VMs ab, die diesen Host teilen. Wenn diese benachbarten ccloud³ VMs eine hohe Last haben, könnte eine ccloud³ VM Bruchteile von Hyper-Threads statt dedizierten Zugang zu den zugrundeliegenden physischen Prozessoren erhalten. In der Praxis bedeutet dies, dass gemeinsam genutzte CPU-ccloud³ VMs Zugang zu vollen Hyper-Threads haben können, aber dies ist nicht garantiert.



### Datengesteuerte Entscheidung

Bevor Sie sich für einen bestimmten ccloud³ VM-Typ entscheiden, empfehlen wir, Ihre Arbeitslast zu benchmarken und Lasttests durchzuführen, um zu sehen, wie sie unter simulierter Last abschneidet. Für burstige Apps oder Batch-Jobs sollten Sie die Ressourcennutzung beobachten, wenn die Last auf ihrem erwarteten Höhepunkt ist, insbesondere bei gemeinsam genutzten CPU Basic ccloud³ VMs. Wenn Sie feststellen, dass die Leistung Ihrer App für Ihre Produktionsanforderungen zu variabel ist, sollten Sie einen ccloud³ VM-Typ mit dedizierten vCPUs in Betracht ziehen.



### CPU und RAM

Mit ccloud³ VM-Graphen können Sie mehr Informationen über die CPU-Last und den Speicherverbrauch Ihrer ccloud³ VM erhalten:

* Bei hoher CPU- und gleichzeitig signifikanter Speicherauslastung sollten Sie sowohl vCPUs als auch Speicher skalieren und einen ausgewogenen General Purpose ccloud³ VM-Plan verwenden.
* Bei hoher CPU-Auslastung, aber sehr geringer Speicherauslastung könnten Sie mit einem CPU-Optimized ccloud³ VM-Plan Geld sparen.
* Bei hoher Speicherauslastung (möglicherweise maximiert und auf die Festplatte ausgelagert), aber niedriger oder moderater CPU-Auslastung sollten Sie den Speicher skalieren und einen Memory-Optimized ccloud³ VM-Plan verwenden.
* Auch wenn die CPU- oder Speicherauslastung sich die meiste Zeit niedrig bis moderat hält, kann diese manchmal hochschnellen und an ihre Ressourcengrenzen stoßen. Wenn dies der Fall ist, sollten Sie gemeinsam genutzte CPU Basic ccloud³ VMs in Betracht ziehen und die begrenzende Ressource entsprechend skalieren.



### Festplatte

Alle ccloud³ VMs von centron beinhalten variable Mengen an lokalem Solid-State-Disk (SSD)-Speicher. Wenn Sie zusätzlichen Speicher benötigen, können Sie netzwerkgebundene Blockspeicher verwenden, um zusätzliche Volumes an eine ccloud³ VM anzuhängen oder den Objektspeicher Spaces verwenden, um Dateien und zugehörige Metadaten auszulagern.



### Netzwerk

ccloud³ VMs beinhalten unbegrenzten kostenlosen eingehenden Datenverkehr. Abhängig von Ihrem Arbeitslasttyp und der Bandbreitennutzung könnten Sie Ihre ccloud³ VM skalieren.

Mit Monitoring können Sie sowohl Festplatten- als auch Bandbreitennutzung überwachen, ähnlich wie Sie CPU- und Speicherauslastung überwachen würden.

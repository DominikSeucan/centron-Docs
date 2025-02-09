---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Performance beobachten

Um die Graphen einer ccloud³ VM zu betrachten, klicken Sie einfach auf deren Namen im Dashboard. Sie gelangen direkt auf die Graphenseite. Standardmäßig sind drei Graphen für jede ccloud³ VM verfügbar:

1. **Trafficnutzung (Public)**: Dieser Graph zeigt die Nutzung der öffentlichen Bandbreite in Megabit pro Sekunde an.&#x20;
2. **CPU-Nutzung**: Hier wird der Prozentsatz der insgesamt genutzten Verarbeitungsleistung angezeigt. Nutzeraktivitäten sind in hellblau und Systemprozesse in dunkelblau dargestellt.
3. **Festplatten-I/O**: Dieser Graph zeigt Festplattenlese- und -schreiboperationen in Megabyte pro Sekunde.
4. **Speichernutzung (Memory)**: Zeigt den Prozentsatz des genutzten physischen RAMs an.

Die Zeiten in diesen Graphen entsprechen Ihrer lokalen Zeitzone, wie sie von Ihrem Browser bestimmt wird.

Sollten Sie das private Netzwerk auf der ccloud³ VM aktiviert haben, haben Sie Zugriff auf einen vierten Graphen zur Überwachung der Bandbreitennutzung im VPC-Netzwerk. Wie beim Graphen für die öffentliche Bandbreite erscheint der Graph für die private Bandbreite erst, wenn tatsächlich Netzwerkverkehr vorliegt.&#x20;

Der Graph für die private Bandbreite zeigt die VPC-Netzwerkbandbreitennutzung in Megabit pro Sekunde an, wobei die eingehende Nutzung in dunkellila und die ausgehende Nutzung in helllila dargestellt wird.



### Advanced Monitoring

Die Standardgraphen der ccloud³ VM nutzen Metriken, die von externen Tools gesammelt werden; es sind keine zusätzlichen Dienste auf der ccloud³ VM selbst erforderlich. Sie können zusätzliche Metrikengraphen und Alarmfunktionen mit dem Metrics Agent von centron aktivieren, einem kleinen Dienstprogramm, welches auf der ccloud³ VM läuft.

Sie können den Metrics Agent automatisch bei der Bereitstellung einer ccloud³ VM oder nach deren Erstellung installieren.

Sobald der Agent installiert ist, haben Sie u.a. Zugang zu diesen zusätzlichen Graphen:

* **Durchschnittliche Last (Load Average)**: Misst, ob die CPU mit den wartenden Prozessen Schritt hält. Es gibt drei Linien, die 1-, 5- und 15-minütige Durchschnittslasten in blau, grün und lila darstellen.
* **Festplattennutzung (Disk Usage)**: Zeigt den Prozentsatz des genutzten Speicherplatzes auf der Festplatte der ccloud³ VM an.

Die Zeitrahmenoptionen für die ccloud³ VM-Graphen sind 1 Stunde, 24 Stunden, 7 Tage, 30 Tage oder 1 Jahr. Die Datenauflösung basiert auf der Anzahl der Punkte, wobei eine feste Anzahl von Punkten pro Plot verwendet wird. Wenn Sie mit der Maus über einen der Graphen fahren, erscheint eine Linie auf allen Graphen, die einen Moment in der Zeit markiert. Zusammen mit einer Legende für den Graphen erscheinen Metriken für diesen spezifischen Zeitpunkt.

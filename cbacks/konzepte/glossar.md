---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# Glossar

In diesem Glossar werden grundlegende Konzepte hinter cBacks erklärt. So wollen wir ein besseres Verständnis dafür schaffen, wie cBacks funktionieren und was bestimmte Begriffe in der Dokumentation bedeuten.

**Crash-Consistent Backup**

Ein Crash-Consistent Backup ist ein Disk-Image, das den Zustand einer Festplatte genau so speichert, wie er zu einem bestimmten Zeitpunkt war. Dies bedeutet, dass das Backup Daten enthält, die bis zu dem Zeitpunkt der Erstellung des cBacks vorhanden waren. Es garantiert jedoch nicht, dass die Daten in einem konsistenten Zustand sind, falls die Anwendungen zum Zeitpunkt des cBacks nicht ordnungsgemäß geschlossen wurden.

**Disk Image**

Disk Images sind Softwarekopien von physischen Festplatten. Sie speichern die Daten einer physischen Festplatte (z.B. einer Festplatte oder SSD) in einer oder mehreren Dateien. Diese Images können verwendet werden, um eine Festplatte vollständig zu rekonstruieren - inklusive des Betriebssystems, der Anwendungen und der gespeicherten Daten.

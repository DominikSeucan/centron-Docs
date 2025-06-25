---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 12. November 2024
---

# cBacks aktivieren

Um cBacks während der Erstellung einer centron ccloud³ VM zu aktivieren und cBacks für bestehende ccloud³ VMs zu verwalten, können Sie die nachstehnden Anleitungen verwenden. Sie basieren auf einer Anpassung der DigitalOcean-Anweisungen.

cBacks **während der Erstellung einer ccloud³ VM aktivieren**

1. **Über das Control Panel:**
   * Öffnen Sie das Erstellungs-Menü und wählen Sie ccloud³ VMs.
   * Füllen Sie die Felder gemäß dem normalen Erstellungsprozess aus. Im Abschnitt der empfohlenen Optionen klicken Sie auf "cBacks aktivieren".
   * Wählen Sie alle weiteren Optionen und klicken Sie auf "Erstellen".
2. **Über die API:**
   * Wenn Sie die API zum Erstellen einer ccloud³ VM verwenden, können Sie cBacks aktivieren, indem Sie `"`cBacks`": true` zum Request-Body hinzufügen.

cBacks **für eine bestehende ccloud³ VM aktivieren**

1. **Über Automation:**
   * Verwenden Sie einen entsprechenden Befehl in der centron CLI oder senden Sie eine Anfrage an den ccloud³ VM-Aktions-Endpunkt und setzen Sie das Feld `enable_cbacks`  auf `true`.
2. **Über das Control Panel:**
   * Um cBacks für eine bestehende ccloud³ VM zu aktivieren, klicken Sie auf der ccloud³ VM-Seite im Control Panel auf den Namen der ccloud³ VM und dann auf "cBacks" im Menü der ccloud³ VM.
   * Im Abschnitt "cBacks" klicken Sie auf "cBacks aktivieren".

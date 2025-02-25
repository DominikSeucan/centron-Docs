---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Januar 2025
---

# Dateien mit Ordnern organisieren

Das Bedienfeld und viele Drittanbieter-Clients präsentieren Dateien im centron S3 Object Storage mithilfe der Metapher von Ordnern. Dies soll Ihnen dabei helfen, Ihre Assets zu organisieren.

Jedoch sind Objektspeicher tatsächlich nicht hierarchisch; sie sind flache Schlüssel-/Wert-Dateisysteme, was ihnen ihre charakteristische Skalierbarkeit, Redundanz und Zuverlässigkeit verleiht. Das bedeutet auch, dass sich Ordner in einem Objektspeicher anders verhalten als Ordner in verzweigten, verzeichnisbasierten Dateisystemen.

In centron S3 Object Storage existieren Ordner tatsächlich nicht im Backend. Ihre Existenz wird durch die Namen der Objekte im Speicher impliziert. Dies bedeutet, dass Ordner keine Berechtigungen, Metadaten oder Informationen darüber haben können, was sie enthalten.



### Neuen Ordner Erstellen&#x20;

Von der Hauptseite Ihres centron S3 Object Storage aus fügt der Button „Neuer Ordner“ einen neuen Ordner im Verzeichnis hinzu, in dem Sie sich befinden. Gleichzeitig öffnet sich ein Textfeld, in dem Sie den Namen des neuen Ordners festlegen können.

#### Einen neuen Ordner im centron S3 Object Storage erstellen, mit geöffnetem Textfeld für den Namen des Ordners&#x20;

Nachdem Sie den Namen eingegeben haben, drücken Sie die Eingabetaste oder klicken Sie auf das Häkchen, um das Bearbeitungsfeld zu schließen.



### Elemente in einen Ordner verschieben&#x20;

Ordner können sowohl Dateien als auch andere verschachtelte Ordner enthalten. Sie können ein einzelnes Element in einen Ordner verschieben, indem Sie sein Mehr-Menü öffnen und „In Ordner verschieben“ auswählen. Sie können auch mehrere Elemente gleichzeitig verschieben, indem Sie diese auswählen, das Aktionsmenü öffnen und „In Ordner verschieben“ auswählen.



### Das Fenster „Element in Ordner verschieben“&#x20;

Im Modal „In Ordner verschieben“ können Sie einen Zielordner für Ihre Elemente auswählen. Wählen Sie dafür entweder einen vorhandenen Ordner im Speicher aus oder erstellen Sie einen neuen Ordner.

{% hint style="info" %}
Sie können Berechtigungen für alle Dateien in einem Ordner festlegen, derzeit müssen Sie jedoch einen Drittanbieter-Client verwenden, um Berechtigungen rekursiv festzulegen.&#x20;
{% endhint %}

### Dateien im aktuellen Ordner filtern&#x20;

Das Feld „Tippen, um zu filtern ...“ führt einen „Beginnt mit“-Filter für die Dateien und Ordner auf der aktuellen Ebene durch. Dies bedeutet, dass Sie die ersten Buchstaben eines Dateinamens eintippen können und progressiv filtern, was angezeigt wird, anstatt herunterzuscrollen und auf das Laden weiterer Dateien zu warten.

Der Filter beschränkt sich auf die Datei- und Ordnernamen, wie sie auf der aktuellen Ebene angezeigt werden. Die einzige Ausnahme ist, dass das Filtern nach einem vollständigen Dateinamen auf der Root-Ebene des Speichers die Datei in den Ergebnissen anzeigt.



### Einen Ordner löschen&#x20;

Das Löschen eines Ordners wird rekursiv alle Inhalte darin löschen. Sie können Ordner auf die gleiche Weise löschen, wie Sie Dateien löschen: Indem Sie das Mehr-Menü eines einzelnen Ordners öffnen und auf "Löschen" klicken oder indem Sie mehrere Ordner auswählen, das Aktionsmenü öffnen und auf "Löschen" klicken.

**Das Bestätigungsfenster zum Löschen mehrerer Elemente aus dem Aktionsmenü**&#x20;

Wie bei Dateien sind Löschungen endgültig, daher werden Sie um Bestätigung gebeten, bevor der Ordner tatsächlich gelöscht wird.

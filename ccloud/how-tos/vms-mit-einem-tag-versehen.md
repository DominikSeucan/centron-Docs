---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023.
---

# VMs mit einem Tag versehen

Tags sind benutzerdefinierte Labels, die Sie ccloud³ VMs und anderen centron-Ressourcen zuweisen können. Sie ermöglichen es Ihnen, nach ccloud³ VMs zu filtern, ccloud³ VMs automatisch in centron Firewall- oder Load Balancer-Konfigurationen einzubeziehen oder Überwachungsalarmrichtlinien für Gruppen zu erstellen und die centron API zu nutzen, um Aktionen über mehrere ccloud³ VMs mit initiieren.

Die Wahl von Begriffen, die die Funktion einer ccloud³ VM beschreiben, kann Ihnen helfen, ccloud³ VMs mit gemeinsamen Rollen zu finden und zu verwalten. Beispielsweise könnten Sie ccloud³ VMs taggen nach:

* Umgebung, wie Produktion, Staging oder Entwicklung.
* Anwendung, wie Webserver (Apache) oder Datenbankserver (MariaDB).
* Zweck, wie ein Projektname oder ein anderer Schlüsselbegriff, der die Verwendung der ccloud³ VM beschreibt.
* Person, wie der Einzelne oder das Team, das für die Verwaltung der ccloud³ VM verantwortlich ist.

Sie können Tags zu ccloud³ VMs während oder nach der Erstellung hinzufügen.



### Limits

Tags müssen ein einzelnes Wort sein, das nur Buchstaben, Zahlen, Doppelpunkte, Bindestriche und Unterstriche enthält.



### Bekannte Probleme

* Sie können bestehende Tags nicht bearbeiten. Stattdessen erstellen Sie einen neuen Tag, wenden ihn auf die entsprechenden Ressourcen an und löschen den alten.
* Tag-Namen sind hinsichtlich der Groß- und Kleinschreibung stabil, was bedeutet, dass die von Ihnen bei der erstmaligen Erstellung eines Tags verwendete Schreibweise kanonisch ist.
* Wenn Sie mit Tags in der API arbeiten, müssen Sie die kanonische Schreibweise des Tags verwenden. Zum Beispiel wäre die URL, um diesen Tag einer Ressource hinzuzufügen:&#x20;

```
GET /ccloud/servers/{hostname}/tags
```

### Automatisierung des Taggings von ccloud³ VMs

Beim Taggen einer ccloud³ VM über die API müssen Sie zuvor einen Tag erstellt haben.&#x20;



### ccloud³ VMs während der Erstellung taggen

Um Tags beim Erstellen einer neuen ccloud³ VM hinzuzufügen, suchen Sie im Abschnitt "Abschließende Details" der ccloud³ VM-Erstellungsseite nach dem Tags-Feld. Hier können Sie Tags eingeben und mit der LEERTASTE oder ENTER nach jedem Begriff hinzufügen.



### Vorhandene ccloud³ VMs Taggen

Um Tags für vorhandene ccloud³ VMs hinzuzufügen oder zu ändern, verwenden Sie das "Mehr"-Menü der ccloud³ VM und wählen Sie "Tags bearbeiten" oder verwenden Sie den Tags-Link auf der Detailseite der ccloud³ VM.



### Filtern nach Tag

Wenn Sie auf einen Tag im Kontrollpanel klicken, gelangen Sie zur Liste aller Ressourcen mit diesem Tag. Filterlisten sind auf einen einzelnen Tag beschränkt, der oben in der Liste angezeigt wird.

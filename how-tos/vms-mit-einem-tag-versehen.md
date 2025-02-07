---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# VMs mit einem Tag versehen

Tags sind benutzerdefinierte Labels, welche Sie ccloud³ VMs und anderen centron-Ressourcen zuweisen können. Sie ermöglichen es nach getaggten ccloud³ VMs zu filtern und ccloud³ VMs automatisch in centron Firewall- oder Load Balancer-Konfigurationen anhand von Tags einzubeziehen. Ebenfalls wir die Möglichkeit geboten Überwachungsalarmrichtlinien für Gruppen von getaggten ccloud³ VMs zu erstellen und die centron API zu nutzen, um Aktionen über mehrere ccloud³ VMs mit demselben Tag zu initiieren.

Die Wahl von Begriffen, welche die Funktion einer ccloud³ VM beschreiben, kann Ihnen dabei helfen, ccloud³ VMs mit gemeinsamen Rollen zu finden und zu verwalten. Beispielsweise könnten Sie ccloud³ VMs nach Folgendem taggen :

* Umgebung, wie Produktion, Staging oder Entwicklung.
* Anwendung, wie Webserver (Apache) oder Datenbankserver (MariaDB).
* Zweck, wie ein Projektname oder ein anderer Schlüsselbegriff, der die Verwendung der ccloud³ VM beschreibt.
* Person, wie der Einzelne oder das Team, das für die Verwaltung der ccloud³ VM verantwortlich ist.

Sie können Tags zu ccloud³ VMs während oder nach der Erstellung hinzufügen.

#### Grenzen

* Tags müssen ein einzelnes Wort sein, das nur Buchstaben, Zahlen, Doppelpunkte, Bindestriche und Unterstriche enthält.

#### Bekannte Probleme

* Sie können bestehende Tags nicht bearbeiten. Stattdessen erstellen Sie einen neuen Tag, wenden ihn auf die entsprechenden Ressourcen an und löschen den alten.
* Tag-Namen sind hinsichtlich der Groß- und Kleinschreibung stabil, was bedeutet, dass die von Ihnen bei der erstmaligen Erstellung eines Tags verwendete Schreibweise kanonisch ist.
* Getaggte Ressourcen im Kontrollpanel zeigen immer die kanonische Schreibweise an. Zum Beispiel, wenn Sie einen Tag namens PROD erstellen, können Sie Ressourcen im Kontrollpanel mit "prod" taggen. Der Tag wird jedoch weiterhin mit seiner kanonischen Schreibweise PROD angezeigt.
* Wenn Sie mit Tags in der API arbeiten, müssen Sie die kanonische Schreibweise des Tags verwenden. Zum Beispiel wäre die URL, um diesen Tag einer Ressource hinzuzufügen: `https://api.centron.com/v2/tags/PROD/resources` (nicht /v2/tags/prod/resources).

#### Automatisierung des Taggings von ccloud³ VMs

* Beim Taggen einer ccloud³ VM über die API müssen Sie zuvor einen Tag erstellt haben. Bei Verwendung von `doctl` besteht diese Anforderung nicht.

#### ccloud³ VMs Während der Erstellung Taggen

Um Tags beim Erstellen einer neuen ccloud³ VM hinzuzufügen, suchen Sie im Abschnitt "Abschließende Details" der ccloud³ VM-Erstellungsseite nach dem Tags-Feld. Hier können Sie Tags eingeben und mit der LEERTASTE oder ENTER nach jedem Begriff hinzufügen.

#### Vorhandene ccloud³ VMs Taggen

Um Tags für vorhandene ccloud³ VMs hinzuzufügen oder zu ändern, verwenden Sie das "Mehr"-Menü der ccloud³ VM und wählen Sie "Tags bearbeiten" oder verwenden Sie den Tags-Link auf der Detailseite der ccloud³ VM.

#### Filtern nach Tag

Wenn Sie auf einen Tag im Kontrollpanel klicken, gelangen Sie zur Liste aller Ressourcen mit diesem Tag. Filterlisten sind auf einen einzelnen Tag beschränkt, der oben in der Liste angezeigt wird.

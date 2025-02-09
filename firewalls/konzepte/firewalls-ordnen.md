---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Firewalls ordnen

Centron bietet eine zentrale Lösung für die Verwaltung des Netzwerkverkehrs zu Ihren ccloud³ VMs, die konfigurierbar, schnell anzuwenden und automatisierungsfreundlich ist. Allerdings kann die Organisation der Infrastruktur eine Herausforderung darstellen.

Ohne einen Plan könnten Sie am Ende mit einer Vielzahl von Firewalls enden, die wenig Sinn ergeben. Zu komplizierte Planung kann jedoch zu Analyseparalyse führen.

In diesem Artikel werden wir eine anfängliche Strategie zur Organisation Ihrer Cloud-Firewalls vorstellen, die deren Nutzung und Wartung vereinfacht sowie die Beziehungen innerhalb Ihrer Infrastruktur dokumentiert.

**Aufteilung nach Rolle**&#x20;

Zum Start bauen wir unsere Cloud-Firewalls basierend auf den Rollen ihrer Regeln. Wenn wir beispielsweise eine monolithische Webanwendung haben, wie eine ccloud³ VM namens "Webseite", die eine PHP-Anwendung mit einer lokalen MySQL-Datenbank ausführt, müssen zwei unterschiedliche Rollen erfüllt werden:

1. **Webserver**: Diese öffentlich zugängliche Rolle ist der Hauptzweck der VM, welche Webseiten für die Öffentlichkeit bereitstellt.
2. **Management**: Die Managementrolle ermöglicht privilegierten Zugang für Administratoren zur Wartung des Servers und zum Deployment der Anwendung.

Für kleine Bereitstellungen könnte eine einzelne Cloud-Firewall mit Regeln für beide Aufgaben funktionieren. Wenn wir jedoch planen, die App in Zukunft zu skalieren, können wir diese Anliegen jetzt trennen und zwei verschiedene Firewalls erstellen:

* **webserver-fw**: Öffnet TCP-Ports 80 (für unverschlüsselten Verkehr) und 443 (für SSL) für alle Quellen.
* **management-fw**: Öffnet TCP-Port 22 (SSH) für alle Quellen. Wenn wir den Zugang auf bestimmte Standorte wie einen IP-Bereich in unserem Büro beschränken möchten, würden wir das bei den Quellen dieser Regel hinzufügen.

Wenn die Anwendung wächst, könnten wir Arbeitslasten auf mehrere Server aufteilen. Es ist üblich, Webserver und Datenbank zu trennen und jeden auf einer eigenen ccloud³ VM zu betreiben. Wenn wir eine solche Änderung vornehmen, können wir unsere Firewall-Strategie wie folgt anpassen:

* **management-fw** beibehalten, ohne Änderungen. SSH wird weiterhin für administrative Aufgaben benötigt.
* **webserver-fw** beibehalten, da ihre Funktion gleich bleibt.
* Eine neue Cloud-Firewall namens **database-fw** erstellen, mit einer Regel, die TCP-Port 3306 — den Standard von MySQL — für die Quelle ccloud³ VM "Webseite" öffnet.
* **database-fw** und **management-fw** auf die neue ccloud³ VM anwenden. Administratoren können ihre Arbeit verrichten, und nur der Webserver hat Zugang zum Datenbankport.

Unsere anfängliche Organisation ermöglicht es uns, Änderungen an den zuvor erstellten Cloud-Firewalls zu vermeiden, eine von ihnen wiederzuverwenden, den Dienst auf der neuen Datenbank-VM anzugeben und jedem Server nur den streng notwendigen Zugang zu gewähren.

**Verwendung von Tags**&#x20;

Bisher haben wir über eine kleine Anwendung gesprochen, die von ein oder zwei ccloud³ VMs bedient werden kann, und wir haben die Firewalls unter Verwendung der VM-Namen angewendet. Wenn unser Traffic wächst und wir uns auf das Skalieren vorbereiten, kann die Verwendung von VM-Namen unhandlich werden.

Wir könnten unsere Zwei-Server-Architektur beibehalten und die Server vertikal aufrüsten, indem wir mehr Speicher oder Rechenleistung hinzufügen, damit sie mit den Anfragen Schritt halten können. Dies ändert jedoch nicht die Tatsache, dass jeder einzelne ein potenzieller Single Point of Failure ist. Da wir in der Cloud arbeiten, ist es wahrscheinlicher, dass wir horizontal skalieren, indem wir den Traffic auf mehrere redundante Server verteilen. In diesem Stadium müssen wir beginnen, Werkzeuge und Praktiken zu verwenden, die es uns ermöglichen, VMs als austauschbare Ressourcen zu behandeln. Diese Strategieverschiebung ist in Cloud-Kreisen als "Pets vs. Cattle" bekannt und geht Hand in Hand mit Konfigurationsmanagement-Tools wie Ansible, Chef und Puppet.

Wenn wir anfangen, unsere ccloud³ VMs als Gruppen von redundanten, austauschbaren Ressourcen zu denken, benötigen wir gruppenbasierte Methoden, um mit ihnen zu arbeiten. Centron erleichtert das gruppenbasierte Management mithilfe von Tags, das sind Textlabels, die wir an VMs anbringen, um sie zu klassifizieren. Sobald wir VMs getaggt haben, verwenden wir diese Tags, um Beziehungen zwischen anderen Centron-Ressourcen wie Load Balancern und Cloud-Firewalls herzustellen.

In unserem Fall können wir zwei Tags erstellen, webserver und datenbank, und das entsprechende Tag jeder ccloud³ VM hinzufügen. Wenn wir dies tun, benennen wir auch die VMs in website-01 und datenbank-01 um und kennzeichnen sie explizit als austauschbare Teile unserer Bereitstellung. Dann ändern wir unsere Cloud-Firewalls wie folgt:

* **management-fw**: Fügen Sie sowohl das webserver- als auch das datenbank-Tag hinzu und entfernen Sie die Verknüpfung mit spezifischen VM-Namen.
* **webserver-fw**: Fügen Sie das webserver-Tag hinzu und entfernen Sie die ccloud³ VM website-01.
* **database-fw**: Fügen Sie das datenbank-Tag hinzu und entfernen Sie die ccloud³ VM datenbank-01. Ändern Sie die Quelle in der TCP 3306-Regel vom benannten VM-Namen auf das Tag webserver.

Mit diesem Übergang zu Tags werden die Regeln jeder Cloud-Firewall auf jede VM angewendet, die mit diesen Tags markiert ist. Es spielt keine Rolle, wie viele VMs es gibt. Wenn wir ein paar neue Webserver-VMs wie website-02 und website-03 starten, würden sie automatisch die Regeln von webserver-fw erhalten und Zugang zu jeder VM bekommen, auf die die database-fw angewendet wird. Dies ermöglicht es uns, uns auf das Skalieren der Anwendung nach oben oder unten zu konzentrieren, während die Sicherheitskontrollen von Cloud-Firewalls gehandhabt werden.

Der oben beschriebene Prozess könnte auf komplexere Anwendungen ausgeweitet werden. Wenn wir beispielsweise ein Subsystem für das Anstellen von Anfragen oder eine Gruppe von Servern, die als Prozessarbeiter dienen, hätten, könnten wir sie als queue und workers taggen, die spezifischen Firewall-Regeln darauf anwenden und gemeinsame Aspekte wie management-fw teilen.

Die Verwendung von Tags zur Organisation und Dokumentation unserer Infrastruktur klärt die Beziehungen zwischen verschiedenen ccloud³ VMs und erleichtert deren Verwaltung im Bulk. Wir sind nicht auf ein einzelnes Tag pro VM beschränkt, sodass wir weitere Tags anwenden können, um Automatisierungs- oder Dokumentationsprozesse zu unterstützen.

**Zur Benennung**&#x20;

Wir haben "webserver" und "management" als generische Beispiele für Cloud-Firewall-Namen verwendet. Sie sollten Namen verwenden, die für Sie und den spezifischen Kontext Ihres Teams sinnvoll sind. Vielleicht wäre "deployment" angemessener als "management". Wenn das der Fall ist, verwenden Sie "deployment".

Wir fügen auch -fw am Ende der Firewall-Namen hinzu, um Ressourcen in Situationen zu identifizieren, in denen es keine Benutzeroberfläche gibt und Elemente zu unterscheiden. Nehmen wir an, Sie haben eine ccloud³ VM namens "webserver" mit einem webserver-Tag und eine Firewall namens "webserver". Wenn Sie die Ausgabe eines Befehlszeilentools wie doctl analysieren, welches ist welches? Im Kontrollpanel-UI ist es normalerweise angegeben, aber das ist möglicherweise nicht der Fall in anderen Szenarien, daher kann eine Benennungsstrategie zur Unterscheidung Klarheit schaffen und das Skripting vereinfachen.

\
\

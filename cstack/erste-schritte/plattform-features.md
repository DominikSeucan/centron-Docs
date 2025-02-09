---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Plattform Features

### SSH Key Pairs

Zusätzlich zur Authentifizierung mit Benutzername und Passwort unterstützt cStack die Verwendung von SSH-Schlüsseln zur Anmeldung bei der Cloud-Infrastruktur für zusätzliche Sicherheit.

Da jeder Cloud-Benutzer seinen eigenen SSH-Schlüssel hat, kann sich ein Cloud-Benutzer nicht bei den Instanzen eines anderen Cloud-Benutzers anmelden, es sei denn, sie teilen ihre SSH-Schlüsseldateien. Mit einem einzigen SSH-Schlüsselpaar können Sie mehrere Instances verwalten.&#x20;

### Accounts

Ein Account steht typischerweise für einen Kunden, in einem Account können mehrere Benutzer existieren.&#x20;

### Domains

Accounts werden in Domains gruppiert. Domains beinhalten somit einen oder mehrere Accounts, welche eine logische Beziehung zueinander inkl. unterschiedlicher Berechtigungen über die Domain und dessen Subdomains haben.

Neben dem Root Administrator einer Hauptdomain können zwei unterschiedliche Typen von Accounts angelegt werden: Domain Administrator und Benutzer

### Benutzer

Benutzer sind wie Aliases im Account. Die Benutzer sind nicht voneinander isoliert, lediglich von Benutzern in anderen Accounts.&#x20;

Der Benutzername ist in einer Domäne für alle Konten in dieser Domäne eindeutig. Derselbe Benutzername kann in anderen Domänen, einschließlich Unterdomänen, existieren. Domänennamen können sich nur wiederholen, wenn der vollständige Pfadname von root eindeutig ist. Sie können z. B. root/d1 sowie root/foo/d1 und root/sales/d1 erstellen.

Administratoren sind Konten mit besonderen Rechten im System. Es kann mehrere Administratoren im System geben. Administratoren können andere Administratoren erstellen oder löschen und das Passwort für jeden Benutzer im System ändern.

### Projects

Projekte werden verwendet, um Menschen und Ressourcen zu organisieren. cStack-Benutzer innerhalb einer einzelnen Domain können sich in Projektteams gruppieren, damit sie zusammenarbeiten und virtuelle Ressourcen wie Instances, Snapshots, Vorlagen, Datenfestplatten und IP-Adressen gemeinsam nutzen können. CloudStack verfolgt die Ressourcennutzung sowohl pro Projekt als auch pro Benutzer, so dass die Nutzung entweder einem Benutzerkonto oder einem Projekt in Rechnung gestellt werden kann.

### Events

Ein Ereignis ist im Wesentlichen eine signifikante oder bedeutsame Änderung des Zustands sowohl virtueller als auch physischer Ressourcen, die mit einer Cloud-Umgebung verbunden sind. Ereignisse werden von Überwachungssystemen, Nutzungs- und Abrechnungssystemen oder anderen ereignisgesteuerten Workflow-Systemen verwendet, um ein Muster zu erkennen und die richtige Geschäftsentscheidung zu treffen. In cStack kann ein Ereignis eine Zustandsänderung virtueller oder physischer Ressourcen, eine von einem Benutzer durchgeführte Aktion (Aktionsereignisse) oder richtlinienbasierte Ereignisse (Warnungen) sein.

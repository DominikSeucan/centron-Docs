# Premium Full Managing - Leistungsschein

## 1 Service Name&#x20;

centron Premium Full Managing und Premium Managed Services. Auftragnehmer nachfolgend centron genannt, Auftraggeber nachfolgend Auftraggeber genannt.&#x20;

## 2 High Level Service Description&#x20;

Premium Full Managing bezieht sich ausschließlich auf die von centron selbst betriebenen Systeme und Hardware. Premium Full Managing ist untergliedert in die Basisleistungen Monitoring, Backup und Update Management (Premium Full Managing) sowie optional buchbares Stundenkontingent (Premium Managed Services). Premium Full Managing kann nur in Kombination mit einem bei centron betriebenem System gebucht werden.&#x20;

## 3 Support&#x20;

Alle angebotenen Managed Server beinhalten kostenlosen schriftlichen sowie telefonischen Support zu den angegebenen Supportzeiten. Schriftliche Supportanfragen durch den Auftraggeber werden über ein internes Ticketsystem bearbeitet. Der Support nimmt Meldungen per Telefon an und leitet diese an die richtige Ansprechperson weiter.&#x20;

Der Support ist 24/7/365 erreichbar, dokumentiert den Lösungsweg und geht aktiv auf den Auftraggeber bei Statusinformationen und Rückmeldungen zu. Das Premium Full Managing setzt sich aus den Bestandteilen Monitoring, Patches und Backup zusammen. Inklusive sind das Überwachen der Serverhardware, des Serverbetriebssystems und des Rechenzentrums am Standort Hallstadt, Deutschland. Allgemein sind Supportaufträge durch den Auftraggeber im Pauschalpreis des Produkts und den inkludierten Managing Stunden enthalten.&#x20;

Spezielle Supportanfragen, welche nicht in den Serviceleistungen von centron inkludiert sind, werden für die nachfolgend aufgeführten Preise während der Geschäftszeiten von 09:00 Uhr bis 18:00 Uhr in einem 15 Minuten Takt berechnet. Außerhalb der Geschäftszeiten, von 18:00 Uhr bis 09:00 Uhr findet die Abrechnung für jede angebrochene Stunde statt. Diese Anfragen werden nach den im Angebot enthaltenen Preisen verrechnet.&#x20;

| Zeit                           | Preis    | Intervall  |
| ------------------------------ | -------- | ---------- |
| 09:00 Uhr - 18:00 Uhr          | 40,00 €  | 15 Minuten |
| 18:00 Uhr - 09:00 Uhr          | 240,00 € | 1 Stunde   |
| Samstags, Sonntags & Feiertags | 240,00 € | 1 Stunde   |

| Laufzeit    | Preis   | Intervall  |
| ----------- | ------- | ---------- |
| Pay-per-Use | 40,00 € | 15 Minuten |
| 12 Monate   | 36,00 € | 15 Minuten |
| 24 Monate   | 32,00 € | 15 Minuten |
| 36 Monate   | 28,00 € | 15 Minuten |

## 4 Premium Full Managing&#x20;

Die Managing Basisleistungen setzen sich zusammen aus Backup, Monitoring und Patch Management. Im Folgenden werden die einzelnen Bestandteile sowie das Portfolio an Software, das unter die Managing Basisleistungen fällt, aufgeführt und deren individuellen Leistungen genauer definiert.&#x20;

### 4.1 Monitoring&#x20;

Die stetig wachsende Komplexität von IT-Systemen und Abhängigkeiten macht es umso wichtiger, diese ordnungsgemäß zu dokumentieren und zu überwachen. Ein modernes Monitoring-System unterstützt den täglichen Betrieb der Infrastruktur und hilft, die Systemverfügbarkeit zu erhöhen.&#x20;

#### 4.1.1 Leistungsbeschreibung&#x20;

Monitoring als Teil der Managing Basisleistung ermöglicht ebendies: Probleme frühzeitig erkennen und beheben, bevor sie zu Ausfällen führen. Der Kunde beauftragt centron mit der Erbringung von Überwachungsdiensten. Dieser Teil der „Leistungsbeschreibung“ erläutert die Arten von Überwachung, Alarmierung und Reporting bezüglich der während des Monitorings des überwachten Systems gewonnenen Erkenntnisse. centron trägt die Verantwortung für den Betrieb der Bereitstellung des Dienstes und der Sicherheitsrichtlinien des Monitorings als Bestandteil der Managing Basisleistungen. Der Kunde trägt weiterhin die Verantwortung für den Betrieb der Server und der darauf installierten Monitoring Agenten.&#x20;

#### 4.1.2 Feststellen des Soll – Zustandes&#x20;

Folgende Checks werden standardmäßig aktiviert:&#x20;

**4.1.2.1 system:ipmi:health**&#x20;

Überprüft IPMI Detailausgaben wie z.B. Temperaturen, Spannungen oder Lüfterdrehzahlen&#x20;

**4.1.2.2 system:ipmi:website**&#x20;

Überprüft die Erreichbarkeit des IPMI Devices via Webbrowser&#x20;

**4.1.2.3 system:nsc:certifcate**&#x20;

Prüft auf aktuelles Zertifikat&#x20;

**4.1.2.4 system:nsc:cpu**&#x20;

Prüft, ob CPU Last innerhalb normaler Parameter liegt&#x20;

**4.1.2.5 system:nsc:disk**&#x20;

Prüft auf freien Speicherplatz der Disks&#x20;

**4.1.2.6 system:nsc:mem**&#x20;

Prüft ob Speicherauslastung (RAM) innerhalb der vorgegebenen Parameter liegt&#x20;

**4.1.2.7 system:nsc:ntp**&#x20;

Prüft ob die lokale Zeit der Maschine innerhalb der Threshold Grenzen gegenüber den centron Zeitservern liegt&#x20;

**4.1.2.8 system:nsc:raid:adaptec**&#x20;

Prüft den Status von einem oder mehreren RAID-Controllern&#x20;

**4.1.2.9 system:nsc:scheduledtask**&#x20;

Prüft ob alle Scheduled Tasks erfolgreich bzw. fehlerfrei durchgelaufen sind&#x20;

**4.1.2.10 system:nsc:service**&#x20;

Prüft ob alle auf Automatik stehenden Dienste laufen&#x20;

**4.1.2.11 system:nsc:uptime**&#x20;

Prüft ob System vor Kurzem gestartet wurde&#x20;

**4.1.2.12 system:ssh:certifcate**&#x20;

Prüft auf aktuelles Zertifikat&#x20;

**4.1.2.13 system:ssh:cpu**&#x20;

Prüft, ob CPU Last innerhalb normaler Parameter liegt&#x20;

**4.1.2.14 system:ssh:disk**&#x20;

Prüft auf freien Speicherplatz der Disks&#x20;

**4.1.2.15 system:ssh:ip:sockets**&#x20;

Prüft die Anzahl der aktiven Verbindungen am Server (maximale IP-Sockets 65535)&#x20;

**4.1.2.16 system:ssh:iptables**&#x20;

Prüft ob die Firewalleinstellungen den centron Normen entsprechen&#x20;

**4.1.2.17 system:ssh:memory**&#x20;

Prüft aktuelle Speicherauslastung&#x20;

**4.1.2.18 system:ssh:ntp**&#x20;

Prüft ob die lokale Zeit der Maschine innerhalb der Threshold Grenzen gegenüber den centron Zeitservern liegt&#x20;

**4.1.2.19 system:ssh:procs\_zombie**&#x20;

Prüft die Anzahl der verstorbenen (Zombie) Prozesse.&#x20;

**4.1.2.20 system:ssh:raid:megasas**&#x20;

Prüft den Status eines oder mehrerer RAID Controller.&#x20;

**4.1.2.21 system:ssh:syslog**&#x20;

Prüft ob der SyslogDaemon arbeitet.&#x20;

**4.1.2.22 service:dns:alias**&#x20;

Prüft die gängigen DNS-Einträge (Reverse, Forward, Double)&#x20;

**4.1.2.23 service:ftp**&#x20;

Prüft ob FTP auf Port 21 reagiert.&#x20;

**4.1.2.24 service:http**&#x20;

Prüft ob HTTP auf Port 80 antwortet&#x20;

**4.1.2.25 service:imap**&#x20;

Prüft ob IMAP auf Port 143 antwortet&#x20;

**4.1.2.26 service:mssql**&#x20;

Prüft ob mssql auf Port 1433 reagiert.&#x20;

**4.1.2.27 service:nrpe:hyperv-replication**&#x20;

Prüft den Status der HyperV-Replikation&#x20;

**4.1.2.28 service:pop**&#x20;

Prüft ob POP3 auf Port 110 antwortet&#x20;

**4.1.2.29 service:smtp**&#x20;

Prüft ob SMTP auf Port 25 antwortet&#x20;

**4.1.2.30 service:sshd**&#x20;

Prüft ob SSHD auf Port 22 antwortet&#x20;

**4.1.2.31 service:ssh:fail2ban\_alive**&#x20;

Prüft ob fail2ban Dienst läuft&#x20;

**4.1.2.32 service:ssh:logfile-check**&#x20;

Prüft, ob ein oder mehrere Logfiles > als 1500MB verbraucht.&#x20;

**4.1.2.33 service:ssh:ssh\_root\_login**&#x20;

Prüft ob in /etc/ssh/sshd\_config ob 'PermitRootLogin' auf 'without-password' (Key) gesetzt ist.&#x20;

**4.1.2.34 service:mail:delivery:send**&#x20;

1. Nagios sendet Mail über den Exchange an den ctrmail-bbg-2 zum Postfach nagioscheck@ctrmail-bbg-2
2. Nagios verbindet sich per IMAP auf den ctrmail-bbg-2
3. Nagios prüft, ob Mail vorhanden ist und löscht diese&#x20;

**4.1.2.35 service:mail:delivery:receive**&#x20;

• Nagios sendet Mail über ctrmail-bbg-2 and den Exchange zum Postfach nagioscheck@&#x20;

• Nagios verbindet sich per IMAP auf den Exchange&#x20;

• Nagios prüft, ob Mail vorhanden ist und löscht diese&#x20;

**4.1.2.36 service:ssh:controlmaster Beschreibung**&#x20;

• Check prüft, ob eine SSH Verbindung vom Nagios zum Zielhost besteht&#x20;

• Wenn verschiedene Checks in den Timeout laufen, obwohl die Dienste usw. richtig laufen, kann ein Reschedule des controlmaster-Checks durchgeführt werden, damit die SSH Verbindung neu aufgebaut wird → kann 5-10 Minuten dauern&#x20;

Der Kunde hat die Möglichkeit als Bestandteil des Pflichtenheftes zu wählen, welche Checks aktiviert resp. deaktiviert werden sollen. centron überwacht somit:&#x20;

* Erreichbarkeit&#x20;
* Grundlegende Server Metriken&#x20;
* Dienste&#x20;
* Applikationen&#x20;

Zusätzlich enthalten sind:&#x20;

* E-Mail und SMS Benachrichtigung&#x20;
* Zugriff auf Webinterface&#x20;

Vereinzelt sind erweiterte Überwachungen möglich. Die Umsetzung dieser Erfolgt zu den in Kapitel 3 beschriebenen Managing Stundensätzen. Bei existierender Haftungsfreistellung, insofern Neustarts der Systeme durch den Kunden durchgeführt werden, sind diese centron zwingend zu melden. Findet eine Benachrichtigung centrons durch den Kunden nicht statt, fallen Gebühren in Höhe der entsprechenden Managing Stundensätze aus Kapitel 3 an.&#x20;

centron überwacht zudem als Teil des Premium Full Managings die Überwachung der einzelnen Hypervisoren resp. VMs. Sobald eine Auslastung eine Schwelle von 80% überschreitet, wird der jeweilige Bezugswert (vCPU, RAM, Speicher, Backupspeicher) automatisch kostenpflichtig um 10% erweitert. Der Preis der Erweiterung wird hierbei ebenfalls anteilig durch den jeweiligen Referenzwert kalkuliert.&#x20;

Der Kunde wird 48 Stunden vor der automatischen Erweiterung von centron benachrichtigt. Eine Bestätigung der Erweiterung sowie keine Rückmeldung führen zu dem vorherig beschriebenen Vorgang. Der Kunde hat ebenfalls das Recht, diese Erweiterung abzulehnen. Insofern der Kunde die automatische Erweiterung ablehnt, weißt centron ihn darauf hin, dass centron nicht mehr bei möglichen Schäden haftet, SLAs nicht mehr gelten und der problemlose Betrieb der Systeme nicht mehr gewährleistet werden kann.&#x20;

Die Möglichkeit, abgeschlossene Erweiterungen rückgängig zu machen, existiert nur in Bezug auf die Referenzwerte vCPU und RAM. Eine abgeschlossene Speichererweiterung ist von einer nachträglichen Reduktion ausgeschlossen.&#x20;

#### 4.1.3 Herstellung der Funktionalität&#x20;

Seitens des Kunden sind folgende Beistellungs- und Mitwirkungspflichten zu erfüllen:&#x20;

* Der Kunde stellt die notwendigen Informationen aus dem vorherigen Kapitel dieser Leistungsbeschreibung zur Verfügung. Bei Bedarf unterstützt centron bei dieser Aufgabe.&#x20;
* Der Kunde stellt centron eine E-Mail-Adresse zum Empfang von Benachrichtigungen über das Monitoring System zur Verfügung.&#x20;
* Bei Bedarf werden dem Kunden durch centron Zugangsdaten für das Monitoring als Teil der Managing Basisleistungen zur Einrichtung der zu überwachenden Systeme und Parameter bereitgestellt.&#x20;
* Maßnahmen bei Alarmen werden proaktiv durch centron ausgeführt.&#x20;

Die korrekte Grundfunktionalität und Funktionsweise der eingesetzten Tools wird durch centron mit den folgenden Tests bestätigt:&#x20;

* Testen der Benachrichtigungen per E-Mail&#x20;
* Anlegen eines Hosts welcher abgeschaltet werden kann&#x20;
* Herunterfahren des Hosts und Benachrichtigungen zu prüfen&#x20;
* Starten des Hosts um Benachrichtigungen zu prüfen&#x20;

Der Test gilt als erfolgreich, wenn allen im Monitoring hinterlegten Benutzern zu jedem Vorgang eine E-Mail zugestellt wurde. Der Kunde bestätigt innerhalb von zehn Werktagen nach Erhalt der Bestandsberichtes den erfolgreichen Test bzw. einen notwendigen Korrekturbedarf per E-Mail an centron. Meldet der Kunde keinen weiteren Korrekturbedarf, der einen erneuten Durchlauf notwendig macht, gilt die Einrichtung und Inbetriebnahme des Monitorings als erfolgreich abgeschlossen und geht in den Regelbetrieb über.&#x20;

#### 4.1.4 Leistungserbringung&#x20;

Monitoring als Teil des Premium Full Managings beinhaltet eine 24/7/365 Überwachung des jeweiligen Systems. Ein Ausfall des Systems wird bei gebuchtem Premium Full Managing im Normalfall kostenlos bearbeitet. Dies trägt nicht, falls seitens centron identifiziert werden kann, dass der Ausfall durch Handlungen des Kunden auf dem System verursacht wurden.&#x20;

Außerhalb der Supportzeiten besteht die Option, bei Notfällen den Bereitschaftsdient zu den in Kapitel 3 beschrieben Preisen via Notfallanfrage zu kontaktieren. Die Reaktionszeiten auf einen Systemausfall richten sich nach den in den SLAs definierten Variablen. Eine Ursachenforschung tritt erst dann ein, sobald das betroffene System und somit der jeweilige Notfall behoben ist. Alle Premium Full Managing sowie Premium Managed Services Kunden erhalten die Kontaktdaten des Notfalldienstes.&#x20;

Ein Notfall definiert sich hierbei als Systemausfall. Spezielle Serverklassen sind in den jeweiligen SLAs definiert. centron überwacht keine Software, die nicht im Portfolio aufgelistet ist. Diese ist somit vom Monitoring ausgeschlossen. Um die Sicherheit und Stabilität des Managed Servers zu gewährleisten, erfolgt eine Prozessüberwachung, die bei übermäßiger Laufzeit und/oder RAM-Ausnutzung den entsprechenden Prozess beendet.&#x20;

Ein Anspruch auf solche Änderungen besteht nicht. Wird der stabile Betrieb der Server oder des Netzwerks beeinflusst, behält sich centron das Recht vor, diese Ausnahmeregeln entsprechend zu korrigieren bzw. zu widerrufen. Die Tätigkeiten und Leistungsmomente bilden sich wie folgt:&#x20;

* Bereitstellung der Monitoring Infrastruktur&#x20;
* Backup des Monitoring Managements&#x20;
* Benachrichtigung per E-Mail • Telefon und E-Mail Support
* Prüfung der Konfigurationsparameter&#x20;
* Proaktive Reaktion bei Alarmen durch centron&#x20;
* Proaktiver 24/7 Support&#x20;
* Kostenpflichtige einmalige Einrichtung&#x20;

### 4.2 Backup&#x20;

centron überwacht und prüft die Datensicherung 24/7/365. Bei gebuchtem Premium Full Managing werden Störungen im Datensicherungsablauf beseitigt und Updates sowie Upgrades der Datensicherungslösungen durchgeführt. centron sichert die einzelnen Datenbankbereiche sowie die Datenbank-Archivlogs.&#x20;

#### 4.2.1 Leistungsbeschreibung&#x20;

centron überlässt dem Kunden mit dem Backup als Teil der Managing Basisleistungen ein Datensicherungssystem über das Internet. Mit dem Backup als Teil der Managing Basisleistungen ermöglicht centron dem Kunden die Sicherung der in seinen Systemen vorhandenen Daten auf internen Backup Servern. centron trägt die Verantwortung für den Betrieb der Bereitstellung der Dienste und die Einhaltung der Sicherheitsrichtlinien des Backups als Teil der Managing Basisleistungen.&#x20;

#### 4.2.2 Feststellen des Soll-Zustandes&#x20;

centron stell dem Kunden zum Abspeichern seines Backup Volumens Speicherplatz auf selbst betriebenen Backup Servern zur Verfügung. Im Rahmen der Pflichtenheftbesprechung werden die Partitionen, das Sicherungsintervall sowie die Vorhaltezeit bestimmt.&#x20;

#### 4.2.3 Herstellen der Funktionalität&#x20;

Seitens des Kunden sind folgende Beistellungs- und Mitwirkungspflichten zu erfüllen:&#x20;

* Der Kunde stellt die notwendigen Informationen während der Pflichtenheftbesprechung zur Verfügung. Bei Bedarf übernimmt centron diese Aufgabe in Form einer kostenlosen Beratungsdienstleistung.&#x20;
* Der Kunde stellt für den Empfang der Backup-Protokolle sowie z.B. Informationen zur Erhöhung bzw. Reduzierung der zu sichernden Systeme und Datenmengen eine gültige E-Mail Adresse seitens des Hauptansprechpartners und dessen Stellvertretung zur Verfügung.&#x20;
* Der Kunde verpflichtet sich dazu, keinen Virenscanner, der nicht von centron bereitgestellt wird, auf seinen Systemen zu installieren. centron prüft die Datensicherung und führt eine Qualitätskontrolle nach der Einrichtung mittels Checksumme durch. Änderungen und Erweiterungen können zu einer kurzfristigen Nichtverfügbarkeit des Systems bzw. zu einem Neustart des Systems führen. Diese geplante Ausfallzeit ist von der Verfügbarkeitsberechnung ausgenommen und wird mit Einverständnis des Kunden primär in den fest definierten Wartungsfenstern durchgeführt.&#x20;

#### 4.2.4 Leistungserbringung&#x20;

Bei gebuchtem Premium Full Managing wird der gesamte Datenbestand täglich auf dedizierte Backup Server gesichert. Die Standarddauer, für die die Datensätze gesichert bleiben, beträgt vier Wochen. Dies bedeutet eine monatliche Vollsicherung des Systems, auf der wöchentliche und tägliche Sicherungen aufbauen.&#x20;

Diese Sicherungskette wird solange vorgehalten, bis Ihr Ablaufdatum (EOL = End Of Life) erreicht ist. Das Zurückspielen des Backups (Restore) ist möglich. Die Widerherstellung der gesicherten Dateien beinhaltet den gesamten Sicherungszustand des Systems. Ein Restore einzelner Dateien oder Gegenstände ist möglich. Diese Abweichungen werden zu den Managing Stundensätzen berechnet.&#x20;

Enthalten im Backup als Teil der Managing Basisleistungen ist:&#x20;

* Tägliche Backups (22:00 – 04:00 Uhr)&#x20;
* Standardvorhaltezeit 28 Tage, bei Bedarf auch 14 oder 7 Tage möglich&#x20;
* G – V – S Generationsprinzip&#x20;
* Überwachung des Backupstatus&#x20;
* Generelles Backup der VM/Hardware Server&#x20;
* Dump von MySQL/MSSQL Datenbanken&#x20;
* Dump von Exchange Datenbanken&#x20;
* Automatische Restore Tests von ausgewählten Dateien mit Prüfung der Checksum&#x20;
* Das Durchführen von Restores durch fehlerhafte Updates durch Software von Drittherstellern&#x20;

Nicht im Preis enthalten sind&#x20;

* alternative Sicherungszyklen&#x20;
* die Durchführung von Test-Restores&#x20;
* das Durchführen von Restores&#x20;
* Manuelle Überprüfung der Datenkonsistenz oder Korrektheit der Daten in der Sicherung&#x20;
* Beseitigung von Backupproblemen ausgelöst durch Kundenänderungen oder Kundenanwendungen&#x20;
* Keine Garantie der vom Kunden selbst nachträglich installierten Datenbanken auf Funktionsfähigkeit&#x20;
* Individuelle Anpassungen und Konzepte&#x20;

### 4.3 Patch Management&#x20;

Aktualisierungen („Patches“) dienen zum Schließen von Sicherheitslücken, der Korrektur von Fehlern und Sicherstellung der Betriebsbereitschaft der betroffenen Software. „Patches“ bestehen aus Software, die die vorhandene Software ändert oder neue Software beinhaltet.&#x20;

#### 4.3.1 Leistungsbeschreibung&#x20;

centron installiert automatisch an einem regelmäßigen Termin (im Folgenden „Patch Day“ genannt) die dafür vom Kunden festgelegten Server-Systeme mit den Kunden hierfür freigegebenen Betriebssystemen und Standardanwendungen. centron trägt die Betriebsverantwortung der Dienstbereitstellung, sowie für die Durchführung der Patches. Der Kunden trägt weiterhin die Betriebsverantwortung für die Server, sowie der darauf installierten „Patch Management“-Software.&#x20;

centron übernimmt ausschließlich das Patch Management für Betriebssysteme. Dist- und Inplaceupgrades sind ausgeschlossen. Das Patch Management für Hardware Server bezieht sich hierbei auf Treiber, Firmware und weitere damit verbundene Bestandteile. Es besteht die Möglichkeit, alternative Termine für Notfallpatches zu organisieren. Ein Patch ist ein ein Notfallpatch sobald sicherheits- oder systemrelevante Aspekte des Systems betroffen sind.&#x20;

#### 4.3.2 Feststellen des Soll-Zustandes

Im Rahmen der Pflichtenheftbesprechung werden, falls gewünscht, alternative Zeitfenster sowie die Umsetzung des Update Managements als Teil der Managing Basisleistung detailliert erläutert und abgestimmt.&#x20;

#### 4.3.3 Herstellung der Funktionalität&#x20;

Der Zeitpunkt für Updates der jeweiligen Betriebssysteme lässt sich innerhalb eines Zeitraums von vier Wochen frei wählen. Zusätzlich besteht die Möglichkeit, Updates für Betriebssysteme vollständig zu deaktivieren. Diese Optionen sind für Updates von Applikationen nicht verfügbar. Im Rahmen der Pflichtenheftbesprechung wird die entsprechende Software, insofern nicht im Software-Portfolio befindend, auf ihre Passform für das Update-Management geprüft.&#x20;

#### 4.3.4 Leistungserbringung&#x20;

Updates der Systeme finden einmal im Monat im Zeitraum von 22:00 Uhr bis 04:00 Uhr statt. Das exakte Datum wird von centron frühzeitig bekannt gegeben. Die Updates für die einzelnen Betriebssysteme werden automatisch durchgeführt, wohingegen einzelne Applikationen händisch geupdatet werden. Insofern der Kunde ein anderes Zeitfenster wählt, ist die Funktionsfähigkeit der Server in dieser Zeit nur eingeschränkt verfügbar.&#x20;

Backup und weitere Wartungsdienste müssen von dieser Zeit ausgeschlossen werden. centron installiert automatisch an einem vom Kunden genehmigten regelmäßigen Termin (im Folgenden „Patch Day“ genannt) die dafür vom Kunden festgelegten Server-Systeme mit den vom Kunden hierfür freigegebenen Betriebssystemen und Standardanwendungen, die sich im Software-Portfolio befinden. Die Einrichtung der jeweiligen Systeme stellt einen separaten Teil des Produktes dar. Insofern die Zeit der Einrichtung die der jeweiligen Einschätzung überschreitet, wird die zusätzliche Zeit im Falle von gebuchtem Managing Stundenkontingent anteilig abgezogen. Falls kein zusätzliches Managing Stundenkontingent erworben wurde, wird die zusätzliche&#x20;

Einrichtungszeit anteilig berechnet. Dem Kunden ist bewusst, dass Update Management als Teil des Managing Baukastens Aktualisierungen und Veränderungen an der installierten Software vornimmt, um die Sicherheit zu erhöhen. Bei diesen Veränderungen kann es zu Problemen kommen, die die Lauffähigkeit des Systems negativ beeinflussen. Die Leistungen von centron besteht in der Installation der „Patches“ aber grundsätzlich nicht in der Überprüfung der Funktionsfähigkeit der Software. Deshalb ist es sehr wichtig, dass der Kunde selbst die Verfügbarkeit der betroffenen Systeme und Daten sicherstellt. Eine regelmäßige Überprüfung der erfolgreichen Datensicherung durch einen Rücksicherungstest obliegt dem Kunden.&#x20;

Geeignete Unterstützungs-Maßnahmen können mit centron gesondert vereinbart werden. Der Kunde weist daraufhin, dass die Haftung für die Fehlerfreiheit der „Patches“, die Sinnhaftigkeit der Risiko-Klassifizierung sowie die Kompatibilitätseinschätzung mit der zu aktualisierenden Software beim Hersteller der betroffenen Software liegt. Im Rahmen von Software-„Patches“ sind Störungen – im schlimmsten Fall auch Datenverlust – nie auszuschließen. Daher ist vom Kunden sicherzustellen, dass vor „Patches“, Daten gemäß den Unternehmensrichtlinien gesichert werden. Dies ist turnusmäßig durch den Kunden zu prüfen. Die Datenrücksicherung erfolgt bei Notwendigkeit durch centron. Hierzu kontaktiert der Kunde den centron Support. centron übernimmt bei gesonderter Beauftragung eine Überprüfung der Funktionsfähigkeit des Systems oder der Anwendungssoftware. Zusammengefasst beinhaltet das Monitoring als Teil der Managing Basisleistungen:&#x20;

* Patchday alle 4 Wochen (3. Mittwoch des Monats)
* Kritische Sicherheitslücken werden umgehend analysiert und eingespielt&#x20;
* Individuell gestaltbares Zeitfenster für die Installation der Updates (22:00 – 04:00 Uhr)&#x20;
* Updates können in Abhängigkeit installiert werden&#x20;
* Historie&#x20;

### 4.4 Vergütung&#x20;

Premium Full Managing beinhaltet die zuvor beschriebenen Leistungen Backup, Monitoring und Update Management. Managing Basisleistungen können nur in Kombination mit einer  bestehenden VM gebucht werden. Pro VM wird für Managing Basisleistungen ein Entgelt von 50,00€ zzgl. Backup Speicherplatz berechnet.&#x20;

### 4.5 Kündigung&#x20;

Bei einer monatlichen Laufzeit kann der Leistungsschein jederzeit zum Ende des jeweiligen Monats gekündigt werden. Bei einer Laufzeit von 12 Monaten beträgt die Kündigungsfrist drei Monate vor Auslaufen des Vertrages, bei 24 oder 36 Monaten Laufzeit kann der Vertrag bis zu sechs Monate vor Beendigung der Laufzeit gekündigt werden.&#x20;

### 4.6 Software Portfolio

Folgende Software fällt unter entsprechenden Einschränkungen unter den Bereich des Premium Full Managings:&#x20;

<table><thead><tr><th width="163">OS</th><th width="162">Version</th><th data-type="checkbox">Backup</th><th data-type="checkbox">Aktives Monitoring</th><th data-type="checkbox">Performance Monitoring</th><th data-type="checkbox">Patch</th></tr></thead><tbody><tr><td>Microsoft Server </td><td>2016 / 2019</td><td>true</td><td>true</td><td>true</td><td>true</td></tr><tr><td>Debian / Ubuntu Server </td><td>9 - 11; 18 - 22</td><td>true</td><td>true</td><td>true</td><td>true</td></tr></tbody></table>

<table><thead><tr><th width="156">Web</th><th width="164">Version</th><th data-type="checkbox">Backup</th><th data-type="checkbox">Aktives Monitoring</th><th data-type="checkbox">Performance Monitoring</th><th data-type="checkbox">Patch</th></tr></thead><tbody><tr><td>IIS</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Apache2</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>true</td><td>true</td></tr><tr><td>Nginx</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Varnish</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>true</td><td>true</td></tr></tbody></table>

<table><thead><tr><th width="156">Database</th><th width="164">Version</th><th data-type="checkbox">Backup</th><th data-type="checkbox">Aktives Monitoring</th><th data-type="checkbox">Performance Monitoring</th><th data-type="checkbox">Patch</th></tr></thead><tbody><tr><td>MSSQL Server</td><td>2017 - 2019</td><td>true</td><td>true</td><td>true</td><td>true</td></tr><tr><td>MariaDB</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>true</td><td>true</td></tr><tr><td>MySQL Server</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>true</td><td>true</td></tr><tr><td>Postgres Sevrer</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>true</td><td>true</td></tr></tbody></table>

&#x20;

<table><thead><tr><th width="156">Mail</th><th width="167">Version</th><th data-type="checkbox">Backup</th><th data-type="checkbox">Aktives Monitoring</th><th data-type="checkbox">Performance Monitoring</th><th data-type="checkbox">Patch</th></tr></thead><tbody><tr><td>hMail Server</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Dovecot</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>PostFix</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Exchange</td><td>2016 - 2019</td><td>true</td><td>true</td><td>false</td><td>true</td></tr></tbody></table>

<table><thead><tr><th width="156">Apps</th><th width="167">Version</th><th data-type="checkbox">Backup</th><th data-type="checkbox">Aktives Monitoring</th><th data-type="checkbox">Performance Monitoring</th><th data-type="checkbox">Patch</th></tr></thead><tbody><tr><td>Hyper-V</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>true</td><td>true</td></tr><tr><td>Active Directory, DNS</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>PHP</td><td>5.6 - 8.x</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>RDS (Session)</td><td>Abhängig von OS</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>MS Office</td><td>2016 - 2021</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Filezilla</td><td>>0.9.x</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Plesk</td><td>>18.x</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>LiveConfig</td><td>>2.9</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Mailstore</td><td>Aktuell</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>GFI</td><td>&#x3C;15.x</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>Veeam</td><td>11.x.x</td><td>true</td><td>true</td><td>false</td><td>true</td></tr><tr><td>M365</td><td>Aktuell</td><td>true</td><td>false</td><td>false</td><td>true</td></tr><tr><td>ESET</td><td>>9.0.x</td><td>true</td><td>false</td><td>false</td><td>true</td></tr></tbody></table>

<table><thead><tr><th width="163">Netzwerk</th><th width="162">Version</th><th data-type="checkbox">Backup</th><th data-type="checkbox">Aktives Monitoring</th><th data-type="checkbox">Performance Monitoring</th><th data-type="checkbox">Patch</th></tr></thead><tbody><tr><td>pfSense</td><td>2.5.2 - 2.6</td><td>true</td><td>true</td><td>true</td><td>true</td></tr></tbody></table>

#### 4.6.1 Microsoft Server&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.2 Debian / Ubuntu Server&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung &#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;



#### 4.6.3 IIS&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung / Verwaltung des Servers&#x20;

• Einrichtung und Verwaltung der User und Rechtestruktur&#x20;

• Konfiguration des Servers&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.4 Apache2&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung / Verwaltung des Servers&#x20;

• Einrichtung und Verwaltung der User und Rechtestruktur&#x20;

• Konfiguration des Servers&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.5 nginx&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung / Verwaltung des Servers&#x20;

• Einrichtung und Verwaltung der User und Rechtestruktur&#x20;

• Konfiguration des Servers&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.6 MSSQL Server&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Usern&#x20;

• Einrichtung und Verwaltung der Rechtestruktur&#x20;

• Konfiguration der Datenbank&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.7 Maria DB&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Usern&#x20;

• Einrichtung und Verwaltung der Rechtestruktur&#x20;

• Konfiguration der Datenbank&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

&#x20;• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.8 MySQL&#x20;

Server Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Usern&#x20;

• Einrichtung und Verwaltung der Rechtestruktur&#x20;

• Konfiguration der Datenbank&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

&#x20;• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.9 Postgres Server&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Usern&#x20;

• Einrichtung und Verwaltung der Rechtestruktur&#x20;

• Konfiguration der Datenbank&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.10 hMailServer&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Postfächern&#x20;

• Einrichtung und Verwaltung von Gruppen, Verteilern und Systemordnern&#x20;

• Konfiguration von Replikationsdiensten&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.11 Dovecot&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Postfächern&#x20;

• Einrichtung und Verwaltung von Gruppen, Verteilern und Systemordnern&#x20;

• Konfiguration von Replikationsdiensten&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung &#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.12 PostFix

&#x20;Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Postfächern&#x20;

• Einrichtung und Verwaltung von Gruppen, Verteilern und Systemordnern&#x20;

• Konfiguration von Replikationsdiensten&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.13 Exchange&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung und Verwaltung von Postfächern&#x20;

• Einrichtung und Verwaltung von Gruppen, Verteilern und Systemordnern&#x20;

• Konfiguration von Replikationsdiensten&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.14 Hyper-V&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.15 Active Directory, DNS&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Überwachung von Kommunikations- und unterstützenden Diensten wie DHCP, WINS, DNS etc.&#x20;

• Überwachung der Active Directory Services&#x20;

• Administration von Kommunikations- und unterstützenden Diensten wie DHCP, WINS, DNS etc.&#x20;

• Einrichtung und Verwaltung von Gruppen, Anwendern und Profilen&#x20;

• Pflege von anwenderbezogenen Daten&#x20;

• Zuordnung von Ressourcen zu Gruppen und Anwendern&#x20;

• Verwaltung von Verzeichnissen, Freigaben und Berechtigungen&#x20;

• Einrichtung und Verwaltung von Domänen, Trusts, Sites und Services&#x20;

• Einrichtung und Verwaltung sonstiger ADS - Objekte (bspw. GPOs) • Einrichtung und Verwaltung von Replikationsdiensten&#x20;

• Konfiguration von Replikationsdiensten&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.16 PHP&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung &#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.17 MS Office&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.18 Filezilla&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.19 Plesk&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Einrichtung / Verwaltung des Servers&#x20;

• Einrichtung und Verwaltung der User und Rechtestruktur&#x20;

• Konfiguration des Servers&#x20;

• Installation von Security Patches&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.20 LiveConfig&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren &#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.21 Mailstore&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.22 GFI&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.23 Veeam&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.24 M365&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Anlegen des Tenants&#x20;

• Bestellung der Lizenz&#x20;

• Freischaltung der Lizenzen&#x20;

• Anlegen des Benutzerkontos&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.25 Eset&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Monitoring von Betriebsparametern&#x20;

• Regeländerung / Parameter Tuning&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

#### 4.6.26 pfSense&#x20;

Die von centron im Rahmen dieses Vertrags bereitzustellenden Services sind auf den folgenden Umfang begrenzt:&#x20;

• Monitoring von Betriebsparametern und Events&#x20;

• Regeländerung / Parameter Tuning&#x20;

• Ersteinrichtung und Konfiguration&#x20;

• First- und Second-Level-Supportservices für die Störungsbehebung&#x20;

• Ursachenanalyse und Problemlösung&#x20;

• Verwaltung geringfügiger Anforderungen für Anpassungen der Konfiguration, des Reporting oder anderer Parameter.&#x20;

• Implementierung von Änderungen an vorhandenen Anwendungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Bearbeitung von Serviceanforderungen mit dem Anwendungs- oder Änderungsantragsverfahren&#x20;

• Proaktive Anwendungsüberwachung und Alert-Bearbeitung&#x20;

Alle anderen Services, betreuten Systeme, Anwendungen, Standorte usw. sind nicht im Umfang enthalten.&#x20;

### 4.7 Zusätzliche Leistungen&#x20;

centron bietet zusätzlich folgende Software Setups an:&#x20;

• Galera Cluster&#x20;

• MSSQL Always on&#x20;

• S2D&#x20;

• Failover Cluster&#x20;

• Pacemaker

• SSL (Let’s Encrypt)&#x20;

centron behält sich das Recht, für Leistungen im Bereich des Premium Full Managings, die nicht in dieser Leistungsbeschreibung aufgeführt wurden, ein Entgelt zu den in Kapitel 2.3 Premium Managed Services beschriebenen Preisen zu berechnen.&#x20;

### 4.8 Zugriff auf Server&#x20;

Bei Managed Servern ist generell kein Rootzugriff durch Kunden möglich. Der Zugriff per SSH erfolgt über reguläre Nutzerberechtigungen. Es besteht die Möglichkeit eines Haftungsausschlusses, wodurch ein Rootzugriff ermöglicht wird. Centron Übernimmt ab diesem Zeitpunkt keine Haftung für den Betrieb des Systems.&#x20;

### 4.9 Installation weiterer Software&#x20;

Die Installation weiterer Software oder Bibliotheken wird durch den Support nicht durchgeführt. Dies geschieht jedoch auf eigene Verantwortung des Kunden. Ein Anrecht auf Supportleistungen in diesem Zusammenhang besteht nicht. Der Betrieb zusätzlicher Software, welche Rootrechte zur Installation oder Betrieb erfordert, ist grundsätzlich nicht möglich.

## 5. Salvatorische Klausel

Sollten einzelne Bestimmungen dieses SLA ganz oder teilweise nicht rechtswirksam oder nicht durchführbar sein oder werden, so soll hierdurch die Gültigkeit der übrigen Bestimmungen des jeweiligen Einzelvertrages nicht berührt werden. Das Gleiche gilt für den Fall, dass der jeweilige Vertrag eine Regelungslücke enthält. Anstelle der unwirksamen oder undurchführbaren Bestimmung oder zur Ausfüllung der Lücke soll eine angemessene Regelung gelten, die, soweit möglich, dem am nächsten kommt, was die Vertragsparteien vereinbaren wollten.

Stand: 05/2023

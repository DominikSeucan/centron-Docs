---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Domain Transfers

Wenn Sie eine Domain an jemanden anderes übertragen wollen, benötigen Sie eine Authcode.

### Was ist eine "Authcode"?

Bei Domainnamen mit bestimmten Endungen (z.B. .com oder .info) benötigen wir den sogenannten Authcode, auch Authinfo genannt, um den Providerwechsel starten zu können.

Da nur der Domaininhaber diesen Authcode kennt soll darüber sichergestellt werden, dass keine unrechtmäßige Domainübernahme erfolgen kann. Normalerweise sollte in der bisherigen Domainverwaltung bei der entsprechenden Domain bei den Details der Auth-Code zu finden sein.&#x20;

Andernfalls müssen Sie Kontakt mit Ihrem bisherigen Domainverwalter/ Hoster/ Internetprovider aufnehmen, damit dieser Ihnen den Code zur Verfügung stellt.

Zusätzlich muss der Status der Domain per Kündigungstyp auf **PREACK** gesetzt werden, also einem Transfer bereits zugestimmt sein, falls jemand mit dem passenden Authcode einen Transfer beantragt.

### Was ist ein Registrar-Lock?

Der Registrar-Lock ist eine Sperre für eine gTLD-Domain, mit der ein Domaintransfer zu einem anderen Registrar verhindert wird. Wenn Sie eine Domain zu und von centron transferieren möchten, müssen Sie vorab sicherstellen, dass ein eventuell vorhandener Registrar-Lock des vorhergehenden Registrars deaktiviert wurde.&#x20;

Darüber hinaus wird mit einem Registrar-Lock verhindert, dass eine Domain unter einer gTLD ungewollt aus Ihrer Verwaltung transferiert wird. Die Sperre wird nur aufgehoben, wenn Sie die Domain mit einem **PREACK** (Vorab-Zustimmung) kündigen.

Einen fehlenden **PREACK** erkennt man am Status **LOCK** bzw. am Registry Status clientTransferProhibited bei dem jeweiligen NIC (z.B. nic.com für .com Domains).&#x20;

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

**PREACK** ist vor allem bei folgenden Domainendungen notwendig:

* .com Domains
* .net Domains

### Beispiel kein Transfer möglich:

domain: xy.com\
status: LOCK

Registry Status: clientTransferProhibited



Sie haben sich für eines unserer [Hostingpakete](https://www.centron.de/basic-solutions/webhosting/) entschieden und möchten Ihre bestehende Webseite und E-Mail-Postfächer zu uns umziehen? In diesem Artikel fassen wir das Vorgehen im Falle eines Umzugs von Domain, Webseite und Mailing zusammen. Sollten Sie hier Unterstützung benötigen, stehen wir Ihnen dabei gerne zur Seite.

### Das Vorgehen kurz zusammengefasst <a href="#das_vorgehen_kurz_zusammengefasst" id="das_vorgehen_kurz_zusammengefasst"></a>

1. Kopieren der Daten Ihrer Webseite von Ihrem ursprünglichen Hoster.\
   **Gut zu wissen:** Mit Hilfe einer temporären Domain können Sie sicherstellen, dass Ihre Webseite auch über unsere Server erreichbar ist.
2. Anlegen aller Postfächer auf unserem Mailserver.
3. Umstellung des DNS auf unsere Web- und Mailserver.
4. E-Mails vom alten auf den neuen Mailserver kopieren.
5. Domain in die Verwaltung von centron übergeben.

Einige Provider löschen nach dem Start eines ausgehenden Domaintransfers die Domain sofort von ihren Servern. Wenn keine entsprechenden Maßnahmen ergriffen werden, kann es sein, dass bei einem Domaintransfer zu uns Ihre Webseite und Ihre E-Mail-Konten vorübergehend nicht mehr erreichbar sind.\
\
Aus diesem Grund empfehlen wir Ihnen zuerst Ihre Daten, Webseite und E-Mail-Konten auf unsere Server umzuziehen, um einer eventuellen Nicht-Erreichbarkeit vorzubeugen. So bleibt auch die Übergangsphase während der Umstellung des DNS möglichst gering.

### Schritt 1 | Kopieren der Daten Ihrer Webseite <a href="#schritt_1_kopieren_der_daten_ihrer_webseite" id="schritt_1_kopieren_der_daten_ihrer_webseite"></a>

**Dafür nötig:** FTP- und Datenbank-Zugangsdaten, alternativ: Zugangsdaten zum Verwaltungsinterface Ihres Hosters

Der erste Schritt ist es, die Daten Ihrer Webseite auf unseren Webserver zu kopieren. Dazu zählt im Normalfall auch eine Datenbank. So kann direkt zu Beginn die Erreichbarkeit Ihrer Webseite auf unseren Servern sichergestellt werden. Bei der Buchung des Hostingpakets ist darauf zu achten, das richtige Betriebssystem zu wählen. Ihnen steht Linux und Windows zur Auswahl. Sollte Ihnen dies nicht bekannt sein, kann Ihnen hier Ihr Hoster weiterhelfen.

Verbinden Sie sich zum Kopieren der **Dateien Ihrer Webseite** per FTP mit dem Webserver Ihres Hosters.\
Sie benötigen Unterstützung beim Aufbau einer FTP-Verbindung? [Dieser Artikel hilft Ihnen dabei.](https://wiki8.centron.de/webhosting/ftp)\
Laden Sie alle Dateien Ihrer Webseite herunter. Oft empfiehlt es sich alle Dateien in ein ZIP-Archiv zu verpacken und zu komprimieren um Traffic und Zeit zu sparen. Laden Sie im Anschluss alle Daten in das Verzeichnis der Webseite in Ihrem neuen Hostingpaket wieder hoch. Achten Sie hierbei darauf, das richtige Verzeichnis zu wählen. Normalerweise lauten diese wie folgt:

* Windows-Hosting: _domain.de_\web
* Linux-Hosting: _domain.de_\httpdocs (Der Ordner _domain.de_ ist hier optional.)

Oft gehört zu einer Webseite auch eine **Datenbank**, welche Sie zuerst bei Ihrem bisherigen Hoster sichern müssen. Informieren Sie sich vorher darüber, welche Version des Datenbankservers verwendet wird, um die Kompatibilität mit dem neuen Datenbankservers sicherzustellen. [Hier](https://www.centron.de/hosting/homepage-hosting/) sehen Sie, welche Version des Datenbankservers Ihnen bei Ihrem neuen Hostingpaket zur Verfügung steht.

Gerne unterstützen wir Sie im Rahmen unseres Umzugsservices beim Transfer Ihrer Daten zu uns (weitere Infos finden Sie am Ende dieses Beitrags).

**Gut zu wissen:** Mit Hilfe einer temporären Domain können Sie sicherstellen, dass Ihre Webseite auch über unsere Server erreichbar sind.

### Schritt 2 | Anlegen aller Postfächer <a href="#schritt_2_anlegen_aller_postfacher" id="schritt_2_anlegen_aller_postfacher"></a>

**Dafür nötig:** E-Mail Adressen der Domain (+ ggf. zugehörige Kennwörter)

Um Ihre Erreichbarkeit per E-Mail sicherzustellen, können Ihre Postfächer bereits vor dem Umzug auf unserem Mailserver angelegt werden. Keine Sorge, dies beeinflusst nicht den aktuellen Mailversand und -empfang. Sie können selbst individuell [Postfächer über unser WebPanel anlegen](https://wiki8.centron.de/webhosting/interfaces/webpanel/email). Sollten Sie hierbei Unterstützung benötigen, zögern Sie nicht unseren [Support](https://www.centron.de/kontakt/) zu kontaktieren.\
Um bereits im Voraus die Funktionalität Ihrer neuen Postfächer zu überprüfen und einen reibungslosen Umstieg zu ermöglichen, können Sie die Postfächer bereits in einem Client einrichten. In diesen Artikeln finden Sie Anleitungen zur Einrichtung eines [IMAP/POP-Postfachs](https://wiki8.centron.de/email/imappop/mailbox/setup) bzw. eines [Exchange-Postfachs](https://wiki8.centron.de/email/exchange/mailbox/setup).

Sofern sichere Kennwörter für die Postfächer festgelegt sind und diese mit unserer Kennwortrichtlinie vereinbar sind, können diese auch für Ihre neuen Postfächer übernommen werden. Wenn diese unverändert bleiben, muss nur der Mailserver in den Einstellungen des Clients angepasst werden. Wie das funktioniert, erfahren Sie [hier](https://wiki8.centron.de/email/imappop/mailbox/changehost).\
\
Sollten für die Postfächer neue Kennwörter festgelegt werden, müssen diese [neu in den Clients eingerichtet](https://wiki8.centron.de/email/imappop/mailbox/setup) werden.

### Schritt 3 | Umstellung des DNS <a href="#schritt_3_umstellung_des_dns" id="schritt_3_umstellung_des_dns"></a>

**Dafür nötig:** Zugriff auf das Verwaltungsinterface Ihres bisherigen Providers

Sobald alle Daten der Webseite und die Postfächer auf unseren Servern angelegt sind, können die DNS-Einträge auf die neuen Web- und Mailserver umgestellt werden. Die hierfür nötigen IP-Adressen erhalten Sie von unserem Support. Für Unterstützung beim Umzug können Sie unseren Umzugsservice buchen (mehr Informationen dazu finden Sie am Ende dieses Beitrags).

**Wir empfehlen Ihnen Umstellungen nur Montag - Donnerstag (und nicht vor Feiertagen) während unserer Geschäftszeiten durchzuführen, damit wir Sie bei etwaigen Schwierigkeiten rechtzeitig unterstützen können.**\
Sollten Sie die Umstellung selbst vornehmen wollen, kann dies auch auf eigenes Risiko außerhalb dieser Zeiten erfolgen.

### Schritt 4 | E-Mails kopieren <a href="#schritt_4_e-mails_kopieren" id="schritt_4_e-mails_kopieren"></a>

**Dafür nötig:** Kennwörter der alten und neuen Postfächer

Etwa 30 Minuten nachdem die DNS-Einträge Ihrer Domain angepasst wurden, greifen die Änderungen weltweit. Nach dieser Zeit werden eingehende E-Mails in jedem Fall in Ihren neuen Postfächern zugestellt, somit können die E-Mails aus Ihren alten Postfächern in die Neuen übernommen werden. [Diese Anleitung](https://wiki8.centron.de/email/umzug) unterstützt Sie dabei.

### Schritt 5 | Domain in die Verwaltung von centron übergeben <a href="#schritt_5_domain_in_die_verwaltung_von_centron_uebergeben" id="schritt_5_domain_in_die_verwaltung_von_centron_uebergeben"></a>

**Dafür nötig:** Authcode

Der letzte Schritt ist es, die Domain in die Verwaltung von centron zu übergeben.

**Umstellungen werden von uns grundsätzlich nur von Montag - Donnerstag (und nicht vor Feiertagen) zwischen 9 und 16 Uhr vorgenommen um bei etwaigen Schwierigkeiten rechtzeitig handeln zu können.**\
Sollten Sie die Umstellung selbst vornehmen wollen, kann dies auch auf eigenes Risiko außerhalb dieser Zeiten erfolgen.

Normalerweise ist Ihre Domain in Ihrem Hostingpaket inklusive, wodurch keine weiteren Kosten für Sie entstehen. Die Verwaltung Ihrer Internetpräsenz zu zentralisieren ist empfehlenswert, da Sie zum einen nur noch einen Ansprechpartner haben und zum anderen centron alle nötigen Konfigurationen direkt vornehmen kann.\
Für den Wechsel des Providers ist ein Authorisierungscode (kurz Authcode) nötig. Dieser Code stellt sicher, dass nur berechtigte Personen Ihre Domain transferieren können, ähnlich wie ein Passwort. Den Authcode erhalten Sie von Ihrem aktuellen Provider, sobald Sie dort die Kündigung Ihrer Domain einleiten und den Wechsel Ihres Providers dabei ankündigen. Sobald ein Authcode erstellt wurde, ist dieser **normalerweise 30 Tage gültig**. Bei speziellen TLDs kann dies jedoch abweichen. Sollte dies der Fall sein, werden Sie darüber von Ihrem Provider informiert.

Bei einem Domainumzug oder -transfer werden die sogenannten Nameserver, welche für Ihre Domain zuständig sind, geändert. Bei dieser Änderung kann es bis zu 24 Stunden dauern, bis diese weltweit übernommen werden. Aber keine Sorge: Da wir bereits vor der Nameserveränderung alle restlichen DNS-Einträge auf unsere Server umgestellt haben, bemerken Sie von dieser langen Übergangszeit nichts.

### Der centron-Umzugsservice <a href="#der_centron-umzugsservice" id="der_centron-umzugsservice"></a>

Sollten Sie den Umzug aus zeitlichen Gründen nicht selbst vornehmen können oder nicht das technische Know-How dafür besitzen, nehmen wir die Migration Ihres Hostings gerne für Sie vor. Hierfür benötigen wir folgendes:

* Authcode der Domain
* FTP- und Datenbank-Zugangsdaten, alternativ: Zugangsdaten zum Verwaltungsinterface Ihres Hosters
* E-Mail Adressen der Domain + ggf. zugehörige Kennwörter, sofern …
  * diese übernommen werden sollen und unseren Sicherheitsrichtlinien entsprechen
  * die E-Mails aus Ihren alten Postfächern in die Neuen übernommen werden sollen

Bitte beachten Sie dabei, dass für den Umzugsservice zusätzliche Kosten anfallen. Wenden Sie sich für weitere Informationen einfach an unseren [Support](https://www.centron.de/kontakt/).

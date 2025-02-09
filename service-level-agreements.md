---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Mai 2023
---

# Service Level Agreements

## SLAs

centron bietet Service Level Agreements (SLAs) für mehrere seiner Produkte an, darunter ccloud, S3 Storage, Premium Full Managing und Premium Managed Services. Die SLAs spiegeln unser Engagement wider, unseren Kunden ein hohes Maß an Betriebszeit zu bieten. Dieser Artikel definiert einen Vertrag für jedes Produkt, das ein SLA hat. Diese SLAs sind die Richtlinien für die Nutzung der centron-Services. Sie gelten für jeden Account, der die Services nutzt, separat. Im Falle eines Konflikts zwischen den Bedingungen des SLA und den Bedingungen der centron-Kundenvereinbarung oder einer anderen Vereinbarung mit uns, die Ihre Nutzung unserer Dienste regelt (die „Vereinbarung“), haben die Bedingungen der anwendbaren SLA für die Dienste Vorrang. Dies gilt allerdings nur, insofern ein Konflikt besteht, in dessen Umfang.

### 1. Geltungsbereich <a href="#id-1.-geltungsbereich" id="id-1.-geltungsbereich"></a>

**1.1** Dieses Service Level Agreement (SLA) regelt als wesentlicher Vertragsbestandteil des mit dem Kunden bestehenden Vertragsverhältnisses in der jeweils gültigen Fassung die Bedingungen für die Bereitstellung der durch die centron GmbH angebotenen Dienstleistungen. Das SLA ist lediglich als vertraglich definierter Mindestinhalt der Ansprüche des Kunden zu verstehen und ergänzt die Regelungen der Allgemeinen Geschäftsbedingungen (AGB), die Terms of Services - Nutzungsbedingungen (ToS) und die Leistungsbeschreibungen der einzelnen Produkte und Dienstleistungen.

**1.2** Die centron GmbH kann das SLA jederzeit ohne Nennung von Gründen ändern. Der Geltungsbereich findet ebenfalls Wirksamkeit für ein bestehendes Vertragsverhältnis. Über Änderungen wird die centron GmbH den Kunden zehn Werktage vor Inkrafttreten informieren. Bei nachteiligen wesentlichen Änderungen an dieser Vereinbarung informiert die centron GmbH den Kunden mindestens 30 Tage im Voraus.

### 2. centron ccloud³ <a href="#id-2.-centron-ccloud" id="id-2.-centron-ccloud"></a>

**2.1** Die centron GmbH stellt dem Kunden Rechenkapazität als Instanz zur Verfügung, auf die über Netzwerk mittels standardisierter Protokolle zugegriffen werden kann.

**2.2** Die centron GmbH verpflichtet sich, angemessene Anstrengungen zu unternehmen, um eine Verfügbarkeit der centron ccloud³ von mindestens 99,95 Prozent im monatlichen Durchschnitt zu erreichen. Sollte die centron GmbH dem nicht nachkommen, ist der Kunde zu einer Gutschrift berechtigt.

**2.3** centron ccloud³ gilt als nicht verfügbar, wenn der Zugriff auf die aktive Instanz nicht gewährleistet ist, d.h. die gegenseitige Kommunikation mit der Instanz nicht möglich ist.

**2.4** Die Verfügbarkeit der centron ccloud³ wird über alle Instanzen eines Kunden innerhalb einer monatlichen Abrechnung nach folgender Formel berechnet: 100% - (Nichtverfügbarkeit in Minuten / Instanzzeit in Minuten). Die Instanzzeit bezeichnet die Zeitspanne zwischen dem Anlegen und Löschen einer Cloud Compute Instanz durch den Kunden.

**2.5** Die Gutschrift wird als Prozentsatz auf alle Zahlungen berechnet, die in dem Abrechnungsmonat, in dem die Verfügbarkeit unterschritten wurde, für den centron ccloud³ geleistet wurden (Core, RAM & Speicher).

**2.6** Wird die vereinbarte Verfügbarkeit der centron ccloud³ unterschritten, ist der Kunde berechtigt, eine Gutschrift zu erhalten, die sich aus der nachfolgenden Tabelle ergibt:

| centron ccloud³ Verfügbarkeit im monatlichen Durchschnitt | centron ccloud Verfügbarkeit im monatlichen Durchschnitt gleich oder größer als | Gutschrift bezogen auf eine Monatsabrechnung |
| --------------------------------------------------------- | ------------------------------------------------------------------------------- | -------------------------------------------- |
| kleiner als                                               | gleich oder größer als                                                          |                                              |
| 99,95%                                                    | 99,90%                                                                          | 5%                                           |
| 99,90%                                                    | 99,80%                                                                          | 10%                                          |
| 99,80%                                                    | 99,70%                                                                          | 25%                                          |
| 99,70%                                                    | ​                                                                               | 40%                                          |

### 3. cProtect <a href="#id-3.-cprotect" id="id-3.-cprotect"></a>

**3.1** centron GmbH stellt dem Kunden VM Replikationen zur Verfügung, auf die über Netzwerk mittels standardisierter Protokolle zugegriffen werden kann.

**3.2** Die centron GmbH verpflichtet sich, angemessene Anstrengungen zu unternehmen, um eine Verfügbarkeit von centron cProtect von mindestens 99,95 Prozent im monatlichen Durchschnitt zu erreichen. Sollte die centron GmbH dieser Verpflichtung nicht nachkommen, ist der Kunde zu einer Gutschrift berechtigt.

**3.3** centron cProtect gilt als nicht verfügbar, wenn die Replikation einer aktiven Instanz nicht gewährleistet ist.

**3.4** Die Verfügbarkeit von centron cProtect wird über alle Instanzen eines Kunden innerhalb eines monatlichen Zeitraums nach folgender Formel berechnet: 100% - (Nichtverfügbarkeit in Minuten / Instanzzeit in Minuten). Die Instanzzeit bezeichnet die Zeitspanne zwischen dem Anlegen und Löschen einer Instanz, die mit cProtect versehen wurde.

**3.5** Die Gutschrift wird als Prozentsatz auf alle Zahlungen berechnet, die in dem Abrechnungsmonat, in dem die Verfügbarkeit unterschritten wurde, für den centron cProtect geleistet wurden (Core, RAM & Speicher).

**3.6** Wird die vereinbarte minimale Verfügbarkeit von centron cProtect unterschritten, ist der Kunde berechtigt, eine Gutschrift zu erhalten, die sich aus der nachfolgenden Tabelle ergibt:

| centron cProtect Verfügbarkeit im Monatsmittel | centron cProtect Verfügbarkeit im Monatsmittel gleich oder größer als | Gutschrift bezogen auf eine Monatsabrechnung |
| ---------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------- |
| kleiner als                                    | gleich oder größer als                                                |                                              |
| 99,95%                                         | 99,90%                                                                | 5%                                           |
| 99,90%                                         | 99,80%                                                                | 10%                                          |
| 99,80%                                         | 99,70%                                                                | 25%                                          |
| 99,70%                                         | ​                                                                     | 40%                                          |

### 4. High Availability <a href="#id-4.-high-availability" id="id-4.-high-availability"></a>

**4.1** centron GmbH stellt dem Kunden Ausfallsicherheit durch High Availability zur Verfügung.

**4.2** Die centron GmbH verpflichtet sich, angemessene Anstrengungen zu unternehmen, um eine Verfügbarkeit von centron High Availability von mindestens 99,95 Prozent im Monatsmittel zu erreichen. Sollte die centron GmbH dem nicht nachkommen, ist der Kunde zu einer Gutschrift berechtigt.

**4.3** centron High Availability gilt als nicht verfügbar, wenn der Zugriff auf die aktive Instanz mit High Availability nicht gewährleistet ist, d.h. die Kommunikation mit der Instanz ist nicht möglich.

**4.4** Die Verfügbarkeit von centron High Availability wird über alle Instanzen eines Kunden, die mit High Availability versehen wurden, innerhalb eines monatlichen Zeitraums nach folgender Formel berechnet: 100% - (Nichtverfügbarkeit in Minuten / HA Zeit in Minuten). Die HA Zeit bezeichnet die Zeitspanne zwischen dem Anlegen und Löschen einer Cloud Compute Instanz mit High Availabiltiy.

**4.5** Die Gutschrift wird als Prozentsatz auf alle Zahlungen berechnet, die in dem Abrechnungsmonat, in dem die Verfügbarkeit unterschritten wurde, für den centron High Availability geleistet wurde.

**4.6** Wird die vereinbarte Verfügbarkeit von centron High Availability unterschritten, ist der Kunde berechtigt, eine Gutschrift zu erhalten, die sich aus der nachfolgenden Tabelle ergibt:

| centron High Availability Verfügbarkeit im monatlichen Durchschnitt | centron High Availability Verfügbarkeit im monatlichen Durchschnitt gleich oder größer als | Gutschrift bezogen auf eine Monatsabrechnung |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------- |
| kleiner als                                                         | gleich oder größer als                                                                     |                                              |
| 99,95%                                                              | 99,90%                                                                                     | 5%                                           |
| 99,90%                                                              | 99,80%                                                                                     | 10%                                          |
| 99,80%                                                              | 99,70%                                                                                     | 25%                                          |
| 99,70%                                                              | ​                                                                                          | 40%                                          |

### 5. centron S3 Object Storage <a href="#id-5.-centron-s3-object-storage" id="id-5.-centron-s3-object-storage"></a>

**5.1** centron S3 Object Storage ist eine Object-Storage-Lösung. Der Service ermöglicht dem Kunden Objekte (Dateien zzgl. Metadaten) in Buckets zu speichern und auf diese über APIs bzw. Webservices zuzugreifen.

**5.2** Die centron GmbH verpflichtet sich, angemessene Anstrengungen zu unternehmen, um eine Verfügbarkeit des centron S3 Object Storages von mindestens 99,5 Prozent im monatlichen Durchschnitt zu erreichen. Sollte die centron GmbH dieser Verpflichtung nicht nachkommen, ist der Kunde zu einer Gutschrift berechtigt.

**5.3** centron S3 Object Storage gilt als nicht verfügbar, wenn der Kunde einen Serverfehler mit der Meldung „Internal Server Error“ oder „Service Unavailable“ erhält.

**5.4** Die Verfügbarkeit des centron S3 Object Storages wird über alle Buckets eines Kunden innerhalb eines monatlichen Abrechnungszeitraums bestimmt. Die Verfügbarkeit bildet sich aus 100 Prozent abzüglich des arithmetischen Mittels der Fehlerraten. Die Fehlerrate ist das Verhältnis von Serverfehlern zur Anzahl aller Anfragen innerhalb eines Fünf-Minuten-Intervalls. Wenn keine Anfrage gestellt wurde, beträgt die Fehlerrate für das betrachtete Intervall null Prozent.

**5.5** Die Gutschrift wird als Prozentsatz auf Zahlungen berechnet, die in dem Abrechnungsmonat, in dem die Verfügbarkeit unterschritten wurde, für centron S3 Object Storage geleistet wurden.

**5.6** Wird die vereinbarte minimale Verfügbarkeit des centron S3 Object Storages unterschritten, ist der Kunde berechtigt, eine Gutschrift zu erhalten, die sich aus der nachfolgenden Tabelle ergibt:

| centron S3 Object Storage Verfügbarkeit im Monatsmittel | centron S3 Object Storage Verfügbarkeit im Monatsmittel gleich oder größer als | Gutschrift bezogen auf eine Monatsabrechnung |
| ------------------------------------------------------- | ------------------------------------------------------------------------------ | -------------------------------------------- |
| kleiner als                                             | gleich oder größer als                                                         |                                              |
| 99,50%                                                  | 99,00%                                                                         | 10%                                          |
| 99,00%                                                  | ​                                                                              | 25%                                          |

​

### 6. Premium Full Managing <a href="#id-6.-premium-full-managing" id="id-6.-premium-full-managing"></a>

**6.1** centron GmbH stellt dem Kunden Backup-as-a-Service, Monitoring-as-a-Service & Patch-Management zur Verfügung, auf die über Netzwerk mittels standardisierter Protokolle zugegriffen werden kann.

**6.2** Die centron GmbH verpflichtet sich, angemessene Anstrengungen zu unternehmen, um eine Verfügbarkeit von centron Premium Full Managing von mindestens 80,00 Prozent im monatlichen Durchschnitt zu erreichen. Sollte die centron GmbH dieser Verpflichtung nicht nachkommen, ist der Kunde zu einer Gutschrift berechtigt.

**6.3** centron Premium Full Managing gilt als nicht verfügbar, wenn die Replikation einer aktiven Instanz nicht gewährleistet ist.

**6.4** Die Verfügbarkeit von centron Premium Full Managing wird über alle Instanzen eines Kunden innerhalb eines monatlichen Zeitraums nach folgender Formel berechnet: 100% - (Nichtverfügbarkeit in Minuten / Instanzzeit in Minuten). Die Instanzzeit bezeichnet die Zeitspanne zwischen dem Anlegen und Löschen einer Instanz, die mit cProtect versehen wurde.

**6.5** Die Gutschrift wird als Prozentsatz auf alle Zahlungen berechnet, die in dem Abrechnungsmonat, in dem die Verfügbarkeit unterschritten wurde, für den centron cProtect geleistet wurden (Core, RAM & Speicher).

**6.6** Wird die vereinbarte minimale Verfügbarkeit von centron cProtect unterschritten, ist der Kunde berechtigt, eine Gutschrift zu erhalten, die sich aus der nachfolgenden Tabelle ergibt:

| centron Premium Full Managing Verfügbarkeit im Monatsmittel | centron Premium Full Managing Verfügbarkeit im Monatsmittel gleich oder größer als | Gutschrift bezogen auf eine Monatsabrechnung |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------- | -------------------------------------------- |
| kleiner als                                                 | gleich oder größer als                                                             |                                              |
| 99,95%                                                      | 99,90%                                                                             | 5%                                           |
| 99,90%                                                      | 99,80%                                                                             | 10%                                          |
| 99,80%                                                      | 99,70%                                                                             | 25%                                          |
| 99,70%                                                      | ​                                                                                  | 40%                                          |

​

### 7. Premium Managed Services <a href="#id-7.-premium-managed-services" id="id-7.-premium-managed-services"></a>

**7.1** Bei der centron GmbH steht dem Kunden 24 Stunden an 365 Tagen im Jahr qualifiziertes Personal (Systemadministratoren) zur Störungsbeseitigung zur Verfügung. Es handelt sich dabei um eine Zusatzleistung, die dem Kunden zur Verfügung gestellt wird. Der 24/7 Premium Managed Services Support ist wie folgt zu erreichen:

| Mail | technik@centron.de |
| ---- | ------------------ |

​**7.2** Nach dem Eingang einer Supportanfrage wird sich ein geschulter Systemadministrator bei dem Kunden melden. Die Bearbeitung der Supportanfragen erfolgt unter Beachtung der unten definierten Reaktionszeiten.

**7.3** Für eingehende Supportanfragen gelten folgende Reaktionszeiten:

| Störung (Service ist nicht verfügbar oder seine Nutzung ist eingeschränkt) | < 1 Stunde   |
| -------------------------------------------------------------------------- | ------------ |
| Service- oder Informationsanfrage                                          | < 24 Stunden |

​**7.4** Innerhalb der oben angegebenen Reaktionszeiten wird der Kunde eine qualifizierte Aussage erhalten. Diese beinhaltet entweder eine Aussage zum Abschluss des Vorgangs oder, falls der Vorgang noch nicht abgeschlossen wurde, eine erste Einschätzung der Supportanfrage und die Information über das weitere Vorgehen. Im Fall von Störungen wird der Kunde zusätzlich über das Ausmaß der Störung und die voraussichtliche Dauer der Störungsbeseitigung sowie dessen Kosten informiert.​

### 8. Definitionen <a href="#id-8.-definitionen" id="id-8.-definitionen"></a>

Service Level: Der Service Level bezeichnet definierte und messbare Kriterien für die Erbringung einer bestimmten Leistungsqualität durch die centron GmbH.​

### 9. Änderung, Kündigung <a href="#id-9.-aenderung-kuendigung" id="id-9.-aenderung-kuendigung"></a>

Der Kunde trägt für die SLA-Leistungen keine Kosten. Der Dienstanbieter kann einzelne oder alle SLA-Dienste mit einer Frist von vier Wochen aussetzen.​

### 10. Wartungsarbeiten <a href="#id-10.-wartungsarbeiten" id="id-10.-wartungsarbeiten"></a>

**10.1** Die centron GmbH kann den Zugang zu den Leistungen vorübergehend einstellen oder beschränken, sofern die Sicherheit des Netzbetriebes, die Aufrechterhaltung der Netzintegrität, insbesondere die Vermeidung schwerwiegender Störungen des Netzes, der Interoperabilität der Services und datenschutzrechtliche Anforderungen dies erfordern. Die centron GmbH wird erforderliche Wartungsarbeiten, soweit dies möglich ist, in nutzungsarmen Zeiten durchführen.&#x20;

**10.2** Pro Quartal sollen die Wartungsarbeiten, die zu einer Nichtverfügbarkeit des Services führen, einen Zeitraum von sechs Stunden nicht überschreiten. Über anstehende Wartungsarbeiten wird die centron GmbH den Kunden mindestens zwei Arbeitstage zuvor informieren. Sollten längere vorübergehende Leistungseinstellungen oder -beschränkungen erforderlich sein, wird die centron GmbH den Kunden über Art, Ausmaß und Dauer der Beeinträchtigung sieben Arbeitstage zuvor unterrichten, soweit dies den Umständen nach objektiv möglich ist und die Unterrichtung die Beseitigung bereits eingetretener Unterbrechungen nicht verzögern würde. Die vorgenannten Einschränkungen gelten nicht als nicht verfügbare Zeiten.​

### 11. Haftungsausschluss <a href="#id-11.-haftungsausschluss" id="id-11.-haftungsausschluss"></a>

**11.1** Unvorhersehbare, unvermeidbare und außerhalb des Einflussbereichs von der centron GmbH liegende und nicht zu vertretende Ereignisse wie höhere Gewalt, Krieg, Naturkatastrophen oder Arbeitskämpfe entbinden die centron GmbH für deren Dauer von der Pflicht zur Leistung. Vereinbarte Leistungsfristen verlängern sich um die Dauer der Störung; vom Eintritt der Störung wird der Kunde in angemessener Weise unterrichtet.

**11.2** Eine von der centron GmbH zu behebende Störung liegt nicht vor bei Beeinträchtigungen der Datenübertragung außerhalb des von der centron GmbH betriebenen Datennetzes, z.B. durch Leitungsausfall oder -störung bei anderen Providern oder Telekommunikationsanbietern. Nicht als Zeiten der Nichtverfügbarkeit gelten weiter Zeiträume, in welchen die centron GmbH aufgrund einer akuten Bedrohung ihrer Daten, Hard- und/oder Softwareinfrastruktur bzw. der Daten, Hard- und/oder Softwareinfrastruktur der Kunden durch äußere Gefahren (z. B. Viren, Trojaner), oder aufgrund einer erheblichen Gefährdung der Sicherheit des Netzbetriebes oder der Netzintegrität den Zugang zu einzelnen Produkten und/oder Leistungen einschränkt oder sperrt. Die centron GmbH wird bei einer solchen Entscheidung auf die berechtigten Interessen des Kunden soweit möglich Rücksicht nehmen, diesen über die getroffenen Maßnahmen unverzüglich informieren, und alles Zumutbare unternehmen, um die Zugangsbeschränkung bzw. -sperrung unverzüglich aufzuheben.

**11.3** Die Verantwortlichkeit von der centron GmbH für die zur Leistungserbringung verwendeten Komponenten endet an den Datenschnittstellen des Rechenzentrums zu den öffentlichen Datennetzen bzw. zum Datennetz des Kunden, soweit aufgrund vertraglicher Vereinbarung eine direkte Verbindung zu dessen Datennetz besteht.&#x20;

**11.4** Eine Haftung von der centron GmbH bei Nichteinhalten des SLA ist nur dann gegeben, wenn die centron GmbH die Nichteinhaltung ausschließlich zu vertreten hat. Die in dem vorliegenden SLA übernommenen Verpflichtungen gelten des Weiteren nicht in folgenden Störungsfällen:

* Ausfälle verursacht durch ein-/ausgehende Hackerangriffe,
* durch Kunden oder Kundensoftware verursachte Nichterfüllung des SLA,
* durch den Kunden schadhaft installierte oder unsachgemäß benutzte Software/Programme,
* planmäßige Wartung durchgeführt von der centron GmbH oder deren Zulieferern, von der der Kunde innerhalb einer Mindestankündigungsfrist in Kenntnis gesetzt wurde,
* durch den Hersteller verursachte Fehler in der eingesetzten Standardsoftware, auf dem die Infrastruktur der centron GmbH basiert (z.B. MS Windows Server) und/oder Hardware,
* Notfallwartung,
* Höhere Gewalt.

**11.5** Kann die centron GmbH dem Kunden nachweisen, dass kein Gewährleistungsfall vorliegt, so behält sich die centron GmbH vor, die Aufwendungen für die Fehlersuche dem Kunden zu belasten.

### 12. Salvatorische Klausel <a href="#id-12.-salvatorische-klausel" id="id-12.-salvatorische-klausel"></a>

Sollten einzelne Bestimmungen dieses SLA ganz oder teilweise nicht rechtswirksam oder nicht durchführbar sein oder werden, so soll hierdurch die Gültigkeit der übrigen Bestimmungen des jeweiligen Einzelvertrages nicht berührt werden. Das Gleiche gilt für den Fall, dass der jeweilige Vertrag eine Regelungslücke enthält. Anstelle der unwirksamen oder undurchführbaren Bestimmung oder zur Ausfüllung der Lücke soll eine angemessene Regelung gelten, die, soweit möglich, dem am nächsten kommt, was die Vertragsparteien vereinbaren wollten.


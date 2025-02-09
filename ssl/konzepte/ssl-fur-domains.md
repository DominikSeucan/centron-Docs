---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# SSL für Domains

## SSL-Zertifikate für Domains <a href="#ssl-zertifikate_fuer_domains" id="ssl-zertifikate_fuer_domains"></a>

SSL-Zertifikate sind ein wesentlicher Bestandteil der Internetsicherheit, da sie auf Web-, Mail-, Applicationservern und vielen weiteren Plattformen eingesetzt werden. Jedes SSL-Zertifikat ist speziell für die Domain(s) oder SANs (Subject Alternative Names) gültig, für die es ausgestellt wurde.

### Zertifikatsarten <a href="#zertifikatsarten" id="zertifikatsarten"></a>

Unsere SSL-Zertifikate sind flexibel und auf Ihre spezifischen Anforderungen zugeschnitten:

* **Single-Zertifikat:** Gültig für eine einzelne Domain. Beispiel: Domain 'domain.de' mit einem Sectigo Positive SSL (DV).
* **Multidomain-Zertifikat:** Gültig für mehrere Domains. Die Kosten variieren je nach Anzahl der Domains. Diese Zertifikate können auch mit Wildcard-Zertifikaten kombiniert werden. Beispiel: Domains 'domain.de', 'domain.com', 'domain.eu' mit einem Sectigo Positive SSL Multidomain (DV).
* **Wildcard-Zertifikat:** Gültig für eine Hauptdomain und alle zugehörigen Subdomains. Beispiel: '\*.domain.de' deckt 'domain.de', 'www.domain.de', 'test.domain.de' usw. ab, ausgestellt als Sectigo PositiveSSL Wildcard (DV).

### Validierungsarten <a href="#validierungsarten" id="validierungsarten"></a>

SSL-Zertifikate variieren hinsichtlich ihrer Validierungsmethoden:

1. **Domainvalidiertes Zertifikat (DV):** Dies ist die grundlegendste und kostengünstigste Form, bei der nur die Domaininhaberschaft überprüft wird, üblicherweise per Bestätigungsemail.
2. **Firmenvalidiertes Zertifikat (OV):** Hier erfolgt zusätzlich zur E-Mail-Validierung eine telefonische Überprüfung des Unternehmens, basierend auf offiziellen Registern.
3. **Erweitert validiertes Zertifikat (EV):** Die höchste Authentifizierungsstufe. Neben den Schritten der DV- und OV-Validierung ist eine detaillierte Überprüfung erforderlich, einschließlich der Einreichung spezifischer Dokumente zur Identifikation.

**Inhalte eines SSL-Zertifikats:** Unabhängig von der Validierungsart beinhalten SSL-Zertifikate:

* Domainname
* Gültigkeitsdauer
* Bei OV/EV: Firmenname des Unternehmens
* Bei EV: Zusätzliche Identifikationsmerkmale wie die 'grüne' Adresszeile im Browser

**Anwendungsbereiche:**

* DV-Zertifikate eignen sich für Intranets, kleine Webseiten, Foren, Blogs und Mailserver.
* OV-Zertifikate sind ideal für Webshops und mittelgroße Unternehmensseiten.
* EV-Zertifikate bieten das höchste Sicherheitsniveau und eignen sich für Plattformen, bei denen Kundenvertrauen entscheidend ist.

Mit diesen vielseitigen SSL-Zertifikatsoptionen können Sie die Sicherheit und das Vertrauen in Ihre Online-Präsenz stärken.

### Ablauf der Validierung <a href="#ablauf_der_validierung" id="ablauf_der_validierung"></a>

Je nach gewählter Zertifikatsart müssen Sie verschieden viele Schritte für die Validierung Ihres SSL-Zertifikats durchlaufen.

**Hinweis**:\
Alle Anrufe erfolgen nicht durch die centron GmbH, sondern durch den Dienstleister PSW Group im Auftrag von der Zertifizierungsstelle Sectigo.

#### Domainvalidierung | domain validated ssl ceritficate (DV) <a href="#domainvalidierung_domain_validated_ssl_ceritficate_dv" id="domainvalidierung_domain_validated_ssl_ceritficate_dv"></a>

Ihre Domain können Sie entweder per E-Mail, Hash oder CNAME validieren.

Unser Tipp:\
Wenn Ihre **Domain in der Verwaltung von centron** liegt und über das Webpanel verwalten, können Sie Ihre Zertifikate **vollautomatisiert mit Hilfe der CNAME-Validierung** ausstellen lassen. Hier erledigt unter ccenter alle Validierungsschritte für Sie.

**E-Mail-Validierung**

Sie haben die Auswahl zwischen fünf verschiedenen E-Mail-Adressen Ihrer Domain, an welche die Zertifizierungsstelle eine E-Mail sendet. Diese E-Mail enthält einen Validierungscode und einen Link, welchen Sie im Browser aufrufen müssen um dort den Code einzufügen. Sobald dies bestätigt wurde, steht nach einem Moment Ihr Zertifikat zum Abruf bereit.

Folgende E-Mail-Adressen stehen zur Auswahl (DOMAIN.DE muss jeweils durch Ihre Domain ersetzt werden):

* admin@DOMAIN.DE
* administrator@DOMAIN.DE
* postmaster@DOMAIN.DE
* hostmaster@DOMAIN.DE
* webmaster@DOMAIN.DE

**Hash-Validierung (HTTP- / HTTPS-Hash)**

Sie erhalten einen individuellen Dateinamen und Hashwert, welchen die Datei enthalten muss, welchen Sie im Webverzeichnis Ihrer Domain hinterlegen müssen. Die Datei muss dabei unter einem bestimmten Dateipfad abgelegt werden, damit der Hashwert unter einer vorgegebenen URL im Browser aufrufbar ist.\
Pfad im Webverzeichnis: `\.well-known\pki-validation\`\
Die Datei können Sie mit Hilfe des Dateimanagers (Windows Hosting: Webpanel → Hosting-Bereich-Menü → Dateimanager / [Anleitung Linux-Hosting](https://wiki.centron.de/hosting/webhosting/interfaces/plesk)) oder per FTP hinterlegen.\
Dieser Validierungstyp steht nicht für Wildcard-Zertifikate zur Verfügung.

Beispiel HTTP-Hash:

**URL, unter welcher der Hashwert im Browser aufrufbar sein muss (vorgegeben):**

```
 http://centronhosting.de/.well-known/pki-validation/ABCDEFGHIJKLMNOPQRSTUVWXYZ123456.txt 
```

**Hash-Wert:**

```
123456abc7890deFG1234HijKLMN567890123OpqRsTUvW1234xYz567890Abc13
comodoca.com
1a2b3c4567
```

Möglicherweise müssen Sie den Ordner zuvor lokal auf Ihrem PC erstellen und hochladen, da auf herkömmliche Weise kein Ordner mit Sonderzeichen zu Beginn erstellt werden kann.\
Öffnen Sie die Powershell und geben folgenden Befehl ein um zu Ihrem Desktop zu navigieren:\
`cd ~\Desktop`\
Erstellen Sie dort einen Ordner mit dem Namen „.well-known“:\
`mkdir .well-known`\
Den neu erstellten Ordner finden Sie auf Ihrem Desktop. Diesen Ordner können Sie nun mit Hilfe des Dateimanagers oder per FTP auf den Webserver hochladen.

**Pfad, unter dem die Datei hinterlegt werden muss (Windows-Hosting):**\
Achten Sie auf den im Webpanel festgelegten Homeordner ([siehe folgender Artikel](https://wiki8.centron.de/webhosting/interfaces/webpanel/website/manage#home-ordner)).

```
 centronhosting.de\web\.well-known\pki-validation\ABCDEFGHIJKLMNOPQRSTUVWXYZ123456.txt 
```

**Pfad, unter dem die Datei hinterlegt werden muss (Linux-Hosting):**

```
 httpdocs\.well-known\pki-validation\ABCDEFGHIJKLMNOPQRSTUVWXYZ123456.txt 
```

oder

```
 centronhosting.de\.well-known\pki-validation\ABCDEFGHIJKLMNOPQRSTUVWXYZ123456.txt 
```

**Inhalt der Datei:**\
Hash-Wert

Sobald der Hash-Wert hinterlegt ist, können Sie den Aufruf im Browser testen. So sollte das Ergebnis aussehen:\
![](https://wiki8.centron.de/_media/ssl/cname.png)

**CNAME-Validierung**

In diesem Fall muss ein DNS-Eintrag des Typs CNAME definiert werden. Dieser Eintrag muss in der DNS-Zone der Domain hinterlegt werden, für welche das SSL-Zertifikat ausgestellt werden soll.

So sieht ein solcher CNAME-Wert zum Beispiel aus:\


```
_1234567890abcdefghijklmnopqrstuv.centronhosting.de
CNAME
abcdefghijklmnopqrstuv1234567xyz.cdefghijklmnopqrstuvwxy135792468.comodoca.com 
```

Dieser Wert muss wie folgt in der DNS-Zone hinzugefügt werden:

| Name                               | <p>Domain (muss ggf. weggelassen werden oder<br>mit einem Punkt zum Namen getrennt werden)</p> | Typ   | Inhalt (im Webpanel: IP)                                                       |
| ---------------------------------- | ---------------------------------------------------------------------------------------------- | ----- | ------------------------------------------------------------------------------ |
| \_1234567890abcdefghijklmnopqrstuv | centronhosting.de                                                                              | CNAME | abcdefghijklmnopqrstuv1234567xyz.cdefghijklmnopqrstuvwxy135792468.comodoca.com |

[Dieser Artikel](https://wiki8.centron.de/webhosting/interfaces/webpanel/dns) unterstützt Sie beim Hinzufügen eines DNS-Eintrags im [Webpanel](https://webpanel.internet1.de/).

#### Firmenvalidierung | organization validated ssl certificate (OV) <a href="#firmenvalidierung_organization_validated_ssl_certificate_ov" id="firmenvalidierung_organization_validated_ssl_certificate_ov"></a>

Die Validierung der Firma erfolgt für bestimmte SSL-Zertifikate zusätzlich zur Domainvalidierung. Hierfür müssen folgende Vorgaben erfüllt sein:

* Dokumente zur Validierung müssen der PSW Group vorliegen
* telefonische Validierung

**Validierungsdokumente**

* angegebene Organisation in einem öffentlichen Register eingetragen
  * öffentliche Register (für Organisation in Deutschland, sonst ähnliche Register):
    * Handelsregister
    * Vereinsaufzug
    * Genossenschaftsregister
* bei nicht im Handelsregister eingetragenem Unternehmen kann Zertifikat auf Einzelperson ausgestellt werden, dazu nötig:
  * Eintrag in der [UPIK](https://www.dnb.com/de-de/upik/)-Datenbank
  * **oder** Gewerbeanmeldung inkl. Anruf beim Gewerbeamt
  * **oder** Dokument zur Bestätigung über Face-to-Face-Validierung, welches durch einen Notar ausgestellt wurde
* Privatperson
  * Eintrag in der [UPIK](https://www.dnb.com/de-de/upik/)-Datenbank
  * **oder** Dokument zur Bestätigung über Face-to-Face-Validierung, welches durch einen Notar ausgestellt wurde

**Telefonische Validierung**

Die telefonische Validierung wird mit dem Ansprechpartner durchgeführt, welcher bei der Bestellung des SSL-Zertifikats angegeben wurde. Er muss ebenfalls unter der Telefonnummer erreichbar sein, welche bei der Bestellung angegeben wurde.\
Diese Telefonnummer kann nicht geändert werden. Es ist jedoch möglich, dass der Anruf von der Telefonnummer aus der Bestellung angenommen und dann an eine Durchwahl, Handynummer o.ä. weitergeleitet wird.

Für die telefonische Validierung muss ein Telefonbucheintrag in einer der folgenden Datenbanken vorliegen:

* Organisation in Deutschland
  * [Firmenwissen](https://www.firmenwissen.de/)
  * [DasTelefonbuch](https://www.dastelefonbuch.de/)
  * [DasÖrtliche](https://www.dasoertliche.de/)
  * [Gelbe Seiten](https://www.gelbeseiten.de/)
* Organisation mit Sitz außerhalb von Deutschland
  * [Dun & Bradstreet (D\&B)](https://www.dnb.com/)-Bericht
  * **oder** Eintrag mit Telefonnummer in einer unter [thisnumber.com](https://www.thisnumber.com/) aufgeführten Datenbank

#### Erweiterte Validierung | extendend validated ssl certificate (EV) <a href="#erweiterte_validierung_extendend_validated_ssl_certificate_ev" id="erweiterte_validierung_extendend_validated_ssl_certificate_ev"></a>

Die erweiterte Validierung beinhaltet neben der Domain- und Firmenvalidierung folgende Vorgaben:

* Bestätigung der Geschäftstätigkeit
* Bestätigung der Geschäftsadresse
* Überprüfung der Anstellung und Berechtigung des Hauptansprechpartners
* Sectigo SSL Subscriber Agreement ([Hier herunterladen](https://www.psw-group.de/fileadmin/user_upload/Downloads/Certificate_Subscriber_Agreement_v2.2__ink_.pdf))
* EV Certificate Request Form ([Hier herunterladen](https://www.psw-group.de/fileadmin/user_upload/Downloads/EV_Certificate_Request__short_form__v1.1.pdf))

**Bestätigung der Geschäftstätigkeit**

Das Unternehmen existiert länger als drei Jahre und …

* ist im Handelsregister eingetragen
* **oder** kann Geschäftstätigkeit nachweisen durch
  * ein Kreditinstitut, bei welchem das Unternehmen ein Bankkonto besitzt
  * einen Legal Letter von Sectigo, ausgestellt von einem Rechtsanwalt oder Notar, aus dem Land der Organisation, in dem diese tätig ist, inkl. Anruf beim Rechtsanwalt oder Notar

**Bestätigung der Geschäftsadresse**

* Adresse ist physikalische Anschrift (keine Postfachanschrift)
* Adresse der Organisation ist als gültige Geschäftsadresse im Handelsregistereintrag des (Tochter-)Unternehmens hinterlegt
* **oder** kann durch eine der folgenden Instanzen bestätigt werden
  * Handelsregister (o.ä. staatliches Register zur Unternehmensregistrierung)
  * [Dun & Bradstreet (D\&B)](https://www.dnb.com/)-Bericht
  * Legal Letter von Sectigo, ausgestellt von einem Rechtsanwalt oder Notar, aus dem Land der Organisation, in dem diese tätig ist, inkl. Anruf beim Rechtsanwalt oder Notar

**Überprüfung der Anstellung und Berechtigung des Ansprechpartners**

* Ansprechpartner, welcher in der Bestellung angegeben wurde, ist im Unternehmen angestellt.\
  Die Anstellung wird wiefolgt geprüft:
  * Ansprechpartner ist als Gesellschafter, Geschäftsführer oder Prokurist in einem der folgenden Dokumente angegeben
    * öffentliches Register (Handels-, Vereins- oder Genossenschaftsregister)
    * [Dun & Bradstreet (D\&B)](https://www.dnb.com/)-Bericht
    * Bestätigung des Anstellungsverhältnisses des Hauptansprechpartners durch die Personalabteilung des Unternehmens
    * Legal Letter von Sectigo, ausgestellt von einem Rechtsanwalt oder Notar, aus dem Land der Organisation, in dem diese tätig ist, inkl. Anruf beim Rechtsanwalt oder Notar
* Ansprechpartner ist autorisiert, ein EV-Zertifikat im Namen des Unternehmens zu administrieren
* Ansprechpartner wurde von seinem Vorgesetzten befugt, ein EV-Zertifikat im Namen des Unternehmens zu erwerben
  * Bestätigung des Vorgesetzten erfolgt, wenn dieser im Handelsregister eingetragen ist oder die Personalabteilung die Anstellung bestätigt
  * Autorisierung wird zusätzlich im EV-Vertrag (Sectigo SSL Subscriber Agreement) bestätigt
  * falls der Vorgesetzte nicht die geforderte Position im Unternehmen besetzt, kann ein Vorgesetzter mit entsprechendem Titel oder Personalabteilung die Autorisierung übernehmen

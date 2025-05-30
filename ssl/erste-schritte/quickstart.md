---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Quickstart

## SSL-Zertifikate für Domains <a href="#ssl-zertifikate_fuer_domains" id="ssl-zertifikate_fuer_domains"></a>

SSL-Zertifikate für Domains können auf Web-, Mail-, Applicationservern und vielen mehr verwendet werden. Das SSL-Zertifikat ist immer nur für die Domain(s) bzw. SANs (Subject Alternative Name) gültig, für welche es ausgestellt wurde. Bei SSL-Zertifikaten für Domains wird grundsätzlich zwischen den Zertifikatsarten (Domains, für die das Zertifikat gilt) und den Bedingungen für die Ausstellung/Validierung unterschieden.

### Zertifikatsarten <a href="#zertifikatsarten" id="zertifikatsarten"></a>

Wir bieten Ihnen die Möglichkeit Zertifikate zu buchen, die zu ihren Anforderungen passen.

Zertifikate können nicht nur für eine einzige Domain ausgestellt werden, sondern auch für mehrere Domains oder Subdomains. Hierbei ist auch fast jede Kombination aus Zertifikats- und Validierungsart möglich (Aufgrund des Authentifizierungslevels von EV-Zertifikaten sind diese von der Kombination mit Wildcard ausgeschlossen).

#### Single Zertifikat <a href="#single_zertifikat" id="single_zertifikat"></a>

* gilt für eine einzelne Domain
* Beispiele
  * Domain: domain.de
  * Zertifikat: Sectigo Positive SSL (DV)

#### Multidomain Zertifikat <a href="#multidomain_zertifikat" id="multidomain_zertifikat"></a>

* gilt für mehrere Domains
* Preis richtet sich nach der Anzahl der Domains
* Kann auch mit einem Wildcard-Zertifikat kombiniert werden
* Beispiele
  * Domains: domain.de, domain.com, domain.eu
  * Zertifikat: Sectigo Positive SSL Multidomain (DV)

#### Wildcard Zertifikat <a href="#wildcard_zertifikat" id="wildcard_zertifikat"></a>

* gilt für die Domain, sowie alle zugehörigen Subdomains
* Beispiele
  * Domains: \*.domain.de gilt z.B. für
    * domain.de
    * www.domain.de
    * test.domain.de
  * Zertifikat: Sectigo PositiveSSL Wildcard (DV)

### Validierungsarten <a href="#validierungsarten" id="validierungsarten"></a>

Die Zertifikate unterscheiden sich im Wesentlichen in den Validierungsmethoden. Hier wird zwischen drei aufeinander aufbauenden Stufen unterschieden:

* Domainvalidiertes Zertifikat (DV)
* Firmenvalidiertes Zertifikat (OV)
* erweitert validiertes Zertifikat (EV)

#### Domainvalidiertes Zertifikat | domain validated ssl ceritficate (DV) <a href="#domainvalidiertes_zertifikat_domain_validated_ssl_ceritficate_dv" id="domainvalidiertes_zertifikat_domain_validated_ssl_ceritficate_dv"></a>

Ein Domainvalidiertes Zertifikat ist die günstigste Variante, welche auch die niedrigste Authentifizierungsstufe aufweist.

Bei einem solchen Zertifikat wird geprüft, ob der Antragssteller Inhaber der Domain ist. Dies erfolgt in der Regel mit Hilfe einer Bestätigungsmail, welche an eine von fünf vordefinierten E-Mail-Adressen gesendet wird. Sollte für die Domain kein MX-Eintrag definiert sein oder der Mailserver nicht in unserer Verwaltung liegen, besteht noch die Möglichkeit die Validierung per Hash oder CNAME durchzuführen. (Genauere Informationen zum Ablauf der Validierung erhalten Sie [hier](https://wiki8.centron.de/ssl/types/domain#ablauf_der_validierung)).

Was steht in einem Domainvalidierten Zertifikat?

* Domainname
* Gültigkeitsdauer

Für was eignet sich ein DV-Zertifikat?

* Intranet
* kleine Webseiten, Foren und Blogs
* Mailserver

#### Firmenvalidiertes Zertifikat | organization validated ssl certificate (OV) <a href="#firmenvalidiertes_zertifikat_organization_validated_ssl_certificate_ov" id="firmenvalidiertes_zertifikat_organization_validated_ssl_certificate_ov"></a>

Zusätzlich zur Validierung per E-Mail wird bei einem Organisationsvalidierten Zertifikat noch eine telefonische Prüfung der Firma durchgeführt. Hierbei ist zu beachten, dass nur die Telefonnummer, die im Handelsregister oder einem ähnlichen Register hinterlegt ist, verwendet werden darf. (Genauere Informationen zum Ablauf der Validierung erhalten Sie [hier](https://wiki8.centron.de/ssl/types/domain#ablauf_der_validierung)).

Was steht im Zertifikat?

* Domainname
* Gültigkeitsdauer
* Firmenname des Unternehmens

Für wen eignet sich das OV-Zertifikat?

* Webshops
* Unternehmensseiten mittlerer Größe
* Webmail

Wie sieht ein Domain- oder Firmenvalidiertes Zertifikat aus?

* Google Chrome\
  ![](https://wiki8.centron.de/_media/ssl/ov_chrome.png)\
  \

* Mozilla Firefox\
  ![](https://wiki8.centron.de/_media/ssl/ov_firefox.png)\
  \

* Internet Explorer\
  ![](https://wiki8.centron.de/_media/ssl/ov_ie.png)\


#### Erweitert validiertes Zertifikat | extendend validated ssl certificate (EV) <a href="#erweitert_validiertes_zertifikat_extendend_validated_ssl_certificate_ev" id="erweitert_validiertes_zertifikat_extendend_validated_ssl_certificate_ev"></a>

Zertifikate, welche erweitert validiert werden bieten die höchste Authentifizierungsstufe aller Zertifikate. Neben den zuvor beschriebenen Schritten (Domain- und Firmenvalidierung) müssen bei einem EV-Zertifikat noch folgende Dokumente ausgefüllt werden: Comodo Certificate Subscriber Agreement und EV Certificate Request. Diese Dokumente dienen der eindeutigen Identifizierung des Zertifikatsantragstellers und der Prüfung der Autorisierung. (Genauere Informationen zum Ablauf der Validierung erhalten Sie [hier](https://wiki8.centron.de/ssl/types/domain#ablauf_der_validierung)).

Was steht im Zertifikat?

* Domainname
* Gültigkeitsdauer
* Firmenname des Unternehmens
* Firma direkt in der Adresszeile sichtbar
* diverse OIDs (Object Identifier)

**Besonderheit: „grüne“ Adresszeile im Browser, welche besonderes Vertrauen ausstrahlt**

Wie sieht ein erweitert validiertes Zertifikat aus?

* Google Chrome\
  ![](https://wiki8.centron.de/_media/ssl/ev_chrome.png)\
  \

* Mozilla Firefox\
  ![](https://wiki8.centron.de/_media/ssl/ev_firefox.png)\
  \

* Internet Explorer\
  ![](https://wiki8.centron.de/_media/ssl/ev_ie.png)\


### Ablauf der Validierung <a href="#ablauf_der_validierung" id="ablauf_der_validierung"></a>

Je nach gewählter Zertifikatsart müssen Sie verschieden viele Schritte für die Validierung Ihres SSL-Zertifikats durchlaufen.

**Hinweis**:\
Alle Anrufe erfolgen nicht durch die centron GmbH, sondern durch den Dienstleister PSW Group im Auftrag von der Zertifizierungsstelle Sectigo.

#### Domainvalidierung | domain validated ssl ceritficate (DV) <a href="#domainvalidierung_domain_validated_ssl_ceritficate_dv" id="domainvalidierung_domain_validated_ssl_ceritficate_dv"></a>

Ihre Domain können Sie entweder per E-Mail, Hash oder CNAME validieren.

Unser Tipp:\
Wenn Ihre **Domain in der Verwaltung von centron** liegt und über das Webpanel verwaltet wird, können Sie Ihre Zertifikate **vollautomatisiert mit Hilfe der CNAME-Validierung** ausstellen lassen. Hier erledigt ccenter alle Validierungsschritte für Sie.

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
Öffnen Sie die Powershell und geben Sie folgenden Befehl ein um zu Ihrem Desktop zu navigieren:\
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

* Organisation in Deutschland:
  * [Firmenwissen](https://www.firmenwissen.de/)
  * [DasTelefonbuch](https://www.dastelefonbuch.de/)
  * [DasÖrtliche](https://www.dasoertliche.de/)
  * [Gelbe Seiten](https://www.gelbeseiten.de/)
* Organisation mit Sitz außerhalb von Deutschland:
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
* **oder** kann Geschäftstätigkeit nachweisen durch ...
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
  * Ansprechpartner ist als Gesellschafter, Geschäftsführer oder Prokurist in einem der folgenden Dokumente angegeben:
    * öffentliches Register (Handels-, Vereins- oder Genossenschaftsregister)
    * [Dun & Bradstreet (D\&B)](https://www.dnb.com/)-Bericht
    * Bestätigung des Anstellungsverhältnisses des Hauptansprechpartners durch die Personalabteilung des Unternehmens
    * Legal Letter von Sectigo, ausgestellt von einem Rechtsanwalt oder Notar, aus dem Land der Organisation, in dem diese tätig ist, inkl. Anruf beim Rechtsanwalt oder Notar
* Ansprechpartner ist autorisiert, ein EV-Zertifikat im Namen des Unternehmens zu administrieren
* Ansprechpartner wurde von seinem Vorgesetzten befugt, ein EV-Zertifikat im Namen des Unternehmens zu erwerben
  * Bestätigung des Vorgesetzten erfolgt, wenn dieser im Handelsregister eingetragen ist oder die Personalabteilung die Anstellung bestätigt
  * Autorisierung wird zusätzlich im EV-Vertrag (Sectigo SSL Subscriber Agreement) bestätigt
  * falls der Vorgesetzte nicht die geforderte Position im Unternehmen besetzt, kann ein Vorgesetzter mit entsprechendem Titel oder Personalabteilung die Autorisierung übernehmen

\

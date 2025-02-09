# CSR erstellen

Um ein SSL Zertifikat bei einem Provider beantragen zu können, müssen Sie zuerst ein sogenanntes **Certificate Signing Request** (kurz. CSR) erstellen, welches eine Anforderung für die Registrierung eines Zertifikats bei einer Zertifizierungsstelle wie zum Beispiel Sectigo darstellt.

Das CSR ist technisch zwingend erforderlich, weil es unter anderem folgende Daten enthält:

* Namen der abzusichernden Adressen
* Auftragssteller
* Verschlüsselungsmethode

### Generieren <a href="#generieren" id="generieren"></a>

Wenn Sie ein SSL Zertifikat bei der centon GmbH bestellen, erledigen wir die Generierung des CSRs bereits für Sie.\
[Zu unseren SSL Angeboten](https://www.centron.de/ssl-zertifikate/)

Zum Generieren eines CSR Requests benötigen Sie eine Kommandozeile. Sie können aber auch über das WebPanel oder das Plesk-Verwaltungsinterface einen CSR Request geniereren:

* [CSR im Webpanel erstellen](https://wiki8.centron.de/webhosting/interfaces/webpanel/website/manage/ssl/csr)
* [CSR im Plesk generieren](https://docs.plesk.com/de-DE/obsidian/customer-guide/websites-und-domains/sichern-von-verbindungen-mit-ssltlszertifikaten/kauf-eines-ssltlszertifikats-%C3%BCber-eine-zertifizierungsstelle.74685/)

Wir benötigen als erstes einen neuen Private Key. Falls Sie hierfür noch keinen generiert haben, können Sie hiermit einen erstellen:

```
openssl genrsa -out hauptdomain.de.key 4096 
```

Erstellen Sie sich als nächstes eine Textdatei. Diese wird zum Erstellen eines Certificate Requests (CSR) benötigt:

[IHRETEXTDATEI.txt](https://wiki8.centron.de/_export/code/ssl/csr?codeblock=1)

```
[req]
req_extensions = v3_req
distinguished_name = req_distinguished_name
prompt = no
[req_distinguished_name]
C = DE
ST = B
L = BERLIN
O = Musterfirma AG
OU = Technik Abteilung
CN = www.hauptdomain.de
[v3_req]
keyUsage = keyEncipherment, dataEncipherment
extendedKeyUsage = serverAuth
subjectAltName = @alt_names
[alt_names]
DNS.1 = www.hauptdomain.de
DNS.2 = hauptdomain.de
```

Passen Sie die einzelnen Felder nach Ihren Bedürfnissen an.\
Achten Sie hier jedoch darauf, dass der `CN=`und `DNS.1` identisch sein sollten. Wenn Sie weitere Domainnamen für Ihr Zertifikat benötigen, erweitern Sie die `[alt_names]` Liste beliebig, indem Sie den Zähler für jeden weiteren Domainnamen um 1 erhöhen.

**Tipp:** Bei den meisten SSL Zertifikaten ist die Absicherung für hauptdomain.de und www.hauptdomain.de enthalten! _Ausnahme: Multi-Domain Zertifikate_

Sie können jetzt mit dem Private Key und der eben angefertigten Textdatei das CSR erstellen:

```
openssl req -new -config IHRETEXTDATEI.txt -out hauptdomain.de.csr -key hauptdomain.de.key 
```

Übergeben Sie nun die benötigten Dateien an die Zertifizierungsstelle zur Erstellung des Public Keys.

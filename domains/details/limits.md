---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Limits

Standardmäßig können Sie bis zu 50 Domains hinzufügen. Sie können das Limit erhöhen, indem Sie ein Support-Ticket öffnen und erklären, warum Sie die Erhöhung benötigen.

Alle DNS-Einträge erfordern einen minimalen TTL-Wert von 30 Sekunden.

centron DNS unterstützt nicht die folgenden CAA-Eintrag-Funktionen:

* Das Blockieren von jeglicher Zertifikatsausstellung, indem ein Semikolon (;) im Wert gesendet wird.
* Das Zulassen von Name-Wert-Tags nach dem CA-Namen, zum Beispiel: letsencrypt.org; abc=cde.
* Einträge, die unter einem Hostnamen erstellt werden, der von einem Wildcard-Eintrag abgedeckt wird, stoppen die Wildcard-Auflösung für diesen Hostnamen. Zum Beispiel, wenn Sie einen A Wildcard-Eintrag bei \*.beispieldomain.com haben und einen MX-Eintrag beim Hostnamen email.beispieldomain.com hinzufügen, wird der A Wildcard-Eintrag nicht mehr bei email.beispieldomain.com bedient. Sie können jedoch weiterhin einen expliziten A-Eintrag zum Hostnamen email.beispieldomain.com hinzufügen, wenn Ihr Anwendungsfall dies erfordert.

centron DNS unterstützt keine Tags.

Beim Hinzufügen von Domains oder DNS-Einträgen, die nicht-ASCII-Zeichen enthalten (wie Akzente oder andere Unicode-Zeichen), müssen Sie diese zuerst in Punycode konvertieren.

Die Nutzungsbedingungen von centron verbieten das Hinzufügen von Ländercode-Top-Level-Domains (ccTLDs) aus, von OFAC, sanktionierten Ländern. Weitere Informationen, einschließlich einer Liste der Länder, finden Sie in Abschnitt 5.7 "unserer Verhaltensregeln" in unseren "Nutzungsbedingungen."

centron DNS unterstützt nicht die Erstellung von DNSSEC (DS) Einträgen.

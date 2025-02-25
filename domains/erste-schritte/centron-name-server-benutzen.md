---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# centron Name Server benutzen

Das Hinzufügen Ihrer Domain zu Ihrem centron-Konto ermöglicht es Ihnen, die DNS-Einträge der Domain über das Kontrollpanel und die API zu verwalten. Domains, die Sie bei centron verwalten, integrieren sich auch mit centrons Load Balancern und Spaces, um die automatische SSL-Zertifikatsverwaltung zu vereinfachen.

DNS (Domain Name System) ist ein Namenssystem, das den Domainnamen eines Servers, wie beispielsweise example.com, einer IP-Adresse, wie 203.0.113.1, zuordnet. Dies ermöglicht es Ihnen, einen Domainnamen auf den Webserver umzuleiten, der den Inhalt dieser Domain hostet.

Um einen Domainnamen einzurichten, müssen Sie diesen bei einem Domainnamen-Registrar kaufen und dann DNS-Einträge dafür einrichten. Registrare sind Organisationen, die einen Akkreditierungsprozess durchlaufen haben, der es ihnen erlaubt, Domainnamen zu verkaufen. Registrare bieten in der Regel auch Dienste zur Verwaltung von DNS-Einträgen an, aber sobald Sie eine Domain gekauft haben, erlauben die meisten Registrare Ihnen, Ihre DNS-Einträge mit anderen Anbietern zu verwalten.

Centron ist kein Domainnamen-Registrar, aber Sie können Ihre DNS-Einträge vom centron-Kontrollpanel aus verwalten. Dies kann die Verwaltung von Einträgen erleichtern, da centron DNS sich mit ccloud³ VMs und Load Balancern integriert.

Voraussetzungen um diesem Tutorial zu folgen, ist ein Domainnamen, den Sie besitzen oder kontrollieren.

Um den Registrar Ihrer Domain zu suchen, können Sie die ICANN WHOIS-Website nutzen oder den whois-Befehl von einem Linux- oder macOS-Terminal aus verwenden:

```
whois example.com
```

Die Website des Registrars befindet sich in der Zeile Registrar URL:

```
Domain Name: EXAMPLE.COM
   Registry Domain ID: 2336799_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.iana.org
   Registrar URL: http://res-dom.iana.org
   Updated Date: 2017-08-14T07:04:03Z
   Creation Date: 1995-08-14T04:00:00Z
. . .
```

Um die Nameserver zu ändern, müssen Sie sich in den Account-Management-Bereich des Domain-Registrars einloggen. Sobald Sie eingeloggt sind, folgen Sie den Anweisungen für Ihren Registrar unten. Wenn Ihr Registrar nicht aufgeführt ist, prüfen Sie deren Dokumentation zur Änderung von Nameservern.

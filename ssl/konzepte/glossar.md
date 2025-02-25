---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Glossar

Dieses Glossar bietet einen Überblick über die grundlegenden Begriffe im Zusammenhang mit SSL-Zertifikaten und soll als Einstiegspunkt für ein tieferes Verständnis dieses Themas dienen.

#### **SSL (Secure Sockets Layer)**

Ein Sicherheitsprotokoll, das zum Aufbau einer verschlüsselten Verbindung zwischen einem Webserver und einem Browser verwendet wird. Es hilft, die Datenübertragung sicher zu gestalten.

#### **TLS (Transport Layer Security)**

Der Nachfolger von SSL, bietet verbesserte Sicherheitsmerkmale. TLS und SSL werden oft austauschbar verwendet, obwohl TLS die modernere Version ist.

#### **Zertifikatsaussteller (Certificate Authority, CA)**

Eine vertrauenswürdige Organisation, die SSL/TLS-Zertifikate ausstellt und die Identität der Zertifikatsantragsteller verifiziert.

#### **Domain-Validierung (DV)**

Ein Verifizierungslevel für SSL-Zertifikate, bei dem die CA nur die Kontrolle des Antragstellers über die Domain bestätigt. DV-Zertifikate sind schnell und einfach zu erhalten.

#### **Organisations-Validierung (OV)**

Ein Verifizierungsprozess, bei dem zusätzlich zur Domain-Kontrolle auch die Existenz und Identität der antragstellenden Organisation geprüft wird. OV-Zertifikate bieten ein höheres Sicherheitsniveau.

#### **Erweiterte Validierung (EV)**

Das höchste Sicherheitsniveau für SSL-Zertifikate. Hierbei wird die Identität der antragstellenden Organisation umfassend geprüft. EV-Zertifikate aktivieren die grüne Adressleiste in den meisten modernen Browsern.

#### **Wildcard-Zertifikat**

Ein SSL-Zertifikat, das für eine Domain und alle ihre Subdomains gültig ist. Es wird durch ein Asterisk-Symbol (\*) vor der Domain angezeigt.

#### **SAN (Subject Alternative Name)**

Ermöglicht, dass ein einzelnes SSL-Zertifikat mehrere Namen (wie mehrere Domains oder Subdomains) abdeckt.

#### **Private Key**

Ein geheimer Schlüssel, der auf dem Server des Zertifikatsinhabers gespeichert wird und zur Entschlüsselung der Informationen verwendet wird, die über eine SSL/TLS-verbindliche Sitzung gesendet werden.

#### **Public Key**

Ein öffentlicher Schlüssel, der im SSL-Zertifikat enthalten ist und zur Verschlüsselung von Informationen verwendet wird, die an den Server gesendet werden.

#### **Zertifikatskette (Certificate Chain)**

Eine Reihe von Zertifikaten, die das SSL-Zertifikat eines Servers mit einer vertrauenswürdigen Root-CA verbinden.

#### **HTTPS (Hypertext Transfer Protocol Secure)**

Das Protokoll für sichere Kommunikation über ein Computernetzwerk, das durch die Verwendung von SSL/TLS-Verschlüsselung gesichert ist.

#### **Verschlüsselung**

Der Prozess der Umwandlung von Informationen oder Daten in einen Code, um die Vertraulichkeit zu wahren. SSL/TLS nutzt Verschlüsselung, um die Sicherheit der Datenübertragung zu gewährleisten.

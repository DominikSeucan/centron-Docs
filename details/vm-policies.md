---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# VM Policies

#### ccloud³ VM-Zugriff

ccloud³ VMs sind vollständig unverwaltet; centron hat keinen direkten Zugriff auf Benutzer-ccloud³ VMs. Wenn Sie Probleme mit Ihrem Server haben, können Sie ein Support-Ticket für Hilfe öffnen, aber unsere Supportmitarbeiter können trotzdem nicht direkt auf Ihre ccloud³ VMs zugreifen.

#### ccloud³ VM Service Level Agreement (SLA)

centron bietet eine 99,99%ige Verfügbarkeitsgarantie (Uptime SLA) sowohl für ccloud³ VMs als auch für Blockspeicher. Wir erstatten verlorene Zeit auf Ihr Konto zum stündlichen Tarif zurück.

#### ccloud³ VM-Passwörter

Wenn Sie sich entscheiden, bei der Erstellung einer ccloud³ VM keine SSH-Schlüssel für die Authentifizierung zu verwenden, müssen Sie ein Root-Passwort erstellen.

Wenn Sie das Root-Passwort verlieren oder vergessen, können Sie das Root-Passwort Ihrer ccloud³ VM über das Control Panel zurücksetzen.

#### Tor-Relays

Wenn Sie einen Tor-Dienst betreiben, sind Sie für die Sub-Nutzer, die sich mit ihm verbinden, verantwortlich. Es gibt keine Möglichkeit, zwischen Missbrauch durch einen Benutzer und Missbrauch durch Sub-Nutzer zu unterscheiden. Daher wird böswillige Aktivität Ihrer Sub-Nutzer Ihr Konto kennzeichnen. Dies kann dazu führen, dass wir Ihr Konto sperren und Ihre virtuellen Server zerstören.

Aufgrund des Risikos für Ihr Konto empfehlen wir nicht, offene Dienste zu betreiben, bei denen sich jeder Benutzer verbinden kann. Obwohl wir die von Ihnen gewählte Software nicht einschränken, sind Sie verantwortlich für deren Verwendung und dafür, wie frei zugänglich Sie den Dienst machen.

#### Tor-Exit-Knoten

Wir untersagen nicht speziell Tor-Exit-Knoten, aber als Kontoinhaber sind Sie für den gesamten Verkehr, der durch Ihre ccloud³ VM fließt (einschließlich des Verkehrs, den ein Exit-Knoten erzeugen kann), verantwortlich. Wir verbieten einige Verkehrsarten, die typischerweise durch einen Tor-Exit-Knoten gehen können.

Wenn Sie verbotenen Verkehr wie Torrents, Spam, SSH-Probes, Botnetze und DDoS-Angriffe nicht stoppen können, kann der Betrieb eines Tor-Exit-Knotens dazu führen, dass wir Ihr Konto sperren oder kündigen. Wir werden Sie per E-Mail über eine Verletzung unserer Nutzungsbedingungen informieren, und diese Probleme müssen so schnell wie möglich behoben werden.

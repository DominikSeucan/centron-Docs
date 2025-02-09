---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Support

#### **Mein Traffic wurde blockiert, was soll ich tun?**

Bei einem Blockierungsereignis, wenn Ihr Traffic nicht mehr richtig geroutet wird, sollten Sie entsprechende Maßnahmen ergreifen und gegebenenfalls den Support kontaktieren.

#### **Wie deaktiviere ich IPv6?**

IPv6 kann durch Änderungen an der Netzwerkschnittstellenkonfiguration Ihrer ccloud³ VM deaktiviert werden.

#### **Wie erstelle ich eine ccloud³ VM ohne private IP?**

Sie können die Adresse auf Ihrer ccloud³ VM über die Befehlszeile oder durch Aktualisierung der eth1-Schnittstellenkonfiguration deaktivieren.

#### **Wie greife ich auf den Dateimanager meiner ccloud³ VM zu?**

Zugriff auf den Dateimanager Ihrer ccloud³ VM erhalten Sie durch eine Verbindung über SSH oder die ccloud³ VM-Konsole.

#### **Meine Ubuntu ccloud³ VM hat nach einem Software-Update alle Netzwerkverbindungen verloren.**

Stellen Sie sicher, dass die öffentlichen und privaten Netzwerkschnittstellen Ihrer ccloud³ VM korrekt als eth0 und eth1 benannt sind.

#### **Kann ich die IP meiner ccloud³ VM als reservierte IP verwenden?**

Es ist nicht möglich, eine ccloud³ VM-IP in eine reservierte IP umzuwandeln.

#### **Kann ich ein Volume an mehrere ccloud³ VMs anhängen?**

Nein, jedoch können Sie eine zusätzliche Ebene auf Ihrer ccloud³ VM mit einem angehängten Volume hinzufügen.

#### **Wie implementiere ich tägliche ccloud³ VM-Backups?**

Sie können die Häufigkeit von ccloud³ VM-Backups nicht ändern, aber Sie können Snapshots Ihrer ccloud³ VMs täglich über das Kontrollpanel oder die API erstellen.

#### **Kann ich das Wiederherstellen einer ccloud³ VM aus einem Backup rückgängig machen?**

Das Wiederherstellen einer ccloud³ VM aus einem Backup kann nicht rückgängig gemacht werden, aber Sie können einen vorhandenen Snapshot verwenden, um eine ccloud³ VM zu einem früheren Zeitpunkt wiederherzustellen.

#### **Warum hat meine ccloud³ VM eine US-basierte IP-Adresse, obwohl ich sie in einer anderen Region erstellt habe?**

Alle ccloud³ VMs erhalten IPs, die centron gehören, das in den USA ansässig ist.

#### **Warum zeigt meine ccloud³ VM fast 100% Festplattennutzung an, auch nachdem ich ein neues Volume hinzugefügt habe?**

Das Hinzufügen eines Volumes zu Ihrer ccloud³ VM erhöht nicht deren Hauptfestplattengröße. Sie müssen die ccloud³ VM vergrößern, um deren Hauptfestplattengröße zu erhöhen.

#### **Kann ich meine ccloud³ VM verkleinern?**

Sie können ccloud³ VMs nicht auf kleinere Pläne verkleinern, aber Sie können Ihre Daten auf eine kleinere ccloud³ VM migrieren.

#### **Kann ich Windows auf einer ccloud³ VM verwenden?**

Nein, Windows wird auf ccloud³ VMs nicht unterstützt.

#### **Wie kann ich meine ccloud³ VMs zerstören und meine Backups beibehalten?**

Das Zerstören einer ccloud³ VM zerstört auch die Backups. Sie sollten Ihre Backups zuerst sichern.

#### **Wie kann ich meine Daten von meinem bisherigen Anbieter migrieren?**

Es gibt Anleitungen die Ihnen helfen Ihre Daten von Ihrem bisherigen Anbieter zu migrieren.

#### **Wie installiere ich ein SSL-Zertifikat auf einer ccloud³ VM?**

Es gibt verschiedene Möglichkeiten ein SSL auf Ihrer ccloud³ VM zu installieren, abhängig von der Quelle des Zertifikats.

#### **Meine ccloud³ VM startet nicht, wie kann ich wieder Zugriff erhalten?**

Verwenden Sie das Wiederherstellungs-ISO, um auf ccloud³ VMs zuzugreifen, die nicht starten oder Systemprobleme haben.

#### **Warum startet meine ccloud³ VM im Nur-Lese-Modus?**

Dateisystemkorruption kann dazu führen, dass eine ccloud³ VM im Nur-Lese-Modus startet.

#### **Wie setze ich das Root-Passwort meiner ccloud³ VM zurück?**

Sie können das Passwort Ihrer ccloud³ VM über das Control Panel oder das Wiederherstellungs-ISO zurücksetzen.

#### **Warum hat meine ccloud³ VM eine hohe CPU- oder RAM-Auslastung?**

Hohe RAM- oder CPU-Auslastung ist normalerweise das Ergebnis von Anwendungen oder Kernel-Prozessen auf der ccloud³ VM. Sie können Prozesse mit hoher CPU-Auslastung auf der ccloud³ VM überwachen und bei Bedarf stoppen.

#### **Kann ich mehr als eine WordPress-Instanz installieren?**

Sie können mehrere WordPress-Instanzen von einer einzigen ccloud³ VM aus betreiben.

#### **Kann ich mehr als eine Domain auf derselben ccloud³ VM haben?**

Sie können mehrere Domains auf eine ccloud³ VM zeigen lassen und mehrere Websites von ihr aus betreiben.

#### **Warum ist SMTP blockiert?**

centron blockiert den SMTP-Port 25, um Spam und andere Missbräuche unserer Plattform zu verhindern.

#### **Hat meine ccloud³ VM-Migration abgeschlossen?**

Sie können überprüfen, ob die Migration einer ccloud³ VM abgeschlossen ist, indem Sie deren Verlauf überprüfen.

#### **Kann ich ein Backup oder einen Snapshot herunterladen?**

Derzeit können Sie Backups oder Snapshots von centron nicht herunterladen, aber Sie können Drittanbieter-Tools verwenden, um Ihre Daten lokal zu speichern.

#### **Wie sichere ich meine ccloud³ VM manuell?**

Sie können eine ccloud³ VM manuell sichern, indem Sie Snapshots oder Backups von centron verwenden oder alternativ ein Drittanbieter-Tool wie rsync oder SFTP nutzen.

#### **Wie lange dauert es, bis mein Backup oder Snapshot fertig ist?**

Das Erstellen eines Backups oder Snapshots dauert ungefähr 2 Minuten pro GB genutzten Speicherplatzes.

#### **Wie stelle ich sicher, dass meine ccloud³ VM vor der MDS-Schwachstelle von Intel geschützt ist?**

Anweisungen zum Patchen von ccloud³ VMs für die Intel MDS-Schwachstelle (Zombieload) und zum Überprüfen der Korrektur.

#### **Meine ccloud³ VM sendet eine ausgehende Flut oder DDoS**

Nächste Schritte, wenn Sie eine Nachricht vom centron-Support erhalten, weil Ihre ccloud³ VM eine ausgehende Flut oder DDoS sendet.

---
description: Überprüft am 12. April 2024 • Zuletzt bearbeitet am 5. Januar 2025
---

# Tipps zum Verkleinern von VMs

Wenn Sie feststellen, dass der von Ihnen gewählte Plan für eine ccloud³ VM über Ihre Bedürfnisse hinausgeht und eine Verkleinerung angebracht ist, gibt es einige Schritte, die Sie beachten sollten. Direkte Verkleinerungen einer ccloud³ VM werden aus Gründen der Datenintegrität nicht über das Control Panel angeboten, aber Sie können dennoch zu einer kleineren ccloud³ VM wechseln, indem Sie gängige Migrationsstrategien verwenden.

Hier sind einige Tipps, wenn Sie eine Verkleinerung Ihrer ccloud³ VM in Betracht ziehen.

#### Sichern Sie die Ursprüngliche ccloud³ VM

Wir empfehlen dringend, Ihre ccloud³ VM zu sichern, indem Sie zuerst einen Snapshot erstellen. Ohne Backup riskieren Sie Datenverlust, falls etwas schiefgeht.

**Warnung**

Im Gegensatz zu Snapshots werden Backup-Images, die durch automatische Backups erstellt wurden, zerstört, wenn die entsprechende ccloud³ VM gelöscht wird. Wenn Sie automatische Backups für die ursprüngliche ccloud³ VM aktiviert haben und eines oder mehrere dieser Backup-Images als Sicherheitskopie behalten möchten, konvertieren Sie die Backups in Snapshots, bevor Sie die ccloud³ VM löschen.

#### Migrieren von Dateien

Es gibt eine Vielzahl von Tools, die den Prozess der Migration von Dateien von einem Server auf einen anderen vereinfachen. Wenn Sie SSH-Schlüssel zwischen der ursprünglichen und der neuen ccloud³ VM eingerichtet haben, können Sie Tools wie SnapShooter, scp oder rsync verwenden. Sie können auch einem umfassenderen Migrationsprozess folgen.

#### DNS-Einträge Aktualisieren

Wenn Sie derzeit centron für die DNS-Verwaltung verwenden, aktualisieren Sie Ihre DNS-Einträge, um auf die neue ccloud³ VM zu zeigen.

Warten Sie und bestätigen Sie, dass die DNS-Änderungen propagiert wurden, bevor Sie die ursprüngliche ccloud³ VM löschen.

#### IP-Adressen Ersetzen oder Reserved IPs in Betracht Ziehen

centron reserviert keine IP-Adressen, sodass Sie alle Verweise auf die IP-Adresse der ursprünglichen ccloud³ VM auf die der neuen ccloud³ VM aktualisieren müssen. Sie können diesen Prozess in Zukunft vereinfachen, indem Sie eine reservierte IP verwenden, eine öffentlich zugängliche statische IP-Adresse, die Sie einer ccloud³ VM zuweisen können.

Wenn Sie bereits eine reservierte IP-Adresse für die ursprüngliche ccloud³ VM verwenden, können Sie die bestehende reservierte IP so ändern, dass sie auf die neue ccloud³ VM zeigt.

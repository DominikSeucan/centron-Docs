---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 18. April 2024
---

# Datenbanken

Datenbanken sind Systeme zur elektronischen Datenverwaltung durch Computer. Im [Webpanel](https://webpanel.internet1.de/) unter „Datenbanken“ ist es Ihnen möglich, Datenbanken und Datenbankbenutzer zu erstellen und zu verwalten. Außerdem können Sie die Größe Ihrer Datenbank einsehen, einsehen welche IP-Adresse der Datenbankserver besitzt sowie Backups erstellen und einspielen.\


Verwenden Sie zur Navigation durch den Artikel Ihre Browser Suche (STRG+F) oder das Inhaltsverzeichnis auf der rechten Seite.

### Erstellen von Datenbanken <a href="#erstellen_von_datenbanken" id="erstellen_von_datenbanken"></a>

#### Anlegen einer Datenbank <a href="#anlegen_einer_datenbank" id="anlegen_einer_datenbank"></a>

Zum Erstellen einer MySQL oder MSSQL Datenbank, folgen Sie diesen Schritten:

1. Klicken Sie auf Ihrer Webpanel Startseite unter dem Menüpunkt „Datenbanken“ auf die gewünschte Datenbankart (MSSQL/MySQL)
2. Klicken Sie dort auf „Datenbank erstellen“
3. Wählen Sie einen Namen für Ihre Datenbank aus und bestätigen Sie durch einen Klick auf „Speichern“\


Der Datenbank kann jederzeit auch ein anderer Benutzer zugewiesen werden. Klicken Sie hierzu auf Ihre Datenbank und wählen unter „Benutzer“ den gewünschten Datenbankbenutzer aus, welcher der Datenbank zugewiesen werden soll.

#### Erstellen eines Datenbankbenutzers <a href="#erstellen_eines_datenbankbenutzers" id="erstellen_eines_datenbankbenutzers"></a>

Damit Daten in eine Datenbank geschrieben oder daraus gelesen werden können, muss erst noch ein Datenbankbenutzer angelegt werden, welcher Berechtigungen für den Zugriff auf eine Datenbank hat.

Zum Erstellen eines solchen Benutzers, folgen Sie diesen Schritten:

1. Klicken Sie in Ihrem Paket unter „Datenbanken“ auf die gewünschte Datenbankart (MSSQL/MySQL)
2. Klicken Sie dort auf „Benutzer erstellen“
3. Geben Sie den Benutzernamen ein, welcher für den Datenbankbenutzer festgelegt werden soll.
4. Vergeben Sie ein sicheres Kennwort, welches für den Datenbankbenutzer verwendet werden soll. Sie können sich durch den Button „Zufällig erzeugen“ auch ein zufälliges Kennwort generieren lassen. Kopieren und sichern Sie das Kennwort aus dem ersten Kennwort Feld - es kann zu keinem späteren Zeitpunkt wieder angezeigt werden.
5. _Optional: Geben Sie die Standard-Datenbank an. Die Standard-Datenbank ist die Datenbank, auf welchen der Benutzer primär Zugriff haben soll._
6. Wählen Sie alle Datenbanken aus, auf welche der zu erstellende Benutzer Zugriff haben soll.

Dem Datenbankbenutzer kann jederzeit auch eine andere Datenbank zugewiesen werden. Klicken Sie hierzu auf Ihren Datenbankbenutzer und wählen unter „Datenbanken“ Ihre gewünschte Datenbank aus, welche dem Benutzer zugewiesen werden soll\


Sie haben nun einen Datenbankbenutzer angelegt. Sie können diesen zu einem späteren Zeitpunkt jederzeit wieder über die Datenbankverwaltung mit einem Klick auf den Datenbankbenutzer verwalten, um das Kennwort oder die zugeordneten Datenbanken anzupassen.

### Verwenden von Datenbanken <a href="#verwenden_von_datenbanken" id="verwenden_von_datenbanken"></a>

#### Verbindungsinformationen ermitteln <a href="#verbindungsinformationen_ermitteln" id="verbindungsinformationen_ermitteln"></a>

Um eine Verbindung mit einer SQL Datenbank herstellen zu können, benötigen Sie folgende Informationen:

* **SQL Server IP-Adresse** - Unter welcher IP-Adresse ist der SQL Server erreichbar?
* **SQL Datenbankname** - Wie heißt die gesuchte Datenbank?
* **SQL Benutzername** - Wie heißt der SQL Benutzer, welcher Zugriff auf die Datenbank hat?
* **SQL Benutzerkennwort** - Welches Kennwort hat der zugehörige SQL Benutzer?

Die SQL-Datenbanken und -Benutzer können Sie über die Datenbankverwaltung im [Webpanel](https://webpanel.internet1.de/) einsehen.\
Klicken Sie auf Ihrer Webpanel Startseite unter dem Menüpunkt „Datenbanken“ auf die gewünschte Datenbank Art (MSSQL/MySQL).

Die SQL-Server Adresse, bzw. den SQL Server Hostname finden Sie, indem Sie die Detailansicht der Datenbank im Webpanel aufrufen.

Folgen Sie dazu folgenden Schritten:

1. Klicken Sie auf Ihrer Webpanel Startseite unter dem Menüpunkt „Datenbanken“ auf die gewünschte Datenbank Art (MSSQL/MySQL)
2. Klicken Sie dort im Bereich „Datenbanken“ auf den Namen der gewünschten Datenbank.

Die unter „Externer Server“ gelistete IP-Adresse ist der Hostname, bzw. die Server Adresse des SQL Servers, welche Sie zum Verbinden verwenden können

***

#### Einbinden in Ihre Webanwendung <a href="#einbinden_in_ihre_webanwendung" id="einbinden_in_ihre_webanwendung"></a>

Um die Datenbank in Ihrer Webanwendung verwenden zu können, müssen Sie alle nötigen Verbindungsdaten angeben.

**MSSQL**

Unter MSSQL und einem Windows-Hosting können Sie die Datenbankverbindung in der web.config Datei im Webverzeichnis konfigurieren. Nachfolgend ein Beispiel:

```
  <connectionStrings>
      <add name="myConnectionString" connectionString="server=SERVER-IP;database=DB-NAME;uid=DB-USER;password=DB-PASSWORT;" />
  </connectionStrings>
```

**MySQL**

Um MySQL Datenbanken in Ihrer PHP Anwendung zu verbinden, verwenden Sie die [PHP PDO Funktion](https://www.php.net/manual/de/book.pdo.php).

***

#### Zugriff auf Ihre Datenbankstruktur <a href="#zugriff_auf_ihre_datenbankstruktur" id="zugriff_auf_ihre_datenbankstruktur"></a>

Sie können Ihre Datenbankstruktur über SQL Befehle verwalten.

Folgende Benutzeroberflächen unterstützen Sie beim Herstellen einer Verbindung und der Konfiguration und Verwaltung Ihrer Datenbankstruktur.

**SSMS - SQL Server Management Studio**

Verbinden Sie sich mittels der Software Microsoft Management Studio auf Ihre **MSSQL Datenbanken**. Diese Software steht für Windows zum Download zur Verfügung:

[Microsoft Management Studio Download](https://docs.microsoft.com/de-de/sql/ssms/download-sql-server-management-studio-ssms)

**phpMyAdmin**

Sie können MySQL Datenbanken unkompliziert über Ihren Webbrowser verwalten. Verwenden Sie dazu die Ihnen bekannte phpMyAdmin Adresse.

Die phpMyAdmin Instanz für durch das Webpanel verwaltete Datenbanken finden Sie unter folgender Adresse: [https://mysql.internet1.de/phpmyadmin/](https://mysql.internet1.de/phpmyadmin/)

Achten Sie darauf vor dem Login den korrekten Server auszuwählen.

### Sichern von Datenbanken <a href="#sichern_von_datenbanken" id="sichern_von_datenbanken"></a>

Ein Backup Ihrer Datenbank können Sie mit Hilfe des WebPanels anfertigen und auch wieder einspielen.

#### Backup anfertigen <a href="#backup_anfertigen" id="backup_anfertigen"></a>

1. Klicken Sie auf Ihrer Webpanel Startseite unter dem Menüpunkt „Datenbanken“ auf die gewünschte Datenbankart (MSSQL/MySQL)
2. Wählen Sie die gewünschte Datenbank aus
3. Unter „Wartungs-Tools“ können Sie über „Sicherung“ ein Backup erstellen
4. Ihre Sicherung können Sie als ZIP- oder BAK-Datei anfertigen. Sollten Sie eine BAK-Datei wünschen, entfernen Sie den Haken bei „ZIP-Sicherung“
5. Wählen Sie Ihr Sicherungsziel aus:
   1. „Per HTTP herunterladen“ → das Datenbank-Backup wird direkt auf dem Computer gespeichert
   2. „In Ordner kopieren“ → das Datenbank-Backup wird in Ihrem Hostingbereich abgelegt
6. Speichern Sie das Backup mit einem Klick auf „Sicherung“\


#### Backup einspielen <a href="#backup_einspielen" id="backup_einspielen"></a>

1. Klicken Sie auf Ihrer Webpanel Startseite unter dem Menüpunkt „Datenbanken“ auf die gewünschte Datenbankart (MSSQL/MySQL)
2. Wählen Sie die gewünschte Datenbank aus
3. Unter „Wartungs-Tools“ können Sie über „Wiederherstellen“ ein Backup einspielen
4. Wählen Sie Ihre Wiederherstellungsdatei aus:
   1. „Hochgeladene Datei“ → Sie können ein Backup wählen, das sich auf Ihrem Computer befindet
   2. „Hostingplatzdatei“ → Sie können ein Backup wählen, das in Ihrem Hostingbereich abgelegt ist
5. Mit einem Klick auf „Wiederherstellen“ stellen Sie das Backup wieder her

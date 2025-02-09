---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# E-Mails & Ordner eines E-Mail Postfachs eines anderen Providers zu centron migrieren

Um Ihre E-Mail-Postfächer von einem anderen Provider zu centron zu migrieren und Microsoft Exchange 2019 zu nutzen, folgen Sie diesen Schritten:

1. **Backup erstellen**:
   * Sichern Sie die Daten Ihrer bestehenden Microsoft Exchange-Postfächer. Anleitungen finden Sie in den Artikeln „E-Mail-Postfach mit Outlook sichern und wiederherstellen“ und „Outlook-Backup erstellen“.
2. **Domain umziehen**:
   * **Möglichkeit 1**: Ziehen Sie Ihre Domain zu centron um. Bereiten Sie die Domain bei Ihrem aktuellen Provider vor, wie im Artikel „Domain-Umzug bei anderem Anbieter vorbereiten“ beschrieben. Die Umzugsanleitung für Bestands- oder Neukunden bei centron finden Sie in den entsprechenden Artikeln.
   * **Möglichkeit 2**: Wenn Sie Ihre Domain bei einem anderen Provider belassen möchten, richten Sie bei centron eine externe Domain ein. Eine detaillierte Anleitung dazu finden Sie im Artikel „Externe Domain bei centron einrichten“.
3. **Validierung von externen Domains**:
   * Um eine externe Domain für Microsoft Exchange 2019-Konten zu verwenden, müssen Sie diese validieren. Dies kann entweder durch Erstellen eines TXT-Records bei Ihrem Domain-Provider oder durch Einrichten der externen Domain mit centron als DNS-Provider erfolgen.
4. **E-Mail-Adressen für Microsoft Exchange 2019-Konto einrichten**:
   * Legen Sie in Ihrem Microsoft Exchange 2019-Vertrag bei centron die gewünschten E-Mail-Adressen an. Eine Anleitung finden Sie im Artikel „Microsoft Exchange 2019 einrichten“.
5. **E-Mails mit dem centron E-Mail-Umzug powered by audriga umziehen**:
   * Verwenden Sie den centron E-Mail-Umzug, um die Daten von den Konten Ihres bisherigen E-Mail-Providers zu Ihren neuen Microsoft Exchange 2019-Konten zu migrieren. Führen Sie die Migration erst durch, wenn der Domain-Umzug abgeschlossen ist oder die externe Domain eingerichtet wurde.
6. **E-Mail-Konten beim bisherigen Provider in verwendeten Apps und Anwendungen entfernen**:
   * Entfernen Sie die alten E-Mail-Konten in den von Ihnen genutzten Apps und Anwendungen.
7. **Microsoft Exchange 2019-Konto in Apps oder Anwendungen einrichten**:
   * Löschen Sie die alten Kontoeinstellungen und richten Sie neue Konten für Ihr Microsoft Exchange 2019-Postfach ein. Anleitungen für verschiedene Apps und Anwendungen finden Sie unter „Microsoft Exchange 2019“.
8. **Download der E-Mail-Programme**:
   * Eine Anleitung zum Download von Microsoft Outlook für Microsoft Exchange 2019 finden Sie im Artikel „Microsoft Outlook für Microsoft Exchange 2019 downloaden“.
9. **E-Mail-Konten beim bisherigen Provider oder auf dem lokalen E-Mail-Server entfernen**:
   * Nach erfolgreicher Migration entfernen Sie die E-Mail-Konten bei Ihrem bisherigen Provider oder Ihrem lokalen E-Mail-Server.

Stellen Sie außerdem sicher, dass Sie den Autodiscover-Eintrag bei Ihrem ursprünglichen Domain-Provider aktualisieren, insbesondere wenn Sie eine externe Domain mit den Nameservern Ihres Domain-Providers verwenden.

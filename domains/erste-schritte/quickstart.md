---
description: Validiert am 7. Juli 2024 • Zuletzt bearbeitet am 01. Dezember 2024
---

# Quickstart

Um eine Domain mit centron einzurichten, müssen Sie diese und alle ihre bestehenden DNS-Einträge zum Kontrollpanel hinzufügen und dann die Domain delegieren, indem Sie Ihren Registrar aktualisieren, um centrons Nameserver zu verwenden.

{% hint style="info" %}
Wenn die Domain aktiv genutzt wird, sollten Sie die DNS-Einträge der Domain auf centron neu erstellen, bevor Sie die Domain delegieren, um Ausfallzeiten zu vermeiden.
{% endhint %}



1. Im Kontrollpanel klicken Sie oben rechts auf "Erstellen" und dann auf "Domains/DNS".
2.  Im Abschnitt "Domain eingeben" geben Sie den Domainnamen ein.

    Dies ist in der Regel die Apex-Domain, wie zum Beispiel example.com. Um Subdomains wie [www.example.com](http://www.example.com/) oder images.example.com hinzuzufügen, erstellen Sie DNS-Einträge für diese, nachdem Sie die Apex-Domain hinzugefügt haben.
3. Klicken Sie auf "Domain hinzufügen". Dies führt Sie zur Seite "Neuen Eintrag erstellen" und fügt NS-Einträge für die Domain auf den Nameservern von centron hinzu.
4. Auf der Seite "Neuen Eintrag erstellen" fügen Sie alle DNS-Einträge für die Domain hinzu. Wählen Sie für jeden Eintrag den Eintragstyp aus, füllen Sie die notwendigen Daten aus und klicken Sie auf "Eintrag erstellen".
5. Delegieren Sie Ihre Domain, indem Sie Ihren Domainnamen über Ihren Registrar auf centrons Nameserver zeigen lassen.


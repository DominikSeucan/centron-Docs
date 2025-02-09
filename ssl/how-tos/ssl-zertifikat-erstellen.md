---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# SSL Zertifikat erstellen

## SSL-Manager <a href="#ssl-manager" id="ssl-manager"></a>

Sie können Ihre SSL-Zertifikate selbst über das ccenter verwalten und auch neue SSL-Zertifikate bestellen. Die folgende Anleitung unterstützt Sie dabei, die Informationen zu finden, welche Sie benötigen und Ihre Bestellungen korrekt aufzugeben.

**Achtung:** Eine Domain oder E-Mail-Adresse eines SSL-Zertifikats kann _nachträglich nicht verändert, hinzugefügt oder entfernt_ werden. Ein SSL-Zertifikat kann jedoch zurückgezogen und vorzeitig für ungültig erklärt werden (die Gültigkeit wird bei jedem Aufruf erneut geprüft).\
Sollten Sie eine Veränderung der Domain(s) oder E-Mail-Adresse Ihres SSL-Zertifikats wünschen, kann nur ein neues Zertifikat ausgestellt werden.

### Ihre Möglichkeiten <a href="#ihre_moglichkeiten" id="ihre_moglichkeiten"></a>

* Auswahl des richtigen SSL-Zertifikats
* Bestellung S/MIME Zertifikat (E-Mail-Adresse)
* Bestellung SSL-Zertifikat (Domain)

### Auswahl des richtigen SSL-Zertifikats <a href="#auswahl_des_richtigen_ssl-zertifikats" id="auswahl_des_richtigen_ssl-zertifikats"></a>

Möchten Sie ein SSL-Zertifikat für eine Domain oder eine E-Mail-Adresse ausstellen?\


Domain E-Mail-Adresse    <mark style="color:red;"><- Überschrift?</mark>

### Bestellung SSL-Zertifikat (Domain) <a href="#bestellung_ssl-zertifikat_domain" id="bestellung_ssl-zertifikat_domain"></a>

1. Melden Sie sich mit Ihrer E-Mail-Adresse im [ccenter](https://ccenter.internet1.de/) an.
2. Wählen Sie links im Menü den Punkt „SSL-Manager“ aus.\
   → Dort sehen Sie Ihre bereits vorhandenen SSL-Zertifikate\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_01.png?w=380\&tok=b7e360)
   1. Möchten Sie ein bestehendes SSL-Zertifikat verlängern, wählen Sie in der Detailansicht den Button „Verlängern“ rechts aus.![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_02.png?w=1150\&tok=766f86)\
      ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_03.png?w=1150\&tok=9ede17)
   2. Ab hier läuft die Verlängerung wie eine normale Bestellung ab.\
      Prüfen Sie die vorausgefüllten Daten und achten darauf, die richtige Validierungsart auszuwählen.
3. Um ein neues SSL-Zertifikat zu bestellen, klicken Sie in der Übersicht rechts oben auf den grünen Button.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_04.png?w=450\&tok=90a6d4)
4. Belassen Sie die Zertifikatsart auf „Domain“.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_05.png?w=750\&tok=7df6db)
5. Wählen Sie als Produkt die gewünschte Zertifikatsart aus .\
   → [Dieser Artikel](https://wiki8.centron.de/ssl/types/domain) unterstützt Sie bei der Auswahl der richtigen Zertifikatsart.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_06.png?w=750\&tok=9af115)
6.  Tragen Sie die Domain ein, für die Sie das SSL-Zertifikat ausstellen möchten.\
    \


    In einem Positive-SSL-Zertifikat ist immer die Domain selbst und die www-Subdomain dieser Domain enthalten (z.B.: domain.de und www.domain.de).

    ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_07.png?w=750\&tok=426804)
7. Um die Sicherheit des SSL-Zertifikatsart zu erhöhen, können Sie die Länge des Private Keys auf 4096 Byte anpassen. Die Standardeinstellung von 2048 Byte ist jedoch meistens auch bereits ausreichend.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_08.png?w=750\&tok=723523)
8. Entscheiden Sie sich für eine Validierungsart und wählen diese aus.\
   → [Dieser Artikel](https://wiki8.centron.de/ssl/types/domain#ablauf_der_validierung) unterstützt Sie bei der Auswahl der richtigen Validierungsart und beschreibt den Ablauf der verschiedenen Arten genau.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_09.png?w=750\&tok=0f35d2)\
   Bei der Validierungsart E-Mail müssen Sie auch eine E-Mail-Adresse auswählen.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_10.png?w=750\&tok=0c195a)
9. Mit einem Klick auf den blauen Button rechts können Sie Ihre hinterlegten Kundendaten laden lassen.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_11.png?w=750\&tok=a6d23c)\
   Alternativ können Sie auch die gewünschten Kontaktdaten selbst eintragen.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_12.png?w=750\&tok=fb632d)
10. Prüfen Sie im letzten Schritt nochmals alle Ihre Angaben und klicken dann unten auf „Bestellen“.\
    ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_13.png?w=750\&tok=b174b3)

### Bestellung S/MIME Zertifikat (E-Mail-Adresse) <a href="#bestellung_smime_zertifikat_e-mail-adresse" id="bestellung_smime_zertifikat_e-mail-adresse"></a>

1. Melden Sie sich mit Ihrer E-Mail-Adresse im [ccenter](https://ccenter.internet1.de/) an.
2. Wählen Sie links im Menü den Punkt „SSL-Manager“ aus.\
   → Dort sehen Sie Ihre bereits vorhandenen SSL-Zertifikate.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_01.png?w=380\&tok=b7e360)
   1. Möchten Sie ein bestehendes SSL-Zertifikat verlängern, wählen Sie in der Detailansicht den Button „Verlängern“ rechts aus.![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_02.png?w=1150\&tok=766f86)\
      ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_03.png?w=1150\&tok=9ede17)
   2. Ab hier läuft die Verlängerung wie eine normale Bestellung ab.\
      Prüfen Sie die vorausgefüllten Daten und achten darauf, die richtige Validierungsart auszuwählen.
3. Um ein neues SSL-Zertifikat zu bestellen, klicken Sie in der Übersicht rechts oben auf den grünen Button.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_04.png?w=450\&tok=90a6d4)
4. Wählen Sie als Zertifikatsart „SMIME“ aus.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslordermail_01.png?w=750\&tok=431899)
5. Wählen Sie als Produkt die gewünschte Zertifikatsart aus .\
   → [Dieser Artikel](https://wiki8.centron.de/ssl/types/email) unterstützt Sie bei der Auswahl der richtigen Zertifikatsart.\
   \
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslordermail_02.png?w=750\&tok=ed7aff)
6. Tragen Sie die E-Mail-Adresse ein, für die das S/MIME-Zertifikat ausgestellt werden soll.\
   \
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslordermail_03.png?w=750\&tok=85c5bc)
7. Vergeben Sie ein Kennwort. Achten Sie dabei auf die rechts eingeblendete Kennwortrichtlinie.\
   \
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslordermail_04.png?w=750\&tok=1e804c)
8. Um die Sicherheit des SSL-Zertifikatsart zu erhöhen, können Sie die Länge des Private Keys auf 4096 Byte anpassen. Die Standardeinstellung von 2048 Byte ist jedoch meistens auch bereits ausreichend.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_08.png?w=750\&tok=723523)
9. Mit einem Klick auf den blauen Button rechts können Sie Ihre hinterlegten Kundendaten laden lassen.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_11.png?w=750\&tok=a6d23c)\
   Alternativ können Sie auch die gewünschten Kontaktdaten selbst eintragen.\
   ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_12.png?w=750\&tok=fb632d)
10. Prüfen Sie im letzten Schritt nochmals alle Ihre Angaben und klicken dann unten auf „Bestellen“.\
    ![](https://wiki8.centron.de/_media/webhosting/interfaces/ccenter/sslorderdomain_13.png?w=750\&tok=b174b3)

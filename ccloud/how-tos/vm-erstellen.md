---
description: Erstellt am 29. November 2023
---

# VM erstellen

Der Benutzer, der den Server erstellt, hat volle Root- oder Administratorrechte. Ein einmal eingerichteter Server behält alle seine Einstellungen (Ressourcen, Laufwerkszuweisung, Kennwort usw.) bei, auch nach einem Neustart auf Betriebssystemebene.&#x20;

Eine Ausnahme besteht bei aktiviertem Premium Full Managing. In diesem Fall bleiben Root- und Administratorrechte bei centron, um einen einheitlichen Qualitätsstandard zu gewährleisten. Weitere Informationen finden Sie unter [Premium Full Managing](broken-reference).

Der Server wird erst dann aus Ihrer Serverübersicht entfernt, wenn Sie ihn entgültig löschen. Weitere Informationen finden Sie auf der Seite [Virtual Machines](broken-reference).



## Eine VM erstellen

{% hint style="info" %}
Vorraussetzungen: Stellen Sie sicher, dass Sie über die entsprechenden Berechtigungen verfügen. Nur Vertragsinhaber, Serveradmins oder Benutzer mit der Berechtigung "Serverberechtigungen" können eine VM einrichten. Andere Benutzertypen haben nur Lesezugriff oder gar keinen Zugriff und können keine Änderungen bereitstellen.
{% endhint %}

1. Klicken Sie im ccloud³ Tab oder in der Seitenleiste auf Server erstellen.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

2. Während des Erstellens einer VM, konfigurieren Sie folgende Einstellungen:

* **Pool**: Wählen Sie einen Pool, der Ihren Anforderungen entspricht. Sie erhalten zu jedem Pool eine Anwendungsempfehlung.
* **CPU Architektur**: Innerhalb Ihres Pools können Sie ebenfalls Ihre CPU Architektur (AMD oder Intel) wählen.
* **Betriebssystem**: Wählen Sie zwischen verschiedenen Windows Versionen und Linux Flavors.
* **CPU Cores**: Geben Sie die Anzahl der CPU-Kerne an. Sie können diese nach der Bereitstellung ändern. Bitte beachten Sie, dass es Konfigurationsgrenzen gibt.
* **RAM**: Geben Sie die Größe des Arbeitsspeichers an. Sie können eine beliebige Größe zwischen 1 GB und 64 GB in Schritten von 1 GB wählen. Diese Einstellung kann nach der Bereitstellung erhöht werden.
* **Speicherplatz**: Geben Sie die Größe Ihres Speicherplatz an. Provisionieren Sie pro VM von 100 GB bis 1000 GB in 1 GB Schritten. Ob HDD oder SSD wird von Ihrer Pool Auswahl bestimmt.&#x20;

{% hint style="info" %}
Falls Sie höhere Ressourcenanforderungen haben, kontaktieren Sie bitte Ihren Account Manager oder den centron Support.
{% endhint %}



* [Premium Full Managing](broken-reference): Wählen Sie Premium Full Managing, um Backup-as-a-Service und Monitoring-as-a-Service für Ihre VM einzustellen.&#x20;
* [Advanced Monitoring](broken-reference): Advanced Monitoring gibt Ihnen die Option, Ihre VM selbst zu überwachen.

{% hint style="info" %}
Premium Full Managing kann nicht in Kombination mit Advanced Monitoring gebucht werden. Das Monitoring wird hierbei von centron übernommen.
{% endhint %}



* **Servername**: Wählen Sie einen eindeutigen Servernamen.
* **Passwort / SSH Key**: Wählen Sie ein sicheres Passwort oder einen SSH Key, um auf Ihre VM zuzugreifen.



## Starten, Stoppen, Reset und Löschen einer VM

Wir halten für jeden Kunden dedizierte Ressourcen bereit. Sie teilen Ihre physischen CPUs nicht mit anderen centron Kunden. Aus diesem Grund verursachen die Server, die auf der Ebene des Betriebssystems abgeschaltet sind, immer noch Kosten.&#x20;

{% hint style="warning" %}
Nutzen Sie das ccenter, um virtuelle Maschinen zu löschen. So werden die Ressourcen vollständig freigegeben und Ihnen entstehen keine Kosten.
{% endhint %}



### **Stoppen einer VM**

1. Wählen Sie einen Server aus, den Sie stoppen möchten.
2. (Optional) Stellen Sie im angezeigten Dialogfeld eine Verbindung über die Remote-Konsole her und fahren Sie die VM auf Betriebssystemebene herunter, um Datenverluste zu vermeiden.
3. Richten Sie den Toogle in der Serverübersicht auf die linke Seite, um Ihre VM zu stoppen. Alternativ können Sie auch das Info Icon am rechten Ende der Leiste nutzen und auf **Icon > Stop** klicken, um Ihre VM zu stoppen. Richten Sie den Toggle in der Serverdetailansicht auf die linke Seite.



### **Starten einer VM**

1. Wählen Sie eine VM aus, die Sie starten möchten
2. Richten Sie den Toogle in der Serverübersicht auf die rechte Seite, um Ihre VM zu starten. Alternativ können Sie auch das Info Icon am rechten Ende der Leiste nutzen und auf **Icon > Start** klicken, um Ihre VM zu starten. Richten Sie den Toggle in der Serverdetailansicht auf die rechte Seite
3. Der Server wird gebootet. Eine neue öffentliche IP-Adresse wird je nach Konfiguration zugewiesen.&#x20;



### **Reset einer VM**

1. Wählen Sie eine VM aus, die Sie neu starten möchten.
2. Gehen Sie in der Serverübersicht auf das Info Icon am rechten Ende der Leiste und klicken Sie **Icon > Reset**, um Ihre VM neu zu starten. Anschließend klicken Sie in der Serverdetailansicht auf das Reset Icon.
3. Der Server wird heruntergefahren und ein Hard Reset wird durchgeführt.



### **Löschen einer VM**

1. Wählen Sie eine VM aus, die Sie löschen möchten.
2. Gehen Sie in der Server Detailansicht unter **Serverdatails > Ressourcen** auf **Löschen**, um Ihre VM zu löschen
3. Die VM und Ihr Speicher werden gelöscht. Die Abrechnung für diese VM wird angehalten.&#x20;

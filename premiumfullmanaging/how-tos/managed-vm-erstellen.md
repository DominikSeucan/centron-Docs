---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Managed VM erstellen

Der Benutzer, der den Server erstellt, hat volle Root- oder Administratorrechte. Ein einmal eingerichteter Server behält alle seine Einstellungen (Ressourcen, Laufwerkszuweisung, Kennwort usw.) bei, auch nach einem Neustart auf Betriebssystemebene.&#x20;

Eine Ausnahme besteht bei aktiviertem Premium Full Managing. Hierbei bleiben Root- und Administratorrechte bei centron, um einen einheitlichen Qualitätsstandard zu gewährleisten. Weitere Informationen finden Sie unter [Premium Full Managing](broken-reference).

Der Server wird erst dann aus Ihrer Serverübersicht entfernt, wenn Sie ihn entgültig löschen. Weitere Informationen finden Sie auf der Seite [Virtual Machines](broken-reference).



## Eine VM erstellen

{% hint style="info" %}
Vorraussetzungen: Stellen Sie sicher, dass Sie über die entsprechenden Berechtigungen verfügen. Nur Vertragsinhaber, Serveradmins oder Benutzer mit der Berechtigung "Serverberechtigungen" können eine VM einrichten. Andere Benutzertypen haben nur Lesezugriff oder gar keinen Zugriff und können keine Änderungen bereitstellen.
{% endhint %}

1. Klicken Sie in der [Serverübersicht ](broken-reference)oder in der Seitenleiste auf "Server erstellen".

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



2. Während des Erstellens einer VM, konfigurieren Sie folgende Einstellungen:

* **Pool**: Wählen Sie einen Pool, der Ihren Anforderungen entspricht. Sie erhalten zu jedem Pool eine Anwendungsempfehlung.
* **CPU Architektur**: Innerhalb Ihres Pools können Sie ebenfalls Ihre CPU Architektur (AMD oder Intel) wählen.
* **Betriebssystem**: Wählen Sie zwischen verschiedenen Windows Versionen und Linux Flavors.



* **CPU Cores**: Geben Sie die Anzahl der CPU-Kerne an. Sie können diese nach der Bereitstellung ändern. Bitte beachten Sie, dass es Konfigurationsgrenzen gibt.
* **RAM**: Geben Sie die Größe des Arbeitsspeichers an. Sie können eine beliebige Größe zwischen 1 GB und 64 GB in Schritten von 1 GB wählen. Diese Einstellung kann nach der Bereitstellung erhöht werden.
* **Speicherplatz**: Geben Sie die Größe Ihres Speicherplatzes an. Provisionieren Sie pro VM von 100 GB bis 1000 GB in 1 GB Schritten. Ob HDD oder SSD wird von Ihrer Pool Auswahl bestimmt.&#x20;

{% hint style="info" %}
Falls Sie höhere Ressourcenanforderungen haben, kontaktieren Sie bitte Ihren Acocunt Manager oder den centron Support.
{% endhint %}



* [Premium Full Managing](broken-reference): Wählen Sie Premium Full Managing, um Backup-as-Service und Monitoring-as-Service für Ihre VM einzustellen.&#x20;

{% hint style="info" %}
Premium Full Managing kann nur zusammen mit Premium Managed Services gebucht werden, nicht mit Advanced Monitoring.
{% endhint %}



* **Servername**: Wählen Sie einen eindeutigen Servernamen.
* **Passwort / SSH Key**: Wählen Sie ein sicheres Passwort oder einen SSH Key, um auf Ihre VM zuzugreifen.



## Starten, Stoppen, Reset und Löschen einer VM

Wir halten für jeden Kunden dedizierte Ressourcen bereit. Sie teilen Ihre physischen CPUs nicht mit anderen centron Kunden. Aus diesem Grund verursachen die Server, die auf der Ebene des Betriebssystems abgeschaltet sind, immer noch Kosten.&#x20;

{% hint style="warning" %}
Sie sollten das ccenter nutzen, um virtuelle Maschinen zu löschen, damit die Ressourcen vollständig freigegeben werden und keine Kosten entstehen.
{% endhint %}



**Stoppen einer VM**

1. Wählen Sie einen Server aus, den Sie stoppen möchten.
2. (Optional) Stellen Sie in dem angezeigten Dialogfeld eine Verbindung über die Remote-Konsole her und fahren Sie die VM auf Betriebssystemebene herunter, um Datenverluste zu vermeiden.
3. In der Serverübersicht, richten Sie den Toogle auf die linke Seite, um Ihre VM zu stoppen oder nutzen Sie das Info Icon am rechten Ende der Leiste und klicken Sie **Icon > Stop**, um Ihre VM zu stoppen. In der Serverdetailansicht, richten Sie den Toggle auf die linke Seite.



**Starten einer VM**

1. Wählen Sie eine VM aus, die Sie starten möchten.
2. In der Serverübersicht, richten Sie den Toogle auf die rechte Seite, um Ihre VM zu starten oder nutzen Sie das Info Icon am rechten Ende der Leiste und klicken Sie **Icon > Start**, um Ihre VM zu starten. In der Serverdetailansicht, richten Sie den Toogle auf die rechte Seite.
3. Der Server wird gebootet. Eine neue öffentliche IP-Adresse wird je nach Konfiguration zugewiesen.&#x20;



**Reset einer VM**

1. Wählen Sie eine VM aus, die Sie neu starten möchten.&#x20;
2. In der Serverübersicht, klicken Sie das Info Icon am rechten Ende der Leiste und klicken Sie **Icon > Reset**, um Ihre VM neu zu starten. In der Serverdetailansicht, klicken Sie das Reset Icon. ![](broken-reference)
3. Der Server wird heruntergefahren und ein Hard Reset wird durchgeführt.



**Löschen einer VM**

1. Wählen Sie eine VM aus, die Sie löschen möchten.
2. In der Server Detailansicht, gehen Sie unter **Serverdatails > Ressourcen** auf **Löschen**, um Ihre VM zu löschen.
3. Die VM und Ihr Speicher wird gelöscht. Die Abrechnung für diese VM wird angehalten.&#x20;

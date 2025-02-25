---
description: Validiert am 28.05.2024 • Zuletzt bearbeitet am 17. September 2024
---

# Monitoring as a Service

Monitoring-as-a-Service (MaaS) erhebt Metriken Ihrer VM auf verschiedenen Ebenen.&#x20;

{% hint style="info" %}
MaaS kann nur als Teil von **Premium Full Managing** gebucht werden. Damit verwaltet centron die komplette VM und kontrolliert damit auch die Gesundheit des Systems.
{% endhint %}

centron überprüft Ihre virtuellen Instanzen auf ihre Gesundheit. Checks reichen hierbei von IPMI über NSC hinzu SSH, um einen reibungslosen Verlauf Ihrer Systeme zu grantieren.



## Verfügbarkeit der Metriken

Die Sammlung von Überwachungsmetriken beginnt, wenn eine neue Instanz bereitgestellt wird. Allerdings sind die ersten Metriken nicht sofort nach der Bereitstellung verfügbar. Es dauert etwa 10 Minuten, bis die ersten Metriken gesammelt werden und im ccenter oder über die API abgerufen werden können. Nach Ablauf dieser ersten 10 Minuten können Sie jederzeit Metriken abrufen.



## MaaS mit Premium Full Managing

Mit gebuchtem Premium Full Managing, können Sie in der Serverdetailansicht unter **Serverübersicht > Performance** die wichtigsten Metriken einsehen.



In diesem Teil der Server Detailansicht können Sie CPU, Network, Storage und RAM Metriken in verschiedenen Zeiträumen einsehen und filtern.&#x20;



## Advanced Monitoring

Falls Sie sich dafür entscheiden, selbst Ihre VM verwalten zu wollen, können Sie Ihre Instanz mit Advanced Monitoring überwachen.&#x20;

Gehen Sie hierfür unter der Server Detailansicht > Advanced Monitoring. Dieses Addon wird zu der monatlichen Berechnung der VM addiert. Sobald Sie Advanced Monitoring für Ihre VM aktiviert haben, werden Sie auf ein separates Interface weitergeleitet, auf dem Sie verschiedene Metriken Ihrer VM verwalten können.&#x20;

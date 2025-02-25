---
description: Überprüft am 12. April 2023 • Zuletzt bearbeitet am 4. April 2024
---

# Affinity Groups

Durch die Definition von Affinitätsgruppen und die Zuweisung von Instanzen zu diesen Gruppen kann der Benutzer oder Administrator beeinflussen (aber nicht vorschreiben), welche Instanzen entweder auf demselben oder auf getrennten Hosts ausgeführt werden sollen. Mit dieser Funktion können Benutzer die Affinitätsgruppen festlegen, denen eine Instanz angehören kann.&#x20;

Instanzen mit demselben "Host-Anti-Affinitäts"-Typ werden nicht auf demselben Host ausgeführt, was der Erhöhung der Fehlertoleranz dient. Wenn ein Host ausfällt, ist eine andere Instanz, die denselben Dienst anbietet (z. B. das Hosting der Website des Benutzers), auf einem anderen Host weiterhin betriebsbereit. Außerdem kann der Benutzer festlegen, dass Instanzen mit demselben Host-Affinitätstyp auf demselben Host laufen müssen, was für die Gewährleistung der Konnektivität und geringer Latenz zwischen Gastinstanzen nützlich sein kann.&#x20;

"non-strict host anti-affinity" ist ähnlich, aber flexibler als "host anti-affinity". In diesem Fall werden die Instanzen auf verschiedenen Hosts bereitgestellt, solange genügend Hosts vorhanden sind, um die Anforderung zu erfüllen. Andernfalls können sie auf demselben Host bereitgestellt werden. "Nicht-strikte Host-Affinität" ist ähnlich, aber flexibler als "Host-Affinität". Instanzen werden idealerweise zusammen auf demselben Host bereitgestellt, aber nur, wenn dies möglich ist.

## Affinity Groups erstellen

Damit Sie eine Affinitätsgruppe erstellen können navigieren Sie wie folgt im cStack Webinterface:

1. Klicken Sie in der linken Navigationsspalte auf "Compute/Berechne"
2. Wählen Sie Affinitätsgruppen aus&#x20;
3. zum Erstellen einer neuen Affinitätsgruppe klicken Sie oben rechts auf den Button "Affinitätsgruppe hinzufügen"

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Bei erstellten Affinitätsgruppen können anschließend beim Deployment einer Instanz in den erweiterten Einstellungen ausgewählt werden.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

## Affinity Groups bearbeiten

Möchten Sie die Server in den Affinitätsgruppen ändern, so muss dies über die jeweilige Instanz erfolgen. Navigieren Sie zu der Übersicht Ihrer Instanzen und öffnen Sie eine Instanz mit dem Klick auf deren Namen.

Nun haben Sie in der oberen horizontalen Navigationsleiste den Button "Affinität ändern". Darüber können Sie die Zugehörigkeit der Affinitätsgruppen anpassen.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

Um zu sehen welche Instanzen sich in welcher Affinitätsgruppen befinden können Sie über die jeweilige Affinitätsgruppe und dem Button "Ansicht Instanzen" zur Übersicht navigieren.

<figure><img src="../.gitbook/assets/Bildschirmfoto 2024-04-04 um 17.39.22.png" alt=""><figcaption></figcaption></figure>

## Affinity Groups löschen

Um die erstellten Affinitätsgruppen zu bearbeiten navigieren Sie erneut in die Übersicht und wählen die gewünschte Gruppe per Auswahl oder über dessen Namen direkt aus. Nun kann die gewünschte Affinitätsgruppe mit dem roten Papierkorb gelöscht werden.

<figure><img src="../.gitbook/assets/Bildschirmfoto 2024-04-04 um 17.33.35.png" alt=""><figcaption></figcaption></figure>

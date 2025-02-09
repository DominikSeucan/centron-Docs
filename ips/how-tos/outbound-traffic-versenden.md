---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Outbound Traffic versenden

Sie können die Netzwerkeinstellungen Ihrer ccloud³ VM bei centron so konfigurieren, dass der ausgehende Verkehr über eine ihr zugewiesene reservierte IP-Adresse geleitet wird. Dies bewirkt, dass der Verkehr von der reservierten IP-Adresse und nicht von der ursprünglichen IPv4-Adresse der ccloud³ VM stammt.

**Voraussetzungen** Um eine ccloud³ VM so zu konfigurieren, dass ihr ausgehender Verkehr über eine ihr zugewiesene reservierte IP-Adresse geleitet wird, benötigen Sie die Gateway-Adresse der Anker-IP-Adresse der ccloud³ VM.

Die meisten ccloud³ VMs haben bereits eine Anker-IP, aber ccloud³ VMs, die vor Oktober 2015 erstellt wurden und ccloud³ VMs, die mit benutzerdefinierten Images erstellt wurden, haben standardmäßig keine Anker-IPs zugewiesen.

Bei ccloud³ VMs ohne Anker-IP müssen Sie zuerst manuell eine Anker-IP der ccloud³ VM zuweisen und dann diesem Leitfaden folgen.

Bei ccloud³ VMs mit einer Anker-IP erhalten Sie die Gateway-Adresse, indem Sie deren Metadaten mit einem curl-Befehl abfragen. Das -s-Flag unterdrückt alle Fortschrittsanzeigen oder Fehlermeldungen und gibt nur die Ausgabe zurück.

```bash
curl -s http://169.254.169.254/metadata/v1/interfaces/public/0/anchor_ipv4/gateway
```

Der Befehl gibt eine IPv4-Adresse zurück, wie zum Beispiel 198.51.100.237, die die Gateway-Adresse der Anker-IP ist. Sie verwenden diese Adresse, um das Standard-IPv4-Gateway Ihres Servers zu aktualisieren und so den ausgehenden Verkehr von Ihrer reservierten IP zu ermöglichen.

**Sofortige Aktivierung des ausgehenden Verkehrs über die reservierte IP**&#x20;

Um Ihre Netzwerkkonfiguration sofort zu aktualisieren, verwenden Sie den Befehl `ip route`, um diese Adresse als Gateway für die Standardroute hinzuzufügen. Der folgende Befehl entfernt die Standardroute von der öffentlichen Netzwerkschnittstelle Ihrer ccloud³ VM und ersetzt sie durch eine Route, die das Gateway der Anker-IP verwendet. Ersetzen Sie `<anchor-gateway-IP-address>` durch die im Schritt zuvor abgerufene IP-Adresse:

```css
cssCopy codesudo sh -c "ip route del 0/0; ip route add default via <anchor-gateway-IP-address> dev eth0"
```

Der Befehl kann einen Moment dauern und gibt keine Ausgabe aus.

Überprüfen Sie, ob der Verkehr der ccloud³ VM durch die reservierte IP-Adresse geleitet wird, indem Sie eine curl-Anfrage an icanhazip.com senden, eine Webseite, die die öffentliche IP-Adresse der anfragenden Quelle zurückgibt. Der -4-Flag weist curl an, nur die IPv4-Adresse der ccloud³ VM zu verwenden:

```arduino
curl -4 https://icanhazip.com/
```

Änderungen, die mit dem `ip route`-Befehl vorgenommen wurden, gehen verloren, wenn Sie Ihre ccloud³ VM neu starten. Um die Einstellung nach einem Neustart beizubehalten, müssen Sie die Netzwerkkonfigurationsdateien der ccloud³ VM ändern. Wie Sie dies tun, hängt von Ihrem Betriebssystem ab.

**Persistenz des ausgehenden Verkehrs über die reservierte IP nach einem Neustart**&#x20;

Deaktivieren Sie zunächst die automatische Netzwerkkonfiguration von cloud-init, da sonst Ihre Einstellungen überschrieben werden könnten:

```bash
echo "network: {config: disabled}" | sudo tee /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg
```

Öffnen Sie die Netzwerkschnittstellenkonfigurationsdatei der ccloud³ VM:

```bash
sudo nano /etc/netplan/50-cloud-init.yaml
```

Aktualisieren Sie unter der eth0-Konfiguration das Feld `via` im Abschnitt `routes`, um die Gateway-Adresse der Anker-IP der ccloud³ VM zu verwenden. Speichern und schließen Sie die Konfigurationsdatei, und wenden Sie die Änderungen mit dem `netplan apply`-Befehl an:

```bash
sudo netplan apply
```

Aktualisieren Sie in der eth0-Konfiguration das Feld "via" im Abschnitt "routes", um die Anker-IP-Gateway-Adresse der VM zu verwenden:

```yaml
yamlCopy codenetwork:
    version: 2
    ethernets:
        eth0:
            addresses:
            - 203.0.113.216/20
            - 10.17.0.5/16
            match:
                macaddress: da:f8:7a:69:ce:ea
            mtu: 1500
            nameservers:
                addresses:
                - 67.207.67.2
                - 67.207.67.3
                search: []
            routes:
            -   to: 0.0.0.0/0
                via: <ccloud³-VM-Gateway-IP-Adresse>
            set-name: eth0
        eth1:
            addresses:
            - 10.132.0.5/16
            match:
                macaddress: a6:08:53:fb:fb:7d
            mtu: 1500
            nameservers:
                addresses:
                - 67.207.67.2
                - 67.207.67.3
                search: []
            set-name: eth1 
```

Nachdem Sie die Konfigurationsdatei angepasst und gespeichert haben, wenden Sie die Änderungen mit dem netplan-Befehl an:

```bash
sudo netplan apply
```

Um zu überprüfen, ob die Änderungen an Ihrem Netzwerk auch nach einem Neustart bestehen bleiben, führen Sie folgenden Befehl aus:

```bash
sudo reboot
```

Nach dem Neustart der ccloud³ VM melden Sie sich erneut an und überprüfen, ob der Datenverkehr durch die festgelegte IP-Adresse geleitet wird, indem Sie erneut eine curl-Anfrage an icanhazip.com senden:

```bash
curl -4 https://icanhazip.com/
```

Beachten Sie, dass spezifische Details wie IP-Adressen und MAC-Adressen je nach Ihrer individuellen Konfiguration und dem Setup bei centron variieren können.\

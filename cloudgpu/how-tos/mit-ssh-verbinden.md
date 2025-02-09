---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# Mit SSH verbinden

Während des Erstellens einer VM können Sie SSH Keys für den Zugang Ihrer VM verwenden. Das erlaubt Ihnen, auf Ihre VM sicher zuzugreifen und eine sichere Verbindung herzustellen.&#x20;

## SSH Key Typen

**Default SSH Keys**: SSH Keys, die öfter benutzt werden sollen.&#x20;

**Ad hoc SSH Keys**: SSH Keys, die nur einmal benutzt und nicht häufiger verwendet werden sollen.&#x20;



## SSH Key Generieren

SSH-Schlüssel können unter macOS oder Linux erzeugt und verwendet werden, wenn sowohl OpenSSH als auch die ssh-keygen-Befehlszeilenwerkzeuge installiert sind. OpenSSH ist eine Sammlung von Tools zum Herstellen von SSH-Verbindungen zu Remote Servern, während ssh-keygen ein Dienstprogramm zum Erzeugen von SSH-Schlüsseln ist.&#x20;

Generieren Sie SSH-Schlüssel manuell, wenn Sie mit OpenSSH über die Terminal-Anwendung arbeiten, indem Sie die folgenden Schritte ausführen:

1. Geben Sie den folgenden Befehl in das Terminalfenster ein und drücken Sie ENTER.

```
ssh-keygen
```

Der Schlüsselgenerierungsprozess wird durch den oben genannten Befehl eingeleitet. Wenn Sie diesen Befehl ausführen, fordert das Dienstprogramm "ssh-keygen" Sie auf, einen Speicherort für den Schlüssel anzugeben.

2. Akzeptieren Sie den Standardspeicherort, indem Sie die ENTER-Taste drücken, oder geben Sie den Pfad der Datei ein, in der Sie den Schlüssel speichern möchten. `/home/username/.ssh/id_rsa`

```
Enter file in which to save the key (/home/username/.ssh/id_rsa):
```

{% hint style="info" %}
Wenn Sie zuvor ein Schlüsselpaar erzeugt haben, wird möglicherweise die folgende Aufforderung angezeigt. Wenn Sie sich dafür entscheiden, den Schlüssel zu überschreiben, können Sie sich nicht mehr mit dem zuvor erzeugten Schlüssel authentifizieren.
{% endhint %}

```
/home/username/.ssh/id_rsa already exists.
Overwrite (y/n)?
```

3. Geben Sie die Passphrase ein, die zur Verschlüsselung der privaten Schlüsseldatei auf der Festplatte verwendet wird. Sie können auch ENTER drücken, um die Standardeinstellung (keine Passphrase) zu akzeptieren. Wir empfehlen Ihnen jedoch, eine Passphrase zu verwenden.
4. Geben Sie Ihre Passphrase noch einmal ein. Nachdem Sie die Passphrase bestätigt haben, werden der öffentliche und der private Schlüssel generiert und an dem angegebenen Ort gespeichert. Die Bestätigung sieht dann wie folgt aus:

```
Your identification has been saved in /home/username/.ssh/id_rsa.
Your public key has been saved in /home/username/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:AcP/ieiAOoD7MjrKepXks/qHAhrRasGOysiaIR94Quk username@mb01739.local
The key's randomart image is:
+---[RSA 3072]----+
|     .o          |
|      .o         |
|..     ..        |
|.oo .   ..       |
|+=.+ . .So .     |
|X+. * . . o      |
|&Eo. *           |
|&Oo.o o          |
|@O++..           |
+----[SHA256]-----+
```

Sie können den Public Key in die Zwischenablage kopieren, indem Sie den folgenden Befehl ausführen:

```
 pbcopy < ~/.ssh/id_rsa.pub
```



## Mit einem SSH Key verbinden

Sie können sich über OpenSSH mit Ihrer virtuellen Instanz verbinden. Sie benötigen jedoch die Terminalanwendung, die je nach Betriebssystem unterschiedlich ist. Bei Linux suchen Sie "Terminal" oder drücken "CTRL+ALT+T". Für macOS' suchen sie ebenfalls "Terminal" und bei Windows suchen  sie "Bash". Wenn Sie keine Bash installiert haben, verwenden Sie stattdessen PuTTY. Die folgenden Schritte zeigen Ihnen, wie Sie sich mit Ihrer VM verbinden können.

1. Öffnen Sie die Anwendung "Terminal" und geben Sie den unten stehenden SSH-Verbindungsbefehl ein. Fügen Sie nach dem @ die IP-Adresse Ihrer VM-Instanz hinzu. Drücken Sie dann ENTER.

```
ssh root@215.215.215.215
```

{% hint style="info" %}
Wenn Sie sich zum ersten Mal anmelden, wird der Server auf Ihrem lokalen Rechner nicht erkannt, so dass Sie gefragt werden, ob Sie die Verbindung aufrechterhalten wollen. Sie können "Ja" eingeben und dann ENTER drücken.
{% endhint %}

2. Die Authentifizierung ist der nächste Schritt im Verbindungsprozess. Wenn Sie die SSH-Schlüssel hinzugefügt haben, können Sie sich sofort oder nach Eingabe der Passphrase Ihres Schlüsselpaars mit der VM verbinden.&#x20;

Wenn Sie noch keine SSH-Schlüssel hinzugefügt haben, werden Sie nach Ihrem Passwort gefragt:

```
root@215.215.215.215's password:
```

3. Sobald Sie das Passwort eingegeben haben, drücken Sie ENTER.&#x20;

Wenn der SSH-Schlüssel richtig konfiguriert ist, melden Sie sich damit bei VM an.

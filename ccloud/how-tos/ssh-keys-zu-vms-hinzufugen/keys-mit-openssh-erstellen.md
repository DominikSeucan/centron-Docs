---
description: Überprüft am 28. August 2019 • Zuletzt bearbeitet am 6. November 2023
---

# Keys mit OpenSSH erstellen

Die Erstellung eines SSH-Schlüsselpaares mit OpenSSH ist ein grundlegender Schritt für eine sichere Verbindung zu Ihren ccloud³ VMs bei centron. So gehen Sie es an:

## SSH-Schlüsselpaar mit OpenSSH generieren

1.  **SSH-Keygen ausführen:**

    Öffnen Sie Ihr Terminal. Geben Sie den Befehl `ssh-keygen` ein, um ein 2048-Bit-RSA-Schlüsselpaar zu generieren. Dies ist für die meisten Anwendungen ausreichend.
2.  **Speicherort auswählen:**

    Sie werden aufgefordert, einen Speicherort für die Schlüssel zu wählen. Standardmäßig werden sie im Verzeichnis `~/.ssh` gespeichert, wobei `id_rsa` der private Schlüssel und `id_rsa.pub` der öffentliche Schlüssel ist. Die Verwendung der Standardorte ermöglicht es Ihrem SSH-Client, Ihre SSH-Schlüssel automatisch zu finden. Es wird empfohlen, dies zu akzeptieren, indem Sie ENTER drücken.

```
Generating public/private rsa key pair.
Enter file in which to save the key (/home/username/.ssh/id_rsa): 
```

3. **Vorsicht bei vorhandenen Schlüsseln:**

Wenn Sie bereits ein Schlüsselpaar generiert haben, erhalten Sie möglicherweise eine Aufforderung, die besagt, dass `/home/username/.ssh/id_rsa` bereits existiert. Wenn Sie sich entscheiden, den Schlüssel auf der Festplatte zu überschreiben, können Sie den vorherigen Schlüssel nicht mehr verwenden. Das Überschreiben ist ein irreversibler Prozess.

4. **Optionales Passwort eingeben:**

Sie werden aufgefordert, ein optionales Passwort einzugeben, welches die private Schlüsseldatei auf der Festplatte verschlüsselt. Wenn Sie ein Passwort eingeben, müssen Sie es jedes Mal angeben, wenn Sie diesen Schlüssel verwenden. Es wird empfohlen, ein Passwort zu verwenden, mit ENTER drücken können Sie diese Aufforderung allerdings auch überspringen.

```
Created directory '/home/username/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again: 
```

5. **Abschluss des Erstellungsprozesses**

Nach Abschluss des Prozesses haben Sie ein öffentliches und ein privates Schlüsselpaar, das Sie zur Authentifizierung verwenden können.

```
Your identification has been saved in /home/username/.ssh/id_rsa.
Your public key has been saved in /home/username/.ssh/id_rsa.pub.
The key fingerprint is:
a9:49:EX:AM:PL:E3:3e:a9:de:4e:77:11:58:b6:90:26 username@203.0.113.0
The key's randomart image is:
+--[ RSA 2048]----+
|     ..o         |
|   E o= .        |
|    o. o         |
|        ..       |
|      ..S        |
|     o o.        |
|   =o.+.         |
|. =++..          |
|o=++.            |
+-----------------+
```

## Nächste Schritte

**Öffentlichen Schlüssel zu Ihrem centron-Konto hinzufügen:**

Fügen Sie Ihren öffentlichen Schlüssel zu Ihrem centron-Konto hinzu, um ihn bei der Erstellung in neue ccloud³ VMs einbetten zu können.

**Öffentlichen Schlüssel zu bestehenden ccloud³ VMs hinzufügen:**

Fügen Sie Ihren öffentlichen Schlüssel zu bestehenden ccloud³ VMs hinzu, um die SSH-Schlüsselauthentifizierung für das Einloggen zu verwenden.

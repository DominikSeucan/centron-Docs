---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# VM aus Custom Image erstellen

**Erstellen von ccloud³ VMs aus benutzerdefinierten Images über das Kontrollpanel**

Nachdem Sie ein benutzerdefiniertes Image auf Ihr Konto hochgeladen haben, können Sie ccloud³ VMs auf zwei Arten aus diesem Image erstellen:

1. **Über den Bildschirm zur VM-Erstellung** \
   Während der Erstellung der ccloud³ VM können Sie auf dem Bildschirm zur VM-Erstellung im Abschnitt "Wählen Sie ein Image" den Tab für "benutzerdefinierte Images" öffnen und das gewünschte benutzerdefinierte Image auswählen.
2. **Über das "Mehr"-Menü des benutzerdefinierten Images**\
   Auf der Seite "Images", im Tab für benutzerdefinierte Images, öffnen Sie das Menü "Mehr" des benutzerdefinierten Images, von welchem Sie eine ccloud³ VM erstellen möchten. Klicken Sie hier auf "Starte eine ccloud³ VM". Dies führt Sie zum Bildschirm zur VM-Erstellung mit Ihrem vorab ausgewählten benutzerdefinierten Image.

Unabhängig von der gewählten Methode, wählen Sie Ihre Optionen auf der Seite zur VM-Erstellung aus und klicken Sie dann auf "Erstelle ccloud³ VM". Sie können ccloud³ VMs nur in derselben Region wie Ihr benutzerdefiniertes Image erstellen, aber Sie können benutzerdefinierte Images zu anderen Regionen hinzufügen.

Nachdem Ihre ccloud³ VM erstellt wurde, können Sie sich mit SSH mit ihr verbinden.

**Hinweis:** Wenn Sie aufgefordert werden, ein Root-Passwort einzugeben, und Sie keines haben, überprüfen Sie, ob die Version von cloud-init auf Ihrem Image mindestens 0.7.7 ist. Sie können auch versuchen, Ihren SSH-Schlüssel dem Image hinzuzufügen, bevor Sie es hochladen.

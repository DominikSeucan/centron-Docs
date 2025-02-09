---
description: Validiert am 19.07.2024 • Zuletzt bearbeitet am 17.07.2024
---

# Features

Mit Kontingenten können Sie Ihre centron-Ressourcen in Gruppen organisieren, die zu Ihrer Arbeitsweise passen. Erstellen Sie Kontingente, die mit den Anwendungen, Umgebungen und Clients übereinstimmen, die Sie bei centron hosten.

***

Kontingente sind ein übergeordnetes Organisationstool, das es Ihnen erleichtert, sich zu fokussieren und auf der Plattform zu navigieren, wenn Sie Ihre Infrastruktur skalieren. Mithilfe von Kontingenten können Sie Ressourcen in Gruppen einteilen, die dem Zweck entsprechen, für den Sie diese Ressourcen verwenden. Sie können Ressourcen für verschiedene Anwendungen, für verschiedene Kunden oder für Entwicklungs- und Produktionsumgebungen trennen.

Nativ sind nur Ressourcen in Ihren Kontingenten enthalten, wenn Sie zuvor einen Ressourcenpool-Vertrag abgeschlossen haben. Alle Ihre Ressourcen werden standardmäßig in der jeweiligen Produktübersicht erstellt. Sie können Ressourcen in großen Mengen oder einzeln zwischen Kontingente verschieben, und Sie können neue Projekte bei deren Erstellung mit Daten füllen.

### Ressourcen-Typen

Es gibt drei verschiedene Typen an Ressourcen:

| Kontingent-basiert                 | VM-basiert                                          | Unabhängige Ressourcen                     |
| ---------------------------------- | --------------------------------------------------- | ------------------------------------------ |
| _Muss zu einem Kontingent gehören_ | _Gehört zu einem Kontingent durch VM-Zugehörigkeit_ | _Kann nicht mit Kontingenten interagieren_ |
| Premium Managed Services           | Disks                                               | cStack                                     |
|                                    | cProtect                                            | Housing                                    |
|                                    | Snapshots                                           | Domains                                    |
|                                    | cBacks                                              | SSL Zertifikate                            |
|                                    | Full Backup                                         | S3 Object Storage                          |
|                                    | IPs                                                 |                                            |
|                                    | Premium Full Managing                               |                                            |



VM-basierte Ressourcen sind über die VM, dem sie zugeordnet sind, mit Kontingenten verbunden. Sie können auf diese Ressourcen innerhalb eines Projekts über die zugehörige VM zugreifen.

Unabhängige Ressourcen interagieren nicht mit Kontingenten.

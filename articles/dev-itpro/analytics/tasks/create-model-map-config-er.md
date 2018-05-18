--- 
title: Modellkonfigurationszuordnung (ER) erstellen
description: "Verwenden Sie diese Prozedur, um eine neue Modellzuordnungskonfiguration für elektronische Berichterstellung (EB) zu entwerfen und integrierte EB-Funktionen für effiziente Aggregationsberechnungen zu verwenden."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: f7206126bfa6150078f1bfb4f7e07c1cf2819ce0
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-model-mapping-configuration-er"></a>Modellkonfigurationszuordnung (ER) erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Verwenden Sie diese Prozedur, um eine neue Modellzuordnungskonfiguration für elektronische Berichterstellung (EB) zu entwerfen und integrierte EB-Funktionen für effiziente Aggregationsberechnungen zu verwenden. In dieser Prozedur erstellen Sie eine Konfiguration für das Beispielunternehmen Litware, Inc. 

Diese Prozedur wird für Verwendungszwecke erstellt, die die Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung haben, die ihnen zugewiesen sind.

Diese Schritte können mithilfe eines beliebigen Dataset abgeschlossen werden. Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.  
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Klicken Sie auf "Filter anzeigen".
4. Geben Sie im Feld „Name” den Filterwert „Intrastat” ein, und verwenden Sie den Filteroperator „beginnt mit”.
    * Wenden Sie diesen Filter an, um die Datenmodellkonfiguration „Intrastat” zu suchen. Dieses Modell besteht möglicherweise bereits in der Konfigurationsstruktur. Wenn es der Fall, überspringen Sie nächste Unteraufgabe.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Intrastat-Modellkonfiguration von Microsoft erhalten
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Microsoft-Anbieterkachel aus.  
5. Klicken Sie auf Repositorys.
    * Klicken Sie auf „Repositorys” in der Kachel „Microsoft-Anbieter”.  
6. Klicken Sie auf "Filter anzeigen".
7. Geben Sie im Feld „Name eingeben” den Filterwert „Ressourcen” ein, und verwenden Sie den Filteroperator „enthält”. 
8. Klicken Sie auf "Öffnen".
9. In der Struktur wählen Sie „Intrastatmodell” aus.
10. Klicken Sie auf Import.
11. Klicken Sie auf "Ja".
    * Sie haben die EB-Modellkonfiguration importiert, die das Datenmodell enthält, das Sie verwenden werden, um zu erkunden, wie die neuen EB-Funktionen verwendet werden können.  
12. Schließen Sie die Seite.
13. Schließen Sie die Seite.
14. Klicken Sie auf "Berichterstellungskonfigurationen".

## <a name="add-a-new-model-mapping-configuration"></a>Neue Modellzuordnungskonfiguration hinzufügen
1. In der Struktur wählen Sie „Intrastatmodell” aus.
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld „Neu” folgende Bezeichnung ein: „Modellzuordnung auf Grunlage des Datenmodells Intrastat”.
4. Geben Sie im Feld „Name” die Bezeichnung „Intrastat-Beispielzuordnung” ein.
    * Intrastat-Beispielzuordnung  
5. Klicken Sie auf Konfiguration erstellen.



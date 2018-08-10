--- 
title: "Einem von einem Ladungsträger gesteuerten Lagerplatz als abgeschlossen melden "
description: Dieser Aufgabenleitfaden zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist.
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a>Einem von einem Ladungsträger gesteuerten Lagerplatz als abgeschlossen melden  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieser Aufgabenleitfaden zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist. Eine anwendbare Arbeitsrichtlinie ist die Voraussetzung für diese Aufgabe. Ein vorheriger Aufgabenleitfaden zeigte die Einstellungen der Arbeitsrichtlinie an. Dieser Aufgabenleitfaden erfordert eine Dynamics AX-Anwendung der Version 7.0.1 oder später.




## <a name="set-up-an-output-location"></a>Richten Sie einen Ausgabelagerplatz ein
1. Wechseln Sie zu Organisationsverwaltung > Ressourcen > Ressourcengruppen.
2. Wählen Sie in der Liste Ressourcengruppe "5102" aus.
3. Klicken Sie auf Bearbeiten.
4. Geben Sie im Feld "Ausgangslagerort" den Wert "51" ein.
5. Geben Sie im Feld "Ausgangslagerplatz" den Wert "001" ein.
    * Lagerplatz 001 ist kein kennzeichengesteuerter Lagerplatz. Sie können einen Ausgabelagerplatz ohne Kennzeichen nur einrichten, wenn eine anwendbare Arbeitsrichtlinie für den Lagerplatz vorhanden ist.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Erstellen Sie einen Produktionsauftrag und melden Sie ihn als abgeschlossen
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
3. Klicken Sie auf "Neuer Produktionsauftrag".
4. Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein.
5. Klicken Sie auf Erstellen.
6. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
7. Klicken Sie auf "Vorkalkulation".
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Start".
10. Klicken Sie auf die Registerkarte Allgemeines.
11. Wählen Sie im Feld "Stücklistenverbrauch" die Option "Nie" aus.
12. Klicken Sie auf "OK".
13. Klicken Sie auf Fertigmeldung.
14. Klicken Sie auf die Registerkarte Allgemeines.
15. Wählen Sie "Ja" im Feld "Fehler akzeptieren" aus.
16. Klicken Sie auf "OK".
17. Klicken Sie im Aktivitätsbereich auf "Lagerort".
18. Klicken Sie auf "Arbeitsdetails".
    * Wenn der Produktionsauftrag als fertig gemeldet wurde, wurde keine Arbeit für die Einlagerung generiert. Dies tritt auf, weil eine Arbeitsrichtlinie definiert ist, die verhindert, dass Arbeit generiert wird, wenn Produkt L0101 als fertig nach Lagerplatz 001 gemeldet wird.  



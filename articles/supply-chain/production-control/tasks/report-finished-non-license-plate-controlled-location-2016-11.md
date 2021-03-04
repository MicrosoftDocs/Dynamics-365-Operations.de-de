---
title: Melden Sie einen nicht kennzeichengesteuerte Lagerplatz als beendet (Anwendung, Mai 2016)
description: Dieser Aufgabenleitfaden zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a9010b95cfd0528cd3b532627d19a3b340bdca4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428397"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Melden Sie einen nicht kennzeichengesteuerte Lagerplatz als beendet (Anwendung, Mai 2016)

[!include [banner](../../includes/banner.md)]

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
15. Wählen Sie „Ja“ im Feld "Fehler akzeptieren" aus.
16. Klicken Sie auf "OK".
17. Klicken Sie im Aktivitätsbereich auf "Lagerort".
18. Klicken Sie auf "Arbeitsdetails".
    * Wenn der Produktionsauftrag als fertig gemeldet wurde, wurde keine Arbeit für die Einlagerung generiert. Dies tritt auf, weil eine Arbeitsrichtlinie definiert ist, die verhindert, dass Arbeit generiert wird, wenn Produkt L0101 als fertig nach Lagerplatz 001 gemeldet wird.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
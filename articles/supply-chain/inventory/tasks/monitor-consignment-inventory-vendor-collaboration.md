---
title: Lagerbestand mithilfe der Kreditorenkooperation überwachen
description: Dieses Verfahren zeigt, wie Sie Kreditor-Kooperationen nutzen, um Informationen zum Bestand des Produkts anzuzeigen, den Sie in der Lieferung des Debitors platziert haben.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8186b553e8518f3153bfd88b89121d4b0567501b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329435"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Lagerbestand mithilfe der Kreditorenkooperation überwachen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie Sie Kreditor-Kooperationen nutzen, um Informationen zum Bestand des Produkts anzuzeigen, den Sie in der Lieferung des Debitors platziert haben. Sie können außerdem den Verbrauch des Bestandes überwachen, wenn der Debitor den Besitz übernimmt. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="view-consumed-inventory"></a>Verbrauchten Bestand anzeigen
1. Wechseln Sie zu "Kreditor-Kooperation" > "Lieferbestand" > "Aus Unterlieferungsbestand erhaltene Produkte".
    * Die Liste enthält die Produktzugangspositionen, die generiert wurden, als der Besitzer des Lieferungsbestandes vom Kreditor auf den Debitor geändert wurde. Möglicherweise müssen Sie rechts nach unten scrollen, um die Mengen und weitere Informationen anzuzeigen. Sie können die Informationen in dieser Liste verwenden, um Rechnungen für den Debitor zu generieren. Sie können die Daten auch nach Microsoft Excel exportieren.   
2. Klicken Sie auf "Bestellung anzeigen".
3. Erweitern Sie den Abschnitt "Positionsdetails".
    * Die Position wird als Lieferung markiert und der Kopfbereich zeigt an, dass die Bestellung den Status "Eingegangen" hat.  
4. Schließen Sie die Seite.

## <a name="view-on-hand-inventory"></a>Verfügbaren Lagerbestand anzeigen
1. Wechseln Sie zu "Kreditor-Kooperation" > "Lieferbestand" > "Verfügbarer Lagerbestand".
    * Die Seite "Verfügbare Lieferungsbestand" zeigt den Bestand, den Sie am Lagerort des Debitors besitzen. Sie können zusätzliche Dimensionen eingegeben, z. B. der Standort und der Lagerort, indem Sie auf die Registerkarte "Dimensionen anzeigen" klicken.   


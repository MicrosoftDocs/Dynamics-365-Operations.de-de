--- 
title: "Eine Bestellung für einen einmaligen Lieferanten erstellen"
description: "Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Eine Bestellung für einen einmaligen Lieferanten erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen. Der Lieferant wird automatisch mit der Bestellung erstellt und somit muss das Kreditorenkonto nicht manuell erstellt werden. Bestellungen werden normalerweise von einem Einkaufsvertreter erstellt. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Es ist eine Voraussetzung, dass ein einmaliges Kreditorenkonto auf der Seite "Kreditorenkontenparameter" eingerichtet wurde.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Eine Bestellung für einen einmaligen Lieferanten erstellen
1. Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Wählen Sie "Ja" im Feld "Einmaliger Lieferant" aus.
    * Ein Kreditorenkonto wird automatisch erstellt und der Bestellung zugewiesen. Das Kreditorenkonto wird auf Basis der Vorlage erstellt, die auf der Registerkarte "Allgemein" auf der Seite "Kreditorenkontenparameter" angegeben wird.  
4. Geben Sie im Feld "Name" einen Namen für den Lieferanten ein.
5. Klicken Sie auf "OK".
    * Die Bestellung kann jetzt wie jeder andere Auftrag abgeschlossen und verarbeitet werden. Es gibt keine speziellen Eigenschaften, in Bezug darauf, wie dies erfolgen soll. Die Rechnung berücksichtigt eine fällige Transaktion zum Kreditorenkonto, das mit dem Auftrag erstellt wurde, und die Zahlung wird dann verarbeitet. Wenn dies abgeschlossen ist, kann das Kreditorenkonto gelöscht werden. Dies erfolgt gewöhnlich durch die Kreditorenkontenabteilung.  



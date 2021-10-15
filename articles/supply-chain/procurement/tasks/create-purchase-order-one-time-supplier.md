---
title: Eine Bestellung für einen einmaligen Lieferanten erstellen
description: Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e89a9d1b382efa3b90b8d70e84777321e9595f4a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579543"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Eine Bestellung für einen einmaligen Lieferanten erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen. Der Lieferant wird automatisch mit der Bestellung erstellt und somit muss das Kreditorenkonto nicht manuell erstellt werden. Bestellungen werden normalerweise von einem Einkaufsvertreter erstellt. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Es ist eine Voraussetzung, dass ein einmaliges Kreditorenkonto auf der Seite "Kreditorenkontenparameter" eingerichtet wurde.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Eine Bestellung für einen einmaligen Lieferanten erstellen
1. Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Wählen Sie "Ja" im Feld "Einmaliger Lieferant" aus.
    * Ein Kreditorenkonto wird automatisch erstellt und der Bestellung zugewiesen. Das Kreditorenkonto wird auf Basis der Vorlage erstellt, die auf der Registerkarte "Allgemein" auf der Seite "Kreditorenkontenparameter" angegeben wird.  
4. Geben Sie im Feld "Name" einen Namen für den Lieferanten ein.
5. Klicken Sie auf "OK".
    * Die Bestellung kann jetzt wie jeder andere Auftrag abgeschlossen und verarbeitet werden. Es gibt keine speziellen Eigenschaften, in Bezug darauf, wie dies erfolgen soll. Die Rechnung berücksichtigt eine fällige Transaktion zum Kreditorenkonto, das mit dem Auftrag erstellt wurde, und die Zahlung wird dann verarbeitet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
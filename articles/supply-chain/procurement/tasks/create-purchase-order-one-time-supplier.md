---
title: Eine Bestellung für einen einmaligen Lieferanten erstellen
description: Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe76a3d481c3bc8dd3a3d45eda031df61ece4aa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812372"
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
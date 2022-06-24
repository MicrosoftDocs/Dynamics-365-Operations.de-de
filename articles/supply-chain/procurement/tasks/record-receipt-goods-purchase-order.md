---
title: Den Warenzugang auf der Bestellung erfassen
description: In diesem Artikel wird erläutert, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882459"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Den Warenzugang auf der Bestellung erfassen

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird. Es ist auch möglich, den Produktzugang im Lagerort zu erfassen und ihn dann später auf der Bestellung aufzuzeichnen. Diese Aufgabe wird gewöhnlich von einem Einkäufer oder einem Kreditorenkontenkoordinator ausgeführt. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Das Beispiel umfasst Schritte, um eine einfache Bestellung zu erstellen, damit Sie die Prozedur als Aufgabenleitfaden wiedergeben können. Wenn Sie die Prozedur mit Ihren eigenen Daten verwenden, müssen Sie bei der Unteraufgabe **Warenzugang erfassen** beginnen.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Eine neue Bestellung für den Warenzugang vorbereiten
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Bestellungen > Alle Bestellungen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Kreditorenkonto** den Wert `US-101` ein.
4. Wählen Sie **OK**.
5. Geben Sie im Feld **Artikelnummer** den Wert `M0001` ein.
6. Geben Sie im Feld **Menge** den Wert `5` ein.
7. Wählen Sie im Aktivitätsbereich **Einkauf** aus.
8. Wählen Sie **Bestätigen** aus.

## <a name="record-receipt-of-goods"></a>Warenzugang erfassen
1. Wählen Sie im Aktivitätsbereich **Wareneingang** aus.
2. Wählen Sie **Produktzugang** aus. Das Feld **Menge** ermöglicht es Ihnen, verschiedene Optionen für die Menge auszuwählen, die Sie empfangen möchten. Zum Beispiel wenn eine Menge vorher im Lagerort registriert worden ist, können Sie **Erfasste Menge** auswählen. Für dieses Beispiel verwenden Sie den Wert **Bestellte Menge**.
3. Erweitern Sie den Abschnitt **Übersicht**.
4. Geben Sie im Feld **Produktzugang** irgendeinen Wert ein. Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.  
5. Erweitern Sie den Abschnitt **Positionen**.
6. Legen Sie **Menge** auf „4“ fest. Hier sind Sie in der Lage, die Menge manuell zu anzugeben, die für jede Position zum Auftrag empfangen wird.  
7. Wählen Sie **OK**. Die Waren sind jetzt auf der Bestellung als empfangen erfasst worden und eine Produktzugangserfassung ist als Dokument, um dies widerzuspiegeln, erstellt worden. Sie können die Aktivität "Produktzugang" verwenden, um die Erfassungen zu überprüfen, die mit der Bestellung erstellt wurden und um zu sehen, was wann empfangen wurde.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Eine Bestellung mit einem Lieferzeitplan erstellen
description: In diesem Thema wird gezeigt, wie ein Lieferzeitplan für eine Bestellung erstellt wird.
author: RichardLuan
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8cbcd46e84ca9e718a0f8f59c106147544a3751
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021803"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Eine Bestellung mit einem Lieferzeitplan erstellen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird gezeigt, wie ein Lieferzeitplan für eine Bestellung erstellt wird. Ein Lieferzeitplan wird verwendet, wenn eine Menge für einen Auftrag oder eine Erfassung angefordert wird, um in mehreren Lieferungen geliefert zu werden. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Diese Prozedur würde normalerweise durch einen Einkaufsvertreter erfolgen.

## <a name="create-a-delivery-schedule"></a>Lieferzeitplan erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Bestellungen > Alle Bestellungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Kreditorenkonto** den Wert `US-101` ein.
4. Wählen Sie **OK**.
5. Geben Sie im Feld **Artikelnummer** den Wert `M0001` ein.
6. Geben Sie im Feld **Menge** den Wert `10` ein.
7. Wählen Sie **Bestellposition**.
8. Wählen Sie **Lieferzeitplan**.
- Die Seite **Lieferzeitplan** gestattet es Ihnen, die Anzahl von Lieferungen anzugeben, in denen die Gesamtmenge der Auftragsposition vom Kreditor geliefert wird.  
- Standardmäßig kopiert das System die Gesamtmenge und andere Lieferdetails der ursprünglichen Bestellposition in die erste Lieferzeitplanposition. In diesem Beispiel erstellen wir einen Zeitplan für zwei Lieferungen, wobei das Datum von der zweiten Lieferung um eine Woche nach der ersten Lieferung verschoben ist.  
9. Ändern Sie im Feld **Menge** die Menge in `4`.
10. Wählen Sie **Neu** aus.
11. Geben Sie im Feld **Menge** die Zahl `6` als die verbleibende Menge ein.
- Im Lieferdatumsfeld wählen Sie ein Datum aus, das eine Woche nach dem Datum der ersten Lieferposition liegt.  
- Sie können die Gesamtmenge nachverfolgen, die den Lieferzeitplanpositionen zugeordnet ist, indem Sie die Felder **Summe** und **Verbleibend** ansehen. Wenn die Restmenge Null ist, ist die gesamte Menge aus der ursprünglichen Position dem Zeitplan zugewiesen worden.  
12. Erweitern Sie den Abschnitt **Konvertierung von Belastungen**.
- Die Optionen hier erlauben es Ihnen zu steuern, wie Sie möchten, dass Belastungen über die Lieferzeitplanpositionen verteilt werden. Wenn Sie **Bruttobeträge kopieren** auswählen, wird der Belastungsbetrag auf der ursprünglichen Auftragsposition zu jeder Lieferposition kopiert. Die Option **Zu Lieferpositionen zuordnen** teilt die ursprüngliche Positionsbelastung gemäß der Menge zu jeder Lieferposition.  
13. Reduzieren Sie den Abschnitt **Konvertierung von Belastungen**.
14. Wählen Sie **OK**.
- Der Lieferzeitplan ist jetzt auf den Auftrag angewendet worden.  
- Die ursprüngliche Auftragsposition, die jetzt als "Geschäftsbezogene Position" bezeichnet wird, ist in eine "Auftragsposition mit mehreren Lieferungen" umgewandelt worden. Sie ist mit einem eindeutig identifizierbarem Symbol markiert und fungiert als Kopfzeile für die Lieferpositionen.  
15. Wählen Sie die zweite Auftragsposition aus, die die erste der zwei Lieferpositionen ist.
- Die beiden neuen Positionen, die als "Lieferpositionen" bezeichnet werden, bilden einen Lieferzeitplan. Der Auftrag wird anhand dieser Positionen und nicht der ursprünglichen Position verarbeitet. Wenn Dokumente wie Bestätigungen, Produktzugangserfassungen oder Rechnungen gedruckt werden, werden nur die Lieferpositionen angezeigt.  

## <a name="change-the-delivery-schedule"></a>Den Lieferzeitplan ändern
Sie können die Menge bei Lieferpositionen ändern. Wenn Sie diesen Schritt ausführen, wird die geschäftsbezogene Position automatisch auf die Gesamtmenge in den Lieferpositionen aktualisiert.  
1. Ändern Sie im Feld **Menge** der ersten Lieferposition die Menge von `4` in `5`.
2. Wählen Sie die erste Auftragsposition (die geschäftsbezogene Position) aus.  
- Die Menge in der geschäftsbezogenen Position ist zu "11" geändert worden.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Den Produktempfang unter Verwendung der Lieferzeitpläne verarbeiten
Die Bestellung muss bestätigt werden, bevor der Produktzugang verarbeitet werden kann. In diesem Beispiel wird der Zugang direkt zur Bestellung aufgezeichnet. Der Zugang könnte auch erfasst worden sein, wenn die Waren im Lager ankamen.  
1. Wählen Sie im Aktivitätsbereich **Einkauf** aus.
2. Wählen Sie **Bestätigen** aus.
3. Wählen Sie im Aktivitätsbereich **Wareneingang** aus.
4. Wählen Sie **Produktzugang** aus. Geben Sie im Feld **Produktzugang** irgendeinen Wert ein.
- Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.  
- Wählen Sie im Feld **Menge** die Option **Bestellte Menge** aus. Diese Option bedeutet, dass der Zugang für die Menge verarbeitet wird, mit der die Auftragspositionen erstellt wurden.  
- Stellen Sie sicher, dass das Feld **Produktzugang drucken** auf **Nein** festgelegt ist. Drucken ist in diesem Beispiel nicht erforderlich.  
5. Erweitern Sie den Abschnitt **Positionen**.
- Beachten Sie, wie der Produktzugang für die zwei Lieferpositionen und nicht die ursprüngliche Auftragsposition erstellt wird. Wenn der Zugang am Lagerort erfasst worden wäre, wäre er auch in den Lieferzeitplanpositionen erfasst worden.  
6. Reduzieren Sie den Abschnitt **Positionen**.
7. Klicken Sie auf **OK**, um den Zugang zu buchen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
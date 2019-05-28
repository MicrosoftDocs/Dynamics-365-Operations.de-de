---
title: Eine Bestellung mit einem Lieferzeitplan erstellen
description: Diese Prozedur zeigt, wie ein Lieferzeitplan für eine Bestellung erstellt wird.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a9b7b233339d41605e1b115bd14a18b706ef226
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547536"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Eine Bestellung mit einem Lieferzeitplan erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie ein Lieferzeitplan für eine Bestellung erstellt wird. Ein Lieferzeitplan wird verwendet, wenn eine Menge für einen Auftrag oder eine Erfassung angefordert wird, um in mehreren Lieferungen geliefert zu werden. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Diese Prozedur würde normalerweise durch einen Einkaufsvertreter erfolgen.


## <a name="create-a-delivery-schedule"></a>Lieferzeitplan erstellen
1. Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Kreditorenkonto" den Wert US-101 ein.
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" den Wert M0001 ein.
6. Geben Sie im Feld "Menge" den Wert "10" ein.
7. Klicken Sie auf die Bestellposition.
8. Klicken Sie auf "Lieferzeitplan".
    * Die Seite "Lieferzeitplan" gestattet es Ihnen, die Anzahl von Lieferungen anzugeben, in denen die Gesamtmenge der Auftragsposition vom Kreditor geliefert wird.  
    * Standardmäßig kopiert das System die Gesamtmenge und andere Lieferdetails der ursprünglichen Bestellposition in die erste Lieferzeitplanposition. In diesem Beispiel erstellen wir einen Zeitplan für zwei Lieferungen, wobei das Datum der zweiten Lieferung um eine Woche nach der ersten Lieferung verschoben ist.  
9. Ändern Sie im Feld "Menge" die Menge zu "4".
10. Klicken Sie auf "Neu".
11. Geben Sie im Feld "Menge" die Zahl "6" als die verbleibende Menge ein.
    * Im Lieferdatumsfeld wählen Sie ein Datum aus, das eine Woche nach dem Datum auf der ersten Lieferposition liegt.  
    * Sie können die Gesamtmenge nachverfolgen, die den Lieferzeitplanpositionen zugeordnet ist, indem Sie die Felder "Summe" und "Verbleibend" betrachten. Wenn die Restmenge Null ist, ist die gesamte Menge aus der ursprünglichen Position dem Zeitplan zugewiesen worden.  
12. Erweitern Sie den Abschnitt "Konvertierung von Belastungen".
    * Die Optionen hier erlauben es Ihnen zu steuern, wie Sie möchten, dass Belastungen über die Lieferzeitplanpositionen verteilt werden. Wenn Sie "Bruttobeträge kopieren" auswählen, wird der Belastungsbetrag auf der ursprünglichen Auftragsposition zu jeder Lieferposition kopiert. Die Option "Zu Lieferpositionen zuordnen" teilt die ursprüngliche Positionsbelastung gemäß der Menge zu jeder Lieferposition.  
13. Reduzieren Sie den Abschnitt "Konvertierung von Belastungen".
14. Klicken Sie auf "OK".
    * Der Lieferzeitplan ist jetzt auf den Auftrag angewendet worden.  
    * Die ursprüngliche Auftragsposition, die jetzt als "Geschäftsbezogene Position" bezeichnet wird, ist in eine "Auftragsposition mit mehreren Lieferungen" umgewandelt worden. Sie ist mit einem eindeutig identifizierbarem Symbol markiert und fungiert als Kopfzeile für die Lieferpositionen.  
15. Wählen Sie die zweite Auftragsposition aus, die die erste der zwei Lieferpositionen ist.
    * Die beiden neuen Positionen, die als "Lieferpositionen" bezeichnet werden, bilden einen Lieferzeitplan. Der Auftrag wird anhand dieser Positionen und nicht der ursprünglichen Position verarbeitet. Wenn Dokumente wie Bestätigungen, Produktzugangserfassungen oder Rechnungen gedruckt werden, werden nur die Lieferpositionen angezeigt.  

## <a name="change-the-delivery-schedule"></a>Den Lieferzeitplan ändern
    * Sie können die Menge bei Lieferpositionen ändern. Wenn Sie diesen Schritt ausführen, wird die geschäftsbezogene Position automatisch auf die Gesamtmenge in den Lieferpositionen aktualisiert.  
1. Ändern Sie im Feld "Menge" der ersten Lieferposition die Menge von 4 auf 5.
2. Wählen Sie die erste Auftragsposition (die geschäftsbezogene Position) aus.
    * Die Menge in der geschäftsbezogenen Position ist zu "11" geändert worden.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Den Produktempfang unter Verwendung der Lieferzeitpläne verarbeiten
    * Die Bestellung muss bestätigt werden, bevor der Produktzugang verarbeitet werden kann. In diesem Beispiel wird der Zugang direkt zur Bestellung aufgezeichnet. Der Zugang könnte auch erfasst worden sein, wenn die Waren im Lager ankamen.  
1. Klicken Sie im Aktivitätsbereich auf "Einkauf".
2. Klicken Sie auf "Bestätigen".
3. Klicken Sie im Aktivitätsbereich auf "Empfangen".
4. Klicken Sie auf "Produktzugang".
5. Geben Sie im Feld "Produktzugang" irgendeinen Wert ein.
    * Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.  
    * Wählen Sie im Feld "Menge" die Option "Bestellte Menge" aus. Diese Option bedeutet, dass der Zugang für die Menge verarbeitet wird, mit der die Auftragspositionen erstellt wurden.  
    * Stellen Sie sicher, dass das Feld "Produktzugang drucken" auf "Nein" festgelegt ist. Drucken wird in diesem Beispiel nicht benötigt.  
6. Erweitern Sie den Abschnitt "Positionen".
    * Beachten Sie, wie der Produktzugang für die zwei Lieferpositionen und nicht die ursprüngliche Auftragsposition erstellt wird. Wenn der Zugang am Lagerort erfasst worden wäre, wäre er auch auf den Lieferzeitplan-Positionen erfasst worden.  
7. Reduzieren Sie den Abschnitt "Positionen".
8. Klicken Sie auf OK, um den Zugang zu buchen.


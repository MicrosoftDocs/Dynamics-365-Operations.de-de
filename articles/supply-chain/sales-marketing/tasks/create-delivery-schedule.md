---
title: Lieferzeitplan erstellen
description: Diese Prozedur zeigt, wie ein Lieferzeitplan für einen Auftrag erstellt wird.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97dbbcc7173dcece9aea833551e8f985246bdbb2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578967"
---
# <a name="create-delivery-schedule"></a>Lieferzeitplan erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie ein Lieferzeitplan für einen Auftrag erstellt wird. Ein Lieferzeitplan wird verwendet, wenn eine Menge für einen Auftrag oder ein Angebot angefordert wird, um in mehreren Lieferungen geliefert zu werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.


## <a name="create-delivery-schedule"></a>Lieferzeitplan erstellen
1. Wechseln Sie zu "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Menge" eine Zahl ein, die größer als 1 ist.
7. Klicken Sie auf "Auftragsposition".
8. Klicken Sie auf "Lieferzeitplan".
    * Die Seite "Lieferzeitplan" ist der Ort, an dem Sie die Anzahl von Lieferungen angeben können, in denen die Gesamtmenge der Auftragsposition an den Debitor geliefert wird.    
    * Standardmäßig kopiert das System die Gesamtmenge und andere Lieferdetails der ursprünglichen Auftragsposition in die erste Lieferzeitplanposition. In diesem Beispiel erstellen wir einen Zeitplan für zwei Lieferungen, wobei das Datum für die zweite Lieferung um eine Woche nach der ersten verschoben ist.  
9. Geben Sie im Feld "Menge" eine Zahl ein, die Teil der Gesamtmenge ist.
10. Klicken Sie auf Neu.
11. Geben Sie im Feld "Menge" die verbleibende Menge ein.
12. Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein, das eine Woche nach dem Datum der ersten Lieferposition liegt.
    * Die beiden Optionen im Inforegister „Konvertierung von Belastungen“ steuern, wie Sie die Belastungen über die Lieferzeitplanpositionen verteilen möchten, sobald diese der ursprünglichen Auftragsposition zugewiesen wurden. Wenn Sie "Bruttobeträge kopieren" auswählen, wird derselbe Belastungsbetrag zu jeder Position kopiert. Die Option "Zu Lieferpositionen zuordnen" verteilt die Belastung gleichmäßig auf die Lieferpositionen.  
    * Nur feste Belastungen können aufgeteilt werden, wohingegen variable Belastungen nach wie vor in die Positionen kopiert werden.  
13. Verschieben Sie den Cursor weg von der zweiten Lieferposition, um die Seite zu aktualisieren.
    * Sie können die Gesamtmenge nachverfolgen, die den Lieferzeitplanpositionen zugeordnet ist, indem Sie die Felder Summe und Verbleibend ansehen. Wenn die Restmenge Null ist, ist die gesamte Menge aus der ursprünglichen Position dem Zeitplan zugewiesen worden.   
14. Klicken Sie auf "OK".
    * Der Lieferzeitplan wurde jetzt in die Auftragspositionen kopiert.   
    * Die ursprüngliche Auftragsposition, die als "Geschäftsbezogene Position" bezeichnet wird, ist in eine "Auftragsposition mit mehreren Lieferungen" umgewandelt worden. Sie ist mit einem eindeutig identifizierbarem Symbol markiert und fungiert als eine Kopfzeile für die Lieferpositionen.  
    * Die beiden neuen Positionen, die als Lieferpositionen bezeichnet werden, bilden einen Lieferzeitplan. Der Auftrag wird anhand dieser Positionen und nicht der ursprünglichen Position verarbeitet. Wenn Dokumente wie Auftragsbestätigungen, Kommissionierlisten, Lieferscheine oder Rechnungen gedruckt werden, werden nur die Lieferpositionen angezeigt.   
    * Die Lieferpositionen können verschiedene Lieferdaten, Mengen, Lieferarten und Lagerdimensionen haben, wie Standort und Lagerort. Allerdings müssen die Produktdimensionen immer mit denen in der geschäftsbezogenen Position übereinstimmen und können nicht geändert werden.  
15. Geben Sie im Feld "Menge" eine Zahl ein, die größer als die aktuelle ist.
16. Wählen Sie die geschäftsbezogene Position aus, um die Auswirkung der Mengenneuberechnung anzuzeigen.
17. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".
18. Klicken Sie auf "Lieferschein buchen".
19. Erweitern Sie den Abschnitt "Parameter".
20. Wählen Sie im Feld "Menge" die Option "Alle" aus.
    * Beachten Sie, dass der Lieferschein für die beiden Lieferzeitplanpositionen und nicht die ursprüngliche Auftragsposition erstellt wird.  
21. Wählen Sie "Ja" im Feld "Lieferschein drucken" aus.
22. Klicken Sie auf "OK".
23. Klicken Sie auf "Ja".
24. Schließen Sie die Seite.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
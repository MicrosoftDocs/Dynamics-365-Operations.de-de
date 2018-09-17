--- 
title: Auftragsrechnungen erstellen
description: "Dieses Aufgabenhandbuch beschreibt, wie ein Auftrag fakturiert wird, einschließlich des Zusammenführens von Rechnungen sowie der Stapelverarbeitung."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-order-invoices"></a>Auftragsrechnungen erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Aufgabenhandbuch beschreibt, wie ein Auftrag fakturiert wird, einschließlich des Zusammenführens von Rechnungen sowie der Stapelverarbeitung. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="create-an-invoice-from-a-sales-order"></a>Eine Rechnung von einem Auftrag erstellen
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Versendete, jedoch nicht fakturierte Aufträge".
2. Wählen Sie einen Auftrag in der Liste aus. 
3. Klicken Sie im Aktivitätsbereich auf "Rechnung".
4. Klicken Sie auf "Rechnung".
    * Beachten Sie, dass diesem Auftrag mehrere Lieferscheine zugeordneten sind. Darin wird nur das Wort <multiple> anstelle der Lieferscheinnummer angezeigt.  
5. Erweitern Sie den Abschnitt "Parameter".
    * Buchen muss auf "Ja" festgelegt werden, um die Rechnung zu buchen. Sie können auch das Buchen ausschalten und die Rechnung nur drucken. Sie können jedoch das gleiche Ergebnis erreichen, indem Sie eine Proforma-Rechnung anstelle einer Rechnung erstellen.  
    * Diese Option wird für Stapelverarbeitungsaufträge genutzt. Die Anfrage läuft, wenn der Batchauftrag ausgeführt wrid.    
6. Wählen Sie im Feld "Drucken" die Option "Nach" aus.
7. Wählen Sie "Ja" für "Rechnung drucken" aus.
    * Die Druckverwaltung kann mehrere Kopien der Rechnung drucken und auch die Rechnung per E-Mail als PDF-Datei senden.  
8. Wählen Sie im Feld "Chargen Drucken" die Option "Zusammenfassen" aus.
9. Wählen Sie im Feld "Kreditlimit prüfen" die Option "Saldo" aus.
10. Klicken Sie auf "Abbrechen".

## <a name="combine-orders-into-a-single-invoice"></a>Aufträge in einer einzelnen Rechnung kombinieren
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Suchen Sie einen Debitoren, bei dem mehrere Rechnungen offen sind.
3. Wählen Sie einen offenen Auftrag aus.
4. Wählen Sie einen weiteren offenen Auftrag für denselben Debitoren aus.
5. Klicken Sie im Aktivitätsbereich auf "Rechnung".
6. Klicken Sie auf "Rechnung".
7. Erweitern Sie den Abschnitt "Parameter".
8. Wählen Sie im Feld "Menge" die Option "Alle" aus.
    * Beachten Sie, dass zwei Rechnungen im Abschnitt "Übersicht" aufgeführt sind. Jetzt führen wir sie in einer einzelnen Rechnung zusammen.  
9. Wählen Sie im Feld "Sammelaktualisierung für" die Option "Rechnungskonto" aus.
10. Klicken Sie auf "Anordnen", um die Aufträge in einer einzelnen Rechnung zusammenzuführen.
    * Die beiden Aufträge werden nun in einer einzelnen Rechnung zusammengeführt.   
11. Klicken Sie auf "Abbrechen".
12. Klicken Sie auf "Ja".

## <a name="post-invoices-in-a-batch"></a>Rechnungen in einer Charge buchen
1. Wechseln Sie zu "Debitoren" > "Rechnungen" > "Chargenrechnungsstellung" > "Rechnung".
2. Klicken Sie auf Auswählen.
3. Klicken Sie auf "OK".
4. Klicken Sie auf "Charge".
5. Klicken auf "Ja", um die Stapelverarbeitung zu aktivieren.
6. Klicken Sie auf "Wiederholung".
7. Tage auswählen
8. Klicken Sie auf "OK".
9. Klicken Sie auf "OK".
10. Klicken Sie auf "Abbrechen".
11. Klicken Sie auf "Ja".



---
title: Auftragsrechnungen erstellen
description: Dieser Artikel beschreibt, wie Sie einen Verkaufsauftrag fakturieren, einschließlich der Zusammenführung von Rechnungen und Batch-Verarbeitung.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778383"
---
# <a name="create-sales-order-invoices"></a>Auftragsrechnungen erstellen

[!include [banner](../../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie einen Verkaufsauftrag fakturieren, einschließlich der Zusammenführung von Rechnungen und Batch-Verarbeitung. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="create-an-invoice-from-a-sales-order"></a>Eine Rechnung von einem Auftrag erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Versendete, jedoch nicht fakturierte Aufträge**.
2. Wählen Sie einen Auftrag in der Liste aus. 
3. Klicken Sie im **Aktionsbereich** auf **Rechnung > Generieren > Rechnung**. Beachten Sie, dass diesem Auftrag mehrere Lieferscheine zugeordneten sind. Es wird nur das Wort *Mehrfach* anstelle der Lieferscheinnummer angezeigt.  
4. Erweitern Sie den Abschnitt **Parameter**.
    - Buchen muss auf **Ja** festgelegt werden, um die Rechnung zu buchen. Sie können auch das Buchen ausschalten und die Rechnung nur drucken. Sie können jedoch das gleiche Ergebnis erreichen, indem Sie eine Proforma-Rechnung anstelle einer Rechnung erstellen.  
    - Diese Option wird für Stapelverarbeitungsaufträge genutzt. Die Anfrage läuft, wenn der Batchauftrag ausgeführt wrid.
5. Wählen Sie im Feld **Drucken** die Option **Nach** aus.
6. Wählen Sie **Ja** für **Rechnung drucken** aus. Die Druckverwaltung kann mehrere Kopien der Rechnung drucken und auch die Rechnung per E-Mail als PDF-Datei senden.  
7. Wählen Sie im Feld **Zuschläge drucken** die Option **Zusammenfassen** aus.
8. Wählen Sie im Feld **Kreditlimit prüfen** die Option **Saldo** aus.
9. Klicken Sie auf **Abbrechen**.

## <a name="combine-orders-into-a-single-invoice"></a>Aufträge in einer einzelnen Rechnung kombinieren
1. Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Alle Aufträge**.
2. Suchen Sie einen Debitoren, bei dem mehrere Rechnungen offen sind.
3. Wählen Sie mehrere offene Aufträge desselben Debitors aus.
4. Klicken Sie im **Aktionsbereich** auf **Rechnung > Generieren > Rechnung**.
5. Erweitern Sie den Abschnitt **Parameter**.
6. Wählen Sie im Feld **Menge** die Option **Alle** aus. Beachten Sie, dass zwei Rechnungen im Abschnitt "Übersicht" aufgeführt sind. Jetzt führen wir sie in einer einzelnen Rechnung zusammen.  
7. Wählen Sie im Feld **Sammelaktualisierung für** die Option **Rechnungskonto**. aus.
8. Klicken Sie auf **Anordnen**, um die Aufträge in einer einzelnen Rechnung zusammenzuführen. Die beiden Aufträge werden nun in einer einzelnen Rechnung zusammengeführt.   
9. Klicken Sie auf **Abbrechen**.
10. Klicken Sie auf **Ja**.

## <a name="post-invoices-in-a-batch"></a>Rechnungen in einer Charge buchen
1. Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Rechnungen > Rechnungsstellung in Chargen > Rechnung**.
2. Klicken Sie auf **Auswählen**.
3. Klicken Sie auf **OK**.
4. Klicken Sie auf **Charge**.
5. Wählen Sie für **Stapelverarbeitung** die Option **Ja** aus.
6. Klicken Sie auf **Wiederholung**.
7. Wählen Sie **Tage** aus.
8. Klicken Sie auf **OK**.
9. Klicken Sie auf **OK**.
10. Klicken Sie auf **Abbrechen**.
11. Klicken Sie auf **Ja**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

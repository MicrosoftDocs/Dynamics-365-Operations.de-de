---
title: Eine Angebotsanforderung erstellen
description: Diese Prozedur zeigt Ihnen, wie Sie eine Angebotsanforderung erstellen.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68624a0288f9eaaf8f74b361bb308b8ca3c03b29
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428573"
---
# <a name="create-a-request-for-quotation"></a>Eine Angebotsanforderung erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie eine Angebotsanforderung erstellen. Dies würde normalerweise durch einen Einkaufsvertreter erfolgen. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Sie müssen Anfragetypen eingerichtet haben, bevor Sie beginnen. Sobald Sie diese Aufgabe abgeschlossen haben und eine Angebotsanforderung erstellt und gesendet haben, können Sie die Antworten nach Händler eingeben, diese vergleichen und den Vertrag erteilen.


## <a name="prepare-a-new-rfq"></a>Bereiten Sie eine neue Angebotsanforderung vor
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Angebotsanforderungen > Alle Angebotsanforderungen**.
2. Klicken Sie auf **Neu**.
    Die folgenden Bestelltypen sind verfügbar: Bestellung (dies ist standardmäßig): ein Dokument, das das Angebot bestätigt, Produkte zu kaufe,n oder die Annahme eines Angebots, Produkte gegen Bezahlung zu verkaufen. Bestellanforderung: Dieser Typ wird automatisch ausgewählt, wenn Sie eine Angebotsanforderung direkt auf Grundlage einer Bestellanforderung erstellen. Wenn Sie diese Option manuell auswählen, erhalten Sie einen Fehler. Kaufvertrag: Eine Vereinbarung über den Erwerb von Produkten in einer bestimmten Menge oder mit einem bestimmten Wert über einen gewissen Zeitraum. Wenn Sie diese Option auswählen, muss auch der Datumsbereich für den Kaufvertrag ausgewählt werden.  
3. Geben Sie im Feld **Dokumenttitel** einen Wert ein.
4. Geben Sie im Feld **Anfragetyp** einen Wert ein, oder wählen Sie einen Wert aus.
    + Wenn eine Bewertungsmethode dem Anfragetyp zugeordnet wird, wird dies dann die Standardbewertungsmethode für die Angebotsanforderung sein, die Sie erstellen. Es ist möglich, die Bewertungsmethode später zu ändern.  
    + Geben Sie im Feld **Lieferdatum** ein Datum ein.  
    + Wählen Sie das Datum aus, bis zu dem Sie die Artikel erhalten möchten.  
    + Geben Sie im Feld **Ablaufdatum und -uhrzeit** ein Datum und eine Uhrzeit ein.  
    + Geben Sie das Datum und die Uhrzeit an, bis zu denen die Händler auf die Angebotsanforderung antworten müssen.  
5. Geben Sie im Feld **Lagerort** einen Wert ein, oder wählen Sie einen Wert aus. Die Lieferadresse wird standardmäßig die Lagerortadresse sein.  
6. Klicken Sie auf **OK**.

## <a name="add-lines"></a>Positionen hinzufügen

Nachdem Sie die grundlegenden Informationen zu Ihrer Angebotsanforderung angegeben haben, geben Sie die Waren oder Dienstleistungen an, für die die Kreditoren Angebote abgeben sollen. Der Artikel ist der standardmäßigen Positionstyp.

1. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus. Wenn Sie USMF verwenden, können Sie T0020 auswählen.  
2. Geben Sie im Feld **Menge** eine Zahl ein.
3. Klicken Sie auf **Position hinzufügen**.
4. Wählen Sie im Feld **Positionstyp** die Option „Kategorie“ aus. Sie können den Kategoriepositionstyp verwenden, um Angebotsanforderungen für Nicht-Bestandswaren oder -dienstleistungen zu erstellen. Sie müssen anschließend den Typ von Gütern oder Dienstleistungen aus einer Hierarchie der Beschaffungskategorien auswählen.  
5. Geben Sie im Feld **Beschaffungskategorie** einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld **Produktname** einen Wert ein.
7. Geben Sie im Feld **Menge** eine Zahl ein.
8. Geben Sie im Feld **Einheit** einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="add-vendors"></a>Kreditoren hinzufügen
1. Klicken Sie auf **Kopfzeile**, um von der „Positionsansicht“ zur „Kopfzeilenansicht“ zu wechseln. 
2. Erweitern Sie den Abschnitt **Kreditor**.
3. Klicken Sie auf **Kreditoren automatisch hinzufügen**. Sie können der Angebotsanforderung automatisch Händler hinzufügen, basierend auf der Beschaffungskategorie der angeforderten Artikel. Wenn es keine für die Kategorien genehmigte Händler gibt, die in den Positionen enthalten sind, können Sie manuell Händler hinzufügen.  
4. Klicken Sie auf **Hinzufügen**.
5. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie auf **Hinzufügen**.
7. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus. Sobald Sie einen Händler ausgewählt haben, ist der Status Erstellt. Das bedeutet, dass die Kreditorinformationen in der Angebotsanforderung gespeichert wurden, die Angebotsanforderung jedoch noch nicht an den Kreditor gesendet wurde. Sie können einer Angebotsanforderung einen Kreditor unabhängig vom Kreditorstatus hinzufügen.  

## <a name="send-the-rfq-to-vendors"></a>Die Angebotsanforderung an Kreditoren senden
1. Klicken Sie im **Aktivitätsbereich** auf **Senden**. Überprüfen Sie auf der Seite "Angebotsanforderung wird gesendet.", dass es sich bei den in der Liste aufgeführten Händler um die gewünschten Empfänger der Angebotsanforderung handelt.  
2. Klicken Sie auf **Drucken**. Dieses Dialogfeld ermöglicht Ihnen, die Angebotsanforderung zu drucken. Wenn Sie sich dafür entscheiden, ein Antwortblatt zu drucken, wird der Inhalt von diesem in den Beschaffungsparametern definiert. Um auszuwählen, wie Antwortblätter gedruckt werden sollen, sobald Sie den Dialog Drucken geöffnet haben, klicken Sie auf Erweiterte Druckoptionen. Eine Angebotsanforderung wird für jeden Händler gedruckt. Diese enthält die Positionen, die den Status "Erstellt" oder "Versendet" haben. Stornierte Positionen und Positionen mit erfassten Antworten werden nicht gedruckt.   
3. Klicken Sie auf **Abbrechen**.
4. Klicken Sie auf **OK**.
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.

## <a name="view-the-rfq-journal"></a>Zeigen Sie die Angebotsanforderungserfassung an
1. Wechseln Sie zu **Beschaffung > Angebotsanforderungen > Weiterverfolgung von Angebotsanforderungen > Angebotsanforderungserfassungen**.
2. Klicken Sie auf **Vorschau anzeigen/Drucken**.
3. Klicken Sie auf **Vorschau des Originals**.
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.


---
title: Verkaufsangebote erstellen und bearbeiten
description: Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a8fe4928e2fdaeaeb568597b336d301193a8c8
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830468"
---
# <a name="create-and-edit-sales-quotations"></a>Verkaufsangebote erstellen und bearbeiten

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird. Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.


## <a name="create-a-sales-quotation"></a>Ein Verkaufsangebot erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Verkaufsangebote > Alle Angebote**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Feld **Kontotyp** „Interessent“ aus.
4. Geben Sie im Feld **Interessent** einen Wert ein, oder wählen Sie einen Wert aus.
5. Erweitern Sie den Abschnitt **Allgemein**. Da Sie sich für die Erstellung eines Angebots über den Bereich „Vertrieb und Marketing“ entschieden haben, wird der Typ automatisch auf „Verkaufsangebot“ festgelegt. Um ein Angebot für ein Projekt zu erstellen, müssen Sie über das **Projektverwaltungs- und Buchhaltungsmodul** darauf zugreifen.
6. Klicken Sie auf **OK**. Die Felder und Aktivitäten der Angebotspositionen sind mit denen in den Auftragspositionen vergleichbar.   Wie Aufträge können auch Angebote für einen bestimmten Artikel erstellt werden. Wenn Artikelnummer nicht bekannt ist oder nicht zum Zeitpunkt der Erstellung Angebots vorhanden ist, können Angebote für eine Verkaufskategorie erstellt werden.     
7. Geben Sie im Feld **Artikel** einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie in das Feld **Lagerort** einen Wert ein.
9. Geben Sie im Feld **Menge** eine Zahl ein. Sind gültige Handelsvereinbarungen für den zur Position ausgewählten Artikel vorhanden, werden die entsprechenden Preise und Rabatte automatisch in die Angebotsposition kopiert. Stellen Sie sicher, dass das Feld "Preis je Einheit" einen Wert enthält. Sie können auch Rabattwerte eingeben. 
10. Klicken Sie auf **Speichern**.
11. Klicken Sie im **Aktivitätsbereich** auf **Verkaufsangebot**.
12. Klicken Sie auf **Summen**.
13. Klicken Sie auf **OK**.
14. Wählen Sie das Verkaufsangebot aus.
15. Klicken Sie im **Aktivitätsbereich** auf **Angebot**.
16. Klicken Sie auf **Preissimulation**.
    - Auf der Seite **Preissimulation ausführen** können Sie mit der Anpassung des erwarteten Umsatzerlöses oder der Rentabilität des Angebots auf Grundlage des gewünschten „Preis je Einheit“, des Rabattbetrags, des Rabattprozentsatzes, des Gesamtbetrags, der Gewinnspanne bzw. des Deckungsbeitrags experimentieren. Wenn Sie mit den Zielvorgaben zufrieden sind, wenden Sie den Vorschlag auf die Angebotsposition an und die preisbezogene Felder werden entsprechend aktualisiert.  
    - Sie können so viele Preissimulationen erstellen wie gewünscht. Wenn Sie auf **Neu** klicken, werden die Preisbedingungen von der aktuellen Angebotsposition zur Seite kopiert. Sie können die Werte in jedem der preisbezogene Felder auf die Zielwerte ändern. Eine Änderung in einem der Felder löst eine Neuberechnung für alle anderen Felder aus. Damit das System die Handelsspanne und den Deckungsbeitrag berechnen kann, müssen die Einheitenkosten des Produkts muss bekannt sein. Verwenden Sie Registerkarte "Simulierte Preise" für eine detaillierte Ansicht der ursprünglichen Preise, der vorgeschlagenen Änderungen und ihrer Auswirkungen auf den Angebotssummen. Wenn eine Simulation für einen neuen Betrag auf ein Angebot angewendet wird, berechnet das System neu und legt einen neuen Wert für das Feld Preis je Einheit" fest. Wenn die Simulation auf Grundlage eines neuen Deckungsbeitrags oder ein neues Deckungsbeitragsverhältnis basiert, wird nur das Feld "Nettobetrag" aktualisiert. Der Preis je Einheit ist leer. In beiden Fällen werden alle Rabatten für die Angebotsposition gelöscht.
17. Klicken Sie im **Aktivitätsbereich** auf **Angebot**.
18. Klicken Sie auf **Angebot versenden**.
19. Wählen Sie „Ja“ im Feld **Angebot drucken** aus.
20. Klicken Sie auf **OK**. Der Bericht kann einige Minute dauern. Schließen Sie die Seite nicht.

## <a name="update-a-sales-quotation"></a>Ein Verkaufsangebot aktualisieren
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Verkaufsangebote > Alle Angebote**.
2. Klicken Sie im **Aktivitätsbereich** auf **Nachverfolgung**.
3. Klicken Sie auf **In Debitor konvertieren**.
4. Geben Sie im Feld **Kundenkonto** einen Wert ein.
5. Klicken Sie auf **Prüfen**. Stellen Sie sicher, das eine Nachricht anzeigt, dass die Kontonummer frei ist.  
6. Klicken Sie auf **OK**. Das System hat nun ein neues Debitorenkonto für den Interessenten im Angebot erstellt.  
7. Schließen Sie die Seite.
8. Klicken Sie im **Aktivitätsbereich** auf **Nachverfolgung**.
9. Klicken Sie auf **Bestätigen**.
10. Geben Sie im Feld **Grund** einen Wert ein, oder wählen Sie einen Wert aus.
11. Klicken Sie auf **OK**.
12. Klicken Sie im **Aktivitätsbereich** auf **Allgemein**.
13. Klicken Sie auf **Aufträge**
14. Schließen Sie die Seite.


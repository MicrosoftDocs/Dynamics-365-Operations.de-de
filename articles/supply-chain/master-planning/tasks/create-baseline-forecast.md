--- 
title: Grundplanung erstellen
description: Ein Produktionsplaner kann eine Grundplanung erstellen, indem er entweder Zeitserien-Planungsmodelle verwendet oder indem er den historischen Bedarf in die Planung kopiert.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e6363ee48c0d13c79a6c623205dfa10f50d6070f
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-baseline-forecast"></a>Grundplanung erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ein Produktionsplaner kann eine Grundplanung erstellen, indem er entweder Zeitserien-Planungsmodelle verwendet oder indem er den historischen Bedarf in die Planung kopiert. In diesem Verfahren wird dargestellt, wie Sie den historischen Bedarf zur Erstellung einer Grundplanung für alle Produkte mit einem Artikelverteilungsschlüssel erstellen. 


## <a name="set-up-an-item-allocation-key"></a>Einrichten eines Artikelverteilungsschlüssels
1. Wechseln Sie zu Masterplan > Einrichten >Intercompany-Planungsgruppen.
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".
    * Bedarfsplanungsausführungen zu juristischen Personen. Daher müssen Sie alle Unternehmen einrichten, für die Sie Planungen in einer unternehmensübergreifenden Planungsgruppe generieren möchten.  
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie auf "Artikelzuteilungsschlüssel".
    * Wählen Sie alle Artikelverteilungsschlüssel aus, für die Sie Planungen erstellen möchten.  
5. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den D_Aloc-Artikelverteilungsschlüssel aus.  
6. Klicken >.
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.

## <a name="set-up-the-demand-forecasting-paramters"></a>Bedarfsplanungsparameter einrichten
1. Wechseln Sie zu "Masterplan" > "Einrichten" > "Bedarfsplanung" > "Bedarfsplanungsparameter".
2. Erweitern Sie den Planungsalgorithmusparameter-Abschnitt.
3. Wählen Sie im Feld "Planungsgenerierungsstrategie" "Über historischen Bedarf kopieren" aus.
4. Klicken Sie auf "Speichern".

## <a name="create-a-baseline-forecast"></a>Grundplanung erstellen
1. Wechseln Sie zu Masterplan > Planung > Bedarfsplanung > Statistische Grundplanung generieren.
2. Geben Sie in das Feld "Von Datum" ein Datum ein.
    * Wenn Aufträge ab dem 1. Januar 2015 vorliegen, geben Sie dieses Datum ein. Falls nicht, geben Sie das früheste Datum Ihrer Aufträge ein.  
3. Geben Sie in das Feld "Bis Datum" ein Datum ein.
    * Geben Sie das letzte Datum Ihrer Aufträge ein, beispielsweise "31.03.2015".  
4. Geben Sie in das Feld "Von Datum" ein Datum ein.
    * Geben Sie "01.04.2015" ein. Dieses Datum wird automatisch als Startdatum des folgenden Planungszeitrahmens berechnet.  
5. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
6. Klicken Sie auf "Filter".
7. Markieren Sie in der Liste die ausgewählte Zeile.
    * Markieren Sie die Zeile mit Feld = Intercompany-Planungsgruppe.  
8. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Geben Sie die Intercompany-Planungsgruppe ein (z. B. 10), die Sie in der ersten Aufgabe verwendet haben.  
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Zeile aus mit Feld = Artikelzuteilungsschlüssel.  
10. Geben Sie im Feld "Kriterien" einen Wert ein.
11. Klicken Sie auf "OK".
12. Erweitern Sie den Abschnitt "Erweiterte Parameter".
13. Wählen Sie im Feld "Planungszeitrahmen" die Option "Monat" aus.
14. Geben Sie im Feld "Planungshorizont" eine "3" ein.
15. Geben Sie im Feld "Nichtplanungszeitraum" den Wert "1" ein.
16. Klicken Sie auf "OK".

## <a name="visualize-the-demand-forecast"></a>Visualisieren der Bedarfsplanung
1. Wechseln Sie zu >Masterplan > Planung > Bedarfsplanung > Angepasste Bedarfsplanung".
2. Wählen Sie in der Tabelle "AggregatedViewTable" die Zelle in Zeile "1", Spalte "2" aus. Dies ist der zweiten Monat, für den Sie die Planung erstellt haben.
3. Legen Sie QtyCell auf "400" fest.
    * Geben Sie in der Zelle eine andere Anzahl als das Ergebnis der Planung an, z. B. 400.  
4. Sie haben eine manuelle Regulierung der Planung vorgenommen. Beachten Sie die grafische Anzeige im nächsten Schritt.
5. Klicken Sie auf "Details für Planungspositionen".
    * Auf dieser Seite können Sie die Genauigkeitswerte, den historischen Bedarf und die Planung finden. Sie können auch Änderungen an der Planung vornehmen.  



---
title: Planzahlenverrechnungsschlüssel
description: Dieser Artikel enthält Beispiele, die zeigen, wie Sie einen Planzahlenverrechnungsschlüssel einrichten. Er umfasst Informationen zu den verschiedenen Einstellungen der Planzahlenverrechnungsschlüssel und deren Ergebnissen. Mithilfe von Planzahlenverrechnungsschlüsseln wird definiert, wie der Planungsbedarf verringert werden soll.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "770915"
---
# <a name="reduction-keys"></a>Planzahlenverrechnungsschlüssel

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Beispiele, die zeigen, wie Sie einen Planzahlenverrechnungsschlüssel einrichten. Er umfasst Informationen zu den verschiedenen Einstellungen der Planzahlenverrechnungsschlüssel und deren Ergebnissen. Mithilfe von Planzahlenverrechnungsschlüsseln wird definiert, wie der Planungsbedarf verringert werden soll.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Beispiel 1: Prozent - Planzahlenverrechnungsschlüssel-Planungsverringerungsprinzip
---------------------------------------------------------------

Dieses Beispiel verdeutlicht, wie ein Planzahlenverrechnungsschlüssel den Bedarf der Bedarfsplanung verringert, und zwar gemäß den vom Planzahlenverrechnungsschlüssel definierten Prozentsätzen und Perioden.

1. Wählen Sie auf der Seite **Planzahlenverrechnungsschlüssel** die folgenden Positionen.

   | Rückgeld | Einheit  | Prozentsatz |
   |--------|-------|---------|
   |   1    | Monat |   100   |
   |   2    | Monat |   75    |
   |   3    | Monat |   50    |
   |   4    | Monat |   25    |


2. Verknüpfen Sie den Planzahlenverrechnungsschlüssel mit der Deckungsgruppe des Artikels.
3. Auf der **Produktprogrammpläne**-Seite im Feld **Reduktionsprinzip** wählen Sie **Prozent - Planzahlenverrechnungsschlüssel** aus.
4. Erstellen Sie eine Bedarfsplanung von 1000 Stück pro Monat.

Wird der Umsatzplanungslauf am 1. Januar ausgeführt, wird der Bedarf der Bedarfsplanung entsprechend den Prozentwerten verbraucht, die Sie auf der Seite **Planzahlenverrechnungsschlüssel** angegeben haben. Die folgenden Bedarfsmengen werden in den Produktprogrammplan übertragen.

| Monat                | Erforderliche Stückzahl |
|----------------------|---------------------------|
| Januar              | 0                         |
| Februar             | 250                       |
| März                | 500                       |
| April                | 750                       |
| Mai - Dezember | 1.000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Beispiel 2: Buchungen - Planzahlenverrechnungsschlüssel-Planungsverringerungsprinzip
Dieses Beispiel verdeutlicht, wie tatsächliche Aufträge, die in den vom Planzahlenverrechnungsschlüssel definierten Perioden anfallen, den Bedarf der Bedarfsplanung verringern.

-   Auf der **Produktprogrammpläne**-Seite im Feld **Reduktionsprinzip** wählen Sie **Buchungen - Planzahlenverrechnungsschlüssel** aus.

Am 1. Januar lagen die folgenden Aufträge vor.

| Monat    | Bestellte Stückzahl |
|----------|--------------------------|
| Januar  | 956                      |
| Februar | 1.176                    |
| März    | 451                      |
| April    | 119                      |

Unter Verwendung derselben Bedarfsplanung von 1000 Stück pro Monat werden die folgenden Bedarfsmengen in den Produktprogrammplan übertragen:

| Monat                | Erforderliche Stückzahl |
|----------------------|---------------------------|
| Januar              | 44                        |
| Februar             | 0                         |
| März                | 549                       |
| April                | 881                       |
| Mai - Dezember | 1.000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Beispiel 3: Buchungen - dynamische Periode Planungsverringerungsprinzip
In den meisten Fällen werden Systeme so eingerichtet, das Buchungen Bedarfsplanung innerhalb bestimmter Prognoseperioden reduzieren (Wochen, Monate usw.). Die Perioden werden im Planzahlenverrechnungsschlüssel definiert. Jedoch können die Zeit zwischen zwei Bedarfsplanungspositionen auch eine Periode *implizieren*.

1. Erstellen Sie eine Bedarfsplanung für die folgenden Datumsangaben und Mengen.

   | Datum       | Bedarfsplanung |
   |------------|-----------------|
   | 1. Januar  | 1.000           |
   | 5. Januar  | 500             |
   | 12. Januar | 1.000           |

   In dieser Planung gibt es keinen klaren Zeitraum zwischen den Planungsdaten. Zwischen der ersten und zweiten Datumsangabe besteht eine viertägige Spanne und zwischen der zweiten und dritten Datumsangabe besteht eine siebentägige Spanne. Diese verschiedenen Spannen sind die dynamischen Perioden.
2. Erstellen Sie Auftragspositionen wie folgt:

   | Datum                             | Auftragsmenge |
   |----------------------------------|----------------------|
   | 15. Dezember Im Jahr zuvor | 500                  |
   | 3. Januar                        | 100                  |
   | 10. Januar                       | 200                  |

Die Planung wird wie folgt reduziert:

-   Der erste Auftrag liegt nicht innerhalb einer Periode. Damit sich keine Planung.
-   Der zweite Auftrag liegt zwischen dem 1. Januar und dem 5. Januar. Damit reduziert er die Planung für den 1. Januar um 100.
-   Der dritte Auftrag liegt zwischen dem 5. Januar und dem 12. Januar. Damit reduziert er die Planung für den 5. Januar um 200.

Der nächste Bestellvorschlag wird zur Erfüllung der Planung erstellt.

| Bedarfsplanungsdatum | Verringerte Menge |
|----------------------|------------------|
| 1. Januar            | 900              |
| 5. Januar            | 300              |
| 12. Januar           | 1.000            |

Hier eine Zusammenfassung der **Buchungen - dynamische Periode**-Verringerung:

-   Der Planungsbedarf wird durch die tatsächlichen Auftragsbuchungen verringert, die während der dynamischen Periode stattfinden. Die dynamische Periode erstreckt sich über die aktuellen Planungsdaten und endet beim Beginn der nächsten Planung.
-   Für diese Methode wird kein Planzahlenverrechnungsschlüssel verwendet.
-   Wenn diese Option verwendet wird, tritt das folgende Verhalten auf:
    -   Wenn die Planung vollständig verringert wird, wird der Planungsbedarf für die aktuelle Planung 0.
    -   Wenn keine zukünftige Planung vorhanden ist, wird der Planungsbedarf der letzten eingegebenen Planung verringert.
    -   Planungszeiträume sind in der Berechnung der Planungsverringerung enthalten.
    -   Positive Tage sind in der Berechnung der Planungsverringerung enthalten.
    -   Wenn die tatsächlichen Auftragsbuchungen größer sind als der geplante Bedarf, werden die verbleibenden Buchungen nicht in die nächste Planungsperiode vorgetragen.


<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Produktprogrammpläne](master-plans.md)




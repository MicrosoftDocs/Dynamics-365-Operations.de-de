---
title: "Kosteneinträge"
description: "Dieser Artikel enthält Informationen zu Kosteneinträgen und wenn sie erstellt werden. Ein Kosteneintrag ist ein Datensatz, der die Menge und die Kosten eines gegebenen Ereignisses erfasst."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ac83ec4f37f5bafde30e5afc131a138df8dae419
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="cost-entries"></a>Kosteneinträge

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Kosteneinträgen und wenn sie erstellt werden. Ein Kosteneintrag ist ein Datensatz, der die Menge und die Kosten eines gegebenen Ereignisses erfasst.

Kosteneinträge sind Aggregationen von Lagerbuchungen, die zu aktiven Dimensionen des wertmäßigen Bestands erfasst werden.

## <a name="examples"></a>Beispiele
### <a name="example-1-no-cost-entries-are-created"></a>Beispiel 1: Keine Kosteneinträge werden erstellt

Ein Umlagerungserfassungsereignis wird erfasst. Das Ereignis überträgt ein Stück des Artikels A vom Lagerplatz A zum Lagerplatz B. Die Lagerplatzlagerungsdimension ist nicht Teil des Kostenobjekts. Daher erstellt das Ereignis zwei Lagerbuchungen und keine Kosteneinträge.

### <a name="example-2-cost-entries-are-created"></a>Beispiel 2: Kosteneinträge werden erstellt

Ein Umlagerungserfassungsereignis wird erfasst. Das Ereignis überträgt zur Produktion eines Artikels von einem Standort 1 an Standort 2. Die Standortlagerdimension wird als Teil des Kostenträgers betrachtet. Daher erstellt das Ereignis zwei Lagerbuchungen und zwei Kosteneinträge.

### <a name="example-3-one-cost-entry-is-created"></a>Beispiel 3: Ein Kosteneintrag wird erstellt

Ein Produktzugangsereignis wird für eine Bestellung erfasst. Das Ereignis erfasst 100 Stück des Artikels A zu Einheitenkosten von 10,00 Euro. Da Artikel A eine Seriennummer verwendet, um den Zweck der Lagerverwaltung zu verfolgen, wird eine eindeutige Seriennummer für jeden Artikel erstellt, der eingegangen ist. Daher erstellt das Ereignis 100 Lagerbuchungen und einen Kosteneintrag.

## <a name="cost-entries-page"></a>Kosteneinträge-Seite
Die neue **Kosteneinträge**-Seite ermöglicht die Anzeige und Steuerung von Erfassungen für Mengen und Kosten. Diese Seite ergänzt die Seiten **Lagerbuchung** und **Lagerausgleich**. Datensätze werden in chronologischer Reihenfolge für ein Ereignis erfasst. Daher können Sie die kumulierten Kosten eines bestimmten Ereignisses oder aller Ereignisse zu einem Dokument schnell finden und steuern. Hier ist ein Beispiel:

-   Ein Produktzugangsereignis wird für Artikel A. erfasst. Es werden hundert Stück zu Einheitenkosten von EUR 10,00 empfangen.
-   Eine paar Tage nach der Erfassung des Rechnungsereignisses steigen die Kosten auf 11,00 EUR. Daher ist der Gesamtbetrag nun 1.100 EUR. Ein zweiter Beleg wird erstellt, um die Differenz von 100 EUR zu buchen.
-   Einige Tage später, wird ein sonstiger Zuschlag von 15,00 EUR zur Abdeckung der Transportkosten auf der Bestellung erfasst.

| Beleg | Datum       | Referenz      | Anzahl | Loskennung  | Leistung | Betrag  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01.01.2015 | Bestellung | 100001 | 0000101 | 100,00   | 1000,00 |
| 00002   | 20.01.2015 | Bestellung | 100001 | 0000101 |          | 100,00  |
| 00003   | 31.01.2015 | Regulierung     | 100001 | 0000101 |          | 15:00   |

Die **Kosteneinträge**-Seite ermöglicht das Filter nach der Dokumentenkennung und dem Dokumentdatum. 

> [!NOTE]
> Kosteneinträge sind nur für [Kostenobjekte ](cost-object.md)oder freigegebene Produkte verfügbar.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Kostenobjekte](cost-object.md)





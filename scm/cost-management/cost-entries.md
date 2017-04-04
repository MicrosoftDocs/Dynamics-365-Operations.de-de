---
title: "Kosteneinträge"
description: "Dieser Artikel enthält Informationen zu Kosteneinträgen und wenn sie erstellt werden. Ein Kosteneintrag ist ein Datensatz, der die Menge und die Kosten eines gegebenen Ereignisses erfasst."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 55f5ee731c40acc40e8fe20c24d4ed707fe2c81a
ms.lasthandoff: 03/31/2017


---

# <a name="cost-entries"></a>Kosteneinträge

Dieser Artikel enthält Informationen zu Kosteneinträgen und wenn sie erstellt werden. Ein Kosteneintrag ist ein Datensatz, der die Menge und die Kosten eines gegebenen Ereignisses erfasst.

Kosteneinträge sind Aggregationen von Lagerbuchungen, die zu aktiven Dimensionen des wertmäßigen Bestands erfasst werden.

## <a name="examples"></a>Beispiele
### <a name="example-1-no-cost-entries-are-created"></a>Beispiel 1: Keine Kosteneinträge werden erstellt

Ein Umlagerungserfassungsereignis wird erfasst. Das Ereignis überträgt ein Stück des Artikels A vom Lagerplatz A zum Lagerplatz B. Die Lagerplatzlagerungsdimension ist nicht Teil des Kostenobjekts. Daher erstellt das Ereignis zwei Lagerbuchungen und keine Kosteneinträge.

### <a name="example-2-cost-entries-are-created"></a>Beispiel 2: Kosteneinträge werden erstellt

Ein Umlagerungserfassungsereignis wird erfasst. Das Ereignis überträgt zur Produktion eines Artikels von einem Standort an Standort 1. 2. Die Standortlagerdimension wird als Teil des Kostenträgers. Daher erstellt das Ereignis zwei Lagerbuchungen und zwei Kosteneinträge.

### <a name="example-3-one-cost-entry-is-created"></a>Beispiel 3: Ein Kosteneintrag wird erstellt

Ein Produktzugangsereignis wird für eine Bestellung erfasst. Das Ereignis erfasst 100 Stück des Artikels A zu Einheitenkosten von 10,00 Euro. Da Artikel A eine Seriennummer verwendet, um den Zweck der Lagerverwaltung zu verfolgen, wird eine eindeutige Seriennummer für jeden Artikel erstellt, der eingegangen ist. Daher erstellt das Ereignis 100 Lagerbuchungen und einen Kosteneintrag.

## <a name="cost-entries-page"></a>Kosteneinträge-Seite
Die neue **Kosteneinträge**-Seite ermöglicht die Anzeige und Steuerung von Erfassungen für Mengen und Kosten. Diese Seite ergänzt die Seiten **Lagerbuchung** und **Lagerausgleich**. Datensätze werden in chronologischer Reihenfolge für ein Ereignis erfasst. Daher können Sie die kumulierten Kosten eines bestimmten Ereignisses oder aller Ereignisse zu einem Dokument schnell finden und steuern. Hier ist ein Beispiel:

-   Ein Produktzugangsereignis wird für Artikel A. erfasst. Es werden hundert Stück zu Einheitenkosten von EUR 10,00 empfangen.
-   Eine paar Tage nach der Erfassung des Rechnungsereignisses steigen die Kosten auf 11,00 EUR. Daher ist der Gesamtbetrag nun 1.100 EUR. Ein zweiter Beleg wird erstellt, um die Differenz von 100 EUR zu buchen.
-   Einige Tage später, wird ein sonstiger Zuschlag von 15,00 EUR zur Abdeckung der Transportkosten auf der Bestellung erfasst.

| Beleg | Datum       | Referenz      | Nummer | Loskennung  | Los-Referenz | Rücklieferungsloskennung | Menge | Betrag  |
|---------|------------|----------------|--------|---------|---------------|---------------|----------|---------|
| 00001   | 01.01.2015 | Bestellung | 100001 | 0000101 |               |               | 100,00   | 1000,00 |
| 00002   | 20.01.2015 | Bestellung | 100001 | 0000101 |               |               |          | 100,00  |
| 00003   | 31.01.2015 | Regulierung     | 100001 | 0000101 |               |               |          | 15:00   |

Die **Kosteneinträge**-Seite ermöglicht das Filter nach der Dokumentenkennung und dem Dokumentdatum. ** Hinweis: ** Einträge mit Kosten sind nur für cost-object.md [] (Kostenträger) oder freigegebene Produkte verfügbar.

<a name="see-also"></a>Siehe auch
--------

[Cost objects](cost-object.md)



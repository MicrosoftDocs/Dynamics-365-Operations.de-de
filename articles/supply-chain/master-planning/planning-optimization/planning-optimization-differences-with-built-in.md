---
title: Unterschiede zwischen integrierter Masterplanung und Planungsoptimierung
description: Dieses Thema listet Funktionen auf, die von der Planungsoptimierung noch nicht unterstützt werden und die nicht auf der Seite Planungsoptimierung-Fit-Analyse aufgeführt sind.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e271ddd3331d7b5de78f00a02b60a0479879c172
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700004"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Unterschiede zwischen integrierter Masterplanung und Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Die Ergebnisse der Planungsoptimierung können von den Ergebnissen der integrierten Produktprogrammplanung abweichen. Die Unterschiede können durch noch nicht unterstützte Funktionen verursacht werden. Dieses Thema listet Funktionen auf, die die Planungsoptimierung noch nicht unterstützt und die nicht auf der Seite **[Planungsoptimierung-Fit-Analyse](planning-optimization-fit-analysis.md)** aufgelistet sind].

| Funktion | Aktuelles Verhalten in der Planungsoptimierung |
|---|---|
| Artikelgewicht-Produkte | Artikelgewichte werden als übliche Produkte betrachtet.|
| Erweiterbare Dimensionen | Erweiterbare Dimensionen sind bei geplanten Aufträgen leer, auch wenn das Kontrollkästchen **Planung nach Dimension** auf der Seite **Lagerungs-Dimensionsgruppen** oder **Tracking-Dimensionsgruppen** aktiviert ist. |
| Gefilterte Produktionsläufe | Für Details siehe [Produktionsplanung - Filter](production-planning.md#filters). |
| Absatzplanung | Die Planung von Prognosen wird nicht unterstützt. Wir empfehlen die Verwendung der Produktprogrammplanung, bei der dem Masterplan ein Prognosemodell zugewiesen ist. |
| Nummernkreise für geplante Aufträge | Nummernkreise für geplante Aufträge werden nicht unterstützt. Geplante Auftragsnummern werden auf der Serviceseite generiert. Die Nummer des geplanten Auftrags wird normalerweise mit 10 Stellen angezeigt, aber die Reihenfolge ist tatsächlich aus 20 Zeichen aufgebaut, wobei 10 Stellen der Anzahl der Planungsausführungen und die anderen 10 Stellen der Anzahl der geplanten Aufträge zugewiesen sind. |
| Plan kopieren, Plan löschen und Planversion bereinigen | <p>Die folgenden Elemente sind unter **Produktprogrammplanung \> Masterplanung \> Pläne pflegen** im Navigationsbereich deaktiviert:</p><ul><li>Plan kopieren</li><li>Plan löschen</li><li>Planversionsbereinigung</li></ul> |
| Rücklieferungen | Rücklieferungen werden nicht berücksichtigt. |
| Funktionen für die Planung | Details finden Sie unter [Planung mit unendlicher Kapazität](infinite-capacity-planning.md#limitations). |
| Sicherheitslagerbestandserfüllung | Die Planungsoptimierung verwendet immer die Option *Heutiges Datum + Beschaffungszeit* für das Feld **Mindestbestand auffüllen** auf der Seite **Artikelabdeckung**. Dadurch können nicht gewünschte geplante Aufträge und andere Probleme vermieden werden. Wenn die Beschaffungszeit für den Sicherheitsbestand nicht enthalten ist, werden Planaufträge, die für den niedrigen Lagerbestand erstellt werden, aufgrund der Vorlaufzeit immer verzögert. |
| Bedarfsverursacher für Sicherheitslagerbestand und Nettobedarf | Der Anforderungstyp *Sicherheitslagerbestand* ist nicht enthalten und wird auf der Seite **Nettobedarf** nicht angezeigt. Der Sicherheitslagerbestand stellt keinen Bedarf dar und ist mit keinem Bedarfstermin verknüpft. Stattdessen legt er eine Einschränkung fest, wie viel Inventar zu jeder Zeit vorhanden sein muss. Allerdings wird der Feldwert **Minimum** weiterhin bei der Berechnung von Planaufträgen während der Produktprogrammplanung berücksichtigt. Wir empfehlen Ihnen, die Spalte **Aufgelaufene Menge** auf der Seite **Nettobedarf** zu prüfen, um zu erkennen, ob dieser Wert berücksichtigt wurde. |
| Transport-Kalender | Der Wert in der Spalte **Transportkalender** auf der Seite **Liefermodi** wird ignoriert. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Passanalyse zur Planungsoptimierung](planning-optimization-fit-analysis.md)
- [In der Planungsoptimierung nicht verwendete Parameter](not-used-parameters.md)
- [In der Planungsoptimierung verwendete Datums- und Zeitparameter](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
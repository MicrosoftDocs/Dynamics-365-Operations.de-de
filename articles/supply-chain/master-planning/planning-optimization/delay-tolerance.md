---
title: Verzögerungstoleranz (negative Tage)
description: Dieser Artikel enthält Informationen über die Berechnung der Verzögerungstoleranz und wie sie sich auf die Erstellung geplanter Aufträge in der Planungsoptimierung auswirkt.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 78ba4236705f1a200d9fe796eb80d0241b0fa537
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740467"
---
# <a name="delay-tolerance-negative-days"></a>Verzögerungstoleranz (negative Tage)
<!-- KFM: Split topic into PO and classic -->

[!include [banner](../../includes/banner.md)]

Die Verzögerungstoleranz-Funktionalität ermöglicht der Planungsoptimierung, den Wert **Negative Tage** zu berücksichtigen, der für Dispositionssteuerungsgruppe, Artikelabdeckung und/oder Produktprogrammplan festgelegt ist. Sie wird verwendet, um die Verzögerungstoleranz zu verlängern, die während der Produktprogrammplanung angewendet wird. Auf diese Weise können Sie vermeiden, neue Vorräte zu erstellen, wenn der vorhandene Vorrat den Bedarf nach einer kurzen Verzögerung decken kann. Der Zweck der Funktionalität besteht darin, festzustellen, ob es sinnvoll ist, einen neuen Vorrat für einen bestimmten Bedarf zu erstellen.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Die Verzögerungstoleranz-Funktion ein- oder ausschalten

Um die Verzögerungstoleranz-Funktionalität in Ihrem System verfügbar zu machen, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen ein:

- *Negative Tage für die Planungsoptimierung*: Diese Funktion ermöglicht Einstellungen für negative Tage für Dispositionssteuerungsgruppen und Artikelabdeckung. Ab Supply Chain Management Version 10.0.29 ist die Funktion obligatorisch und kann nicht deaktiviert werden.
- *Automatisierung der Lieferungen zur Auftragsfertigung*: Diese Funktion aktiviert Einstellungen für negative Tage für Produktprogrammpläne. (Weitere Informationen finden Sie unter [Automatisierung der Lieferungen zur Auftragsfertigung](../make-to-order-supply-automation.md).)

## <a name="delay-tolerance-in-planning-optimization"></a>Verzögerungstoleranz in der Planungsoptimierung

Die Verzögerungstoleranz stellt die Anzahl der Tage über die Vorlaufzeit hinaus dar, die Sie bereit sind, zu warten, bevor Sie eine neue Wiederbeschaffung bestellen, wenn die bestehende Beschaffung bereits geplant ist. Die Verzögerungstoleranz wird durch die Verwendung von Kalendertagen und nicht von Geschäftstagen definiert.

Zum Zeitpunkt der Produktprogrammplanung, wenn das System die Verzögerungstoleranz berechnet, berücksichtigt es die Einstellung **Negative Tage**. Sie können den Wert **Negative Tage** auf der Seite **Dispositionssteuerungsgruppe** oder auf der Seite **Artikelabdeckung** oder der Seite **Produktprogrammpläne** festlegen. Wenn negative Tage auf mehr als einer Ebene zugewiesen werden, wendet das System die folgende Hierarchie an, um zu entscheiden, welche Einstellung verwendet werden soll:

- Wenn negative Tage auf der Seite **Produktprogrammpläne** aktiviert sind, überschreibt diese Einstellung alle anderen Einstellungen für negative Tage, wenn der Plan ausgeführt wird.
- Wenn negative Tage auf der Seite **Artikelabdeckung** konfiguriert sind, überschreibt diese Einstellung die Einstellung der Abdeckungsgruppe.
- Negative Tage, die auf der Seite **Dispositionssteuerungsgruppe** konfiguriert sind, gelten nur, wenn negative Tage nicht für einen relevanten Artikel oder Plan konfiguriert wurden.

Das System verknüpft die Berechnung der Verzögerungstoleranz mit dem *frühesten Datum der Wiederbeschaffung*, das dem heutigen Datum plus der Vorlaufzeit entspricht. Die Verzögerungstoleranz wird mit Hilfe der folgenden Formel berechnet, wobei *max()* den größeren von zwei Werten findet:

*max(Frühestes Wiederbeschaffungsdatum, Fälligkeitsdatum des Bedarfs)* – *Fälligkeitsdatum des Bedarfs* + *Negative Tage*

Diese Formel stellt sicher, dass die Produktprogrammplanung keine neuen Vorratsaufträge erstellt, wenn während der Vorlaufzeit des Produkts genügend Vorrat vorhanden ist.

> [!NOTE]
> Die Berechnung der Verzugstoleranz in der Planungsoptimierung verwendet immer die dynamische Berechnung der negativen Tage aus dem veralteten Produktprogrammplanungsmodul. Die Einstellung **Dynamische negative Tage verwenden** auf der Seite **Parameter der Produktprogrammplanung** hat keinen Einfluss auf dieses Verhalten.

Wenn der vorhandene Vorrat eine Verzögerung des Bedarfs impliziert, die kleiner oder gleich der berechneten Verzögerungstoleranz ist, koppelt die Planungsoptimierung den vorhandenen Vorrat an den Bedarf. In einigen Fällen ist es besser, den Bedarf zu verzögern, als mit einem Überangebot zu enden.

In den folgenden Unterabschnitten finden Sie Beispiele, die zeigen, wie sich die Verzögerungstoleranz auf die Erstellung von geplanten Aufträgen in der Planungsoptimierung auswirkt.

### <a name="example-1"></a>Beispiel 1

Ein Produkt hat die folgende Konfiguration:

- **Vorlaufzeit:** *10*
- **Negative Tage:** *2*

Für das Produkt bestehen der folgende Vorrat und Bedarf:

- **Bedarf für heute:** Ein Verkaufsauftrag für eine Menge von 10
- **Vorrat in 12 Tagen:** Eine Einkaufsbestellung für eine Menge von 10

Der vorhandene Vorrat kann den Bedarf innerhalb von 12 Tagen decken, und dieser Zeitraum entspricht der Verzögerungstoleranz. Wenn die Produktprogrammplanung ausgeführt wird, werden daher keine geplanter Aufträge erstellt.

### <a name="example-2"></a>Beispiel 2

Ein Produkt hat die folgende Konfiguration:

- **Vorlaufzeit:** *10*
- **Negative Tage:** *0*

Für das Produkt bestehen der folgende Vorrat und Bedarf:

- **Bedarf für heute:** Ein Verkaufsauftrag für eine Menge von 10
- **Vorrat in 12 Tagen:** Eine Einkaufsbestellung für eine Menge von 10

Der vorhandene Vorrat kann den Bedarf erst nach 12 Tagen decken. Die Verzögerungstoleranz beträgt jedoch 10 Tage. Wenn die Produktprogrammplanung ausgeführt wird, wird daher ein geplanter Auftrag für eine Menge von 10 erstellt.

### <a name="example-3"></a>Beispiel 3

Ein Produkt hat die folgende Konfiguration:

- **Vorlaufzeit:** *10*
- **Negative Tage:** *2*

Für das Produkt bestehen der folgende Vorrat und Bedarf:

- **Bedarf in 11 Tagen:** Ein Verkaufsauftrag für eine Menge von 10
- **Nachschub in 14 Tagen:** Eine Einkaufsbestellung für eine Menge von 10

Der vorhandene Vorrat kann den Bedarf erst nach drei Tagen decken. Die Verzögerungstoleranz beträgt jedoch zwei Tage. (In diesem Fall umfasst die Verzögerungstoleranz nur die beiden negativen Tage. Das Datum des Bedarfs wird nicht berücksichtigt, da es nach der Vorlaufzeit des Produkts liegt.) Wenn die Produktprogrammplanung ausgeführt wird, wird daher ein geplanter Auftrag für eine Menge von 10 erstellt.

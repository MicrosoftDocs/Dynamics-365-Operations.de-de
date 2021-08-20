---
title: Verzögerungstoleranz (negative Tage)
description: Dieses Thema enthält Informationen über die Berechnung der Verzögerungstoleranz und wie sie sich auf die Erstellung geplanter Aufträge in der Planungsoptimierung auswirkt.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c0bc3d429a1bf13285b385130d419f628330bb3728c6f071cf118edac2a59d87
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778699"
---
# <a name="delay-tolerance-negative-days"></a>Verzögerungstoleranz (negative Tage)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Die Verzögerungstoleranz-Funktionalität ermöglicht der Planungsoptimierung, den Wert **Negative Tage** zu berücksichtigen, der für Deckungsgruppen festgelegt ist. Sie wird verwendet, um die Verzögerungstoleranz zu verlängern, die während der Produktprogrammplanung angewendet wird. Auf diese Weise können Sie vermeiden, neue Vorräte zu erstellen, wenn der vorhandene Vorrat den Bedarf nach einer kurzen Verzögerung decken kann. Der Zweck der Funktionalität besteht darin, festzustellen, ob es sinnvoll ist, einen neuen Vorrat für einen bestimmten Bedarf zu erstellen.

## <a name="turn-on-the-feature-in-your-system"></a>Funktion in Ihrem System aktivieren

Um die Verzögerungstoleranz-Funktionalität in Ihrem System verfügbar zu machen, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Negative Tage für Planungsoptimierung* ein.

## <a name="delay-tolerance-in-planning-optimization"></a>Verzögerungstoleranz in der Planungsoptimierung

Die Verzögerungstoleranz stellt die Anzahl der Tage über die Vorlaufzeit hinaus dar, die Sie bereit sind, zu warten, bevor Sie eine neue Wiederbeschaffung bestellen, wenn die bestehende Beschaffung bereits geplant ist. Die Verzögerungstoleranz wird durch die Verwendung von Kalendertagen und nicht von Geschäftstagen definiert.

Zum Zeitpunkt der Produktprogrammplanung, wenn das System die Verzögerungstoleranz berechnet, berücksichtigt es die Einstellung **Negative Tage**. Sie können den Wert **Negative Tage** entweder auf der Seite **Abdeckungsgruppen** oder auf der Seite **Elementabdeckung** festlegen.

Das System verknüpft die Berechnung der Verzögerungstoleranz mit dem *frühesten Datum der Wiederbeschaffung*, das dem heutigen Datum plus der Vorlaufzeit entspricht. Die Verzögerungstoleranz wird mit Hilfe der folgenden Formel berechnet, wobei *max()* den größeren von zwei Werten findet:

*max(Frühestes Wiederbeschaffungsdatum, Fälligkeitsdatum des Bedarfs)* – *Fälligkeitsdatum des Bedarfs* + *Negative Tage*

Diese Formel stellt sicher, dass die Produktprogrammplanung keine neuen Vorratsaufträge erstellt, wenn während der Vorlaufzeit des Produkts genügend Vorrat vorhanden ist.

> [!NOTE]
> Die Berechnung der Verzugstoleranz in der Planungsoptimierung verwendet immer die dynamische Berechnung der negativen Tage aus der integrierten Produktprogrammplanung. Die Einstellung **Dynamische negative Tage verwenden** auf der Seite **Parameter der Produktprogrammplanung** hat keinen Einfluss auf dieses Verhalten.

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

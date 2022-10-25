---
title: Planung und Terminierung begrenzter Kapazität
description: Die Planung und Terminierung von begrenzter Kapazität hilft Ihnen zu verstehen, wie viel Arbeit in einem bestimmten Zeitraum produziert werden kann, wenn Einschränkungen bei den verschiedenen Ressourcen berücksichtigt werden.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 3d116b5f7f456630415378e6cc069907e339068b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689692"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Planung und Terminierung begrenzter Kapazität

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Die begrenzte Kapazität ist ein Ansatz, der Ihnen hilft zu verstehen, wie viel Arbeit in einem bestimmten Zeitraum produziert werden kann, wenn die Beschränkungen der verschiedenen Ressourcen berücksichtigt werden. Der Zweck der begrenzten Kapazitätsplanung besteht darin, sicherzustellen, dass die Arbeit im gesamten Werk gleichmäßig und effizient abläuft.

Die Planung begrenzter Kapazität erstellt einen realistischeren Zeitplan für die Produktionsprozesse, als dies bei der unendlichen Ladung der Fall ist. Wenn die Kapazität der Ressourcen nicht ausreicht, wird der Liefertermin verschoben, und der Auftrag wird eingeplant, wenn genügend Kapazität vorhanden ist.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Planungsoptimierung Unterstützung für die Planung begrenzter Kapazität

Die Planung begrenzter Kapazität und die Terminierung funktionieren fast auf die gleiche Weise, unabhängig davon, ob Sie die Planungsoptimierung oder die integrierte Planungsengine verwenden. Die Planungsoptimierung verwendet jedoch nicht den Parameter **Bottleneck-Zeit**. Wenn Sie die Planungsoptimierung verwenden, werden Ressourcen mit Engpässen immer unter Verwendung des gleichen Zeitraums eingeplant wie Ressourcen ohne Engpässe (wie durch den Zeitrahmen für begrenzte Kapazität angezeigt).

## <a name="set-up-finite-capacity-functionality"></a>Funktionalität der begrenzten Kapazität festlegen

Um die Funktionalität der begrenzten Kapazität nutzen zu können, müssen Sie die Kapazitätsplanung global aktivieren und die Planung begrenzter Kapazität sowohl für den Masterplan, in dem Sie sie nutzen wollen, als auch für jede Ressource, für die sie gilt, aktivieren. Für Pläne und Ressourcen, bei denen die begrenzte Kapazität aktiviert ist, wird bei der Terminierung geplanter Fertigungsaufträge die bereits reservierte Kapazität berücksichtigt. Geplante Fertigungsaufträge werden ab dem Bedarfstermin rückwärts eingeplant. Wenn die Kapazität nicht ausreicht, um den optimalen Zeitplan einzuhalten, wird das System versuchen, die Elemente zu einem früheren Zeitpunkt anzufordern. Wenn sich Ihre Kapazität ändern kann, wenn sich der Bedarf ändert (z.B. wenn Sie mit Schichten arbeiten), sollten Sie die Funktion der begrenzten Kapazität nicht verwenden, da die berechneten Bearbeitungszeiten dann nicht korrekt sind. Die Terminierung berücksichtigt nur Kapazitäten, die bereits für Ressourcen reserviert sind, bei denen die begrenzte Kapazität aktiviert ist. Indem Sie die begrenzte Kapazität für eine Ressource aktivieren, können Sie den Zeitraum für die begrenzte Kapazität ändern.

### <a name="activate-master-planning-parameters"></a>Aktivieren Sie die Parameter der Produktprogrammplanung

Um die Funktionalität der begrenzten Kapazität zu nutzen, müssen Sie die Produktprogrammplanung auf der Seite **Begrenzte Kapazität** aktivieren.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Produktprogrammplanparameter**.
1. Auf der Registerkarte **Geplante Aufträge**, im Abschnitt **Kapazitätsplanung**, legen Sie die Option **Produktion** auf *Ja* fest.

### <a name="activate-a-master-plan"></a>Aktivieren Sie einen Masterplan

Sie müssen die Planung begrenzter Kapazität und die Terminierung für jeden Masterplan, den Sie verwenden möchten, aktivieren.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie im Listenbereich einen Masterplan aus, für den Sie die Planung begrenzter Kapazität und die Terminierung festlegen möchten.
1. Auf dem Inforegister **Allgemein**, im Abschnitt **Geplante Fertigungsaufträge**, legen Sie die Option **Begrenzte Kapazität** auf *Ja* fest.
1. Wiederholen Sie die Schritte 2 und 3 für jeden weiteren Masterplan, den Sie festlegen möchten.

### <a name="activate-resources"></a>Aktivieren Sie Ressourcen

Sie müssen die Planung begrenzter Kapazität und die Terminierung für jede Ressource, die Sie verwenden möchten, aktivieren.

1. Gehen Sie zu **Produktionssteuerung \> Setup \> Ressourcen \> Ressourcen**.
1. Wählen Sie im Listenbereich eine Ressource aus, für die Sie die Planung begrenzter Kapazitäten und die Terminierung festlegen möchten.
1. Legen Sie im Inforegister **Vorgang** im Bereich **Kapazitätsschaltfläche** die Option **Begrenzte Kapazität** auf *Ja* fest.
1. Wiederholen Sie die Schritte 2 und 3 für jede weitere Ressource, die Sie festlegen möchten.

## <a name="examples"></a>Beispiele

In diesem Abschnitt finden Sie die folgenden Beispiele, die zeigen, wie Sie mit der Planung begrenzter Kapazität und der Terminierung arbeiten können:

- Beispiel 1 - Planung unbegrenzter Kapazität
- Beispiel 2 - Planung begrenzter Kapazität mit einem Zeitraum von einem Tag
- Beispiel 3 - Planung begrenzter Kapazität mit einem Zeitraum von zwei Tagen

### <a name="preconditions"></a>Vorbedingungen

Alle drei Beispiele gehen von den Voraussetzungen aus, die in diesem Abschnitt beschrieben werden.

Produkt *Produkt1* hat eine Route, die die folgenden Vorgänge enthält.

| Vorgang Nr. | Name des Arbeitsgangs | Ressource        | Bearbeitungszeit | Bearb. Menge | Nächste |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Schweißen        | Linie Schweißen    | 1        | 2            | 20   |
| 20            | Zusammenstellung     | Montagelinie | 1        | 4            |      |

Die Arbeitskräfte in Ihrer Firma arbeiten in einer Schicht für acht Stunden (8:00-16:00).

Es gibt einen geplanten Produktionsauftrag für *24 Stk* von *Produkt1*. Er hat ein Lieferdatum von *Heute + 3 Tage*.

Als Ergebnis der Planung lädt das System die Ressourcen auf folgende Weise:

- **Schweißlinie:** Diese Ressource wird von *Heute um 8:00* bis *Heute + 1 um 12:00* geladen.
- **Montagelinie:** Diese Ressource wird von *Heute + 1 um 12:00* bis *Heute + 2 um 10:00* geladen.

Die folgende Abbildung zeigt das resultierende Gantt-Diagramm (wählen Sie es aus, um eine größere Ansicht zu erhalten).

[![Gantt-Diagramm mit Vorbedingungen.](media/finite-examples-conditions-small.png "Gantt-Diagramm mit Vorbedingungen")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Beispiel 1 - Planung unbegrenzter Kapazität

Dieses Beispiel zeigt die Planungsergebnisse, wenn Sie die Planung unbegrenzter Kapazität anstelle der Planung begrenzter Kapazität verwenden.

Der Masterplan hat die folgende relevante Einstellung, die die Planung begrenzter Kapazität für den Plan deaktiviert:

- **Begrenzte Kapazität:** *Nein*

Die Option **Begrenzte Kapazität** ist für die beiden relevanten Ressourcen ebenfalls auf *Nein* festgelegt, um die Planung der begrenzten Kapazität für sie zu deaktivieren:

- Linie Schweißen
- Linie Montage

Sie fügen nun einen neuen Verkaufsauftrag für *8 Stk* von *Produkt1* hinzu und führen die Planung aus. Als Ergebnis lädt das System die Schweißlinie von *Heute um 8:00* bis *Heute um 12:00*. Nachdem die Vorgänge an der Schweißlinie abgeschlossen sind, lädt das System die Montagelinie von *Heute um 12:00* bis *Heute um 14:00*.

Die folgende Abbildung zeigt das resultierende Gantt-Diagramm (wählen Sie es aus, um eine größere Ansicht zu erhalten).

[![Gantt-Diagramm mit einem Beispiel für die Planung unbegrenzter Kapazität.](media/finite-examples-example1-small.png "Gantt-Diagramm mit einem Beispiel für die Planung unbegrenzter Kapazität")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Beispiel 2 - Planung begrenzter Kapazität mit einem Zeitraum von einem Tag

Dieses Beispiel zeigt die Planungsergebnisse, wenn Sie die Planung begrenzter Kapazität und einen Zeitraum von einem Tag verwenden.

Der Masterplan hat die folgenden relevanten Einstellungen, die die Planung begrenzter Kapazität ermöglichen und einen Zeitraum für die Planung festlegen:

- **Begrenzte Kapazität:** *Ja*
- **Begrenzter Zeitraum für die Kapazität:** *1*

Die Option **Begrenzte Kapazität** ist für die beiden relevanten Ressourcen ebenfalls auf *Ja* festgelegt, um die Planung begrenzter Kapazität für diese Ressourcen zu ermöglichen:

- Linie zum Schweißen
- Zeile für die Montage

Sie fügen nun einen neuen Verkaufsauftrag für *8 Stk* von *Produkt1* hinzu und führen die Planung aus. Infolgedessen lädt das System die Schweißlinie von *Heute + 1 um 8:00* bis *Heute + 1 um 12:00*. Nachdem die Vorgänge auf der Schweißlinie abgeschlossen sind, lädt das System die Montagelinie von *Heute + 1 um 12:00* bis *Heute + 1 um 14:00*. Das System berücksichtigt die begrenzte Kapazität nur für einen Tag.

Die folgende Abbildung zeigt das resultierende Gantt-Diagramm (wählen Sie es aus, um eine größere Ansicht zu erhalten).

[![Gantt-Diagramm zur Planung begrenzter Kapazität mit einem Zeitraum von einem Tag.](media/finite-examples-example2-small.png "Gantt-Diagramm für die Planung begrenzter Kapazität mit einem Zeitraum von einem Tag")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Beispiel 3 - Planung begrenzter Kapazität mit einem Zeitraum von zwei Tagen

Dieses Beispiel zeigt die Planungsergebnisse bei der Planung begrenzter Kapazität und einem Zeitraum von zwei Tagen.

Der Masterplan hat die folgenden relevanten Einstellungen, die die Planung begrenzter Kapazität ermöglichen und einen Zeitraum für die Planung festlegen:

- **Begrenzte Kapazität:** *Ja*
- **Begrenzte Kapazität Zeitraum:** *2*

Die Option **Begrenzte Kapazität** ist für die beiden relevanten Ressourcen ebenfalls auf *Ja* festgelegt, um die Planung begrenzter Kapazität für diese Ressourcen zu ermöglichen:

- Linie zum Schweißen
- Zeile für die Montage

Sie fügen nun einen neuen Verkaufsauftrag für *8 Stk* von *Produkt1* hinzu und führen die Planung aus. Folglich lädt das System die Schweißlinie von *Heute + 1 um 12:00* bis *Heute + 1 um 16:00*. Nachdem die Vorgänge auf der Schweißlinie abgeschlossen sind, lädt das System die Montagelinie von *Heute + 2 um 8:00* bis *Heute + 2 um 10:00*. Das System berücksichtigt die begrenzte Kapazität nur für zwei Tage.

Die folgende Abbildung zeigt das resultierende Gantt-Diagramm (wählen Sie es aus, um eine größere Ansicht zu erhalten).

[![Gantt-Diagramm zur Planung begrenzter Kapazität mit einem Zeitraum von zwei Tagen.](media/finite-examples-example3-small.png "Gantt-Diagramm für die Planung begrenzter Kapazität mit einem Zeitraum von zwei Tagen")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Sie sollten den Zeitraum für die begrenzte Kapazität immer so festlegen, dass er Ihren geschäftlichen Anforderungen entspricht. Die Beispiele in diesem Artikel dienen lediglich zur Veranschaulichung der Funktionalität. In der Realität ist ein Zeitraum von einem Tag für die meisten Hersteller, die die Planung begrenzter Kapazitäten verwenden, wahrscheinlich zu niedrig.

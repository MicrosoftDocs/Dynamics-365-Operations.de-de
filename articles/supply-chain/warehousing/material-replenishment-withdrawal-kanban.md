---
title: Wiederbeschaffung mit Entnahme-Kanbans
description: In diesem Thema wird beschrieben, wie der Entnahme-Kanban für die Materialwiederbeschaffung für Fertigungsaktivitäten verwendet wird.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edc6da8a54de98696322ace67ada5dfe97af2024
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189943"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Wiederbeschaffung mit Entnahme-Kanbans

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie der Entnahme-Kanban für die Materialwiederbeschaffung für Fertigungsaktivitäten verwendet wird.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Workflow für die Materialwiederbeschaffung, die den Entnahme-Kanban verwendet

Der Entnahme-Kanban kann verwendet werden, um einen Kanban eines einzelnen Artikels zwischen Lagerorten und Produktionslagerplätze zu verschieben, in denen das Material verbraucht wird. Der Entnahme-Kanban unterstützt eine entnahmebasierte Lösung für die Materialwiederbeschaffung, wobei das Entnahmesignal erforderlich ist, um die Lieferung für einen bestimmten Bedarf zu starten. 

Im folgenden Szenario wird ein entnahmebasierten Wiederbeschaffungssystem gezeigt, bei dem das Entnahmesignal die Erstellung eines Kanbans auslöst, um Material für einen Produktionsprozess zu ergänzen. 

[![Entnahmesignal löst die Erstellung eines Kanban aus, um Material für einen Produktionsprozess wiederzubeschaffen](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Entnahme-Kanban
2.  Kanban "von" Lagerplatz und Einlieferungslagerplatz für Lagerortarbeit
3.  Kanban "an"- Lagerplatz und Lagerplatz für Produktions-Wareneingang
4.  Herstellungsprozess
5.  Lagerortarbeit für Kanbanentnahme
6.  Lagerortlagerplätze für Rohmaterial
7.  Materiallagerort
8.  Fertigungslagerort

In diesem Szenario verbraucht ein Produktionsprozess (4) Material von einer Produktions-Wareneingang (3) im Fertigungslagerort (8). Wenn eine Materialhandhabungseinheit (Kanban) verbraucht ist, wird diese als leer erfasst. Ein Wiederbeschaffungssignal wird für den Artikelursprung erstellt, und ein neuer Kanban (1) wird erstellt. In diesem Fall besteht der Artikelursprung aus Lagerplätzen im Materiallagerort (7). Der Material für den Kanban wird entnommen und zum Lagerplatz (2) im gleichen Lagerort verschoben. Wenn das Material entnommen wird, kann es von Lagerplatz 2 zum Produktions-Wareneingang (3) im Fertigungslagerort (8) übertragen werden.

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Konfigurieren von Lagerortarbeit für die Kanban-Entnahme mit dem Entahme-Kanban

Um Rohmaterialentnahme für den Entnahme-Kanban zu aktivieren, konfigurieren Sie Wellenvorlagen, Arbeitsvorlagen und Lagerplatzdirektiven für den **Kanbanentnahme**-Arbeitsauftragstyp. Dieser Arbeitsauftragstyp unterstützt nicht den Entnahmeprozess für den Entnahme-Kanban. Er unterstützt außerdem den Entnahmeprozess für den Fertigungskanban. Allerdings können Sie einen separaten Entnahmeprozess für die einzelnen Kanbantypen konfigurieren, indem Sie die Wellenvorlagen, die Arbeitsvorlagen und die Lagerplatzdirektiven trennen. Zum Trennen von Wellenvorlagen, Arbeitsvorlagen und Lagerplatzdirektiven, legen Sie Kriterien im Aktivitätstyp (**Prozess** oder **Übertragen**) in Abfragen für diese Entitäten fest.

## <a name="configure-the-withdrawal-kanban"></a>Konfigurieren des Entnahme-Kanban

Die Umlagerungsaktivität, die für den Entnahme-Kanban verwendet wird, wird als Teil eines aktivierten Aktivitätsplans in einem Lean-Produktionsfluss konfiguriert. Als Teil der Konfiguration der Umlagerungsaktivität geben Sie für die Übertragung „von“ und „an“ an. Nach der Konfiguration der Umlagerungsaktivität können Sie sie zu einer Kanban-Regel vom Typ **Entnahme** zuweisen. Die Kanban-Regel legt die Richtlinien und Konfigurationen für den Entnahme-Kanban fest. Die Menge des Kanban definiert, wie viele Einheiten der Handhabungseinheit der Kanban während des Übertragungsprozesses trägt. Die feste Kanban-Menge wird verwendet, wenn die feste Wiederbeschaffungsstrategie ausgewählt ist. Diese Menge definiert, wie viele Kanbans erforderlich sind, um zu verhindert, dass der Bestand an der Bedarfsquelle ausgeht. Die feste Menge kann basierend auf dem tatsächlichen Bedarf, dem historischen Bedarf und den Serviceleveln berechnet werden. Die folgenden beiden Szenarien beschreiben, wie Sie eine Materialwiederbeschaffung verwalten, die den Entnahme-Kanban verwendet.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Szenario 1: Auffüllen eines Produktions-Wareneingangs mit einem festen Entnahme-Kanban

Ein Fertigungsprozess verbraucht gekauftes Rohmaterial eines Produktions-Wareneingang im Fertigungslagerort. Wenn das Rohmaterial vom Kreditor empfangen wird, wird es an Lagerplätzen im Materiallagerort gelagert. Da der Bedarf für das Material über einen Zeitraum als stabil gilt, wird er so eingerichtet, dass die Produktion mittels eines festen Mengenkanbanflusses versorgt wird. Wenn ein Kanban am Lagerplatz für Produktions-Wareneingang verbraucht wird, wird ein Leersignal erfasst und ein Kanban vom selben Typ zum Fluss hinzugefügt. 

Das Leersignal kann so konfiguriert werden, dass es automatisch ausgelöst wird, wenn ein Kanban abgeschlossen ist. Alternativ kann das Leersignal als manuelle Interaktion eingerichtet werden, die entweder von der Kanban-Umlagerungsübersicht oder einem Menü auf dem Handgerät ausgelöst wird. Die Kanban-Umlagerungsübersicht ist der Arbeitsbereich, an dem alle Aktivitäten im Kanbanlebenszyklus verwaltet werden. 

Wenn der Kanban erstellt wird, wird eine Wellenposition für das Rohmaterial zur Kanban-Welle für den Materiallagerort hinzugefügt. Im Kommissionierlistenabschnitt der Kanban-Umlagerungsübersicht können der Materialstatus und zugehörige Lagerortprozesse von der Wellenerstellung bis zur Arbeitserstellung überwacht werden, bis das Material am „Übertragung von“-Lagerplatz verfügbar ist und zu den Lagerplätzen für Produktions-Wareneingang übertragen werden kann. Dem Kanban kann entweder über die Kanban-Umlagerungsübersicht oder über das Menü auf dem Handgerät abgeschlossen werden. 

In diesem Szenario wird die Entnahmearbeit im Materiallagerort als eine Aktivität verarbeitet. Die Umlagerungsaktivität zwischen dem Materiallagerort und dem Produktionslagerort wird als separate Aktivität verarbeitet. Dieser Ansatz ist beispielsweise hilfreich bei großen Distanzen zwischen zwei Lagerorten. In diesem Fall kann die Kanbanumlagerungsaktivität eine LKW-Auslastung darstellen. 

Wenn der Abstand zwischen den Lagerort-Lagerplätzen und dem Lagerplatz für Produktions-Wareneingang klein ist, ist es möglicherweise effizienter, die Umlagerungsaktivität in den Entnahmeprozess einzuschließen. Anschließend kann das Material nach der Entnahme direkt am Lagerplatz für Produktions-Wareneingang eingelagert werden. Um diesen Prozess zu unterstützen, konfigurieren Sie die Umlagerungsaktivität so, dass sie automatisch abgeschlossen wird, wenn die Entnahmearbeit des Entnahme-Kanban verarbeitet wird.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Szenario 2: Automatisches Abschließen der Umlagerungsaktivität nach Verarbeitung der Kanban-Entnahmearbeit

Im folgenden Szenario wird die Umlagerungsaktivität des Entnahme-Kanban für die Umlagerung zwischen zwei Lagerplätzen am selben Lagerort konfiguriert. Die Umlagerungsaktivität des Entnahme-Kanbank ist so eingerichtet, dass diese automatisch abgeschlossen wird. 

[![Automatischer Abschluss der Umlagerungsaktivität nach Verarbeitung der Kanban-Entnahmearbeit](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Gemeinsamer Lagerort für Rohmaterialen und Produktion
2.  Lagerortlagerplätze für Rohmaterialen
3.  Kanban "von" Lagerplatz und Einlieferungslagerplatz für Lagerortarbeit
4.  Entnahme-Kanban
5.  Lagerplatz für Produktions-Wareneingang
6.  Herstellungsprozess

Wenn ein Kanban am Lagerplatz für Produktions-Wareneingang verbraucht ist, wird der Kanban als leer erfasst und eine neuer Kanban wird zum Fluss hinzugefügt. Wenn der Kanban erstellt wird, wird eine Wellenposition zu einer Kanbanwelle hinzugefügt. Wenn die Kanbanwelle verarbeitet wird, wird Lagerortarbeit für die Kanban-Entnahme erstellt. Der Lagerarbeiter verarbeitet die Arbeit für die Kanban-Entnahme und wird angewiesen, das Material für den Kanban von einem Lagerort-Lagerplatz zu entnehmen. Wenn der Lagerarbeiter die Entnahme bestätigt hat, wird der Kanban automatisch abgeschlossen, und der Lagerarbeiter wird angewiesen, das Material im Lagerplatz für Produktions-Wareneingang einzulagern.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
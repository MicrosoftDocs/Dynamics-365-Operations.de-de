---
title: Visuelle Zeitplanung für Lean Manufacturing
description: Dieses Thema enthält Informationen zur Behandlung der Kanban-Zeitplanübersicht, die der Produktionsplaner verwenden kann, um den Produktionsplan für Kanban-Einzelvorgänge zu steuern und zu optimieren.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 337b6b0b7ec25851f5dc156effad9ff07256a44d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814205"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Visuelle Zeitplanung für Lean Manufacturing

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur Behandlung der Kanban-Zeitplanübersicht, die der Produktionsplaner verwenden kann, um den Produktionsplan für Kanban-Einzelvorgänge zu steuern und zu optimieren.

Dieses Thema enthält Informationen zur Behandlung der Kanban-Zeitplanübersicht, die der Produktionsplaner verwenden kann, um den Produktionsplan für Kanban-Einzelvorgänge zu steuern und zu optimieren.

Die Kanban-Zeitplanübersicht ermöglicht dem Produktionsplaner den Produktionsplan für Kanban-Einzelvorgänge zu steuern und zu optimieren. Er macht den Ausstoßes der Kanban-Einzelvorgänge transparent  nd gibt dem Produktionsplaner ein Tool, das die Produktionsplanung auf die Produktionsfertigungszelle optimiert und anhält.

## <a name="visual-scheduling-of-kanban-jobs"></a>Visuelle Planung von Kanban-Einzelvorgängen
Ein Kanban-Einzelvorgang kann aus einem oder vielen Kanban-Einzelvorgängen bestehen. Die Buchungen können in zwei Typen unterteilt werden:

-   Bearbeiten
-   Übertragen

Es können nur Ursachencodes vom Typ **Prozess** ausgewählt werden. Der Kanban-Einzelvorgang und dessen Eigenschaften, wie Aktivitätszeit, werden im Produktionskanbanfluss definiert. Im Produktionskanbanfluss einer Fertigungszelle wird der Kanban-Einzelvorgang auch zugewiesen. Die Höchstkapazität der Fertigungszelle wird basierend auf der Fertigungszellenkapazität berechnet, die für die Ressourcengruppe festgelegt wird. Sie wird nach der täglichen Arbeitszeit im zugehörigen Kalender reguliert. Wenn ein Kanban-Einzelvorgang geplant wird, lädt der Einzelvorgang die Kapazität der Fertigungszelle. Die Kanban-Zeitplanübersicht bietet die folgenden Hauptmerkmale:

-   Eine grafische Übersicht des Produktionsplans in einer Arbeitsgruppe. In dieser Übersicht werden die geplanten Kanbanbearbeitungseinzelvorgänge in bestimmten Perioden angezeigt.
-   Ein Tool, mit dem Sie ungeplante Kanban-Einzelvorgänge planen und geplanten Einzelvorgänge bereits neu planen können.

## <a name="kanban-schedule-board"></a>Kanban-Zeitplanübersicht
Die Seite **Kanban-Zeitplanübersicht** enthält sieben wichtige Elemente, wie in der folgenden Abbildung dargestellt. 

![Kanban-Zeitplanübersicht](./media/kanban-schedule-board-1024x554.png)
1.  Aktivitätsbereich
2.  Filter (Felder)
3.  Schaltfläche für ungeplante Einzelvorgänge
4.  Periodenknoten
5.  Kanban-Einzelvorgang
6.  Kapazitätsleiste
7.  Zeitraum

### <a name="view-the-time-scale"></a>Zeigt die Zeitskala an

Die Karte ist in Perioden aufgeteilt, die jeweils als Knoten (4) dargestellt sind. Die Periodenknoten werden auf der vertikalen Achse aufgeführt, und der horizontale Zugriff stellt einen Zeitraum (7) dar, mit dem die Länge der Periode angezeigt wird. Eine Periode hat eine Länge entweder von einem Tag oder eine Woche. Die Periodenlänge wird von der Konfiguration der Fertigungszelle bestimmt, die für die Kanban-Zeitplanübersicht (2) ausgewählt wird. Für jeden Periodenknoten gibt die Kanban-Zeitplanübersicht an, wie viel die geplanten Kanban-Einzelvorgänge die Periode laden. Es gibt auch hier eine Indikation für den maximalen Durchsatz für die Periode. Wenn der geplante Durchsatz den maximalen Durchsatz überschreitet, wird die Periode als überladen betrachtet und ein rotes Warnsymbol angezeigt. Ein geplanter Kanban-Einzelvorgang wird in einer Periode angezeigt, die Start- und Endzeiten (5) geplant hat. Die Länge des Einzelvorgangs entspricht der Aktivitätszeit. Kanban-Einzelvorgänge werden als überschneidend in einer Periode angezeigt, wenn deren Aktivitätszeiten der Taktzeit der Fertigungszelle überschreiten.

### <a name="view-job-status"></a>Den Einzelvorgangsstatus anzeigen

Weitere Informationen über ein Formular Quickinfo Kanban-Einzelvorgang sind in den Tooltips verfügbar, die angezeigt werden, wenn Sie den Mauszeiger über den Einzelvorgang anzeigen. Ein Symbol enthält Informationen zum Status des Einzelvorgangs. Beispielsweise gibt ein Uhrsymbol an, dass der Kanban-Einzelvorgang überfällig ist.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Verwendungsfarben, um die Kanban-Zeitplanübersicht anzuzeigen

Um den Überblick zu erhöhen, den die Kanban-Zeitplanübersicht bereitstellt, können Sie Farben verwenden, die Kanban-Einzelvorgänge unterscheiden. Die Farbe eines Kanban-Einzelvorgangs wird in der Lean Schedule-Gruppe konfiguriert, in der Sie Produkte aggregieren können, die in den gleichen Nummernkreis erzeugt werden sollen. Mit der Schaltfläche **Verwendungsthemenfarben** auf der Registerkarte **Karte** im Aktivitätsbereich können Sie zwischen der Anwendungsthemenfarben wechseln, die in der Lean Schedule-Gruppe konfiguriert werden. Für jede Periode zeigt eine Kapazitätsleiste (6) an, wie viele der verfügbaren Stunden für die Periode mit Kanban-Einzelvorgängen geladen wurden. Wenn die Periode überlastet ist, erscheint die Kapazitätsleiste rot und dicker. Alle diese Funktionen sind auf der Registerkarte **Karte** im Aktivitätsbereich (1) am Anfang der Seite **Kanban-Zeitplanübersicht** verfügbar.

## <a name="plan-unplanned-jobs"></a>Nicht geplante Einzelvorgänge planen
Sie können ungeplante Kanban-Einzelvorgänge planen im Dialogfeld **Ungeplante Einzelvorgänge des Plans**. Zum Öffnen dieses Dialogfelds klicken Sie auf die Schaltfläche **Ungeplante Einzelvorgänge**, die die aktuelle Anzahl nicht geplanter Einzelvorgänge anzeigt. Alternativ klicken Sie **Ungeplante Einzelvorgänge planen** auf der Registerkarte **Karte** im Aktivitätsbereich. Das Dialogfeld zeigt eine Liste der nicht geplanter Kanban-Einzelvorgänge für die Fertigungszelle an. Sie können das Feld **Filtern** verwenden, um alle Felder im Raster zu filtern. So können Sie auf Kanban-Einzelvorgängen für ein bestimmtes Produkt filtern. Nachdem Sie eine gefilterten Liste der Einzelvorgänge haben, die Sie einplanen möchten, wählen Sie sie in der Liste aus, und klicken Sie dann **OK**. Um die automatische Planung für die Einzelvorgänge zu planen, legen Sie die Option **Automatische Planung** auf **Ja** fest. In diesem Fall werden die Einzelvorgänge in einer Periode gemäß den jeweiligen Fälligkeitsdaten geplant. Sie können die Einzelvorgänge auch nach Periode planen. Wählen Sie im Feld **Periode** einen Periodencode aus. In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Ungeplante Einzelvorgänge des Plans** angezeigt. 

![Dialogfeld nicht geplante Einzelvorgänge planen](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Nummernkreiskanbaneinzelvorgänge in derselben Periode
Sie können den Nummernkreis von einem oder mehreren ausgewählten Einzelvorgängen in eine Periode ändern. Diese Funktion ist hilfreich, wenn Sie mehrere Einzelvorgänge, die in der Periode vorgenommen wurden, priorisieren möchten. Vielleicht möchten Sie zu den Nummernkreiseinzelvorgängen dieselben Produktattribute haben, um die Einzelvorgangsausführung zu optimieren. Sie können die Reihenfolge ändern durch Ziehen mit der Maus oder die Menüoptionen **Rückwärts** und **Vorwärts** auf der Registerkarte **Karte** im Aktivitätsbereich verwenden.

## <a name="reassign-kanban-jobs-across-periods"></a>Zuweisen von Kanban-Einzelvorgängen periodenübergreifend neu zu
Einzelvorgänge können von einer Periode zur anderen neu zugeordnet werden. Diese Funktion ist hilfreich, wenn eine Periode überlastet wird und Sie die Ebene Last in Perioden werden sollen, die die freie Kapazität verfügen. Sie können Jobs durch Ziehen mit der Maus oder mithilfe der Menüoptionen **Nächste Periode** und **Vorgängige Periode** auf der Registerkarte **Karte** im Aktivitätsbereich verwenden.

## <a name="open-the-kanban-schedule-board"></a>Kanban-Zeitplanübersicht öffnen
Sie können die Kanban-Zeitplanübersicht mit dem Menüeintrag auf den folgenden Seiten verwenden:

-   Seite **Produktionsbereich**
-   Seite **Kanban-Feinterminierung**
-   Seite **Produktionsfluss darstellen**


<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Kanban-Feinterminierung für Lean Manufacturing](lean-manufacturing-kanban-job-scheduling.md)


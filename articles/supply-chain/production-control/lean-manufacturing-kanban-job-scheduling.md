---
title: "Kaban-Einzelvorgang für Lean-Manufacturing"
description: "Dieser Artikel enthält Informationen zum Sichtsteuerelement zur Kanban-Einzelvorgangs-Planung und zu unterschiedlichen Methoden, um Kanban-Einzelvorgänge zu planen."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6ac4c1afecb72d4007d830a9927bd3171ddd48ec
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kaban-Einzelvorgang für Lean-Manufacturing

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zum Sichtsteuerelement zur Kanban-Einzelvorgangs-Planung und zu unterschiedlichen Methoden, um Kanban-Einzelvorgänge zu planen.  

Die **Kanban-Feinterminierung**-Seite bietet die visuelle Steuerung der Zeitpläne von Lean Manufacturing-Arbeitsgruppen. Sie enthält eine Übersicht aller Kanban-Einzelvorgänge und bietet mehrere Filterfunktionen. Von dieser Seite können Sie zu allen anderen Seiten wechseln, die zur Kanban-Konfiguration und -Ausführung zugeordnet sind.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatische Planung von Kanban-Einzelvorgängen
Planung kann automatisch eingeräumt werden beim Festlegen wurde dem **Automatische Planungsmenge** Parameter auf der Kanban-Regel. Wenn Sie festgelegt **Automatische Planungsmenge** auf **1**, umgehend jeder Kanban-Einzelvorgang geplant werden, wenn dieser erstellt hat. Das Ergebnis ist eine Reihe von "Was zuerst abgerufen wird, kommt zuerst dran"-Vorgängen. Wenn Sie **Automatische Planungsmenge** auf einen Wert festlegen, der größer ist als 1, werden Kanban-Einzelvorgänge gruppiert, bevor sie geplant werden. 

So können Kanban-Größen unter die tatsächlichen wirtschaftlichen Chargengrößen reduziert werden. Beispielsweise ist die wirtschaftliche Chargengröße für einen bestimmten Artikel oder Artikelfamilie (30). Anstatt Kanbans zu erstellen, die die Fertigproduktmenge 30 verwenden, können Sie die Kanban-Regel konfigurieren, so dass Sie eine Produktmenge von 10 und einen **Automatischen Planungsmengen**-Wert von **3** haben. Obwohl die automatische Planung die Kanban-Einzelvorgänge für die Arbeitsgruppe nur plant, wenn drei ungeplante Einzelvorgänge vorhanden sind, wird dem Terminplaner und dem Vorgesetzten für Zeiterfassung/BDE vollständig angezeigt, dass zwei ungeplante Einzelvorgänge möglicherweise die Ausführung erwarten. Der Terminplaner oder Vorgesetzte für Zeiterfassung/BDE kann dann diese beiden Einzelvorgänge in die Produktion übernehmen, indem sie manuell geplant oder zusätzlicher Kanbans erstellt werden.

## <a name="manual-scheduling"></a>Manuelle Zeitplanung
Für die manuelle Planung hat Microsoft Dynamics AX 2012 die Kanban-Zeitplanübersicht eingeführt. Manuelle Planung kann mit automatischer Planung kombiniert werden. Mit der Kanban-Zeitplanübersicht können Sie Einzelvorgänge planen und nicht planen, nacheinander verschieben oder von Periode zu Periode verschieben. Einzelvorgänge, die auf einer Kanban-Regel basieren, in der der **Automatische Planung**-Wert mehr als **0** ist, können manuell ungeplant sein. Jedoch werden diese Einzelvorgänge neu geplant, wenn das nächste automatische Planungsereignis auftritt (das heißt, wenn ein neues Kanban erstellt wird). Die folgenden Optionen sind für die manuelle Zeitplanung verfügbar:

-   **Zeitplan** plant die ausgewählten Einzelvorgänge gemäß ihrem Fälligkeitsdatum. (Diese Option ähnelt der automatischen Planung.)
-   **Anfangsdatum für die Vorausplanung** versucht, die ausgewählten Einzelvorgänge gemäß ihrem Fälligkeitsdatum zu planen, aber beschränkt das Ergebnis durch die Verwendung des angegebenen frühesten Startdatums.
-   **Rückwärts** verschiebt die ausgewählten geplanten Einzelvorgänge zurück in die Abfolge innerhalb der Periode.
-   **Vorwärts** verschiebt die ausgewählten geplanten Einzelvorgänge nach vorne in die Abfolge innerhalb der Periode.
-   **Vorherige Periode** verschiebt die ausgewählten geplanten Einzelvorgänge an den Anfang oder an das Ende der vorherigen Periode.
-   **Nächste Periode** verschiebt die ausgewählten geplanten Einzelvorgänge an den Anfang oder an das Ende der nächsten Periode.
-   Mit **Plan** &gt; **Einzelvorgangsstatus zurücksetzen** können Sie die Zeitplanung eines geplanten Einzelvorgangs aufheben.

## <a name="lean-scheduling-groups"></a>Lean-Planungsgruppen
Jede Farbe stellt eine Lean-Planungsgruppe dar. Lean-Planungsgruppen können frei als generische Gruppen oder als Gruppen definiert werden, die zu einer einzelnen Arbeitsgruppe gehören. Artikel und Dimensionen können den Planungsgruppen frei zugewiesen werden. In einer Zeichnen-Zelle kann eine Schedule-Gruppe z. B. eine Farbe des Produkts darstellen. In der Arbeit, die auf bestimmten Werkzeugausstattungsanforderungen basiert, werden Artikel möglicherweise nach einer Toolanforderung gruppiert, und eine Verpackungsarbeitsgruppe könnte Artikel nach einer Verpackungsvorlage gruppieren. Die Verwendung von Farben für lean-Planungsgruppen ist optional, jedoch empfohlen. Sichtbarkeit verbessert Sie im den Status des Plans. Beispielsweise ist es sehr einfach, zu sehen, welche Farben an welchem Tag produziert werden, und Sie können auf einen Blick sagen, wie diese Arbeit optimiert werden kann.

## <a name="work-cell-capacity-and-period-capacity"></a>Arbeitsgruppenkapazität und Periodenkapazität
Die Kapazität einer Lean-Arbeitsgruppe ist immer gleichzeitige Kapazität. Das bedeutet, dass mehrere Einzelvorgänge in einer Arbeitsgruppe gleichzeitig aktiv sein können. Die Kapazität kann in zwei Modi verfolgt werden: Durchsatz und Stunden.

### <a name="throughput"></a>Durchsatz

Die Kapazität einer Arbeitsgruppe wird nach der durchschnittlichen Durchsatzmenge eines Referenzzeitraums definiert (Standardarbeitstag, -woche oder -monat). Die tatsächliche Kapazität pro Tag oder Woche wird anschließend auf Basis der Arbeitszeiten des Kalenders berechnet, der der Arbeitsgruppe zugewiesen wird. Die Kapazität, die nach Einzelvorgang geladen wird, ist die Menge des Einzelvorgangs, angepasst nach Durchsatzverhältnis des Artikels in der Arbeitsgruppe.

### <a name="hours"></a>Stunden

Die verfügbare Kapazität pro Tag oder Woche wird anhand des Kalenders definiert, der der Arbeitsgruppe zugeordnet wird. Die Kapazität, die nach Einzelvorgang geladen wird, ist die Zykluszeit der Aktivität, angepasst nach Menge (Standardaktivitätsmenge im Vergleich zur tatsächlichen Einzelvorgangsmenge) und Durchsatzverhältnis des Artikels in der Arbeitsgruppe.

#### <a name="period-capacity-factbox"></a>Periodenkapazität-Infobox

Die **Kanban-Feinterminierung**-Listenseite enthält eine Infobox, die die verfügbare und gebuchte Periodenkapazität für die ausgewählte Arbeitsgruppe anzeigt. Abhängig von den ausgewählten Zeitplanperioden im Produktionsflussmodell zeigen die Perioden Tage oder Wochen an.

<a name="see-also"></a>Siehe auch
--------





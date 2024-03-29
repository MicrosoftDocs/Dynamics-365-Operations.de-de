---
title: Lean Manufacturing Übersicht
description: Dieser Artikel stellt eine Übersicht und Beschreibung der Lean Manufacturing-Funktionen in Dynamics 365 Supply Chain Management bereit.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow, Kanban, KanbanQuantityOverview, KanbanAssignCard, KanbanCirculatingCards, KanbanRules, WHSKanbanWaveTableManagePickingListPool
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19371"
- intro-internal
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c8b5ec4d4a391773e32a61a321c28868678baa
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985935"
---
# <a name="lean-manufacturing-overview"></a>Übersicht über Lean Manufacturing

[!include [banner](../includes/banner.md)]

Dieser Artikel stellt eine Übersicht und Beschreibung der Lean Manufacturing-Funktionen in Dynamics 365 Supply Chain Management bereit.

Lean Manufacturing stellt Tools bereit, die Sie für die Modellierung schlanker Arbeitsgänge verwenden können. Diese Tools unterstützen und fördern die folgenden Konzepte und Geschäftsaktivitäten:
-   Erstellen einer Grundlage für das Lean Manufacturing, indem Sie Produktions- und Logistikprozesse als Produktionsflüsse modellieren.
-   Implementieren eines schlankes Pullsystems, indem Sie Kanbans verwenden, um Bedarfsanforderungen zu signalisieren.
-   Überwachen und Verwalten von Kanban-Einzelvorgängen.

Die Lean Manufacturing-Architektur besteht aus Produktionsflüssen, Aktivitäten und Kanban-Regeln. Diese Strukturen sind vollständig mit Supply Chain Management-Prozessen integriert. Sie können Lean Manufacturing in einer gemischten Produktionsumgebung verwenden, in der verschiedene Lieferanten-, Produktions- und Beschaffungsstrategien kombiniert sind. Diese Strategien enthalten Produktionsaufträge, Chargenaufträge für die verarbeitende Industrie, Bestellungen und Umlagerungsaufträge.

| **Wichtig**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sie können Supply Chain Management verwenden, um die Implementierung von Lean Manufacturing mit Kanbans zu unterstützen. Die erfolgreiche Implementierung von schlanken Prinzipien ist jedoch von den internen Geschäftsprozessen abhängig, die Sie verwenden, und von den tatsächlichen Produktionsbedingungen und -umgebungen. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a>Modellierung von Fertigungs- und Logistikprozessen als Produktionsflüssen
Um die Grundlage für das Lean Manufacturing zu erstellen, modellieren Sie die Fertigungs- und Logistikprozesse als Produktionsflüsse. Diese Aktivität besteht aus den folgenden Aufgaben:
1.  Identifizieren der Prozesse, für die Sie eine schlanke Auffüllungsstrategie implementieren möchten, und die anschließende Modellierung dieser Prozesse als Produktionsflüsse. Sie können die Prozesse anschließend analysieren und optimieren. Eines der Ziele einer schlanken Implementierung besteht darin, den Abfall zu reduzieren, indem Materialfluss und Informationen verbessert werden.
2.  Definieren eines Produktionsflusses als Folge von Aktivitäten, die den Materialfluss beschreibt. Eine Umlagerungsaktivität definiert die Bewegung eines Produkts oder von Produkten von einem Lagerort zu einem anderen Lagerort. Eine Verarbeitungsaktivität definiert einen Mehrwertprozess, der auf ein Produkt angewendet wird.
3.  Erstellen einer Version des Produktionsflusses, der die Anforderungen für die Taktzeit definiert. Diese Anforderungen werden verwendet, um die Zykluszeiten der einzelnen Aktivitäten im Produktionsfluss zu berechnen. Sie können mehrere Versionen von Produktionsflüssen erstellen und anschließend diese Versionen verwenden, um die Prozesse zu verbessern.

## <a name="using-kanbans-to-signal-demand-requirements"></a>Verwenden von Kanbans, um Bedarfsanforderungen zu signalisieren
Ein Pullsystem produziert nur dann Waren, wenn Waren erforderlich sind. Diese Methode verringert Lieferzeiten und überschüssige Bestände. Sie können Kanbans verwenden, um Anforderungen zu planen, nachzuverfolgen und zu bearbeiten, die auf Produktionsflüssen basieren. Wenn Sie ein Kanban-Framework erstellen möchten, erstellen Sie Kanban-Regeln, die definieren, wann Kanbans erstellt werden und wie die Anforderungen erfüllt werden. Sie können zwei Arten von Kanban-Regeln erstellen. Fertigungsregeln erstellen Kanban-Bearbeitungseinzelvorgänge, und Kanban-Widerrufsregeln erstellen Kanban-Übertragungseinzelvorgänge. Sie können die folgenden Auffüllungsstrategien einrichten:
-   Kanban-Regeln für **Feste Menge** sind einer festen Anzahl von Handhabungseinheiten zugeordnet, was bedeutet, dass die Zahlen von aktiven Kanbans konstant sind. Sobald alle Produkte aus einem Kanban verbraucht und die Handhabungseinheiten manuell geleert sind, wird ein neues Kanban desselben Typs erstellt. Wenn Sie Regeln für Kanbans für feste Mengen erstellen, können Sie die optimalen Kanban-Mengen und die Produktmengen berechnen, die verwendet werden. Die Berechnung berücksichtigt Planung, tatsächlichen Bedarf aus offenen Aufträgen, die Lieferzeit zum Auffüllen von Artikeln und historische Nachfragen.
-   **Geplante** Kanban-Regeln füllen Anforderungen auf, die durch den Produktprogrammplan berechnet werden. Produktprogrammplan generiert geplante Kanbans, die zu Kanbans umgewandelt werden können.
-   Kanban-Regeln für **Ereignisse** füllen Anforderungen auf, die aus Auftragspositionen, Produktionsstücklistenpositionen, Kanban-Positionen oder Einstellungen für den Mindestlagerbestand entstehen. Wenn Ereignis-Kanbans generiert werden, werden sie den Quellanforderungen zugewiesen.

Wenn Kanbans erstellt werden, werden ein oder mehrere Kanban-Einzelvorgänge generiert, basierend auf den Kanban-Flussaktivitäten, die in den Kanban-Regeln definiert sind.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Überwachen und Verwalten von Kanban-Einzelvorgängen
Lean Manufacturing stellt Transparenz für den aktuellen Status der Produktions- und Logistikaktivitäten bereit, die durch die Kanban-Regeln gesteuert werden. Somit können Sie die folgenden Aufgaben planen und priorisieren:

-   Erhalten einer Übersicht über den Zeitplan des aktuellen Kanban-Einzelvorgangs.
-   Planen und Neuplanen von Kanban-Einzelvorgängen.
-   Überwachen und Registrieren des Status von Kanban-Einzelvorgängen.

In der folgenden Liste werden die speziellen Kanban-Übersichten beschrieben:
-   Kanban-Einzelvorgangs-Planung – Bietet eine Übersicht der Kanban-Einzelvorgänge. In der Übersicht werden Kanban-Einzelvorgänge und deren Status für eine oder mehrere Arbeitsgruppen angezeigt. Die Einzelvorgänge sind nach Planungsperioden (Tage oder Wochen) aufgelistet, die im Produktionsflussmodell definiert sind. Die Übersicht zeigt außerdem den Kapazitätsverbrauch für jede Planungsperiode an, sodass Sie die geplante Auslastung überwachen können. Sie können den Status von Kanban-Einzelvorgängen ändern, Kanban-Einzelvorgänge für verschiedene Planungsperioden neu planen und andere Aufgaben ausführen.
-   Kanban-Übersicht für Umlagerungseinzelvorgänge – Diese Übersicht stellt einen Überblick über die aktuellen Umlagerungseinzelvorgänge bereit. Sie können Entnahmelisten aktualisieren und erfassen, Umlagerungseinzelvorgänge starten und abschließen und andere Aufgaben ausführen.
-   Kanban-Übersicht für Bearbeitungs-Einzelvorgänge – Diese Übersicht wurde entworfen, um den normalen Produktionsfluss zu unterstützen und einen Überblick über den aktuellen Status in einer oder mehreren Arbeitsgruppen zu geben. Mit dieser Übersicht können Kanbans priorisiert, entnommen oder produziert werden. Die Karte ist außerdem so konzipiert, dass sie Barcode-Scans für die Meldung von Kanbans unterstützt.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanban-Einzelvorgänge und Integration in Supply Chain Management-Prozesse
Kanban-Einzelvorgänge sind vollständig in aktuelle Prozesse für Lagerbuchungen in Supply Chain Management integriert.
-   Sie können Kommissionieraktivitäten ausführen, um Material aufzufüllen, das verwendet wird, um die Anforderungen von Kanban-Einzelvorgängen zu erfüllen.
-   Sie können Kanban-Karten, Kanban-Karten im Umlauf und Entnahmelisten drucken, um die Verwendung von Kanbans zu unterstützen. Diese Dokumente werden verwendet, um Kanban-Einzelvorgänge am Lagerort und in der Produktion darzustellen, zu überwachen und zu erfassen.
-   Sie können die Entnahme- und die Umlagerungsaktivitäten im Lager mittels Strichcodes erfassen.

Darüber hinaus unterstützt Lean Manufacturing die Einkaufs- und Rechnungsstellungsverfahren für Dienstleistungen, auf die durch Fremdarbeitsaktivitäten verwiesen wird.
-   Sie können Kaufvertragspositionen und Dienste Fremdarbeitsaktivitäten zuweisen.
-   Sie können periodische Bestellungen und Empfangsbestätigungen erstellen, um den Einkauf und die Rechnungsstellung von Dienstleistungen zu unterstützen.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
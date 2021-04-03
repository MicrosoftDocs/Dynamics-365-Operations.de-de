---
title: Produktionsplanung
description: In diesem Thema wird die Planung für die Produktion beschrieben und erläutert, wie Sie geplante Produktionsaufträge mithilfe der Planungsoptimierung ändern können.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470832"
---
# <a name="production-planning"></a>Produktionsplanung

Die Planungsoptimierung unterstützt mehrere Produktionsszenarien. Wenn Sie vom bestehenden integrierten Masterplanungsmodul migrieren, ist es wichtig, dass Sie einige geänderte Verhaltensweisen beachten.

Das folgende Video gibt eine kurze Einführung in einige der in diesem Thema besprochenen Konzepte: [Dynamics 365 Supply Chain Management: Erweiterungen der Planungsoptimierung](https://youtu.be/u1pcmZuZBTw).

## <a name="planned-production-orders"></a>Geplante Produktionsaufträge

Wenn die Masterplanung geplante Aufträge erstellt, um Anforderungen zu erfüllen, wird der Auftragstyp durch den Wert des Felds **Geplante Auftragsart** bestimmt. Wenn das Feld **Geplante Auftragsart** auf *Produktion* festgelegt ist, werden geplante Produktionsaufträge erstellt. Diese geplanten Produktionsaufträge enthalten Informationen zur aktiven Stückliste und zur Routenkennung aus dem zugehörigen Produktionsaufbau.

## <a name="requirements-from-boms"></a>Anforderungen aus Stücklisten

Stücklisteninformationen werden bei der Masterplanung berücksichtigt. Die Planausgabe umfasst die Materialversorgung zur Deckung des damit verbundenen Materialbedarfs für die Produktion.

Während der Masterplanung wird anhand der aktuellen aktiven Stückliste ermittelt, welche Materialien für die Produktion benötigt werden. Dieser Schritt wird auf allen Ebenen der Stücklistenstruktur ausgeführt, die sich auf den erforderlichen Produktionsauftrag beziehen. Der Materialbedarf wird durch die Verwendung des verfügbaren Bestands, der laufenden Vorratsbestellungen und der genehmigten geplanten Aufträge erfüllt. Wenn zusätzliches Material benötigt wird, wird ein geplanter Auftrag erstellt, um den Bedarf zu decken.

## <a name="scheduling-during-firming"></a>Planung während der Umwandlung

Geplante Produktionsaufträge enthalten die Routenkennung, die zur Produktionsplanung erforderlich ist. Der Planungssupport während des Planungslaufs für geplante Aufträge steht jedoch noch aus. Die Routenkennung wird verwendet, um geplante Produktionsaufträge während der Umwandlung zu planen. Daher kann die Vorlaufzeit für geplante Produktionsaufträge von der Vorlaufzeit für zugehörige geplante, umgewandelte Produktionsaufträge abweichen, die aus ihnen generiert werden, wie hier beschrieben:

- **Geplanter Produktionsauftrag** – Die Vorlaufzeit basiert auf der statischen Vorlaufzeit des freigegebenen Produkts.
- **Umgewandelter Produktionsauftrag** – Die Vorlaufzeit basiert auf einer Zeitplanung, die Routeninformationen und zugehörige Ressourcenbeschränkungen verwendet.

Weitere Informationen zur erwarteten Verfügbarkeit von Funktionen finden Sie unter [Passanalyse zu Planungsoptimierung](planning-optimization-fit-analysis.md).

Wenn Sie auf Produktionsfunktionen angewiesen sind, die zur Planungsoptimierung noch nicht verfügbar sind, können Sie weiterhin das integrierte Masterplanungsmodul verwenden. Eine Ausnahme ist nicht erforderlich.

## <a name="delays"></a>Verzögerungen

Wenn die Vorlaufzeit für das erforderliche Material länger ist als der Zeitraum zwischen dem heutigen Datum und dem Materialbedarfsdatum, wird der geplante Auftrag für das erforderliche Material und den zugehörigen Produktionsauftrag verzögert. Bei geplanten Aufträgen wird die Verzögerung (in Tagen) anhand der Vorlaufzeit des freigegebenen Produkts berechnet. Die Verzögerungsinformationen werden dann über alle Ebenen der Stücklistenstruktur weitergegeben. Daher können Sie die Auswirkungen von Verzögerungen beim Rohmaterial bis zum Kundenauftrag verfolgen.

## <a name="modifying-planned-orders"></a>Ändern von geplanten Aufträgen

Wenn Sie Informationen zu einem geplanten Auftrag ändern, wird folgende Meldung angezeigt: „Beachten Sie, dass die Auswirkungen manueller Änderungen auf geplante Aufträge für die restliche Planung erst im nächsten Masterplanungslauf berücksichtigt werden.“

Wenn Sie Informationen zu einem geplanten Auftrag ändern und die Auswirkungen auf die zugehörigen Materialanforderungen sehen möchten, führen Sie die folgenden Schritte aus.

1. Aktualisieren Sie den geplanten Auftrag.
2. Genehmigen Sie den geplanten Auftrag.
3. Führen Sie die Masterplanung aus.

Wenn Sie die Masterplanung ausführen, sollten Sie keine Filter verwenden, wenn geplante Produktionsaufträge enthalten sind. Weitere Informationen finden Sie im Abschnitt [Filter](#filters) weiter unten in diesem Thema.

> [!NOTE]
> Wenn das Lieferdatum für den geplanten Auftrag auf einen späteren Zeitpunkt verschoben wird, kann die Nachfrage an einen neuen geplanten Auftrag gebunden sein. Dieses Verhalten tritt auf, wenn der neue Liefertermin eine Verzögerung für die gebundene Nachfrage verursacht, die Verzögerung jedoch gemäß den Einstellungen für die Vorlaufzeit vermieden werden kann.

## <a name="explosion-page"></a>Die Seite „Auflösung“

Sie können die Seite **Auflösung** verwenden, um den erforderlichen Bedarf für einen bestimmten oder geplanten Produktionsauftrag, die zugehörige Abdeckung und die Informationen zum Bedarfsverursacher zu analysieren. Die Informationen auf der Seite **Auflösung** werden während der Masterplanung aktualisiert. Sie können die Informationen nicht direkt über die Seite **Auflösung** aktualisieren.

## <a name="filters"></a><a name="filters"></a>Filter

Für Planungsszenarien inklusive Produktion empfehlen wir, gefilterte Masterplanungsläufe zu vermeiden. Um sicherzustellen, dass die Planungsoptimierung über die erforderlichen Informationen zur Berechnung des korrekten Ergebnisses verfügt, müssen Sie alle Produkte berücksichtigen, die in irgendeiner Beziehung zu Produkten in der gesamten Stücklistenstruktur des geplanten Auftrags stehen.

Obwohl abhängige untergeordnete Artikel automatisch erkannt und in Masterplanungsläufe einbezogen werden, wenn das integrierte Masterplanungsmodul verwendet wird, führt die Planungsoptimierung diese Aktion nicht aus.

Wenn beispielsweise eine einzelne Schraube aus der Stücklistenstruktur von Produkt A auch zur Herstellung von Produkt B verwendet wird, müssen alle Produkte in der Stücklistenstruktur der Produkte A und B in den Filter aufgenommen werden. Da es sehr komplex sein kann, sicherzustellen, dass alle Produkte Teil des Filters sind, empfehlen wir, gefilterte Masterplanungsläufe zu vermeiden, wenn Produktionsaufträge betroffen sind.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
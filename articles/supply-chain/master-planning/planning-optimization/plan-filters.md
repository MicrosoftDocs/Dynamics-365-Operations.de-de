---
title: Filter auf einen Plan anwenden
description: In diesem Thema wird erläutert, wie Sie Filter auf einem Plan verwenden, wenn Sie die Funktionalität der Planungsoptimierung verwenden.
author: ChristianRytt
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3612dd45a3f4b8c3597c81962a66c21ed14fb206
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729026"
---
# <a name="apply-filters-to-a-plan"></a>Filter auf einen Plan anwenden

[!include [banner](../../includes/banner.md)]

Wenn Sie die Funktionalität der Planungsoptimierung nutzen, können Sie einen Filter auf einen Plan anwenden. Der **Planfilter** wird immer während einer Masterplanungsausführung angewendet. Ein **Planfilter** ist sinnvoll, wenn Sie einen Plan auf eine bestimmte Gruppe von Positionen beschränken und sicherstellen wollen, dass keine weiteren Positionen in die resultierende Masterplanung einbezogen werden.

Wenn ein **Planfilter** angewendet wird und während der Masterplanungsausführung auch ein Laufzeitfilter angewendet wird, wird nur die Schnittmenge der beiden Filter in die Planungsausführung einbezogen.

Der **Planungsfilter** kann über **Masterpläne** aufgerufen werden, wenn die Planungsoptimierung verwendet wird.

## <a name="example-scenario"></a>Beispielszenario

Es wird ein Planfilter eingerichtet, der die Positionen A, B und C enthält. Die Masterplanungsläufe werden dann für den gleichen Plan ausgeführt, wobei jedoch unterschiedliche Laufzeitfilter angewendet werden:

- **Laufzeitfilter, der Element D enthält:** Es werden keine Elemente geplant, da es keinen Schnittpunkt zwischen dem Planfilter und dem Laufzeitfilter gibt.
- **Laufzeitfilter, der Position A und D enthält:** Nur Position A wird in den Planungslauf einbezogen, da Position D nicht Teil des Planfilters ist.
- **Laufzeitfilter, der Position B enthält:** Nur Position B wird in den Planungslauf einbezogen, und die bisherige Planungsausgabe für Position A bleibt erhalten.
- **Laufzeitfilter, der alle Positionen beinhaltet (Blindfilter):** Die Positionen A, B und C werden in den Planungslauf einbezogen, und die bisherige Planungsausgabe für die Positionen A und B wird überschrieben.

> [!NOTE]
> Wenn Sie einen Planfilter für den Plan festlegen, der als **Aktueller dynamischer Produktprogrammplan** auf der Seite **Produktprogrammplanparameter** ausgewählt wird, dann wird die Funktionalität des dynamischen Produktprogrammplans auf die gefilterten Elemente beschränkt. Wenn beispielsweise der Nettobedarf für eine Position aktualisiert wird, die nicht Teil des Planfilters ist, wird kein Ergebnis erzeugt.

## <a name="related-resources"></a>Zugehörige Ressourcen

[Planungsoptimierung – Übersicht](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

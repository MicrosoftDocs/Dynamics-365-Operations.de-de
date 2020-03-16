---
title: Planung mit negativen Vorgabemengen
description: In diesem Thema wird erläutert, wie mit dem Negativ-Bestand umgegangen wird, wenn Sie die Planungsoptimierung einsetzen.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca12d13f7318f649cb1dbc0f7c3cf56502c9d3ea
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077483"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planung mit negativen Vorgabemengen

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Wenn das System eine negative aggregierte Bestandsmenge anzeigt, behandelt die Planungsmaschine die Menge als 0 (Null), um ein Überangebot zu vermeiden. Im Folgenden wird erläutert, wie diese Funktionalität funktioniert:

1. Die Planungsoptimierung aggregiert die Bestandsmengen auf der untersten Ebene der Deckungsdimensionen. (Wenn z.B. *Lagerplatz* keine Deckungsdimension ist, aggregiert die Planungsoptimierung die verfügbaren Mengen auf der Ebene *Lager*).
1. Wenn die aggregierte Bestandsmenge auf der untersten Ebene der Deckungsdimensionen negativ ist, geht das System davon aus, dass die Bestandsmenge tatsächlich 0 (Null) ist.

> [!IMPORTANT]
> Das Planungssystem kann nur so genau sein wie die Eingabedaten. Wenn die Eingabedaten ungenau sind, zeigen negative Datensätze auf dem Datenbestand an, dass die Bestandsinformationen in Microsoft Dynamics 365 Supply Chain Management nicht mit der realen Welt übereinstimmen. Daher wird das Planungsergebnis fehlerhaft sein. Um ein präzises Planungsergebnis zu erhalten, sollten Sie die Anzahl der Datensätze, die eine negative Bestandsmenge aufweisen, minimieren.

## <a name="example-1"></a>Beispiel 1

Lager 13 ist wie folgt konfiguriert:

- **Deckungscode:** Min./Max.
- **Minimum:** 15 Stück (Stk.)
- **Maximal:** 25 Stk.

Die niedrigste Ebene der Deckungsdimensionen ist *Lager*, und die folgenden vorrätigen Mengen werden auf der Ebene *Lagerplatz* erfasst:

- **Standort 1, Lager 13, Lagerplatz 1:** 20 Stk.
- **Standort 1 Lager 13, Lagerplatz 2:** &minus;8 Stk.

Somit beträgt die aggregierte Bestandsmenge für Lager 13 12 Stk. (= 20 Stk. &minus; 8 Stk.).

In diesem Fall verwendet die Planungsmaschine eine Aggregat-Bestandsmenge von 12 Stk. für Lager 13.

Das Ergebnis ist ein Planauftrag von 13 Stück. (= 25 Stk. &minus; 12 Stk.), um Lager 13 aus 12 Stk. wieder aufzufüllen. auf 25 Stk.

## <a name="example-2"></a>Beispiel 2

Lager 13 ist wie folgt konfiguriert:

- **Abdeckungscode:** Min./Max.
- **Minimum:** 15 Stk.
- **Maximum:** 25 Stk.

Die niedrigste Ebene der Deckungsdimensionen ist *Lager*, und die folgenden vorrätigen Mengen werden auf der Ebene *Lagerplatz* erfasst:

- **Standort 1, Lager 13, Lagerplatz 1:** 4 Stk.
- **Standort 1 Lager 13, Lagerplatz 2:** &minus;8 Stk.

Daher beträgt die gesamte verfügbare Menge für Lager 13 &minus;4 Stk. (= 4 Stk. &minus; 8 Stk.). Mit anderen Worten, sie ist weniger als 0 (Null).

In diesem Fall geht das Planungsmodul davon aus, dass die vorrätige Menge für Lager 13 0 St. beträgt. statt &minus;4 Stk.

Das Ergebnis ist ein Planauftrag von 25 Stück. (= 25 Stk. &minus; 0 Stk.), um Lager 13 aus 0 Stk. wieder aufzufüllen. bis 25 Stk.

## <a name="related-resources"></a>Zugehörige Ressourcen

[Übersicht zur Planungsoptimierung](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)

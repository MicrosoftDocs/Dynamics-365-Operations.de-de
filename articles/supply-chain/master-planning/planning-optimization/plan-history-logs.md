---
title: Anzeigen der Planhistorie und der Planungsprotokolle
description: In diesem Thema wird erläutert, wie Sie die Historie von Planungsjobs anzeigen, die durch die Funktionalität der Planungsoptimierung ausgelöst werden.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187246"
---
# <a name="view-plan-history-and-planning-logs"></a>Anzeigen der Planhistorie und der Planungsprotokolle

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Historie von Planungsjobs anzeigen, die durch die Funktionalität der Planungsoptimierung in Microsoft Dynamics 365 Supply Chain Management ausgelöst werden.

Um die Historie für einen Plan anzuzeigen, öffnen Sie den Plan, indem Sie zu **Masterplanung** \> **Einrichtung** \> **Pläne** \> **Masterpläne** gehen und **Historie** auswählen. Die Historie listet alle Aufträge für den ausgewählten Plan auf. Die Liste enthält erledigte und aktive Aufträge.

Die Historie der Jobs für die Masterplanungsläufe der Planungsoptimierung enthält nur bis zu 60 Datensätze pro Masterplan. Wenn Sie eine neue Hauptplanungsberechnung ausführen, wird der früheste Historiensatz dieses Plans gelöscht.

Sie können nicht nur die Startzeit und den Status der Jobs einsehen, sondern auch das Protokoll für einen bestimmten Job anzeigen. Das Protokoll enthält zusätzliche Informationen und Warnungen. Nicht alle Aufträge haben ein Protokoll. Um das Protokoll für einen Auftrag anzuzeigen, wählen Sie **Protokoll**. Log-Einträge werden nur 30 Tage nach Auftragsende gespeichert und danach automatisch gelöscht.

## <a name="related-resources"></a>Zugehörige Ressourcen

- [Übersicht zur Planungsoptimierung](planning-optimization-overview.md)
- [Erste Schritte mit der Planungsoptimierung](get-started.md)
- [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)
- [Filter auf einen Plan anwenden](plan-filters.md)
- [Abbrechen eines Planungsauftrags](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
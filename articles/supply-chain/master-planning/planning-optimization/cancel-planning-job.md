---
title: Abbrechen eines Planungsauftrags
description: In diesem Thema wird erläutert, wie Sie einen aktiven Planungseinzelvorgang stornieren, der die Funktion „Planungsoptimierung“ verwendet.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773968"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a>Abbrechen eines Planungsauftrags

In Microsoft Dynamics 365 Supply Chain Management können Sie einen aktiven Planungseinzelvorgang stornieren, der die Funktion „Planungsoptimierung“ verwendet.

Um einen aktiven Planungseinzelvorgang zu stornieren, führen Sie die folgenden Schritte aus.

> [!NOTE]
> Es können nur aktive Aufträge abgebrochen werden.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne**.
2. Wählen Sie einen entsprechenden Plan für den Planungslauf aus.
3. Wählen Sie **Verlauf** aus.
4. Wählen Sie den zu stornierenden Planungseinzelvorgang aus.
5. Wählen Sie **Abbrechen** aus.

Der Status des Einzelvorgangs lautet **Wird storniert**, bis der Planungsoptimierungsdienst bestätigt, dass der Auftrag storniert wurde. Der Status wird anschließend in **Storniert** geändert.

> [!NOTE]
> Um Statusänderungen anzuzeigen, müssen Sie die Seite aktualisieren, indem Sie die Schaltfläche **Aktualisieren** auswählen.

## <a name="related-resources"></a>Zugehörige Ressourcen

[Planungsoptimierung – Übersicht](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

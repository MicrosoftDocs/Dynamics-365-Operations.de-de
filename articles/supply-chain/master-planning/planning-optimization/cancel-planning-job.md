---
title: Abbrechen eines Planungsauftrags
description: In diesem Thema wird erläutert, wie ein aktiver Planungsauftrag, der die Planungsoptimierungsfunktionalität verwendet, abgebrochen werden kann.
author: ChristianRytt
manager: tfehr
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428675"
---
# <a name="cancel-a-planning-job"></a>Abbrechen eines Planungsvorgangs

[!include [banner](../../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management können Sie einen aktiven Planungsauftrag, der die Planungsoptimierungsfunktionalität verwendet, abbrechen. Wenn Sie im Dialogfenster **Abbrechen** wählen, wenn ein Planungsoptimierungsjob direkt von der Benutzeroberfläche aus (nicht im Hintergrund) ausgelöst wird, wird der Planungsoptimierungsjob nicht abgebrochen. Selbst wenn Sie eine Warnung wie „Vorgang abgebrochen“ erhalten, müssen Sie die folgenden Schritte durchführen, um einen Planungsjob mit Planungsoptimierung abzubrechen.


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

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Planungsoptimierung](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

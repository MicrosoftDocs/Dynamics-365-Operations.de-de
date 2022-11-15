---
title: Planungsvorgang abbrechen
description: In diesem Artikel wird erläutert, wie ein aktiver Planungsauftrag, der die Planungsoptimierungsfunktionalität verwendet, abgebrochen werden kann.
author: t-benebo
ms.date: 02/18/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5f1f2c8e3e43e36d837ebf989422b0dca7819d6
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741175"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
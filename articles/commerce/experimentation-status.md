---
title: Den Status eines Experiments überprüfen
description: In diesem Thema wird erläutert, welchen Status ein Experiment im Experimentierlebenszyklus in Dynamics 365 Commerce hat.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5ae29fe5ac49d92c261c59d115664b50e87880a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965102"
---
# <a name="review-the-status-of-an-experiment"></a>Den Status eines Experiments überprüfen
Das Einrichten und Ausführen eines Experiments in Dynamics 365 Commerce umfasst viele Schritte. Informationen zum Experimentierlebenszyklus finden Sie unter [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).

Um zu erfahren, wo sich ein Experiment im Lebenszyklus befindet, wählen Sie **Experimente** im linken Navigationsbereich im Commerce Site Builder. Eine Liste von Experimenten wird mit dem Status jedes Experiments sowohl in Commerce als auch im Drittanbieterdienst angezeigt, der zum Erstellen von Experimenten, Zuweisen von Variationen und Analysieren von Daten verwendet wird.

In der Spalte **Commerce-Status** können die folgenden Werte angezeigt werden. 
- **Entwurf** – Das Experiment ist mit einer Seite oder einem Fragment in Commerce verbunden und wird bearbeitet.
- **Veröffentlicht** – Die Experimentvarianten können auf Ihrer Website angezeigt werden. Wenn das Experiment im Dienst eines Drittanbieters ausgeführt wird, sehen Benutzer der Website eine Variation der Seite oder des Fragments, die bzw. das vom Dienst eines Drittanbieters ausgewählt wurde.
- **Unveröffentlicht** – Das Experiment ist auf Ihrer Website nicht mehr verfügbar. Benutzer der Website sehen nur eine Standardversion der Seite oder des Fragments, auch wenn das Experiment im Dienst eines Drittanbieters ausgeführt wird.
- **Abgeschlossen** – Das Experiment hat seinen Lauf genommen und eine Variation wurde für die Benutzung durch alle Website-Benutzer höher gestuft.

Entsprechend können in der Spalte **Drittanbieterstatus** die folgenden Werte angezeigt werden, um anzuzeigen, welchen Status die Experimente im Drittanbieterdienst haben.
- **Entwurf** – Das Experiment wird im Drittanbieterdienst eingerichtet, aber noch nicht gestartet.
- **Wird ausgeführt** – Das Experiment wurde im Drittanbieterdienst gestartet und sammelt Daten.
- **Angehalten** – Das Experiment wird angehalten und es werden keine Daten erfasst. Sie müssen das Experiment fortsetzen, damit die Daten erneut erfasst werden.
- **Archiviert** – Das Experiment hat seinen Lauf genommen und wurde für spätere Referenzzwecke im Drittanbieterdienst katalogisiert.

Das folgende Diagramm zeigt beide Statussätze und ihre Beziehung zueinander.

[ ![Experimentierstatus](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
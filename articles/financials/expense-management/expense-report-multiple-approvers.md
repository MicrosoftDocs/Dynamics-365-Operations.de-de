---
title: Spesenabrechnungen und mehrere Genehmiger
description: "Dieses Thema enthält Informationen zu Spesenabrechnungen, für die die Genehmigung von mehr als einer Person erforderlich ist."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: de-de
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a>Spesenabrechnungen und mehrere Genehmiger

[!include[banner](../includes/banner.md)]

Je nach den Ausgabengenehmigungsrichtlinien der Organisation müssen u. U. mehrere Personen eine Spesenabrechnung genehmigen, die von einem Mitarbeiter eingereicht wird. Wenn Sie den Workflowprozess für die Genehmigung von Spesenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für eine oder mehrere für Spesenabrechnungen zuständige genehmigende Personen enthalten. Sie können beispielsweise anfordern, dass alle Spesenabrechnungen zunächst vom Vorgesetzten des Mitarbeiters genehmigt werden, der die Abrechnung eingereicht hat, und dann vom Kreditorenkoordinator.

Wenn Sie festlegen, dass bei Spesenabrechnungen mehrere genehmigende Personen erforderlich sind, können Sie die Workflowelemente auf eine der folgenden Weisen hinzufügen:

- Ein Genehmigungselement hinzufügen, das einen Schritt enthält. Der Schritt kann z. B. verlangen, dass eine Spesenabrechnung einer Benutzergruppe zugeordnet wird und dass sie von 50 % der Benutzergruppenmitglieder genehmigt werden muss.
- Ein Genehmigungselement hinzufügen, das mehrere Schritte enthält. Die Schritte im Genehmigungselement können z. B. folgende sein:

    1. Der Vorgesetzte des Mitarbeiters, der die Spesenabrechnung eingereicht hat, genehmigt sie.
    2. Der Kreditorensachbearbeiter überprüft die Zugänge und die Spesenabrechnungsartikel.
    3. Der Budgetbesitzer genehmigt die Spesenabrechnung.

- Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat. Beispielsweise müssen Sie möglicherweise ein gesondertes Genehmigungselements für jeden der folgenden Schritte hinzufügen:

    1. Der Vorgesetzte des Mitarbeiters genehmigt die Spesenabrechnung.
    2. Der Budgetbesitzer genehmigt die Spesenabrechnung.


---
title: Erstellen von Wartungsbudgets
description: In diesem Artikel wird erläutert, wie Wartungsbudgets in der Anlagenverwaltung erstellt werden.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858039"
---
# <a name="create-maintenance-budgets"></a>Erstellen von Wartungsbudgets

[!include [banner](../../includes/banner.md)]

 



Wartungsbudgets werden verwendet, um eine Übersicht über die erwarteten Kosten für vorbeugende Wartungsaufträge bereitzustellen. Budgetpositionen werden auf Grundlage der Wartungsplanpositionen berechnet, die ein voraussichtliches Startdatum während der Budgetperiode haben.

Wartungsbudgets basieren auf den Kostentypen, die in der Anlagenverwaltung verwendet werden: **Vorbeugend**, **Korrektiv** und **Investition**. Budgetkosten für die Investitionswartung sind für aktive Anlagen enthalten, die ein Ersetzungsdatum während der Budgetperiode und einen zugehörigen Wiederbeschaffungswert haben. Budgetkosten für korrektive Wartung werden eingeschlossen, wenn ein Korrekturdatum in der Vergangenheit in der Budgetkalkulation enthalten ist. In diesem Fall werden Korrekturkosten einer früheren Periode für die gleiche zukünftige Periode berechnet, für die Sie das Wartungsbudget berechnen.

## <a name="create-a-maintenance-budget"></a>Erstellen eines Wartungsbudgets

1. Wählen Sie **Anlagenverwaltung** \> **Abfragen** \> **Wartungsbudget** \> **Budget** aus.
2. Wählen Sie **Budget erstellen** aus.
3. Geben Sie im Feld **Wartungsbudget** eine Budgetkennung ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Geben Sie auf dem Inforegister **Periode** in den Feldern **Anfangsdatum** und **Enddatum** das Start- und Enddatum für die Budgetperiode ein.
5. Um korrektive Budgetkosten einzubeziehen, die basierend auf den Istkosten aus einer vorherigen Periode berechnet werden, geben Sie im Feld **Anfangsdatum für Korrektur** das Startdatum der Periode an, ab dem diese Kosten enthalten sein sollen.
6. Je nach der Detailebene, die im Budget erforderlich ist, legen Sie die entsprechenden Optionen in die fünf Inforegistern **Gruppieren nach** fest.
7. Wählen Sie **OK**.
8. Wählen Sie **Budgetpositionen** aus, um die Seite **Wartungsbudgetpositionen** zu öffnen, in der Sie alle Budgetpositionen anzeigen können, die für den Zeitraum erstellt wurden.
9. Um das Budget zu genehmigen, wählen Sie dieses auf der Seite **Wartungsbudgets** aus, und wählen Sie dann **Genehmigen** aus. Im Dialogfeld **Budget genehmigen** wählen Sie **OK** aus. Ihr Name wird im Feld **Genehmigt von** auf der Seite **Wartungsbudgets** eingegeben.

    > [!NOTE]
    > Nachdem Sie ein Wartungsbudget genehmigt haben, können Sie die zugehörigen Positionen der Seite **Wartungsbudgetpositionen** nicht neu berechnen oder anpassen, sofern Sie die Genehmigung nicht zunächst entfernen. Um die Genehmigung eines Wartungsbudgets zu entfernen, wählen Sie dieses auf der Seite **Wartungsbudgets** aus, und wählen Sie dann **Genehmigen** aus. Im Dialogfeld **Budget genehmigen** wählen Sie **OK** aus.

![Wartungsbudgets.](media/01-maintenance-budgets.png)

Sie können auch ein neues Wartungsbudget erstellen, indem Sie ein vorhandenes Budget kopieren. Wählen Sie auf der Seite **Wartungsbudgets** das zu kopierende Budget aus, und wählen Sie dann **Kopieren** aus. Dieser Ansatz ist hilfreich, wenn Sie z. B. ein Budget für einen Monat erstellt haben und dieses in andere Monate kopieren möchten.

> [!NOTE]
> Das Wartungsbudget berechnet nur Budgetkosten auf Grundlage der Wartungsplanpositionen. Um Istkosten für die gleiche Periode zu berechnen, können Sie diese Berechnung auf der Seite **Kostensteuerung für Anlagen** vornehmen. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
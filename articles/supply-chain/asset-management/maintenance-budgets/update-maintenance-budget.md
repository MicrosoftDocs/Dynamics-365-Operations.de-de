---
title: Aktualisierung der Wartungsbudgets
description: In diesem Artikel erfahren Sie, wie Sie ein Instandhaltungsbudget im Anlagenmanagement aktualisieren.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a9333c9ad48c87159ed4071a8b4843fc0e55ceb5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860956"
---
# <a name="update-maintenance-budgets"></a>Aktualisierung der Wartungsbudgets

[!include [banner](../../includes/banner.md)]

 

Auf der Seite **Wartungsbudgetzeilen** werden alle Budgetzeilen angezeigt, die für das Budget angelegt wurden, das auf der Seite **Wartungsbudgets** ausgewählt wurde. (Weitere Informationen finden Sie unter [Wartungsbudgets anlegen](create-maintenance-budget.md).) Sie können Wartungsbudgetpositionen neu berechnen und anpassen, bis das Wartungsbudget genehmigt ist. Nach Ablauf der Budgetperiode und der Buchung von Kosten im Anlagenmanagement können Sie die Budgetpositionen auch mit Istkosten aktualisieren.

## <a name="recalculate-a-maintenance-budget"></a>Neuberechnung eines Wartungsbudgets

Sie können ein Wartungsbudget auf der Seite **Wartungsbudgetzeilen** neu berechnen. Wenn Sie ein Wartungsbudget neu berechnen, werden die vorhandenen Budgetpositionen gelöscht und eine Neuberechnung durchgeführt.

1. Wählen Sie auf der Seite **Wartungsbudgetlinien** **Neu berechnen**.
2. Nehmen Sie im Dialogfenster **Budget neu berechnen** die erforderlichen Änderungen für die neue Kalkulation vor und wählen Sie dann **OK**.

Neue Budgetpositionen werden entsprechend den von Ihnen festgelegten Werten angelegt.

## <a name="adjust-budget-lines"></a>Anpassung der Budgetzeilen

Anstatt das gesamte Wartungsbudget neu zu berechnen, können Sie ausgewählte Zeilen, die sich auf die Budgetkosten beziehen, anpassen.

1. Markieren Sie auf der Seite **Wartungsbudgetlinien** die Zeilen, für die die Budgetkosten aktualisiert werden sollen.
2. Wählen Sie **Anpassen**.
3. Um einen Betrag zu den ausgewählten Zeilen hinzuzufügen, aktivieren Sie das Kontrollkästchen **Kosten hinzufügen**, und geben Sie dann den Wert in das Feld **Wert hinzufügen** ein.
4. Um die Budgetkosten auf den ausgewählten Budgetpositionen mit einem Faktor zu multiplizieren, aktivieren Sie das Kontrollkästchen **Kosten multiplizieren** und geben Sie den Faktor in das Feld **Wert multiplizieren** ein.

    Wenn Sie z.B. **1,2** in das Feld **Multiplizierter Wert** eingeben, erhöhen Sie die Budgetkosten für die ausgewählten Zeilen um 20 Prozent. Wenn Sie **0,7** eingeben, reduzieren Sie die Budgetkosten auf den ausgewählten Zeilen um 30 Prozent.

5. Wählen Sie **OK**.

Die ausgewählten Budgetpositionen werden entsprechend den Werten aktualisiert, die Sie in Schritt 3 oder 4 festgelegt haben.

## <a name="update-actual-costs"></a>Fortschreibung der Istkosten

Nachdem die Termine der Budgetzeilen abgelaufen sind und die Istkosten in der Anlagenbuchhaltung gebucht wurden, können Sie die Istkosten auf dem Wartungsbudget aktualisieren.

1. Wählen Sie auf der Seite **Wartungsbudgetlinien** **Aktualisierungskosten**.
2. Wählen Sie im Dialogfenster **Istkosten berechnen** **OK**.

Die Felder **Istkosten** auf den Budgetzeilen werden aktualisiert, wenn Istkosten gebucht wurden. Neue Budgetpositionen können erzeugt werden, wenn seit der Erstellung des Budgets neue Anlagenarten angelegt wurden und wenn diese Anlagenarten auf Anlagen verwendet wurden, für die Arbeitsaufträge angelegt wurden und für die entsprechende Kosten gebucht wurden. Neue Budgetpositionen zeigen nur die Istkosten an, da für sie keine Budgetkosten berechnet wurden.

> [!NOTE]
> Um eine Übersicht über die Istkosten gegliedert nach Präventions-, Korrektur- und Investitionskosten zu erhalten, können Sie auf der Seite **Assetkostenkontrolle** eine Berechnung für den gleichen Zeitraum durchführen. 

## <a name="manually-add-budget-lines"></a>Budgetpositionen manuell hinzufügen

Auf der Seite **Wartungsbudgetlinien** können Sie manuell eine neue Budgetposition hinzufügen, indem Sie **Neu** auswählen und dann auf der Position auswählen. Hier sind einige Beispiele für Situationen, in denen dieser Ansatz nützlich sein könnte:

- Sie wissen, dass sich die Renovierung einiger Anlagen derzeit in der Planungsphase befindet, aber damit verbundene Arbeitsplätze im Asset Management noch nicht geschaffen wurden. Sie möchten jedoch, dass die Budgetkosten für diese Stellen in das Wartungsbudget aufgenommen werden.
- Neue Anlagen oder Anlagenarten wurden seit der Erstellung des Wartungsbudgets angelegt, aber für diese Anlagen oder Anlagenarten wurden noch keine Wartungspläne eingerichtet. Sie möchten jedoch, dass die Budgetkosten für diese Anlagenarten in das Wartungsbudget aufgenommen werden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
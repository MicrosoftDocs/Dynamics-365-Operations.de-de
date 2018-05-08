---
title: Positionsbudgetierung-Problembehebung
description: "Diesee Artikel enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Positionsbudgetierung konfigurieren. Es adressiert häufig gestellten Fragen, wie Budgetkostenelemente, Vergütungsgruppen und Kompensationsraster."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f2ef04008a5e6339a2193f9fcc77f2e0e6643557
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="position-budgeting-troubleshooting"></a>Positionsbudgetierung-Problembehebung

[!include [banner](../includes/banner.md)]

Diesee Artikel enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Positionsbudgetierung konfigurieren. Es adressiert häufig gestellten Fragen, wie Budgetkostenelemente, Vergütungsgruppen und Kompensationsraster. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Warum kann ich die Planungspositionsseite in der Personalverwaltung nicht finden?
---------------------------------------------------------------

Planungspositionen wurden in die Budgetierung verschoben.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Warum kann ich einBudgetkostenelement nicht löschen?
Sie können ein Budgetkostenelement nicht löschen, das einer Prognoseposition zugewiesen ist. Bevor Sie ein Budgetkostenelement löschen können, müssen Sie es aus allen Planungspositionen entfernen. **Tipp:** Um alle Positionen, die einem Budgetkostenelement zugeordnet sind, zu suchen, wählen Sie das Kostenelement auf der Seite **Budgetkostenelemente** aus, und klicken Sie anschließend auf **Positionen aktualisieren**. Die Positionen, die das Kostenelement verwenden, werden im oberen Raster aufgeführt.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Wie kann ich ein Kostenelement aus mehreren Planungspositionen entfernen, ohne jede einzelne zu öffnen?
Sie können einen Kostenelement nicht entfernen. Wenn Sie aber das Start- und Enddatum ändern, sodass sie außerhalb der Datumsangaben des Budgetplanungszyklus liegen, sind sie nicht mehr den Planungspositionen in diesem Budgetplanungszyklus zugewiesen. Um diese Änderung vorzunehmen, öffnen Sie das Budgetkostenelement, klicken dann auf dem Inforegister **Kostenberechnung** auf **Datum ändern** und ändern das Gültigkeits- oder das Ablaufdatum. Dann klicken Sie auf **OK**, um alle Planungspositionen, die dem Kostenelement zugewiesen sind, automatisch zu aktualisieren. **Tipp:** Wenn Sie diese Methode verwenden, beachten Sie, dass das Budgetkostenelement aus **allen** Prognosepositionen entfernt wird, in denen das Start- und Enddatum nicht mehr innerhalb des entsprechenden Bereichs liegen. Wenn dies nicht das ist, was Sie beabsichtigen, müssen Sie jede Planungsposition öffnen, aus der Sie das Budgetkostenelement entfernen möchten und die Änderung manuell vornehmen.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Warum kann ich für das Budgetkostenelement keinen jährlichen Betrag in das Inforegister der Kostenberechnung eingeben?
Sie können keinen jährlichen Betrag eingeben, wenn Budgetkostenelemente im Inforegister **Berechnungsbasis** vorhanden sind, da das System einen Prozentsatz erfordert, um den Wert zu berechnen. Um diesen Wert zu ändern, entfernen Sie alle Budgetkostenelemente aus dem Inforegister **Berechnungsbasis**.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Warum kann ich den Budgetkostentyp nicht von "Einkünfte" in einen anderen Budgetkostentyp ändern?
Einige Budgetkostenelemente verwenden das Einkünftekostenelement als Berechnungsbasis. Um das Feld **Budgetkostentyp** zu ändern, entfernen Sie den Einkünftekostenelement aus dem Inforegister **Berechnungsbasis** aller Budgetkostenelemente.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Warum kann ich das Datum auf Positionen des Budgetkostenelements für ein Budgetkostenelement nicht ändern?
Sie können das Datum in einer Position eines Budgetkostenelements nicht ändern, wenn ein Budgetkostenelement von einer Planungsposition verwendet wird. Diese Einschränkung stellt sicher, dass die Planungspositionen immer innerhalb der Richtlinien des Budgetkostenelements sind. Um das Datum zu ändern, klicken Sie im Inforegister **Kostenberechnung** auf, ändern **Datum ändern** und geben das neue Datum ein. Dann klicken Sie auf **OK**, um alle Positionen, die dem Kostenelement zugewiesen sind, automatisch zu aktualisieren.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Warum kann ich die Kosten für ein Budgetkostenelement auf der Seite "Vergütungsgruppe" nicht ändern?
Sie können Budgetkostenelemente nur auf der Seite **Budgetkostenelemente** erstellen und ändern.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Warum erhalte ich eine Fehlermeldung, wenn ich die Datumsangaben für ein Kostenelement in einer Planungsposition ändere?
Die Datumsangaben in der Kostenelementposition der Planungsposition müssen innerhalb der folgenden Bereiche liegen:

-   Das Aktivierungs- und Deaktivierungsdatum der Position.
-   DasAktivierungs- und Deaktivierungsdatum des Budgetkostenelements.
-   Start- und Enddatum des Budgetzyklus, der dem Budgetplanungsprozess der Planungsposition zugeordnet ist.






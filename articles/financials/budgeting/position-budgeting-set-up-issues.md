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

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="81b69-104">Positionsbudgetierung-Problembehebung</span><span class="sxs-lookup"><span data-stu-id="81b69-104">Position budgeting troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="81b69-105">Diesee Artikel enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Positionsbudgetierung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="81b69-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="81b69-106">Es adressiert häufig gestellten Fragen, wie Budgetkostenelemente, Vergütungsgruppen und Kompensationsraster.</span><span class="sxs-lookup"><span data-stu-id="81b69-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="81b69-107">Warum kann ich die Planungspositionsseite in der Personalverwaltung nicht finden?</span><span class="sxs-lookup"><span data-stu-id="81b69-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="81b69-108">Planungspositionen wurden in die Budgetierung verschoben.</span><span class="sxs-lookup"><span data-stu-id="81b69-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="81b69-109">Warum kann ich einBudgetkostenelement nicht löschen?</span><span class="sxs-lookup"><span data-stu-id="81b69-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="81b69-110">Sie können ein Budgetkostenelement nicht löschen, das einer Prognoseposition zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="81b69-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="81b69-111">Bevor Sie ein Budgetkostenelement löschen können, müssen Sie es aus allen Planungspositionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="81b69-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="81b69-112">**Tipp:** Um alle Positionen, die einem Budgetkostenelement zugeordnet sind, zu suchen, wählen Sie das Kostenelement auf der Seite **Budgetkostenelemente** aus, und klicken Sie anschließend auf **Positionen aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="81b69-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="81b69-113">Die Positionen, die das Kostenelement verwenden, werden im oberen Raster aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="81b69-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="81b69-114">Wie kann ich ein Kostenelement aus mehreren Planungspositionen entfernen, ohne jede einzelne zu öffnen?</span><span class="sxs-lookup"><span data-stu-id="81b69-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="81b69-115">Sie können einen Kostenelement nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="81b69-115">You can’t remove a cost element.</span></span> <span data-ttu-id="81b69-116">Wenn Sie aber das Start- und Enddatum ändern, sodass sie außerhalb der Datumsangaben des Budgetplanungszyklus liegen, sind sie nicht mehr den Planungspositionen in diesem Budgetplanungszyklus zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="81b69-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="81b69-117">Um diese Änderung vorzunehmen, öffnen Sie das Budgetkostenelement, klicken dann auf dem Inforegister **Kostenberechnung** auf **Datum ändern** und ändern das Gültigkeits- oder das Ablaufdatum.</span><span class="sxs-lookup"><span data-stu-id="81b69-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="81b69-118">Dann klicken Sie auf **OK**, um alle Planungspositionen, die dem Kostenelement zugewiesen sind, automatisch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="81b69-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="81b69-119">**Tipp:** Wenn Sie diese Methode verwenden, beachten Sie, dass das Budgetkostenelement aus **allen** Prognosepositionen entfernt wird, in denen das Start- und Enddatum nicht mehr innerhalb des entsprechenden Bereichs liegen.</span><span class="sxs-lookup"><span data-stu-id="81b69-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="81b69-120">Wenn dies nicht das ist, was Sie beabsichtigen, müssen Sie jede Planungsposition öffnen, aus der Sie das Budgetkostenelement entfernen möchten und die Änderung manuell vornehmen.</span><span class="sxs-lookup"><span data-stu-id="81b69-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="81b69-121">Warum kann ich für das Budgetkostenelement keinen jährlichen Betrag in das Inforegister der Kostenberechnung eingeben?</span><span class="sxs-lookup"><span data-stu-id="81b69-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="81b69-122">Sie können keinen jährlichen Betrag eingeben, wenn Budgetkostenelemente im Inforegister **Berechnungsbasis** vorhanden sind, da das System einen Prozentsatz erfordert, um den Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="81b69-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="81b69-123">Um diesen Wert zu ändern, entfernen Sie alle Budgetkostenelemente aus dem Inforegister **Berechnungsbasis**.</span><span class="sxs-lookup"><span data-stu-id="81b69-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="81b69-124">Warum kann ich den Budgetkostentyp nicht von "Einkünfte" in einen anderen Budgetkostentyp ändern?</span><span class="sxs-lookup"><span data-stu-id="81b69-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="81b69-125">Einige Budgetkostenelemente verwenden das Einkünftekostenelement als Berechnungsbasis.</span><span class="sxs-lookup"><span data-stu-id="81b69-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="81b69-126">Um das Feld **Budgetkostentyp** zu ändern, entfernen Sie den Einkünftekostenelement aus dem Inforegister **Berechnungsbasis** aller Budgetkostenelemente.</span><span class="sxs-lookup"><span data-stu-id="81b69-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="81b69-127">Warum kann ich das Datum auf Positionen des Budgetkostenelements für ein Budgetkostenelement nicht ändern?</span><span class="sxs-lookup"><span data-stu-id="81b69-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="81b69-128">Sie können das Datum in einer Position eines Budgetkostenelements nicht ändern, wenn ein Budgetkostenelement von einer Planungsposition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81b69-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="81b69-129">Diese Einschränkung stellt sicher, dass die Planungspositionen immer innerhalb der Richtlinien des Budgetkostenelements sind.</span><span class="sxs-lookup"><span data-stu-id="81b69-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="81b69-130">Um das Datum zu ändern, klicken Sie im Inforegister **Kostenberechnung** auf, ändern **Datum ändern** und geben das neue Datum ein.</span><span class="sxs-lookup"><span data-stu-id="81b69-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="81b69-131">Dann klicken Sie auf **OK**, um alle Positionen, die dem Kostenelement zugewiesen sind, automatisch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="81b69-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="81b69-132">Warum kann ich die Kosten für ein Budgetkostenelement auf der Seite "Vergütungsgruppe" nicht ändern?</span><span class="sxs-lookup"><span data-stu-id="81b69-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="81b69-133">Sie können Budgetkostenelemente nur auf der Seite **Budgetkostenelemente** erstellen und ändern.</span><span class="sxs-lookup"><span data-stu-id="81b69-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="81b69-134">Warum erhalte ich eine Fehlermeldung, wenn ich die Datumsangaben für ein Kostenelement in einer Planungsposition ändere?</span><span class="sxs-lookup"><span data-stu-id="81b69-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="81b69-135">Die Datumsangaben in der Kostenelementposition der Planungsposition müssen innerhalb der folgenden Bereiche liegen:</span><span class="sxs-lookup"><span data-stu-id="81b69-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="81b69-136">Das Aktivierungs- und Deaktivierungsdatum der Position.</span><span class="sxs-lookup"><span data-stu-id="81b69-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="81b69-137">DasAktivierungs- und Deaktivierungsdatum des Budgetkostenelements.</span><span class="sxs-lookup"><span data-stu-id="81b69-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="81b69-138">Start- und Enddatum des Budgetzyklus, der dem Budgetplanungsprozess der Planungsposition zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81b69-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>






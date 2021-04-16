---
title: Kanban-Mengenvorschläge berechnen
description: Der Schwerpunkt dieser Prozedur liegt auf dem Optimieren der Kanban-Größe und -Menge für eine bestimmte Kanban-Regel mit der Kanban-Mengenberechnung.
author: ChristianRytt
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93845129e057b8729e676123967efefb6bca66f2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829329"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="4d964-103">Kanban-Mengenvorschläge berechnen</span><span class="sxs-lookup"><span data-stu-id="4d964-103">Calculate kanban quantity suggestions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d964-104">Der Schwerpunkt dieser Prozedur liegt auf dem Optimieren der Kanban-Größe und -Menge für eine bestimmte Kanban-Regel mit der Kanban-Mengenberechnung.</span><span class="sxs-lookup"><span data-stu-id="4d964-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="4d964-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4d964-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4d964-106">Diese Vorgehensweise ist für den Wertstrommanager vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4d964-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="4d964-107">Für dieses Verfahren wird vorausgesetzt, dass Sie die Prozedur "Kanban-Berechnungsrichtlinie zur Kanban-Regel hinzufügen" abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="4d964-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="4d964-108">Kanban-Mengenberechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="4d964-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="4d964-109">Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Kanban-Menge berechnen".</span><span class="sxs-lookup"><span data-stu-id="4d964-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="4d964-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4d964-110">Click New.</span></span>
3. <span data-ttu-id="4d964-111">Geben Sie im Feld "Name" "Speaker2016" ein.</span><span class="sxs-lookup"><span data-stu-id="4d964-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="4d964-112">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4d964-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4d964-113">Wählen Sie die Richtlinie aus, die Sie in der Prozedur "Kanban-Berechnungsrichtlinie zur Kanban-Regel hinzufügen" erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4d964-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="4d964-114">Beispielsweise "Speaker2016".</span><span class="sxs-lookup"><span data-stu-id="4d964-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="4d964-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4d964-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4d964-116">Legen Sie im Feld "Stichdatum zur Auswahl von Kanban-Regeln" Datum und Uhrzeit auf "2012-12-17T08:00:00" fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="4d964-117">Anhand dieses Datums wird ermittelt, welche festen Kanban-Regeln in die Kanban-Mengenberechnung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4d964-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="4d964-118">Legen Sie im Feld "Gedeckter Bedarf - Periodenstartdatum" Datum und Uhrzeit auf "2012-11-17T09:00:00" fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="4d964-119">Das Datum, ab dem Buchungen in Bezug auf den Bedarf in der Vergangenheit in die Kanban-Mengenberechnung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4d964-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="4d964-120">Legen Sie im Feld "Gedeckter Bedarf - Periodenenddatum" Datum und Uhrzeit auf "2012-12-17T07:59:59" fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="4d964-121">Das Datum, bis zu dem Buchungen in Bezug auf den Bedarf in der Vergangenheit in die Kanban-Mengenberechnung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4d964-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="4d964-122">Legen Sie im Feld "Bedarf - Periodenstartdatum" Datum und Uhrzeit auf "2012-12-17T08:00:00" fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="4d964-123">Das Datum, ab dem Buchungen in Bezug auf den aktuellen Bedarf in die Kanban-Mengenberechnung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4d964-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="4d964-124">Legen Sie im Feld "Bedarf - Periodenenddatum" Datum und Uhrzeit auf "2013-01-16T07:59:59" fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="4d964-125">Das Datum, bis zu dem Buchungen in Bezug auf den aktuellen Bedarf in die Kanban-Mengenberechnung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4d964-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="4d964-126">Kanban-Mengenvorschlag generieren</span><span class="sxs-lookup"><span data-stu-id="4d964-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="4d964-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4d964-127">Click Save.</span></span>
2. <span data-ttu-id="4d964-128">Klicken Sie "Generieren".</span><span class="sxs-lookup"><span data-stu-id="4d964-128">Click Generate.</span></span>
    * <span data-ttu-id="4d964-129">Dadurch wird eine Kanban-Mengenvorschlagsposition für die Kanban-Regel 000020 generiert.</span><span class="sxs-lookup"><span data-stu-id="4d964-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="4d964-130">Kanban-Mengenberechnung ausführen</span><span class="sxs-lookup"><span data-stu-id="4d964-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="4d964-131">Klicken Sie auf "Berechnen".</span><span class="sxs-lookup"><span data-stu-id="4d964-131">Click Calculate.</span></span>
    * <span data-ttu-id="4d964-132">Dies berechnet den Kanban-Mengenvorschlag.</span><span class="sxs-lookup"><span data-stu-id="4d964-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="4d964-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d964-133">Click OK.</span></span>
3. <span data-ttu-id="4d964-134">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4d964-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4d964-135">Beachten Sie, dass vorgeschlagene Kanban-Menge 2 ist.</span><span class="sxs-lookup"><span data-stu-id="4d964-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="4d964-136">Produktmenge ändern und erneut berechnen</span><span class="sxs-lookup"><span data-stu-id="4d964-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="4d964-137">Legen Sie "Produktmenge" auf '5' fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="4d964-138">Klicken Sie auf "Berechnen".</span><span class="sxs-lookup"><span data-stu-id="4d964-138">Click Calculate.</span></span>
3. <span data-ttu-id="4d964-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d964-139">Click OK.</span></span>
    * <span data-ttu-id="4d964-140">Beachten Sie, dass bei einer Kanban-Menge von 5, der Vorschlag zu einer Kanban-Menge von 4 geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4d964-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="4d964-141">Dies wird durch dadurch verursacht, dass mit einer niedrigeren Produktmenge, mehr Kanbans erforderlich sind, um den Bedarf zu decken.</span><span class="sxs-lookup"><span data-stu-id="4d964-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="4d964-142">Kanban-Regel aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4d964-142">Update kanban rule</span></span>
1. <span data-ttu-id="4d964-143">Geben Sie im Feld "Gültigkeitsdatum der Regeln" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="4d964-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="4d964-144">Legen Sie die "Datum, ab dem die Regel aktiv wird" auf ein Datum in der Zukunft fest.</span><span class="sxs-lookup"><span data-stu-id="4d964-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="4d964-145">Beispielsweise heute + ein Jahr.</span><span class="sxs-lookup"><span data-stu-id="4d964-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="4d964-146">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4d964-146">Click Update.</span></span>
3. <span data-ttu-id="4d964-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d964-147">Click OK.</span></span>
4. <span data-ttu-id="4d964-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4d964-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="4d964-149">Änderung der Kanban-Regel überprüfen</span><span class="sxs-lookup"><span data-stu-id="4d964-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="4d964-150">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="4d964-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="4d964-151">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4d964-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4d964-152">Wählen Sie die Kanban-Regel aus, die in der vorherigen Unteraufgabe erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4d964-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="4d964-153">Diese sollte die erste Kanban-Regel in der nach Nummern sortierten Liste sein.</span><span class="sxs-lookup"><span data-stu-id="4d964-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="4d964-154">Schalten Sie die Erweiterung des Abschnitts "Details" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="4d964-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="4d964-155">Beachten Sie das Gültigkeitsdatum, das anzeigt, dass diese Regel bis zu diesem Datum nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4d964-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="4d964-156">Schalten Sie die Erweiterung des Abschnitts "Mengen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="4d964-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="4d964-157">Beachten Sie, dass dies die Standardmenge ist, die Sie in der Kanban-Mengenberechnung eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="4d964-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="4d964-158">Beachten Sie, dass dies die feste Kanban-Menge von 4 aus der Kanban-Mengenberechnung ist.</span><span class="sxs-lookup"><span data-stu-id="4d964-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="4d964-159">Klicken Sie auf die Registerkarte "ListPanel".</span><span class="sxs-lookup"><span data-stu-id="4d964-159">Click the ListPanel tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
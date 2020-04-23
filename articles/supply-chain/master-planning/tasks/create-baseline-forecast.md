---
title: Grundplanung erstellen
description: Ein Produktionsplaner kann eine Grundplanung erstellen, indem er entweder Zeitserien-Planungsmodelle verwendet oder indem er den historischen Bedarf in die Planung kopiert.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ea5e269f9216fa1dfcaa4377beb7ef52ef153b5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209719"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="0d249-103">Grundplanung erstellen</span><span class="sxs-lookup"><span data-stu-id="0d249-103">Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d249-104">Ein Produktionsplaner kann eine Grundplanung erstellen, indem er entweder Zeitserien-Planungsmodelle verwendet oder indem er den historischen Bedarf in die Planung kopiert.</span><span class="sxs-lookup"><span data-stu-id="0d249-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="0d249-105">In diesem Verfahren wird dargestellt, wie Sie den historischen Bedarf zur Erstellung einer Grundplanung für alle Produkte mit einem Artikelverteilungsschlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d249-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="0d249-106">Einrichten eines Artikelverteilungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="0d249-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="0d249-107">Wechseln Sie zu Masterplan > Einrichten >Intercompany-Planungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="0d249-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="0d249-108">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0d249-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0d249-109">Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".</span><span class="sxs-lookup"><span data-stu-id="0d249-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="0d249-110">Bedarfsplanungsausführungen zu juristischen Personen.</span><span class="sxs-lookup"><span data-stu-id="0d249-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="0d249-111">Daher müssen Sie alle Unternehmen einrichten, für die Sie Planungen in einer unternehmensübergreifenden Planungsgruppe generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0d249-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="0d249-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0d249-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0d249-113">Klicken Sie auf "Artikelzuteilungsschlüssel".</span><span class="sxs-lookup"><span data-stu-id="0d249-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="0d249-114">Wählen Sie alle Artikelverteilungsschlüssel aus, für die Sie Planungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d249-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="0d249-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0d249-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0d249-116">Wählen Sie den D_Aloc-Artikelverteilungsschlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="0d249-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="0d249-117">Klicken >.</span><span class="sxs-lookup"><span data-stu-id="0d249-117">Click >.</span></span>
7. <span data-ttu-id="0d249-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d249-118">Close the page.</span></span>
8. <span data-ttu-id="0d249-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d249-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="0d249-120">Bedarfsplanungsparameter einrichten</span><span class="sxs-lookup"><span data-stu-id="0d249-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="0d249-121">Wechseln Sie zu "Masterplan" > "Einrichten" > "Bedarfsplanung" > "Bedarfsplanungsparameter".</span><span class="sxs-lookup"><span data-stu-id="0d249-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="0d249-122">Erweitern Sie den Planungsalgorithmusparameter-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="0d249-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="0d249-123">Wählen Sie im Feld "Planungsgenerierungsstrategie" "Über historischen Bedarf kopieren" aus.</span><span class="sxs-lookup"><span data-stu-id="0d249-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="0d249-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0d249-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="0d249-125">Grundplanung erstellen</span><span class="sxs-lookup"><span data-stu-id="0d249-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="0d249-126">Wechseln Sie zu Masterplan > Planung > Bedarfsplanung > Statistische Grundplanung generieren.</span><span class="sxs-lookup"><span data-stu-id="0d249-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="0d249-127">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="0d249-128">Wenn Aufträge ab dem 1. Januar 2015 vorliegen, geben Sie dieses Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="0d249-129">Falls nicht, geben Sie das früheste Datum Ihrer Aufträge ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="0d249-130">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0d249-131">Geben Sie das letzte Datum Ihrer Aufträge ein, beispielsweise "31.03.2015".</span><span class="sxs-lookup"><span data-stu-id="0d249-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="0d249-132">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="0d249-133">Geben Sie "01.04.2015" ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="0d249-134">Dieses Datum wird automatisch als Startdatum des folgenden Planungszeitrahmens berechnet.</span><span class="sxs-lookup"><span data-stu-id="0d249-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="0d249-135">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="0d249-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="0d249-136">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="0d249-136">Click Filter.</span></span>
7. <span data-ttu-id="0d249-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0d249-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0d249-138">Markieren Sie die Zeile mit Feld = Intercompany-Planungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0d249-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="0d249-139">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0d249-140">Geben Sie die Intercompany-Planungsgruppe ein (z. B. 10), die Sie in der ersten Aufgabe verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="0d249-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="0d249-141">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0d249-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0d249-142">Wählen Sie die Zeile aus mit Feld = Artikelzuteilungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="0d249-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="0d249-143">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="0d249-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0d249-144">Click OK.</span></span>
12. <span data-ttu-id="0d249-145">Erweitern Sie den Abschnitt "Erweiterte Parameter".</span><span class="sxs-lookup"><span data-stu-id="0d249-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="0d249-146">Wählen Sie im Feld "Planungszeitrahmen" die Option "Monat" aus.</span><span class="sxs-lookup"><span data-stu-id="0d249-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="0d249-147">Geben Sie im Feld "Planungshorizont" eine "3" ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="0d249-148">Geben Sie im Feld "Nichtplanungszeitraum" den Wert "1" ein.</span><span class="sxs-lookup"><span data-stu-id="0d249-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="0d249-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0d249-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="0d249-150">Visualisieren der Bedarfsplanung</span><span class="sxs-lookup"><span data-stu-id="0d249-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="0d249-151">Wechseln Sie zu >Masterplan > Planung > Bedarfsplanung > Angepasste Bedarfsplanung".</span><span class="sxs-lookup"><span data-stu-id="0d249-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="0d249-152">Wählen Sie in der Tabelle "AggregatedViewTable" die Zelle in Zeile "1", Spalte "2" aus.</span><span class="sxs-lookup"><span data-stu-id="0d249-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="0d249-153">Dies ist der zweiten Monat, für den Sie die Planung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="0d249-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="0d249-154">Legen Sie QtyCell auf "400" fest.</span><span class="sxs-lookup"><span data-stu-id="0d249-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="0d249-155">Geben Sie in der Zelle eine andere Anzahl als das Ergebnis der Planung an, z. B. 400.</span><span class="sxs-lookup"><span data-stu-id="0d249-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="0d249-156">Sie haben eine manuelle Regulierung der Planung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="0d249-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="0d249-157">Beachten Sie die grafische Anzeige im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="0d249-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="0d249-158">Klicken Sie auf "Details für Planungspositionen".</span><span class="sxs-lookup"><span data-stu-id="0d249-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="0d249-159">Auf dieser Seite können Sie die Genauigkeitswerte, den historischen Bedarf und die Planung finden.</span><span class="sxs-lookup"><span data-stu-id="0d249-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="0d249-160">Sie können auch Änderungen an der Planung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0d249-160">You can make changes to the forecast as well.</span></span>  


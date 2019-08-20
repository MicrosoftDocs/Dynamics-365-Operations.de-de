---
title: Reihenfolge der Produktions-Einzelvorgänge für Prozessfertigung
description: Bei dieser Prozedur werden Farbenprodukte als Beispiel verwendet, um anzuzeigen, wie Bestellvorschläge gemäß der Priorität von Farbe und Verpackungsgröße nacheinander geordnet werden.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e7cf6adc5c72494d6a9a72765a3d165424c72b2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835825"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="64fbe-103">Reihenfolge der Produktions-Einzelvorgänge für Prozessfertigung</span><span class="sxs-lookup"><span data-stu-id="64fbe-103">Sequence production jobs for process manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64fbe-104">Bei dieser Prozedur werden Farbenprodukte als Beispiel verwendet, um anzuzeigen, wie Bestellvorschläge gemäß der Priorität von Farbe und Verpackungsgröße nacheinander geordnet werden.</span><span class="sxs-lookup"><span data-stu-id="64fbe-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="64fbe-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USPI.</span><span class="sxs-lookup"><span data-stu-id="64fbe-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="64fbe-106">Diese Prozedur ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="64fbe-107">Führen Sie den Produktprogrammplan für USPI aus</span><span class="sxs-lookup"><span data-stu-id="64fbe-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="64fbe-108">Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Ausführen" > "Produktprogrammplan".</span><span class="sxs-lookup"><span data-stu-id="64fbe-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="64fbe-109">Klicken Sie im Feld "Produktprogrammplan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="64fbe-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="64fbe-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="64fbe-111">Wählen Sie "MasterPlan" aus.</span><span class="sxs-lookup"><span data-stu-id="64fbe-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="64fbe-112">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="64fbe-112">Click OK.</span></span>
    * <span data-ttu-id="64fbe-113">Dadurch wird der Produktprogrammplan gestartet, einschließlich des Sequenzprozesses.</span><span class="sxs-lookup"><span data-stu-id="64fbe-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="64fbe-114">Dieser Prozess kann einige Minuten in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="64fbe-115">Zeigen Sie Bestellvorschläge für die Farbenprodukte an</span><span class="sxs-lookup"><span data-stu-id="64fbe-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="64fbe-116">Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="64fbe-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="64fbe-117">Erweitern Sie die Infobox "Artikeldetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="64fbe-118">Erweitern Sie die Infobox "Zeitplandetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="64fbe-119">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="64fbe-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="64fbe-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="64fbe-121">Wählen Sie "MasterPlan" aus.</span><span class="sxs-lookup"><span data-stu-id="64fbe-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="64fbe-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="64fbe-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="64fbe-123">Verwenden Sie den Schnellfilter, um im Feld "Artikelnummer" nach dem Wert "P300" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="64fbe-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="64fbe-124">Heben Sie die Sperrung auf, um einen Bildlauf nach rechts durchzuführen, um das Auftragsdatum und das Lieferdatum anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="64fbe-125">Beachten Sie, dass diese Artikel als Auftragsdatum "Heute" haben und die Lieferdaten für die Bestellvorschläge folgen nicht aufeinander nach Priorität von Farbe und Paketgröße, wie im Produktname angezeigt.</span><span class="sxs-lookup"><span data-stu-id="64fbe-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="64fbe-126">Sie können auf eine Artikelnummer zeigen, um den Produktname und die Priorität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="64fbe-127">Ordnen Sie Bestellvorschläge für Farbe der Reihe nach ein</span><span class="sxs-lookup"><span data-stu-id="64fbe-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="64fbe-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="64fbe-128">Close the page.</span></span>
2. <span data-ttu-id="64fbe-129">Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Sequenzierte Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="64fbe-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="64fbe-130">Erweitern Sie die Infobox "Artikeldetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="64fbe-131">Erweitern Sie die Infobox "Zeitplandetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="64fbe-132">Hinweis: Hier sehen Sie, dass das Startdatum/die Startuhrzeit für die Bestellvorschläge gemäß Farbe und Paketgröße innerhalb einer Periode für den Zeitraum von 28 Tagen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="64fbe-133">Diese Perioden werden durch eine Nummer im Feld "Kampagne" definiert.</span><span class="sxs-lookup"><span data-stu-id="64fbe-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="64fbe-134">Das Formular für sequenzierte Bestellvorschläge fungiert als Standardformular für Bestellvorschläge und der Produktionsplaner kann hier die Bestellvorschläge umwandeln.</span><span class="sxs-lookup"><span data-stu-id="64fbe-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="64fbe-135">Markieren Sie alle Zeilen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-135">Mark all rows.</span></span>
6. <span data-ttu-id="64fbe-136">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="64fbe-136">Click Accept.</span></span>
    * <span data-ttu-id="64fbe-137">Dadurch werden die Bestellvorschläge mit der ausgewählten Sequenzaktion, entweder "Verschieben" oder "Vorziehen", aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="64fbe-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="64fbe-138">Überprüfen Sie die Reihenfolge der Bestellvorschläge</span><span class="sxs-lookup"><span data-stu-id="64fbe-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="64fbe-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="64fbe-139">Close the page.</span></span>
2. <span data-ttu-id="64fbe-140">Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="64fbe-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="64fbe-141">Erweitern Sie die Infobox "Artikeldetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="64fbe-142">Erweitern Sie die Infobox "Zeitplandetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="64fbe-143">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="64fbe-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="64fbe-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="64fbe-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="64fbe-145">Wählen Sie "MasterPlan" aus.</span><span class="sxs-lookup"><span data-stu-id="64fbe-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="64fbe-146">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="64fbe-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="64fbe-147">Verwenden Sie den Schnellfilter, um im Feld "Artikelnummer" nach dem Wert "P300" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="64fbe-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="64fbe-148">Beachten Sie, dass die Aufträge nun entsprechend der Priorität von Farbe und Größe aufeinander folgen und die Bestellvorschläge beginnen mit dem frühesten Auftragsdatum und Lieferdatum.</span><span class="sxs-lookup"><span data-stu-id="64fbe-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="64fbe-149">Überprüfen Sie die Spalte "Auftragsdatum" oder "Startdatum" in der Infobox "Planungsdetails".</span><span class="sxs-lookup"><span data-stu-id="64fbe-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  


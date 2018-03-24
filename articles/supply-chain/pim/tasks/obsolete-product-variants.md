--- 
title: Suchen von veralteten Produktvarianten
description: Diese Prozedur zeigt, wie Sie veraltete freigegebene Produkte oder Produktvarianten finden und wie Sie den veralteten Produkten einen Produktlebenszyklus-Status zuordnen.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: de-de
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="d4194-103">Suchen von veralteten Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="d4194-103">Find obsolete product variants</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4194-104">Diese Prozedur zeigt, wie Sie veraltete freigegebene Produkte oder Produktvarianten finden und wie Sie den veralteten Produkten einen Produktlebenszyklus-Status zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d4194-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="d4194-105">Voraussetzung: Sie müssen mindestens ein Produktlebenszyklus-Status definieren, der für die Planung inaktiv ist, bevor Sie dieses Aufgabenleitfaden wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="d4194-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="d4194-106">Eine Simulation ausführen</span><span class="sxs-lookup"><span data-stu-id="d4194-106">Run a simulation</span></span>
1. <span data-ttu-id="d4194-107">Wechseln Sie zu „Produktinformationsverwaltung > Periodische Aufgaben >Lebenszyklusstatus für veraltete Produkte ändern.</span><span class="sxs-lookup"><span data-stu-id="d4194-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="d4194-108">Geben Sie im Feld „Neuer Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4194-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="d4194-109">Wählen Sie „Ja” im Feld „Simulation ausführen, ohne Produktdaten zu aktualisieren” aus.</span><span class="sxs-lookup"><span data-stu-id="d4194-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="d4194-110">Geben Sie im Feld „Innerhalb dieser Zahl von Tagen erstellte Produkte ausschließen” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d4194-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="d4194-111">Geben Sie im Feld „Produkte ausschließen, die in Transaktionen verwendet werden (in Anzahl von Tagen)” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d4194-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="d4194-112">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="d4194-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d4194-113">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="d4194-113">Click Filter.</span></span>
8. <span data-ttu-id="d4194-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d4194-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d4194-115">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4194-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="d4194-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4194-116">Click OK.</span></span>
11. <span data-ttu-id="d4194-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4194-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="d4194-118">Es wird empfohlen, die Simulation in einer Charge auszuführen, wenn Sie erwarten, eine große Anzahl von Produkten zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="d4194-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="d4194-119">Stellen Sie außerdem sicher, dass die Simulation nicht während der aktivsten Arbeitszeit des Unternehmens ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4194-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="d4194-120">Die Simulationsergebnisse überprüfen</span><span class="sxs-lookup"><span data-stu-id="d4194-120">Review the simulation results</span></span>
1. <span data-ttu-id="d4194-121">Wechseln Sie zu Produktinformationsverwaltung > Abfragen und Berichte > Wartungsverlauf des Produktlebenszyklus-Status.</span><span class="sxs-lookup"><span data-stu-id="d4194-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="d4194-122">Auf dieser Seite können Sie die Simulationsergebnisse überprüfen und eine Bewertung dazu vornehmen, wie viele Produkte und Produktvarianten einem neuen Produktlebenszyklus-Status zugeordnet werden, wenn das Update ohne Simulation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4194-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="d4194-123">Das Update des Produktlebenszyklus-Status für veraltete Produkte ausführen</span><span class="sxs-lookup"><span data-stu-id="d4194-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="d4194-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4194-124">Close the page.</span></span>
2. <span data-ttu-id="d4194-125">Wechseln Sie zu „Produktinformationsverwaltung > Periodische Aufgaben >Lebenszyklusstatus für veraltete Produkte ändern.</span><span class="sxs-lookup"><span data-stu-id="d4194-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="d4194-126">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="d4194-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="d4194-127">Beachten Sie, dass die letzte Auswahl gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4194-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="d4194-128">Wählen Sie „Nein” im Feld „Simulation ausführen, ohne Produktdaten zu aktualisieren” aus.</span><span class="sxs-lookup"><span data-stu-id="d4194-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="d4194-129">Erweitern Sie den Abschnitt "Ausführen im Hintergrund".</span><span class="sxs-lookup"><span data-stu-id="d4194-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="d4194-130">Abhängig davon, wie viele Produkte und Produktvarianten betroffen sind, sollten Sie erwägen, diesen Einzelvorgang in einer Charge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4194-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="d4194-131">Stellen Sie sicher, dass Sie keinen großen Aktualisierungseinzelvorgang während der aktivsten Arbeitsstunden im Unternehmen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4194-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="d4194-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4194-132">Click OK.</span></span>
7. <span data-ttu-id="d4194-133">Wechseln Sie zu Produktinformationsverwaltung > Abfragen und Berichte > Wartungsverlauf des Produktlebenszyklus-Status.</span><span class="sxs-lookup"><span data-stu-id="d4194-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="d4194-134">Überprüfen Sie die geänderten freigegebenen Produkte und Produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="d4194-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="d4194-135">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d4194-135">In the list, find and select the desired record.</span></span>


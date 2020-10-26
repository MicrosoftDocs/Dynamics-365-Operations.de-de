---
title: Chargenauftragslebenszyklus von der Erstellung bis zum Start
description: Diese Prozedur führt Sie durch den ersten Teils des Lebenszyklus eines Chargenauftrags.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e57cd9254185b73f544e8ff4f7658cf743b672f2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981303"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="dcd7a-103">Chargenauftragslebenszyklus von der Erstellung bis zum Start</span><span class="sxs-lookup"><span data-stu-id="dcd7a-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcd7a-104">Diese Prozedur führt Sie durch den ersten Teils des Lebenszyklus eines Chargenauftrags.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="dcd7a-105">Von der Erstellung, über die Vorkalkulation und vom Produktionseinzelvorgang zum tatsächlichen Beginn eines Chargenauftrages.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="dcd7a-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="dcd7a-107">Die Voraussetzungen für die Ausführung der Prozedur mit einem anderen Dataset sind ein freigegebenes Produkt mit einer aktiven Formel und Arbeitsplanversion.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="dcd7a-108">Erstellen eines Chargenauftrags</span><span class="sxs-lookup"><span data-stu-id="dcd7a-108">Create a batch order</span></span>
1. <span data-ttu-id="dcd7a-109">Welchsen Sie zu "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-109">Go to All production orders.</span></span>
2. <span data-ttu-id="dcd7a-110">Klicken Sie auf "Neuer Chargenauftrag".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-110">Click New batch order.</span></span>
3. <span data-ttu-id="dcd7a-111">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="dcd7a-112">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-112">Click Create.</span></span>
5. <span data-ttu-id="dcd7a-113">Verwenden Sie den Schnellfilter, um im Feld "Produktion" nach dem Wert "b" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="dcd7a-114">Anzeigen von Produktionsformel und erwarteten Kuppelprodukten</span><span class="sxs-lookup"><span data-stu-id="dcd7a-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="dcd7a-115">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="dcd7a-116">Klicken Sie auf Formel.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-116">Click Formula.</span></span>
3. <span data-ttu-id="dcd7a-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-117">Close the page.</span></span>
4. <span data-ttu-id="dcd7a-118">Klicken Sie auf Kuppelprodukte.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-118">Click Co-products.</span></span>
5. <span data-ttu-id="dcd7a-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="dcd7a-120">Vorkalkulation des Chargenauftrags</span><span class="sxs-lookup"><span data-stu-id="dcd7a-120">Estimate the batch order</span></span>
1. <span data-ttu-id="dcd7a-121">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-121">Click Estimate.</span></span>
2. <span data-ttu-id="dcd7a-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-122">Click OK.</span></span>
3. <span data-ttu-id="dcd7a-123">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="dcd7a-124">Klicken Sie auf Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="dcd7a-124">Click View calculation details.</span></span>
5. <span data-ttu-id="dcd7a-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="dcd7a-126">Freigeben des Chargenauftrags</span><span class="sxs-lookup"><span data-stu-id="dcd7a-126">Release the batch order</span></span>
1. <span data-ttu-id="dcd7a-127">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="dcd7a-128">Klicken Sie auf "Freigabe".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-128">Click Release.</span></span>
3. <span data-ttu-id="dcd7a-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="dcd7a-130">Planen von Produktionseinzelvorgängen</span><span class="sxs-lookup"><span data-stu-id="dcd7a-130">Schedule production jobs</span></span>
1. <span data-ttu-id="dcd7a-131">Klicken Sie im Aktivitätsbereich auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="dcd7a-132">Klicken Sie auf Einzelvorgänge planen.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="dcd7a-133">Wählen Sie "Nein" im Feld "Begrenzte Kapazität" aus.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="dcd7a-134">Wählen Sie "Nein" im Feld "Begrenztes Material" aus.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="dcd7a-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-135">Click OK.</span></span>
6. <span data-ttu-id="dcd7a-136">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="dcd7a-137">Klicken Sie auf "Alle Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-137">Click All jobs.</span></span>
8. <span data-ttu-id="dcd7a-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="dcd7a-139">Starten des Chargenauftrags</span><span class="sxs-lookup"><span data-stu-id="dcd7a-139">Start the batch order</span></span>
1. <span data-ttu-id="dcd7a-140">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-140">Click Start.</span></span>
2. <span data-ttu-id="dcd7a-141">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-141">Click the General tab.</span></span>
3. <span data-ttu-id="dcd7a-142">Wählen Sie im Feld "Kommissionierliste jetzt buchen" die Antwort "Nein" aus.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="dcd7a-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-143">Click OK.</span></span>
5. <span data-ttu-id="dcd7a-144">Klicken Sie im Aktivitätsbereich auf "Anzeigen".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="dcd7a-145">Klicken Sie auf "Kommissionierliste".</span><span class="sxs-lookup"><span data-stu-id="dcd7a-145">Click Picking list.</span></span>
7. <span data-ttu-id="dcd7a-146">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="dcd7a-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-147">Close the page.</span></span>
9. <span data-ttu-id="dcd7a-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-148">Close the page.</span></span>
10. <span data-ttu-id="dcd7a-149">Klicken Sie auf Arbeitsplanliste.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-149">Click Route card.</span></span>
11. <span data-ttu-id="dcd7a-150">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dcd7a-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-151">Close the page.</span></span>
13. <span data-ttu-id="dcd7a-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcd7a-152">Close the page.</span></span>


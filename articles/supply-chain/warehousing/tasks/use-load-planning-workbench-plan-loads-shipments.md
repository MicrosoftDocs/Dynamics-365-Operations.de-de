---
title: Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen
description: In diesem Thema wird gezeigt, wie die Ladungsplanungsworkbench verwendet wird, um eine Auslastung für einen Auftrag zu erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a6af2f0623744f2cddf46c0310231afb0870fd7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216734"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="81711-103">Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen</span><span class="sxs-lookup"><span data-stu-id="81711-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81711-104">In diesem Thema wird gezeigt, wie die Ladungsplanungsworkbench verwendet wird, um eine Auslastung für einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81711-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="81711-105">Im Voraus erstellen wir zuerst den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="81711-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="81711-106">Dieses Verfahren ist Teil der täglichen Arbeit für den Transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="81711-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="81711-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="81711-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="81711-108">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="81711-108">Create a sales order</span></span>
1. <span data-ttu-id="81711-109">Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="81711-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="81711-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-110">Select **New**.</span></span>
3. <span data-ttu-id="81711-111">Wählen Sie im Feld **Debitorenkonto** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81711-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="81711-112">Wählen Sie das Konto **US-004** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="81711-113">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="81711-113">Select **OK**.</span></span>
6. <span data-ttu-id="81711-114">Wählen Sie im Feld **Artikelnummer** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81711-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81711-115">Wählen Sie den Artikel **A0001** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-115">Select item **A0001**.</span></span> <span data-ttu-id="81711-116">**A0001** ist für die Transportverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81711-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="81711-117">Wählen Sie im Feld **Standort** die Dropdown-Schaltfläche, um die Suche zu öffnen, und wählen Sie dann einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="81711-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="81711-118">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="81711-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="81711-119">Geben Sie im Feld **Lagerort** „24“ für dieses Beispiel ein.</span><span class="sxs-lookup"><span data-stu-id="81711-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="81711-120">Dieser Lagerort wird für Transportverwaltung und von erweiterten Lagerortverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81711-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="81711-121">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="81711-121">Select **Save**.</span></span>
12. <span data-ttu-id="81711-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81711-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="81711-123">Erstellen Sie eine neue Auslastung</span><span class="sxs-lookup"><span data-stu-id="81711-123">Create a new load</span></span>
1. <span data-ttu-id="81711-124">Wechseln Sie zu **Navigationsbereich > Module > Transportverwaltung > Planung > Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="81711-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="81711-125">Wählen Sie die Registerkarte **Verkaufspositionen** aus. Nun erstellen Sie die Auslastung für den Auftrag, den Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="81711-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="81711-126">Auslastung des Systems während können auf Grundlage Angebot und Nachfrage aus Bestellungen, von den Umlagerungsaufträge und die Aufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="81711-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="81711-127">Wählen Sie im Aktivitätsbereich **Beschaffung und Bedarf** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="81711-128">Wählen Sie **An neue Ladung** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-128">Select **To new load**.</span></span>
5. <span data-ttu-id="81711-129">Wählen Sie im Feld **Ladungsvorlagenkennung** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81711-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="81711-130">Die Auslastungsvorlage definiert maximale Messung für Gewicht und Volumen der gesamten Auslastung.</span><span class="sxs-lookup"><span data-stu-id="81711-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="81711-131">Beispielsweise könnte die Auslastungsvorlage die Größe eines Containers oder des LKWs darstellen.</span><span class="sxs-lookup"><span data-stu-id="81711-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="81711-132">Wählen Sie einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="81711-132">Select an item.</span></span>
6. <span data-ttu-id="81711-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="81711-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="81711-134">Auslastung bewerten und umleiten</span><span class="sxs-lookup"><span data-stu-id="81711-134">Rate and route the load</span></span>
1. <span data-ttu-id="81711-135">Wählen Sie **Bewertung und Weiterleitung** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="81711-136">Wählen Sie **Routen-Workbench-Satz** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="81711-137">Wählen Sie **Shopsatz** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="81711-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81711-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="81711-139">Wählen Sie **Zuweisen** aus.</span><span class="sxs-lookup"><span data-stu-id="81711-139">Select **Assign**.</span></span>
6. <span data-ttu-id="81711-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81711-140">Close the page.</span></span>


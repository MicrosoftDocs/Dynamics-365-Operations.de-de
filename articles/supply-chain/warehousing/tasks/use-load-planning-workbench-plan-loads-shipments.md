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
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976812"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="4c737-103">Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen</span><span class="sxs-lookup"><span data-stu-id="4c737-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c737-104">In diesem Thema wird gezeigt, wie die Ladungsplanungsworkbench verwendet wird, um eine Auslastung für einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c737-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="4c737-105">Im Voraus erstellen wir zuerst den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4c737-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="4c737-106">Dieses Verfahren ist Teil der täglichen Arbeit für den Transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="4c737-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="4c737-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4c737-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="4c737-108">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="4c737-108">Create a sales order</span></span>
1. <span data-ttu-id="4c737-109">Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="4c737-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="4c737-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-110">Select **New**.</span></span>
3. <span data-ttu-id="4c737-111">Wählen Sie im Feld **Debitorenkonto** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c737-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4c737-112">Wählen Sie das Konto **US-004** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="4c737-113">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c737-113">Select **OK**.</span></span>
6. <span data-ttu-id="4c737-114">Wählen Sie im Feld **Artikelnummer** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c737-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4c737-115">Wählen Sie den Artikel **A0001** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-115">Select item **A0001**.</span></span> <span data-ttu-id="4c737-116">**A0001** ist für die Transportverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4c737-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="4c737-117">Wählen Sie im Feld **Standort** die Dropdown-Schaltfläche, um die Suche zu öffnen, und wählen Sie dann einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="4c737-118">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4c737-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="4c737-119">Geben Sie im Feld **Lagerort** „24“ für dieses Beispiel ein.</span><span class="sxs-lookup"><span data-stu-id="4c737-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="4c737-120">Dieser Lagerort wird für Transportverwaltung und von erweiterten Lagerortverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4c737-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="4c737-121">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4c737-121">Select **Save**.</span></span>
12. <span data-ttu-id="4c737-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4c737-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="4c737-123">Erstellen Sie eine neue Auslastung</span><span class="sxs-lookup"><span data-stu-id="4c737-123">Create a new load</span></span>
1. <span data-ttu-id="4c737-124">Wechseln Sie zu **Navigationsbereich > Module > Transportverwaltung > Planung > Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="4c737-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="4c737-125">Wählen Sie die Registerkarte **Verkaufspositionen** aus. Nun erstellen Sie die Auslastung für den Auftrag, den Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4c737-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="4c737-126">Auslastung des Systems während können auf Grundlage Angebot und Nachfrage aus Bestellungen, von den Umlagerungsaufträge und die Aufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4c737-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="4c737-127">Wählen Sie im Aktivitätsbereich **Beschaffung und Bedarf** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="4c737-128">Wählen Sie **An neue Ladung** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-128">Select **To new load**.</span></span>
5. <span data-ttu-id="4c737-129">Wählen Sie im Feld **Ladungsvorlagenkennung** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c737-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="4c737-130">Die Auslastungsvorlage definiert maximale Messung für Gewicht und Volumen der gesamten Auslastung.</span><span class="sxs-lookup"><span data-stu-id="4c737-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="4c737-131">Beispielsweise könnte die Auslastungsvorlage die Größe eines Containers oder des LKWs darstellen.</span><span class="sxs-lookup"><span data-stu-id="4c737-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="4c737-132">Wählen Sie einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-132">Select an item.</span></span>
6. <span data-ttu-id="4c737-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c737-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="4c737-134">Auslastung bewerten und umleiten</span><span class="sxs-lookup"><span data-stu-id="4c737-134">Rate and route the load</span></span>
1. <span data-ttu-id="4c737-135">Wählen Sie **Bewertung und Weiterleitung** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="4c737-136">Wählen Sie **Routen-Workbench-Satz** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="4c737-137">Wählen Sie **Shopsatz** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="4c737-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4c737-139">Wählen Sie **Zuweisen** aus.</span><span class="sxs-lookup"><span data-stu-id="4c737-139">Select **Assign**.</span></span>
6. <span data-ttu-id="4c737-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4c737-140">Close the page.</span></span>


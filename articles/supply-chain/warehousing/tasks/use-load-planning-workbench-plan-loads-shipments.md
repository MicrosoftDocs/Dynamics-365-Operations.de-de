--- 
title: Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen
description: "Im folgenden Verfahren wird gezeigt, wie der Auslastungsplanungswerktisch verwendet wird, um eine Auslastung für einen Auftrag zu erstellen."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="c0990-103">Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen</span><span class="sxs-lookup"><span data-stu-id="c0990-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0990-104">Im folgenden Verfahren wird gezeigt, wie der Auslastungsplanungswerktisch verwendet wird, um eine Auslastung für einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0990-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="c0990-105">Im Voraus erstellen wir zuerst den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c0990-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="c0990-106">Dieses Verfahren ist Teil der täglichen Arbeit für den Transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="c0990-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="c0990-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="c0990-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="c0990-108">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="c0990-108">Create a sales order</span></span>
1. <span data-ttu-id="c0990-109">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="c0990-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c0990-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c0990-110">Click New.</span></span>
3. <span data-ttu-id="c0990-111">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0990-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c0990-112">Wählen Sie das Konto US-004 aus.</span><span class="sxs-lookup"><span data-stu-id="c0990-112">Select account US-004.</span></span>
5. <span data-ttu-id="c0990-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c0990-113">Click OK.</span></span>
6. <span data-ttu-id="c0990-114">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0990-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c0990-115">Artikel A0001 auswählen.</span><span class="sxs-lookup"><span data-stu-id="c0990-115">Select item A0001.</span></span>
    * <span data-ttu-id="c0990-116">A0001 ist für die Verwaltung von Transports aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c0990-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="c0990-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c0990-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c0990-118">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c0990-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="c0990-119">Geben Sie im Feld Lagerort "24" ein.</span><span class="sxs-lookup"><span data-stu-id="c0990-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="c0990-120">In diesem Beispiel wählen Sie Lagerort 24 aus.</span><span class="sxs-lookup"><span data-stu-id="c0990-120">In this example select warehouse 24.</span></span> <span data-ttu-id="c0990-121">Dieser Lagerort wird für Transportverwaltung und von erweiterten Lagerortverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c0990-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="c0990-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c0990-122">Click Save.</span></span>
12. <span data-ttu-id="c0990-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c0990-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="c0990-124">Erstellen Sie eine neue Auslastung</span><span class="sxs-lookup"><span data-stu-id="c0990-124">Create a new load</span></span>
1. <span data-ttu-id="c0990-125">Wechseln Sie zu Transportverwaltung > Planung > Ladungsplanungsworkbench.</span><span class="sxs-lookup"><span data-stu-id="c0990-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="c0990-126">Klicken Sie auf die Registerkarte Verkaufszeilen.</span><span class="sxs-lookup"><span data-stu-id="c0990-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="c0990-127">Nun erstellen Sie die Auslastung für den Auftrag, den Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c0990-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="c0990-128">Auslastung des Systems während können auf Grundlage Angebot und Nachfrage aus Bestellungen, von den Umlagerungsaufträge und die Aufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c0990-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="c0990-129">Klicken Sie im Aktivitätsbereich auf "Angebot und Nachfrage".</span><span class="sxs-lookup"><span data-stu-id="c0990-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="c0990-130">Klicken um in neue Ladung verschieben.</span><span class="sxs-lookup"><span data-stu-id="c0990-130">Click To new load.</span></span>
5. <span data-ttu-id="c0990-131">Klicken Sie im Feld "Ladungsvorlagen-ID" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0990-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c0990-132">Die Auslastungsvorlage definiert maximale Messung für Gewicht und Volumen der gesamten Auslastung.</span><span class="sxs-lookup"><span data-stu-id="c0990-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="c0990-133">Beispielsweise könnte die Auslastungsvorlage die Größe eines Containers oder des LKWs darstellen.</span><span class="sxs-lookup"><span data-stu-id="c0990-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="c0990-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c0990-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c0990-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c0990-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="c0990-136">Auslastung bewerten und umleiten</span><span class="sxs-lookup"><span data-stu-id="c0990-136">Rate and route the load</span></span>
1. <span data-ttu-id="c0990-137">Klicken Sie auf Bewertung und Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="c0990-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="c0990-138">Klicken Sie auf Routen-Workbench-Satz.</span><span class="sxs-lookup"><span data-stu-id="c0990-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="c0990-139">Klicken Sie auf Shopsatz.</span><span class="sxs-lookup"><span data-stu-id="c0990-139">Click Rate shop.</span></span>
4. <span data-ttu-id="c0990-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c0990-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c0990-141">Klicken Sie auf Zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c0990-141">Click Assign.</span></span>
6. <span data-ttu-id="c0990-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c0990-142">Close the page.</span></span>
7. <span data-ttu-id="c0990-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c0990-143">Close the page.</span></span>



---
title: Einen Produktprogrammplanungslauf überwachen
description: Der Produktionsplaner möchte sehen, ob ein Produktprogrammplanungslauf in Bearbeitung ist.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565607"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="1e87e-103">Einen Produktprogrammplanungslauf überwachen</span><span class="sxs-lookup"><span data-stu-id="1e87e-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e87e-104">Der Produktionsplaner möchte sehen, ob ein Produktprogrammplanungslauf in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="1e87e-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="1e87e-105">Verwenden Sie das Demodatenunternehmen USMF, um diese Prozedur abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1e87e-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="1e87e-106">Produktprogrammplanung ausführen</span><span class="sxs-lookup"><span data-stu-id="1e87e-106">Run master planning</span></span>
1. <span data-ttu-id="1e87e-107">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="1e87e-107">Click Master planning.</span></span>
    * <span data-ttu-id="1e87e-108">Sie finden dies auf dem Standard-Dashboard.</span><span class="sxs-lookup"><span data-stu-id="1e87e-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="1e87e-109">Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1e87e-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="1e87e-110">Beispiel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="1e87e-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="1e87e-111">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="1e87e-111">Click Run.</span></span>
4. <span data-ttu-id="1e87e-112">Wählen Sie "Ja" im Feld "Verarbeitungszeit nachverfolgen" aus.</span><span class="sxs-lookup"><span data-stu-id="1e87e-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="1e87e-113">Wenn das Feld bereits ausgewählt ist, überspringen Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="1e87e-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="1e87e-114">Geben Sie im Feld "Anzahl von Threads" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1e87e-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="1e87e-115">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="1e87e-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="1e87e-116">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="1e87e-116">Click Filter.</span></span>
8. <span data-ttu-id="1e87e-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="1e87e-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1e87e-118">Markieren Sie die Zeile, in der "Feld = Artikelnummer" ist.</span><span class="sxs-lookup"><span data-stu-id="1e87e-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="1e87e-119">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1e87e-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="1e87e-120">Beispiel: T0001</span><span class="sxs-lookup"><span data-stu-id="1e87e-120">Example: T0001</span></span>  
10. <span data-ttu-id="1e87e-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1e87e-121">Click OK.</span></span>
11. <span data-ttu-id="1e87e-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1e87e-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="1e87e-123">Überwachen Sie den Produktprogrammplanungslauf</span><span class="sxs-lookup"><span data-stu-id="1e87e-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="1e87e-124">Klicken Sie auf "Historie".</span><span class="sxs-lookup"><span data-stu-id="1e87e-124">Click History.</span></span>
2. <span data-ttu-id="1e87e-125">Klicken Sie auf Abfragen.</span><span class="sxs-lookup"><span data-stu-id="1e87e-125">Click Inquiries.</span></span>
3. <span data-ttu-id="1e87e-126">Klicken Sie auf "Prozessaufgabendauer".</span><span class="sxs-lookup"><span data-stu-id="1e87e-126">Click Process task duration.</span></span>
4. <span data-ttu-id="1e87e-127">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="1e87e-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1e87e-128">Für jeden Artikel können Sie einen Überblick darüber erhalten, wie lange es gedauert hat, um jeden Planungsschritt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1e87e-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


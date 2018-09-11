--- 
title: "Einen Plan für einen Standort erstellen"
description: "Der Produktionsplaner berechnet das Material und die Kapazitätsanforderungen für die Produktion eines bestimmten Artikels."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ebe3841720b4eb76e58e2d6e2f557558b03156d6
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="bbab0-103">Einen Plan für einen Standort erstellen</span><span class="sxs-lookup"><span data-stu-id="bbab0-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbab0-104">Der Produktionsplaner berechnet das Material und die Kapazitätsanforderungen für die Produktion eines bestimmten Artikels.</span><span class="sxs-lookup"><span data-stu-id="bbab0-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="bbab0-105">Nachdem die Beschaffungsvorschläge erstellt wurden, findet er die Aufträge am Standort, für den er plant und die Aufträge umwandelt, beginnend mit den dringenden Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="bbab0-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="bbab0-106">Die dringendsten Aufträge sind diejenigen, die zum aktuellen Datum umgewandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bbab0-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="bbab0-107">Verwenden Sie das Demodatunternehmen USMF, um diese Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bbab0-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="bbab0-108">Erstellen Sie einen Materialien- und Kapazitätsplan für einen Artikel</span><span class="sxs-lookup"><span data-stu-id="bbab0-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="bbab0-109">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="bbab0-109">Click Master planning.</span></span>
    * <span data-ttu-id="bbab0-110">Sie müssen zum standardmäßigen Dashboard navigieren.</span><span class="sxs-lookup"><span data-stu-id="bbab0-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="bbab0-111">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="bbab0-111">Click Run.</span></span>
3. <span data-ttu-id="bbab0-112">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="bbab0-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="bbab0-113">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="bbab0-113">Click Filter.</span></span>
5. <span data-ttu-id="bbab0-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="bbab0-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bbab0-115">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bbab0-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="bbab0-116">Beispiel: D0001</span><span class="sxs-lookup"><span data-stu-id="bbab0-116">Example: D0001</span></span>  
7. <span data-ttu-id="bbab0-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bbab0-117">Click OK.</span></span>
8. <span data-ttu-id="bbab0-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bbab0-118">Click OK.</span></span>
    * <span data-ttu-id="bbab0-119">Das kann einige Minuten in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="bbab0-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="bbab0-120">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bbab0-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="bbab0-121">Identifizieren Sie die dringenden Bestellvorschläge für den Artikel</span><span class="sxs-lookup"><span data-stu-id="bbab0-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="bbab0-122">Öffnen Sie den Spaltenfilter "Artikelnummer".</span><span class="sxs-lookup"><span data-stu-id="bbab0-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="bbab0-123">Verwenden Sie den Filteroperator "Beginnt mit", um einen Filter auf das Feld "Artikelnummer" mit einem Wert von "D0001" anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="bbab0-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="bbab0-124">Öffnen Sie den Spaltenfilter "Auftragsdatum".</span><span class="sxs-lookup"><span data-stu-id="bbab0-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="bbab0-125">Wenden Sie einen Filter auf das Feld "Auftragsdatum" an, mit einem Wert des aktuellen Datums, mithilfe des Filteroperators "Ist genau".</span><span class="sxs-lookup"><span data-stu-id="bbab0-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="bbab0-126">Wandeln Sie alle dringenden Aufträge für den Artikel um</span><span class="sxs-lookup"><span data-stu-id="bbab0-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="bbab0-127">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="bbab0-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="bbab0-128">Klicken Sie auf "Umwandeln".</span><span class="sxs-lookup"><span data-stu-id="bbab0-128">Click Firm.</span></span>
3. <span data-ttu-id="bbab0-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bbab0-129">Click OK.</span></span>



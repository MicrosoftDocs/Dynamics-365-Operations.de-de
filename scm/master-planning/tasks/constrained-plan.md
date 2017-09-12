--- 
title: "Plan mit Einschränkungen erstellen"
description: "Diese Prozedur zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="41e73-103">Plan mit Einschränkungen erstellen</span><span class="sxs-lookup"><span data-stu-id="41e73-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41e73-104">Diese Prozedur zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="41e73-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="41e73-105">Der Plan stellt sicher, dass die Herstellung nicht beginnt, bevor das Material verfügbar ist und die Ressourcen nicht überbucht werden.</span><span class="sxs-lookup"><span data-stu-id="41e73-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="41e73-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="41e73-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="41e73-107">Diese Prozedur ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="41e73-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="41e73-108">Einen eingeschränkten Plan einrichten</span><span class="sxs-lookup"><span data-stu-id="41e73-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="41e73-109">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="41e73-109">Click Master planning.</span></span>
2. <span data-ttu-id="41e73-110">Klicken Sie auf "Produktprogrammpläne".</span><span class="sxs-lookup"><span data-stu-id="41e73-110">Click Master plans.</span></span>
3. <span data-ttu-id="41e73-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="41e73-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="41e73-112">Beispiel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="41e73-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="41e73-113">Wählen Sie "Ja" im Feld "Begrenzte Kapazität" aus.</span><span class="sxs-lookup"><span data-stu-id="41e73-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="41e73-114">Geben Sie im Feld "Begrenzte Kapazität" den Wert "30" ein.</span><span class="sxs-lookup"><span data-stu-id="41e73-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="41e73-115">Erweitern Sie die Planungszeiträume im Tage-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="41e73-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="41e73-116">Wählen Sie "Ja" im Feld "Kapazität" aus.</span><span class="sxs-lookup"><span data-stu-id="41e73-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="41e73-117">Geben Sie im Feld "Zeitraum für Kapazitätsplanung (Tage)" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="41e73-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="41e73-118">Beispiel: 60</span><span class="sxs-lookup"><span data-stu-id="41e73-118">Example: 60</span></span>  
9. <span data-ttu-id="41e73-119">Wählen Sie "Ja" im Feld "Berechnete Verzögerungen" aus.</span><span class="sxs-lookup"><span data-stu-id="41e73-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="41e73-120">Geben Sie im Feld "Planungszeitraum für Verzögerungen berechnen (Tage)" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="41e73-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="41e73-121">Beispiel: 60</span><span class="sxs-lookup"><span data-stu-id="41e73-121">Example: 60</span></span>  
11. <span data-ttu-id="41e73-122">Erweitern Sie den Abschnitt "Berechnete Verzögerungen".</span><span class="sxs-lookup"><span data-stu-id="41e73-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="41e73-123">Wählen Sie "Ja" im Feld "Die berechnete Verzögerung dem Bedarfsdatum hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="41e73-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="41e73-124">Wählen Sie "Ja" im Feld "Die berechnete Verzögerung dem Bedarfsdatum hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="41e73-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="41e73-125">Wählen Sie "Ja" im Feld "Die berechnete Verzögerung dem Bedarfsdatum hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="41e73-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="41e73-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="41e73-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="41e73-127">Einen Plan mit Einschränkungen erstellen</span><span class="sxs-lookup"><span data-stu-id="41e73-127">Create a constrained plan</span></span>
1. <span data-ttu-id="41e73-128">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="41e73-128">Click Run.</span></span>
2. <span data-ttu-id="41e73-129">Geben Sie im Feld "Produktprogrammplan" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41e73-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="41e73-130">Wählen Sie den Plan aus, für den Sie Einschränkungen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="41e73-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="41e73-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="41e73-131">Click OK.</span></span>
    * <span data-ttu-id="41e73-132">Dies kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="41e73-132">This may take a while.</span></span>  
4. <span data-ttu-id="41e73-133">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="41e73-133">Click Planned orders.</span></span>



---
title: Plan mit Einschränkungen erstellen
description: Dieses Thema zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808015"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="7d90c-103">Plan mit Einschränkungen erstellen</span><span class="sxs-lookup"><span data-stu-id="7d90c-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d90c-104">Dieses Thema zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7d90c-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="7d90c-105">Der Plan stellt sicher, dass die Herstellung nicht beginnt, bevor das Material verfügbar ist und die Ressourcen nicht überbucht werden.</span><span class="sxs-lookup"><span data-stu-id="7d90c-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="7d90c-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="7d90c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7d90c-107">Diese Prozedur ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="7d90c-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="7d90c-108">Einen eingeschränkten Plan einrichten</span><span class="sxs-lookup"><span data-stu-id="7d90c-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="7d90c-109">Auf der Startseite wählen Sie den Arbeitsbereich **Produktprogrammplanung** aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="7d90c-110">Wählen Sie **Produktprogrammpläne** in der Liste mit Links ganz rechts im Arbeitsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="7d90c-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="7d90c-112">Beispiel: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="7d90c-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="7d90c-113">Wählen Sie **Ja** im Feld **Begrenzte Kapazität** aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="7d90c-114">Geben Sie im Feld **Planungszeitraum für begrenzte Kapazität** den Wert `30` ein.</span><span class="sxs-lookup"><span data-stu-id="7d90c-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="7d90c-115">Erweitern Sie den Abschnitt **Planungszeitraum in Tagen**.</span><span class="sxs-lookup"><span data-stu-id="7d90c-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="7d90c-116">Wählen Sie **Ja** im Feld **Kapazität** aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="7d90c-117">Geben Sie im Feld **Zeitraum für Kapazitätsplanung (Tage)** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7d90c-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="7d90c-118">Beispiel: `60`</span><span class="sxs-lookup"><span data-stu-id="7d90c-118">Example: `60`</span></span>  
9. <span data-ttu-id="7d90c-119">Wählen Sie **Ja** im Feld **Berechnete Verzögerungen** aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="7d90c-120">Geben Sie im Feld **Planungszeitraum für Verzögerungen berechnen (Tage)** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7d90c-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="7d90c-121">Beispiel: `60`</span><span class="sxs-lookup"><span data-stu-id="7d90c-121">Example: `60`</span></span> 
11. <span data-ttu-id="7d90c-122">Erweitern Sie den Abschnitt **Berechnete Verzögerungen**.</span><span class="sxs-lookup"><span data-stu-id="7d90c-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="7d90c-123">Wählen Sie **Ja** in allen Feldern **Die berechnete Verzögerung dem Bedarfsdatum hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7d90c-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="7d90c-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7d90c-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="7d90c-125">Einen Plan mit Einschränkungen erstellen</span><span class="sxs-lookup"><span data-stu-id="7d90c-125">Create a constrained plan</span></span>
1. <span data-ttu-id="7d90c-126">Wählen Sie **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-126">Select **Run**.</span></span>
2. <span data-ttu-id="7d90c-127">Geben Sie im Feld **Produktprogrammplan** den Plan ein oder wählen Sie den Plan aus, für den Sie Einschränkungen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="7d90c-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="7d90c-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d90c-128">Select **OK**.</span></span>
4. <span data-ttu-id="7d90c-129">Wählen Sie **Bestellvorschläge** aus.</span><span class="sxs-lookup"><span data-stu-id="7d90c-129">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
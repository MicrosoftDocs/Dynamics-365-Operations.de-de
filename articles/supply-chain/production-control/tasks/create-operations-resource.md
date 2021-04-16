---
title: Erstellen einer betrieblichen Ressource
description: Eine betriebliche Ressource führt die Aktivitäten eines Projekts oder eines Produktionsprozesses aus.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ab91c449293338469fa2832156a85c4c32301fd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829041"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="d6ab4-103">Erstellen einer betrieblichen Ressource</span><span class="sxs-lookup"><span data-stu-id="d6ab4-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6ab4-104">Eine betriebliche Ressource führt die Aktivitäten eines Projekts oder eines Produktionsprozesses aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="d6ab4-105">Diese Prozedur zeigt Ihnen an, wie eine betriebliche Ressource definiert wird.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="d6ab4-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d6ab4-107">Wechseln Sie zu "Ressourcen".</span><span class="sxs-lookup"><span data-stu-id="d6ab4-107">Go to Resources.</span></span>
2. <span data-ttu-id="d6ab4-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d6ab4-108">Click New.</span></span>
3. <span data-ttu-id="d6ab4-109">Geben Sie im Feld "Ressource" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="d6ab4-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="d6ab4-111">Kapazitäts- und Verbrauchsparameter definieren</span><span class="sxs-lookup"><span data-stu-id="d6ab4-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="d6ab4-112">Erweitern Sie den Abschnitt "Arbeitstang".</span><span class="sxs-lookup"><span data-stu-id="d6ab4-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="d6ab4-113">Geben Sie im Feld "Ausschuss" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="d6ab4-114">Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="d6ab4-115">Geben Sie die Kostenkategorie an, die definiert, wie die Kosten der Einstellung berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="d6ab4-116">Geben Sie im Feld "Ausführungszeitkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="d6ab4-117">Geben Sie die Kostenkategorie an, die definiert, wie die Kosten der Laufzeit berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="d6ab4-118">Geben Sie im Feld "Stückkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="d6ab4-119">Geben Sie die Kostenkategorie an, die definiert, wie die Ressourcenkosten, basierend auf der Ausgabemenge, berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="d6ab4-120">Wählen Sie im Feld "Kapazitätseinheit" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="d6ab4-121">Geben Sie die Einheit an, in der die Kapazität der betrieblichen Ressource ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="d6ab4-122">Geben Sie im Feld "Kapazität" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="d6ab4-123">Geben Sie im Feld "Effizienzgrad" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="d6ab4-124">Geben Sie die Effizienz an, die Sie von der betrieblichen Ressource erwarten.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="d6ab4-125">Mit dem Effizienzgrad wird der Durchsatz einer betrieblichen Ressource angepasst und er wirkt sich somit auch auf die für die Ressource reservierte Zeit aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="d6ab4-126">Geben Sie im Feld "Grobterminierungsprozentsatz" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="d6ab4-127">Geben Sie den maximalen Prozentsatz der Kapazität der betrieblichen Ressource an, die sie für die Grobterminierung verwendet möchten.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="d6ab4-128">Wählen Sie "Ja" im Feld "Begrenzte Kapazität" aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="d6ab4-129">Legen Sie diese Option auf "Ja" fest, wenn die betriebliche Ressource auf Basis der tatsächlichen Kapazität, die verfügbar ist, geplant werden soll, und wenn vorhandene Kapazitätsreservierungen berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="d6ab4-130">Wenn die Option auf "Nein" festgelegt ist, wird angenommen, dass die betriebliche Ressource unbegrenzte Kapazität hat, und die Ressource kann möglicherweise überbucht werden.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="d6ab4-131">Wählen Sie "Ja" im Feld "Engpassressource" aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="d6ab4-132">Arbeitszeiten definieren</span><span class="sxs-lookup"><span data-stu-id="d6ab4-132">Define working times</span></span>
1. <span data-ttu-id="d6ab4-133">Erweitern Sie den Abschnitt "Kalender".</span><span class="sxs-lookup"><span data-stu-id="d6ab4-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="d6ab4-134">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-134">Click Add.</span></span>
3. <span data-ttu-id="d6ab4-135">Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="d6ab4-136">Geben Sie den Arbeitszeitkalender an, der die Kapazität (in Stunden) der Ressource definiert.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="d6ab4-137">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d6ab4-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="d6ab4-139">Ressourcenfähigkeiten definieren</span><span class="sxs-lookup"><span data-stu-id="d6ab4-139">Define resource capabilities</span></span>
1. <span data-ttu-id="d6ab4-140">Erweitern Sie den Abschnitt "Funktionen".</span><span class="sxs-lookup"><span data-stu-id="d6ab4-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="d6ab4-141">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-141">Click Add.</span></span>
    * <span data-ttu-id="d6ab4-142">Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="d6ab4-143">Das Planungsmodul weist Ressourcen zu, indem die Ressourcenanforderungen jeder Aktivität mit den Funktionen der verfügbaren betrieblichen Ressourcen abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="d6ab4-144">Geben Sie im Feld "Funktion" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="d6ab4-145">Geben Sie im Feld "Ebene" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="d6ab4-146">Geben Sie den Grad der Effizienz an, mit der die Ressource die Funktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="d6ab4-147">Geben Sie im Feld "Priorität" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="d6ab4-148">Geben Sie die Priorität der betrieblichen Ressource hinsichtlich der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="d6ab4-149">Bei der Planung nach Priorität, wird die betriebliche Ressource mit der höchsten Priorität (also mit dem niedrigsten numerischen Wert) zuerst ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="d6ab4-150">Einer Ressourcengruppe eine Ressource zuweisen</span><span class="sxs-lookup"><span data-stu-id="d6ab4-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="d6ab4-151">Erweitern Sie den Abschnitt "Ressourcengruppen".</span><span class="sxs-lookup"><span data-stu-id="d6ab4-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="d6ab4-152">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-152">Click Add.</span></span>
    * <span data-ttu-id="d6ab4-153">Die Ressourcengruppe definiert den Standort-, Produktionseinheits- und Lagerortkontext für betriebliche Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="d6ab4-154">Die betriebliche Ressource kann nur eingeplant werden, wenn sie einer Ressourcengruppe zugewiesen ist, und zwar nur an dem Standort, an dem sich die Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="d6ab4-155">Geben Sie im Feld "Ressourcengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="d6ab4-156">Geben Sie im Feld "Lagerplatz für Wareneingang" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="d6ab4-157">Geben Sie den Lagerort an, von dem aus die betriebliche Ressource Material verbraucht.</span><span class="sxs-lookup"><span data-stu-id="d6ab4-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
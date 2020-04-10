---
title: Produktionsfluss und Version überprüfen
description: Die Prozedur zeigt, wie ein neuer Produktionsfluss und eine erste Version für Lean Manufacturing erstellt werden.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dfd5655ecdfa74d75490b0915c4cea609baebe3
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146501"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="692e8-103">Produktionsfluss und Version überprüfen</span><span class="sxs-lookup"><span data-stu-id="692e8-103">Validate a production flow and version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="692e8-104">Die Prozedur zeigt, wie ein neuer Produktionsfluss und eine erste Version für Lean Manufacturing erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="692e8-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="692e8-105">Voraussetzungen: Die Produktionsparameter für Lean Manufacturing und die Maßeinheiten der Klasse "Zeit" müssen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="692e8-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="692e8-106">Sie müssen einen Wertstrom und ein Produktionsbuchungsprofil definieren.</span><span class="sxs-lookup"><span data-stu-id="692e8-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="692e8-107">Informationen finden Sie in den Whitepapers zu Lean Manufacturing, um sich mit den Konzepten von Produktionsflüssen und Aktivitäten vertraut zu machen.</span><span class="sxs-lookup"><span data-stu-id="692e8-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="692e8-108">Diese Prozedur bezieht sich auf die juristische Person USMF in den Demodaten.</span><span class="sxs-lookup"><span data-stu-id="692e8-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="692e8-109">Jedoch angenommen, dass die juristische Person für Lean Manufacturing konfiguriert ist, können andere juristische Personen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="692e8-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="692e8-110">Einen Produktionsfluss erstellen</span><span class="sxs-lookup"><span data-stu-id="692e8-110">Create a production flow</span></span>
1. <span data-ttu-id="692e8-111">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="692e8-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="692e8-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="692e8-112">Click New.</span></span>
3. <span data-ttu-id="692e8-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="692e8-114">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="692e8-115">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="692e8-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="692e8-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="692e8-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="692e8-117">Ein Wertstrom ist eine Organisationseinheit, die alle Aktivitäten und Flüsse des Wertstroms umfasst.</span><span class="sxs-lookup"><span data-stu-id="692e8-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="692e8-118">Gegenwärtig werden Organisationseinheiten auf eine juristische Person beschränkt und haben keine weitere Funktion.</span><span class="sxs-lookup"><span data-stu-id="692e8-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="692e8-119">Klicken Sie im Feld "Produktionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="692e8-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="692e8-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="692e8-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="692e8-121">Produktionsgruppen ermöglichen die Definition von Material, Arbeit und RIF-Konten für einen Produktionsprozess.</span><span class="sxs-lookup"><span data-stu-id="692e8-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="692e8-122">Um den Buchhaltungskontext zu einem Produktionsfluss zuzuordnen, muss eine Produktionsgruppe ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="692e8-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="692e8-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="692e8-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="692e8-124">Eine Produktionsflussversion erstellen</span><span class="sxs-lookup"><span data-stu-id="692e8-124">Create a production flow version</span></span>
1. <span data-ttu-id="692e8-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="692e8-125">Click Add.</span></span>
2. <span data-ttu-id="692e8-126">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="692e8-127">Sie können das Ablaufdatum der Version auch für aktive Versionen zu einem beliebigen Zeitpunkt aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="692e8-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="692e8-128">Verwenden Sie den Ablauf der Version, um eine Phase außerhalb einer Version zu planen.</span><span class="sxs-lookup"><span data-stu-id="692e8-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="692e8-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="692e8-129">Click OK.</span></span>
4. <span data-ttu-id="692e8-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="692e8-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="692e8-131">Geben Sie im Feld "Einheiten" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="692e8-132">Wählen Sie die Takteinheit.</span><span class="sxs-lookup"><span data-stu-id="692e8-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="692e8-133">Geben Sie eine Zahl in das Feld "Durchschnittliche Taktzeit" ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="692e8-134">Für die Taktkontrolle der Produktionsflussversion , definieren Sie die geplante durchschnittliche Taktzeit.</span><span class="sxs-lookup"><span data-stu-id="692e8-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="692e8-135">Der Takt wird als Menge pro Zeitperiode definiert.</span><span class="sxs-lookup"><span data-stu-id="692e8-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="692e8-136">Im vorliegenden Beispiel ist die Taktzeit 0,2 Stunden pro 10 Stück.</span><span class="sxs-lookup"><span data-stu-id="692e8-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="692e8-137">Bei einer Arbeitszeit von 8 Stunden, entspricht dies einer täglichen Durchsatzkapazität von 400 Stück.</span><span class="sxs-lookup"><span data-stu-id="692e8-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="692e8-138">Geben Sie im Feld "Menge pro Zyklus" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="692e8-139">Erweitern oder reduzieren Sie den Abschnitt "Versionsdetails".</span><span class="sxs-lookup"><span data-stu-id="692e8-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="692e8-140">Geben Sie eine Zahl in das Feld "Minimale Taktzeit" ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="692e8-141">Die Mindesttaktzeit muss kleiner oder gleich der durchschnittlichen Taktzeit sein.</span><span class="sxs-lookup"><span data-stu-id="692e8-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="692e8-142">Geben Sie eine Zahl in das Feld "Maximale Taktzeit" ein.</span><span class="sxs-lookup"><span data-stu-id="692e8-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="692e8-143">Die maximale Taktzeit muß größer oder gleich der durchschnittlichen Taktzeit sein.</span><span class="sxs-lookup"><span data-stu-id="692e8-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="692e8-144">Geben Sie eine Anzahl von Tagen der Periode für tatsächliche Zykluszeit an.</span><span class="sxs-lookup"><span data-stu-id="692e8-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="692e8-145">Die Periode für tatsächliche Zykluszeit ist die Anzahl der Tage, in denen Einzelvorgänge ab der tatsächlichen Minute rückwärts erfasst werden, um die tatsächliche Zykluszeit zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="692e8-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="692e8-146">Der Wert kann jederzeit geändert werden und wird nur für die Berechnung der tatsächlichen Zykluszeiten verwendet.</span><span class="sxs-lookup"><span data-stu-id="692e8-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="692e8-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="692e8-147">Click Save.</span></span>


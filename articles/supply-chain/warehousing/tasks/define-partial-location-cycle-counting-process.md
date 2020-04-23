---
title: Partiellen Lagerplatzzykluszählungsprozess definieren
description: Wenn Sie Zykluszählungspläne verwenden, um Inventurarbeit zu erstellen, können Sie die tatsächlichen Zähleroperationen verwalten, indem Sie diese nur für bestimmte Produkte und Produktvarianten anfordern,  anstelle aller verfügbaren Lagerbestands am Lagerplatz zu zählen.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3d80171ec524e3401d7971cb743d73abdda87ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217033"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="5085e-103">Partiellen Lagerplatzzykluszählungsprozess definieren</span><span class="sxs-lookup"><span data-stu-id="5085e-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5085e-104">Wenn Sie Zykluszählungspläne verwenden, um Inventurarbeit zu erstellen, können Sie die tatsächlichen Zähleroperationen verwalten, indem Sie diese nur für bestimmte Produkte und Produktvarianten anfordern,  anstelle aller verfügbaren Lagerbestands am Lagerplatz zu zählen.</span><span class="sxs-lookup"><span data-stu-id="5085e-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="5085e-105">Indem Sie nach bestimmten Produkten filtern, kann der Lagerortleiter Prüfungsgemeinkosten senken, Konsolidierungsfehler vermeiden und Zeit sparen.</span><span class="sxs-lookup"><span data-stu-id="5085e-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="5085e-106">Normalerweise werden diese Aufgaben von einem Lagerortleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5085e-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="5085e-107">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="5085e-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="5085e-108">Zykluszählungsarbeitsvorlage automatisch erstellen</span><span class="sxs-lookup"><span data-stu-id="5085e-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="5085e-109">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".</span><span class="sxs-lookup"><span data-stu-id="5085e-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="5085e-110">Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Zykluszählung" aus.</span><span class="sxs-lookup"><span data-stu-id="5085e-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="5085e-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5085e-111">Click New.</span></span>
4. <span data-ttu-id="5085e-112">Geben Sie im Feld "Laufende Nummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="5085e-113">Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer.</span><span class="sxs-lookup"><span data-stu-id="5085e-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="5085e-114">Der Wert muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5085e-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="5085e-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5085e-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="5085e-116">Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="5085e-117">Geben Sie im Feld "Arbeitsvorlagenbeschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="5085e-118">Geben Sie im Feld "Pool-ID" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5085e-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="5085e-119">Geben Sie im Feld "Arbeits-Priorität" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="5085e-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5085e-120">Click Save.</span></span>
11. <span data-ttu-id="5085e-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5085e-121">Click New.</span></span>
12. <span data-ttu-id="5085e-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5085e-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="5085e-123">Wählen Sie im Feld "Arbeitstyp" die Option "Zählung" aus.</span><span class="sxs-lookup"><span data-stu-id="5085e-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="5085e-124">Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5085e-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="5085e-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5085e-125">Click Save.</span></span>
16. <span data-ttu-id="5085e-126">Arbeitspositionsumbrüche anklicken.</span><span class="sxs-lookup"><span data-stu-id="5085e-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="5085e-127">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5085e-127">Click New.</span></span>
18. <span data-ttu-id="5085e-128">Geben Sie im Feld "Laufende Nummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="5085e-129">Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer.</span><span class="sxs-lookup"><span data-stu-id="5085e-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="5085e-130">Der Wert muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5085e-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="5085e-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5085e-131">Click Save.</span></span>
20. <span data-ttu-id="5085e-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5085e-132">Close the page.</span></span>
21. <span data-ttu-id="5085e-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5085e-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="5085e-134">Zykluszählungsplan erstellen</span><span class="sxs-lookup"><span data-stu-id="5085e-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="5085e-135">Wechseln Sie zu Lagerortverwaltung > Einrichten > Permanente Inventur > Permanenten Inventurplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="5085e-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="5085e-136">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5085e-136">Click New.</span></span>
3. <span data-ttu-id="5085e-137">Geben Sie im Feld "Zykluszählungs-Plankennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="5085e-138">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5085e-139">Geben Sie im Feld "Maximale Anzahl von Zykluszählungen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="5085e-140">Geben Sie im Feld "Arbeitsvorlage" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5085e-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="5085e-141">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5085e-141">Click New.</span></span>
8. <span data-ttu-id="5085e-142">Geben Sie im Feld "Laufende Nummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="5085e-143">Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer.</span><span class="sxs-lookup"><span data-stu-id="5085e-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="5085e-144">Der Wert muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5085e-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="5085e-145">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5085e-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="5085e-146">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5085e-146">Click Save.</span></span>
11. <span data-ttu-id="5085e-147">Produktabfrage definieren anklicken.</span><span class="sxs-lookup"><span data-stu-id="5085e-147">Click Define product query.</span></span>
12. <span data-ttu-id="5085e-148">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5085e-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="5085e-149">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5085e-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="5085e-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5085e-150">Click OK.</span></span>
15. <span data-ttu-id="5085e-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5085e-151">Close the page.</span></span>


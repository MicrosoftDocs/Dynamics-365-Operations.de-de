---
title: Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f342831d95f9988f9bb7807bac986e43cb317e0f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820008"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="dddb1-103">Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="dddb1-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dddb1-104">Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dddb1-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="dddb1-105">Dieses Verfahren beschreibt auch, wie eine Konfigurationsbezeichnung für eine Produktkonfigurationsmodellkomponente erstellen wird.</span><span class="sxs-lookup"><span data-stu-id="dddb1-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="dddb1-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="dddb1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dddb1-107">Die neue Produktnummernbezeichnung wird dem Produktmaster D0004 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="dddb1-108">Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="dddb1-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="dddb1-109">Erstellen eine Produktnummerbezeichnung</span><span class="sxs-lookup"><span data-stu-id="dddb1-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="dddb1-110">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="dddb1-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="dddb1-111">Klicken Sie auf "Produktbezeichnung".</span><span class="sxs-lookup"><span data-stu-id="dddb1-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="dddb1-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="dddb1-112">Click New.</span></span>
4. <span data-ttu-id="dddb1-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dddb1-114">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="dddb1-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-115">Click Add.</span></span>
7. <span data-ttu-id="dddb1-116">Klicken Sie auf "Produktmasternummer".</span><span class="sxs-lookup"><span data-stu-id="dddb1-116">Click Product master number.</span></span>
8. <span data-ttu-id="dddb1-117">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-117">Click Add.</span></span>
9. <span data-ttu-id="dddb1-118">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="dddb1-118">Click Text constant.</span></span>
10. <span data-ttu-id="dddb1-119">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="dddb1-120">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="dddb1-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-121">Click Add.</span></span>
13. <span data-ttu-id="dddb1-122">Klicken Sie auf "Konfiguration".</span><span class="sxs-lookup"><span data-stu-id="dddb1-122">Click Configuration.</span></span>
14. <span data-ttu-id="dddb1-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dddb1-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="dddb1-124">Zuweisen der Produktnummernbezeichnung zu einem Produktmaster</span><span class="sxs-lookup"><span data-stu-id="dddb1-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="dddb1-125">Klicken Sie auf "Produktmaster".</span><span class="sxs-lookup"><span data-stu-id="dddb1-125">Click Product masters.</span></span>
2. <span data-ttu-id="dddb1-126">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dddb1-127">Filtern Sie beispielsweise im Feld "Produktnummer" mit dem Wert "D".</span><span class="sxs-lookup"><span data-stu-id="dddb1-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="dddb1-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dddb1-129">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="dddb1-129">Click Edit.</span></span>
5. <span data-ttu-id="dddb1-130">Wählen Sie "Ja" im Feld "Bezeichnungen verwenden".</span><span class="sxs-lookup"><span data-stu-id="dddb1-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="dddb1-131">Geben Sie im Feld "Produktvariantennummerbezeichnung" eine Bezeichnung ein oder wählen Sie eine aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="dddb1-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dddb1-132">Close the page.</span></span>
8. <span data-ttu-id="dddb1-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dddb1-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="dddb1-134">Erstellen einer Bezeichnung für eine Produktkonfigurationsmodellkomponente</span><span class="sxs-lookup"><span data-stu-id="dddb1-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="dddb1-135">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="dddb1-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="dddb1-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dddb1-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dddb1-138">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="dddb1-138">Click Edit.</span></span>
5. <span data-ttu-id="dddb1-139">Wählen Sie "Ja" im Feld "Konfigurationsbezeichnungen verwenden".</span><span class="sxs-lookup"><span data-stu-id="dddb1-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="dddb1-140">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-140">Click Add.</span></span>
7. <span data-ttu-id="dddb1-141">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="dddb1-141">Click Attribute value.</span></span>
8. <span data-ttu-id="dddb1-142">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="dddb1-143">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="dddb1-144">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-144">Click Add.</span></span>
11. <span data-ttu-id="dddb1-145">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="dddb1-145">Click Text constant.</span></span>
12. <span data-ttu-id="dddb1-146">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="dddb1-147">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="dddb1-148">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-148">Click Add.</span></span>
15. <span data-ttu-id="dddb1-149">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="dddb1-149">Click Attribute value.</span></span>
16. <span data-ttu-id="dddb1-150">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="dddb1-151">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="dddb1-152">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-152">Click Add.</span></span>
19. <span data-ttu-id="dddb1-153">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="dddb1-153">Click Text constant.</span></span>
20. <span data-ttu-id="dddb1-154">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="dddb1-155">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="dddb1-156">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-156">Click Add.</span></span>
23. <span data-ttu-id="dddb1-157">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="dddb1-157">Click Attribute value.</span></span>
24. <span data-ttu-id="dddb1-158">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="dddb1-159">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="dddb1-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-160">Click Add.</span></span>
27. <span data-ttu-id="dddb1-161">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="dddb1-161">Click Text constant.</span></span>
28. <span data-ttu-id="dddb1-162">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="dddb1-163">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="dddb1-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-164">Click Add.</span></span>
31. <span data-ttu-id="dddb1-165">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="dddb1-165">Click Attribute value.</span></span>
32. <span data-ttu-id="dddb1-166">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="dddb1-167">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="dddb1-168">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-168">Click Add.</span></span>
35. <span data-ttu-id="dddb1-169">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="dddb1-169">Click Text constant.</span></span>
36. <span data-ttu-id="dddb1-170">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="dddb1-171">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dddb1-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="dddb1-172">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dddb1-172">Click Add.</span></span>
39. <span data-ttu-id="dddb1-173">Klicken Sie auf Nummernkreiswert.</span><span class="sxs-lookup"><span data-stu-id="dddb1-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="dddb1-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dddb1-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="dddb1-175">Geben Sie im Feld "Nummernkreis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dddb1-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="dddb1-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dddb1-176">Close the page.</span></span>
43. <span data-ttu-id="dddb1-177">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dddb1-177">Close the page.</span></span>
44. <span data-ttu-id="dddb1-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dddb1-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
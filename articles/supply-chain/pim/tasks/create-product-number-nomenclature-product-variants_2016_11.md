---
title: Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e52b7a5aff3e86e845484e1e84b4003cc4a52c95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992369"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="3699f-103">Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="3699f-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3699f-104">Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3699f-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="3699f-105">Dieses Verfahren beschreibt auch, wie eine Konfigurationsbezeichnung für eine Produktkonfigurationsmodellkomponente erstellen wird.</span><span class="sxs-lookup"><span data-stu-id="3699f-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="3699f-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="3699f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3699f-107">Die neue Produktnummernbezeichnung wird dem Produktmaster D0004 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3699f-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="3699f-108">Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="3699f-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="3699f-109">Erstellen eine Produktnummerbezeichnung</span><span class="sxs-lookup"><span data-stu-id="3699f-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="3699f-110">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="3699f-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3699f-111">Klicken Sie auf "Produktbezeichnung".</span><span class="sxs-lookup"><span data-stu-id="3699f-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="3699f-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3699f-112">Click New.</span></span>
4. <span data-ttu-id="3699f-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3699f-114">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3699f-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-115">Click Add.</span></span>
7. <span data-ttu-id="3699f-116">Klicken Sie auf "Produktmasternummer".</span><span class="sxs-lookup"><span data-stu-id="3699f-116">Click Product master number.</span></span>
8. <span data-ttu-id="3699f-117">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-117">Click Add.</span></span>
9. <span data-ttu-id="3699f-118">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="3699f-118">Click Text constant.</span></span>
10. <span data-ttu-id="3699f-119">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3699f-120">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="3699f-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-121">Click Add.</span></span>
13. <span data-ttu-id="3699f-122">Klicken Sie auf "Konfiguration".</span><span class="sxs-lookup"><span data-stu-id="3699f-122">Click Configuration.</span></span>
14. <span data-ttu-id="3699f-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3699f-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="3699f-124">Zuweisen der Produktnummernbezeichnung zu einem Produktmaster</span><span class="sxs-lookup"><span data-stu-id="3699f-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="3699f-125">Klicken Sie auf "Produktmaster".</span><span class="sxs-lookup"><span data-stu-id="3699f-125">Click Product masters.</span></span>
2. <span data-ttu-id="3699f-126">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3699f-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3699f-127">Filtern Sie beispielsweise im Feld "Produktnummer" mit dem Wert "D".</span><span class="sxs-lookup"><span data-stu-id="3699f-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="3699f-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3699f-129">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3699f-129">Click Edit.</span></span>
5. <span data-ttu-id="3699f-130">Wählen Sie "Ja" im Feld "Bezeichnungen verwenden".</span><span class="sxs-lookup"><span data-stu-id="3699f-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="3699f-131">Geben Sie im Feld "Produktvariantennummerbezeichnung" eine Bezeichnung ein oder wählen Sie eine aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="3699f-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3699f-132">Close the page.</span></span>
8. <span data-ttu-id="3699f-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3699f-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="3699f-134">Erstellen einer Bezeichnung für eine Produktkonfigurationsmodellkomponente</span><span class="sxs-lookup"><span data-stu-id="3699f-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="3699f-135">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="3699f-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="3699f-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3699f-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3699f-138">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3699f-138">Click Edit.</span></span>
5. <span data-ttu-id="3699f-139">Wählen Sie "Ja" im Feld "Konfigurationsbezeichnungen verwenden".</span><span class="sxs-lookup"><span data-stu-id="3699f-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="3699f-140">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-140">Click Add.</span></span>
7. <span data-ttu-id="3699f-141">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="3699f-141">Click Attribute value.</span></span>
8. <span data-ttu-id="3699f-142">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3699f-143">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="3699f-144">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-144">Click Add.</span></span>
11. <span data-ttu-id="3699f-145">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="3699f-145">Click Text constant.</span></span>
12. <span data-ttu-id="3699f-146">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3699f-147">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="3699f-148">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-148">Click Add.</span></span>
15. <span data-ttu-id="3699f-149">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="3699f-149">Click Attribute value.</span></span>
16. <span data-ttu-id="3699f-150">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="3699f-151">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="3699f-152">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-152">Click Add.</span></span>
19. <span data-ttu-id="3699f-153">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="3699f-153">Click Text constant.</span></span>
20. <span data-ttu-id="3699f-154">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="3699f-155">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="3699f-156">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-156">Click Add.</span></span>
23. <span data-ttu-id="3699f-157">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="3699f-157">Click Attribute value.</span></span>
24. <span data-ttu-id="3699f-158">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="3699f-159">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="3699f-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-160">Click Add.</span></span>
27. <span data-ttu-id="3699f-161">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="3699f-161">Click Text constant.</span></span>
28. <span data-ttu-id="3699f-162">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="3699f-163">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="3699f-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-164">Click Add.</span></span>
31. <span data-ttu-id="3699f-165">Klicken Sie auf Attributwert.</span><span class="sxs-lookup"><span data-stu-id="3699f-165">Click Attribute value.</span></span>
32. <span data-ttu-id="3699f-166">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="3699f-167">Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="3699f-168">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-168">Click Add.</span></span>
35. <span data-ttu-id="3699f-169">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="3699f-169">Click Text constant.</span></span>
36. <span data-ttu-id="3699f-170">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="3699f-171">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3699f-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="3699f-172">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3699f-172">Click Add.</span></span>
39. <span data-ttu-id="3699f-173">Klicken Sie auf Nummernkreiswert.</span><span class="sxs-lookup"><span data-stu-id="3699f-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="3699f-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3699f-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="3699f-175">Geben Sie im Feld "Nummernkreis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3699f-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="3699f-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3699f-176">Close the page.</span></span>
43. <span data-ttu-id="3699f-177">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3699f-177">Close the page.</span></span>
44. <span data-ttu-id="3699f-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3699f-178">Close the page.</span></span>


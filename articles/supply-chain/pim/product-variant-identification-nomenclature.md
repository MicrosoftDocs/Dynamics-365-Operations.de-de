---
title: Bezeichnung der Produktvariantennummern und Namen
description: "In diesem Thema wird beschrieben, wie Sie eine Produktnummernbezeichnung einrichten können, um das feste Format [Produktmasternummer – Konfiguration – Größe – Farbe – Stil] zu ersetzen. Die neue Bezeichnung hat ein gezieltes Format, das die Produktmasternummer, aktive Produktdimensionen und Texttrennzeichen Ihrer Wahl umfasst. Darüber hinaus können Sie auch eine Bezeichnung für Produktnamen erstellen. Sie können schließlich auch eine Bezeichnung erstellen, um Konfigurationen zu identifizieren, die vom einschränkungsbasierten Produktkonfigurator erstellt werden. Diese Bezeichnungen können Attribute Ihrer Wahl enthalten."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 4ebebc1d287908dbe8ac7557c34fc6693c88bfae
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="d3b68-107">Bezeichnung der Produktvariantennummern und Namen</span><span class="sxs-lookup"><span data-stu-id="d3b68-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="d3b68-108">In diesem Thema wird beschrieben, wie Sie eine Produktnummernbezeichnung einrichten können, um das feste Format [Produktmasternummer – Konfiguration – Größe – Farbe – Stil] zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="d3b68-109">Die neue Bezeichnung hat ein gezieltes Format, das die Produktmasternummer, aktive Produktdimensionen und Texttrennzeichen Ihrer Wahl umfasst.</span><span class="sxs-lookup"><span data-stu-id="d3b68-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="d3b68-110">Darüber hinaus können Sie auch eine Bezeichnung für Produktnamen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="d3b68-111">Sie können schließlich auch eine Bezeichnung erstellen, um Konfigurationen zu identifizieren, die vom einschränkungsbasierten Produktkonfigurator erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="d3b68-112">Diese Bezeichnungen können Attribute Ihrer Wahl enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3b68-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="d3b68-113">Die neuen Bezeichnungen für Produktvariantennummern und Produktvariantennamen ermöglichen es Ihnen, Segmente in die Bezeichner für Produktvarianten einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="d3b68-114">Diese Segmente können die Produktmasternummer und den Produktmasternamen, die Produktdimensionskennungen und -namen, die Nummernkreise, Textkonstanten und Attribute umfassen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="d3b68-115">Mit dieser Funktionalität können Sie schnell eine bestimmte Produktvariante suchen, wenn einen Auftrag oder eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="d3b68-116">Sie erstellen Bezeichnungen sowohl für Produktvariantennummern als auch Produktvariantennamen mithilfe der Seite **Produktbezeichnung**.</span><span class="sxs-lookup"><span data-stu-id="d3b68-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="d3b68-117">Um diese Seite zu öffnen, klicken Sie auf **Produktinformationsverwaltung** &gt; **Setup**.</span><span class="sxs-lookup"><span data-stu-id="d3b68-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="d3b68-118">Bezeichnung der vordefinierten Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="d3b68-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="d3b68-119">Produktvarianten für Produktmaster werden entsprechend einer der drei Konfigurationstechnologien generiert:</span><span class="sxs-lookup"><span data-stu-id="d3b68-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="d3b68-120">Vordefinierte Variante</span><span class="sxs-lookup"><span data-stu-id="d3b68-120">Predefined variants</span></span>
-   <span data-ttu-id="d3b68-121">Einschränkungsbasiert</span><span class="sxs-lookup"><span data-stu-id="d3b68-121">Constraint-based</span></span>
-   <span data-ttu-id="d3b68-122">Dimensionsbasiert</span><span class="sxs-lookup"><span data-stu-id="d3b68-122">Dimension-based</span></span>

<span data-ttu-id="d3b68-123">Jede Produktvariante hat eine Nummer und einen Namen, und mit den Produktvarianten-Kennungsbezeichnungen können Sie die Segmente auswählen, die in jede Produktvariantennummer oder -name einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="d3b68-124">Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:</span><span class="sxs-lookup"><span data-stu-id="d3b68-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="d3b68-125">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="d3b68-125">Product master number</span></span>
-   <span data-ttu-id="d3b68-126">Produktmastername</span><span class="sxs-lookup"><span data-stu-id="d3b68-126">Product master name</span></span>
-   <span data-ttu-id="d3b68-127">Nummernkreiswert</span><span class="sxs-lookup"><span data-stu-id="d3b68-127">Number sequence value</span></span>
-   <span data-ttu-id="d3b68-128">Textkonstante</span><span class="sxs-lookup"><span data-stu-id="d3b68-128">Text constant</span></span>
-   <span data-ttu-id="d3b68-129">Produktdimensionen</span><span class="sxs-lookup"><span data-stu-id="d3b68-129">Product dimensions</span></span>
    -   <span data-ttu-id="d3b68-130">Konfigurationskennung oder Name</span><span class="sxs-lookup"><span data-stu-id="d3b68-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="d3b68-131">Farbkennung oder Name</span><span class="sxs-lookup"><span data-stu-id="d3b68-131">Color ID or name</span></span>
    -   <span data-ttu-id="d3b68-132">Größenkennung oder Name</span><span class="sxs-lookup"><span data-stu-id="d3b68-132">Size ID or name</span></span>
    -   <span data-ttu-id="d3b68-133">Stilkennung oder Name</span><span class="sxs-lookup"><span data-stu-id="d3b68-133">Style ID or name</span></span>

<span data-ttu-id="d3b68-134">Nachdem Sie eine Produktvarianten-Kennungsnummernbezeichnung definieren, können Sie diese einer Produktdimensionsgruppe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="d3b68-135">Allen Produktmastern, die auf diese Produktdimensionsgruppe verweisen, werden dann Produktvariantennummern entsprechend der Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="d3b68-136">Allerdings können Produktvarianten-Namensbezeichnungen nicht Produktdimensionsgruppen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="d3b68-137">Sie können auch eine Produktvarianten-Kennungsbezeichnung einem Produktmaster direkt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="d3b68-138">In diesem Fall werden die Produktvarianten, die zum Produktmaster gehören, Produktvariantennummern und Namen entsprechend den Bezeichnungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="d3b68-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3b68-139">Example</span></span>

<span data-ttu-id="d3b68-140">Ein T-Shirt (TS1234) wird in drei Größen (S, M, L), in vier Farben (rot, grün, blau, gelb) sowie in zwei Stilen (Polo, mit V-Ausschnitt) hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d3b68-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="d3b68-141">Daher sind 24 Produktvarianten möglich (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="d3b68-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="d3b68-142">Sie erstellen eine Produktvarianten-Nummernbezeichnung, die die folgenden Segmente hat:</span><span class="sxs-lookup"><span data-stu-id="d3b68-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="d3b68-143">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="d3b68-143">Product master number</span></span>
2.  <span data-ttu-id="d3b68-144">Textkonstante: "-"</span><span class="sxs-lookup"><span data-stu-id="d3b68-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="d3b68-145">Farbe</span><span class="sxs-lookup"><span data-stu-id="d3b68-145">Color</span></span>
4.  <span data-ttu-id="d3b68-146">Textkonstante: "-"</span><span class="sxs-lookup"><span data-stu-id="d3b68-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="d3b68-147">Größe</span><span class="sxs-lookup"><span data-stu-id="d3b68-147">Size</span></span>
6.  <span data-ttu-id="d3b68-148">Textkonstante: "-"</span><span class="sxs-lookup"><span data-stu-id="d3b68-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="d3b68-149">Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="d3b68-149">Style</span></span>

<span data-ttu-id="d3b68-150">In diesem Fall ist die Produktvariantennummer für ein rotes kleines Polo-T-Shirt TS1234-rot-klein-Polo.</span><span class="sxs-lookup"><span data-stu-id="d3b68-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="d3b68-151">Einschränkungsbasierte Konfigurationen-Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d3b68-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="d3b68-152">Für einschränkungsbasierte Konfigurationen können Sie eine dedizierte Bezeichnung für die Konfigurationsproduktdimension erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="d3b68-153">Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:</span><span class="sxs-lookup"><span data-stu-id="d3b68-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="d3b68-154">Nummernkreiswert</span><span class="sxs-lookup"><span data-stu-id="d3b68-154">Number sequence value</span></span>
-   <span data-ttu-id="d3b68-155">Textkonstante</span><span class="sxs-lookup"><span data-stu-id="d3b68-155">Text constant</span></span>
-   <span data-ttu-id="d3b68-156">Attributwert</span><span class="sxs-lookup"><span data-stu-id="d3b68-156">Attribute value</span></span>

<span data-ttu-id="d3b68-157">Jede Komponente in einem Produktkonfigurationsmodell kann eine eigene Konfigurationsbezeichnung haben.</span><span class="sxs-lookup"><span data-stu-id="d3b68-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="d3b68-158">Nur Attribute, die der Komponente angehören, können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="d3b68-159">Attribute aus Unterkomponenten oder Benutzeranforderungen können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="d3b68-160">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3b68-160">Example</span></span>

<span data-ttu-id="d3b68-161">Ein Produktkonfigurationsmodell hat eine Stammkomponente, die zwei Attribute hat:</span><span class="sxs-lookup"><span data-stu-id="d3b68-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="d3b68-162">Material (Plastik, Holz Stahl)</span><span class="sxs-lookup"><span data-stu-id="d3b68-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="d3b68-163">Länge (10… 100)</span><span class="sxs-lookup"><span data-stu-id="d3b68-163">Length (10...100)</span></span>

<span data-ttu-id="d3b68-164">Sie erstellen eine Konfigurationsbezeichnung, die die folgenden Segmente hat:</span><span class="sxs-lookup"><span data-stu-id="d3b68-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="d3b68-165">Attributwert: Material</span><span class="sxs-lookup"><span data-stu-id="d3b68-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="d3b68-166">Textkonstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="d3b68-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="d3b68-167">Attributwert: Länge</span><span class="sxs-lookup"><span data-stu-id="d3b68-167">Attribute value: Length</span></span>

<span data-ttu-id="d3b68-168">In diesem Fall ist die Konfigurationskennung für Holzmaterial mit einer Länge von 78 WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="d3b68-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="d3b68-169">Dimensionsbasierte Konfigurationsbezeichnung</span><span class="sxs-lookup"><span data-stu-id="d3b68-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="d3b68-170">Für dimensionsbasierte Konfigurationen können Sie eine dedizierte Bezeichnung für die Konfigurationsproduktdimension erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="d3b68-171">Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:</span><span class="sxs-lookup"><span data-stu-id="d3b68-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="d3b68-172">Nummernkreiswert</span><span class="sxs-lookup"><span data-stu-id="d3b68-172">Number sequence value</span></span>
-   <span data-ttu-id="d3b68-173">Textkonstante</span><span class="sxs-lookup"><span data-stu-id="d3b68-173">Text constant</span></span>
-   <span data-ttu-id="d3b68-174">Konfigurationsgruppenartikel</span><span class="sxs-lookup"><span data-stu-id="d3b68-174">Configuration group item</span></span>

<span data-ttu-id="d3b68-175">Sie können eine Konfigurationsbezeichnung für eine Stückliste (BOM) definieren.</span><span class="sxs-lookup"><span data-stu-id="d3b68-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="d3b68-176">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3b68-176">Example</span></span>

<span data-ttu-id="d3b68-177">Eine Stückliste besitzt vier Stücklistenpositionen, die in zwei Variantengruppen unterteilt sind:</span><span class="sxs-lookup"><span data-stu-id="d3b68-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="d3b68-178">Stücklistenposition: M0007, Standardgehäuse</span><span class="sxs-lookup"><span data-stu-id="d3b68-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="d3b68-179">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="d3b68-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="d3b68-180">Stücklistenposition: M0008, Spitzengehäuse</span><span class="sxs-lookup"><span data-stu-id="d3b68-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="d3b68-181">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="d3b68-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="d3b68-182">Stücklistenposition: M0021, Vordergrill Tuch</span><span class="sxs-lookup"><span data-stu-id="d3b68-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="d3b68-183">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="d3b68-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="d3b68-184">Stücklistenposition: M0022, Vordergrill Metall</span><span class="sxs-lookup"><span data-stu-id="d3b68-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="d3b68-185">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="d3b68-185">Configuration group: Front grill</span></span>

<span data-ttu-id="d3b68-186">Sie erstellen eine Konfigurationsbezeichnung, die die folgenden Segmente hat:</span><span class="sxs-lookup"><span data-stu-id="d3b68-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="d3b68-187">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="d3b68-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="d3b68-188">Textkonstante: "&"</span><span class="sxs-lookup"><span data-stu-id="d3b68-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="d3b68-189">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="d3b68-189">Configuration group: Front grill</span></span>

<span data-ttu-id="d3b68-190">In diesem Fall ist die Konfigurationskennung für ein Standardgehäuse mit Tuchvordergrill M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="d3b68-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="d3b68-191">Bezeichnung für eine Kombination mit Produktvarianten und Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d3b68-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="d3b68-192">Wenn Sie entweder die einschränkungsbasierte Konfigurationstechnologie oder die dimensionsbasierte Konfigurationstechnologie verwenden, um Produktvarianten für einen Produktmaster zu konfigurieren, können die Produktvariantennummern der Produktvarianten die Bezeichnung aus der Konfigurationsdimension umfassen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="d3b68-193">Folgen Sie diesen Schritten, um Varianten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d3b68-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="d3b68-194">Definieren Sie auf der Seite **Produktbezeichnung** eine Produktvarianten-Nummernbezeichnung, die die Konfigurationsdimension umfasst.</span><span class="sxs-lookup"><span data-stu-id="d3b68-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="d3b68-195">Weisen Sie die Bezeichnung einer Produktdimensionsgruppe zu, die die Konfigurationsdimension besitzt.</span><span class="sxs-lookup"><span data-stu-id="d3b68-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="d3b68-196">Definieren Sie eine Konfigurationsbezeichnung für die Komponenten oder die Stücklisten, die für das Konfigurieren von Produktvarianten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="d3b68-197">Sie können auch eine Bezeichnungen für die Produktvariantennamen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="d3b68-198">Die Produktvariantennamen können konfiguriert werden, um die Konfigurationskennung oder den Namen zu umfassen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="d3b68-199">Beispiele für einschränkungsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d3b68-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="d3b68-200">Für dieses Beispiel können Sie eine Produktvarianten-Nummernbezeichnung verwenden, die aus den folgenden Segmenten besteht:</span><span class="sxs-lookup"><span data-stu-id="d3b68-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="d3b68-201">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="d3b68-201">Product master number</span></span>
2.  <span data-ttu-id="d3b68-202">Textkonstante "\_"</span><span class="sxs-lookup"><span data-stu-id="d3b68-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="d3b68-203">Variante</span><span class="sxs-lookup"><span data-stu-id="d3b68-203">Configuration</span></span>

<span data-ttu-id="d3b68-204">Die Konfigurationsbezeichnung besteht aus den folgenden Segmenten:</span><span class="sxs-lookup"><span data-stu-id="d3b68-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="d3b68-205">Attributwert: Material</span><span class="sxs-lookup"><span data-stu-id="d3b68-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="d3b68-206">Textkonstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="d3b68-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="d3b68-207">Attributwert: Länge</span><span class="sxs-lookup"><span data-stu-id="d3b68-207">Attribute value: Length</span></span>

<span data-ttu-id="d3b68-208">Sie geben die folgenden Werte für Segmente ein:</span><span class="sxs-lookup"><span data-stu-id="d3b68-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="d3b68-209">Produktmasternummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="d3b68-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="d3b68-210">Material = **Plastik**</span><span class="sxs-lookup"><span data-stu-id="d3b68-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="d3b68-211">Länge = **12**</span><span class="sxs-lookup"><span data-stu-id="d3b68-211">Length = **12**</span></span>

<span data-ttu-id="d3b68-212">In diesem Fall wird die Produktvariantennummer M0099\_PlasticAAA12 lauten.</span><span class="sxs-lookup"><span data-stu-id="d3b68-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="d3b68-213">Beispiele für einschränkungsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d3b68-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="d3b68-214">Für dieses Beispiel können Sie eine Produktvarianten-Nummernbezeichnung verwenden, die aus den folgenden Segmenten besteht:</span><span class="sxs-lookup"><span data-stu-id="d3b68-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="d3b68-215">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="d3b68-215">Product master number</span></span>
2.  <span data-ttu-id="d3b68-216">Textkonstante "//"</span><span class="sxs-lookup"><span data-stu-id="d3b68-216">Text constant "//"</span></span>
3.  <span data-ttu-id="d3b68-217">Variante</span><span class="sxs-lookup"><span data-stu-id="d3b68-217">Configuration</span></span>

<span data-ttu-id="d3b68-218">Die Konfigurationsbezeichnung besteht aus den folgenden Segmenten:</span><span class="sxs-lookup"><span data-stu-id="d3b68-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="d3b68-219">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="d3b68-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="d3b68-220">Textkonstante: "&"</span><span class="sxs-lookup"><span data-stu-id="d3b68-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="d3b68-221">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="d3b68-221">Configuration group: Front grill</span></span>

<span data-ttu-id="d3b68-222">Sie geben die folgenden Werte für Segmente ein:</span><span class="sxs-lookup"><span data-stu-id="d3b68-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="d3b68-223">Produktmasternummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="d3b68-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="d3b68-224">Gehäuse = **M0008**</span><span class="sxs-lookup"><span data-stu-id="d3b68-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="d3b68-225">Vordergrill = **M0022**</span><span class="sxs-lookup"><span data-stu-id="d3b68-225">Front grill = **M0022**</span></span>

<span data-ttu-id="d3b68-226">In diesem Fall wird die Produktvariantennummer D0123//M0008&M0022 lauten.</span><span class="sxs-lookup"><span data-stu-id="d3b68-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="d3b68-227">Anzahl von Konflikten</span><span class="sxs-lookup"><span data-stu-id="d3b68-227">Numbering conflicts</span></span>
<span data-ttu-id="d3b68-228">In einigen Fällen erzeugt eine Produktvarianten-Nummernbezeichnung, die Sie eingerichtet haben, möglicherweise keine eindeutigen Produktvariantennummern.</span><span class="sxs-lookup"><span data-stu-id="d3b68-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="d3b68-229">Die Produktvariantennummern sind beispielsweise nicht eindeutig, wenn eine aktive Produktdimension nicht in der Bezeichnung für einen Produktmaster enthalten ist, der die vordefinierte Technologie für Variantenkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3b68-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="d3b68-230">Die Art, wie Sie Konflikte handhaben, ist je nach Konfigurationstechnik unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="d3b68-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="d3b68-231">Vordefinierte Variante</span><span class="sxs-lookup"><span data-stu-id="d3b68-231">Predefined variants</span></span>

<span data-ttu-id="d3b68-232">Ein Fehler tritt auf, wenn Sie manuell oder automatisch versuchen, Produktvarianten zu erstellen, bzw. zu generieren, und mehr als eine Produktvariante letztendlich dieselbe Produktvariantennummer besitzt.</span><span class="sxs-lookup"><span data-stu-id="d3b68-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="d3b68-233">Um dieses Szenarios zu vermeiden, sollten Sie alle aktiven Produktdimensionen in der Produktdimensionsgruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3b68-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="d3b68-234">Alternativ beziehen Sie einen Nummernkreis ein, um sicherzustellen, dass die Produktvariantennummern eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="d3b68-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="d3b68-235">Einschränkungsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d3b68-235">Constraint-based configurations</span></span>

<span data-ttu-id="d3b68-236">Abhängig von der Bezeichung versucht das System möglicherweise, eine nicht eindeutige Produktvariantennummer zu einer Konfiguration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d3b68-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="d3b68-237">In diesem Fall verwendet das System stattdessen den Nummernkreis für die Konfigurationsdimension als Produktvariantennummer, und Sie erhalten eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="d3b68-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="d3b68-238">Um dieses Szenarios zu vermeiden, sollten Sie genügend Attribute in die Bezeichnung einbeziehen, um eindeutige Produktvariantennummern zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="d3b68-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="d3b68-239">Sie sollten auch sicherstellen, dass die Option **Wiederverwenden** für die Komponente eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d3b68-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="d3b68-240">Dimensionsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d3b68-240">Dimension-based configurations</span></span>

<span data-ttu-id="d3b68-241">Während eines Schritts im Konfigurationsprozess schlägt das System einen Konfigurationswert gemäß der Bezeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="d3b68-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="d3b68-242">In diesem Schritt können Sie den Konfigurationswert manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="d3b68-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="d3b68-243">Wenn Sie die Konfiguration speichern, überprüft das System, dass der Konfigurationswert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="d3b68-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="d3b68-244">Wenn der Wert, den Sie eingegeben haben, nicht eindeutig ist, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="d3b68-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="d3b68-245">Um die Konfiguration zu speichern, müssen Sie einen eindeutigen Konfigurationswert eingeben.</span><span class="sxs-lookup"><span data-stu-id="d3b68-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="d3b68-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3b68-246">See also</span></span>
--------

[<span data-ttu-id="d3b68-247">Erstellen einer Produktnummerenbezeichnung für vordefinierte Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="d3b68-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="d3b68-248">Erstellen einer Produktnummerenbezeichnung für konfigurierte Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="d3b68-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



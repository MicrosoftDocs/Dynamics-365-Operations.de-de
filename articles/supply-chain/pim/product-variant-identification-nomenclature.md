---
title: Bezeichnung der Produktvariantennummern und Namen
description: In diesem Thema wird beschrieben, wie Sie eine Produktnummernbezeichnung einrichten können, um das feste Format [Produktmasternummer – Konfiguration – Größe – Farbe – Stil] zu ersetzen.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f17f9e1401c68c11e23f327d96028663470b3245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011321"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="b8cb4-103">Bezeichnung der Produktvariantennummern und Namen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8cb4-104">In diesem Thema wird beschrieben, wie Sie eine Produktnummernbezeichnung einrichten können, um das feste Format [Produktmasternummer – Konfiguration – Größe – Farbe – Stil] zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="b8cb4-105">Die neue Bezeichnung hat ein gezieltes Format, das die Produktmasternummer, aktive Produktdimensionen und Texttrennzeichen Ihrer Wahl umfasst.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="b8cb4-106">Darüber hinaus können Sie auch eine Bezeichnung für Produktnamen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="b8cb4-107">Sie können schließlich auch eine Bezeichnung erstellen, um Konfigurationen zu identifizieren, die vom einschränkungsbasierten Produktkonfigurator erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="b8cb4-108">Diese Bezeichnungen können Attribute Ihrer Wahl enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="b8cb4-109">Die neuen Bezeichnungen für Produktvariantennummern und Produktvariantennamen ermöglichen es Ihnen, Segmente in die Bezeichner für Produktvarianten einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="b8cb4-110">Diese Segmente können die Produktmasternummer und den Produktmasternamen, die Produktdimensionskennungen und -namen, die Nummernkreise, Textkonstanten und Attribute umfassen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="b8cb4-111">Mit dieser Funktionalität können Sie schnell eine bestimmte Produktvariante suchen, wenn einen Auftrag oder eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="b8cb4-112">Sie erstellen Bezeichnungen sowohl für Produktvariantennummern als auch Produktvariantennamen mithilfe der Seite **Produktbezeichnung**.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="b8cb4-113">Um diese Seite zu öffnen, klicken Sie auf **Produktinformationsverwaltung** &gt; **Setup**.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="b8cb4-114">Bezeichnung der vordefinierten Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="b8cb4-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="b8cb4-115">Produktvarianten für Produktmaster werden entsprechend einer der drei Konfigurationstechnologien generiert:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="b8cb4-116">Vordefinierte Variante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-116">Predefined variants</span></span>
-   <span data-ttu-id="b8cb4-117">Einschränkungsbasiert</span><span class="sxs-lookup"><span data-stu-id="b8cb4-117">Constraint-based</span></span>
-   <span data-ttu-id="b8cb4-118">Dimensionsbasiert</span><span class="sxs-lookup"><span data-stu-id="b8cb4-118">Dimension-based</span></span>

<span data-ttu-id="b8cb4-119">Jede Produktvariante hat eine Nummer und einen Namen, und mit den Produktvarianten-Kennungsbezeichnungen können Sie die Segmente auswählen, die in jede Produktvariantennummer oder -name einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="b8cb4-120">Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="b8cb4-121">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="b8cb4-121">Product master number</span></span>
-   <span data-ttu-id="b8cb4-122">Produktmastername</span><span class="sxs-lookup"><span data-stu-id="b8cb4-122">Product master name</span></span>
-   <span data-ttu-id="b8cb4-123">Nummernkreiswert</span><span class="sxs-lookup"><span data-stu-id="b8cb4-123">Number sequence value</span></span>
-   <span data-ttu-id="b8cb4-124">Textkonstante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-124">Text constant</span></span>
-   <span data-ttu-id="b8cb4-125">Produktdimensionen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-125">Product dimensions</span></span>
    -   <span data-ttu-id="b8cb4-126">Konfigurationskennung oder Name</span><span class="sxs-lookup"><span data-stu-id="b8cb4-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="b8cb4-127">Farbkennung oder Name</span><span class="sxs-lookup"><span data-stu-id="b8cb4-127">Color ID or name</span></span>
    -   <span data-ttu-id="b8cb4-128">Größenkennung oder Name</span><span class="sxs-lookup"><span data-stu-id="b8cb4-128">Size ID or name</span></span>
    -   <span data-ttu-id="b8cb4-129">Stilkennung oder Name</span><span class="sxs-lookup"><span data-stu-id="b8cb4-129">Style ID or name</span></span>

<span data-ttu-id="b8cb4-130">Nachdem Sie eine Produktvarianten-Kennungsnummernbezeichnung definieren, können Sie diese einer Produktdimensionsgruppe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="b8cb4-131">Allen Produktmastern, die auf diese Produktdimensionsgruppe verweisen, werden dann Produktvariantennummern entsprechend der Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="b8cb4-132">Allerdings können Produktvarianten-Namensbezeichnungen nicht Produktdimensionsgruppen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="b8cb4-133">Sie können auch eine Produktvarianten-Kennungsbezeichnung einem Produktmaster direkt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="b8cb4-134">In diesem Fall werden die Produktvarianten, die zum Produktmaster gehören, Produktvariantennummern und Namen entsprechend den Bezeichnungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="b8cb4-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8cb4-135">Example</span></span>

<span data-ttu-id="b8cb4-136">Ein T-Shirt (TS1234) wird in drei Größen (S, M, L), in vier Farben (rot, grün, blau, gelb) sowie in zwei Stilen (Polo, mit V-Ausschnitt) hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="b8cb4-137">Daher sind 24 Produktvarianten möglich (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="b8cb4-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="b8cb4-138">Sie erstellen eine Produktvarianten-Nummernbezeichnung, die die folgenden Segmente hat:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-139">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="b8cb4-139">Product master number</span></span>
2.  <span data-ttu-id="b8cb4-140">Textkonstante: "-"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="b8cb4-141">Farbe</span><span class="sxs-lookup"><span data-stu-id="b8cb4-141">Color</span></span>
4.  <span data-ttu-id="b8cb4-142">Textkonstante: "-"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="b8cb4-143">Größe</span><span class="sxs-lookup"><span data-stu-id="b8cb4-143">Size</span></span>
6.  <span data-ttu-id="b8cb4-144">Textkonstante: "-"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="b8cb4-145">Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="b8cb4-145">Style</span></span>

<span data-ttu-id="b8cb4-146">In diesem Fall ist die Produktvariantennummer für ein rotes kleines Polo-T-Shirt TS1234-rot-klein-Polo.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="b8cb4-147">Einschränkungsbasierte Konfigurationen-Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="b8cb4-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="b8cb4-148">Für einschränkungsbasierte Konfigurationen können Sie eine dedizierte Bezeichnung für die Konfigurationsproduktdimension erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="b8cb4-149">Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="b8cb4-150">Nummernkreiswert</span><span class="sxs-lookup"><span data-stu-id="b8cb4-150">Number sequence value</span></span>
-   <span data-ttu-id="b8cb4-151">Textkonstante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-151">Text constant</span></span>
-   <span data-ttu-id="b8cb4-152">Attributwert</span><span class="sxs-lookup"><span data-stu-id="b8cb4-152">Attribute value</span></span>

<span data-ttu-id="b8cb4-153">Jede Komponente in einem Produktkonfigurationsmodell kann eine eigene Konfigurationsbezeichnung haben.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="b8cb4-154">Nur Attribute, die der Komponente angehören, können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="b8cb4-155">Attribute aus Unterkomponenten oder Benutzeranforderungen können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="b8cb4-156">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8cb4-156">Example</span></span>

<span data-ttu-id="b8cb4-157">Ein Produktkonfigurationsmodell hat eine Stammkomponente, die zwei Attribute hat:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="b8cb4-158">Material (Plastik, Holz Stahl)</span><span class="sxs-lookup"><span data-stu-id="b8cb4-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="b8cb4-159">Länge (10… 100)</span><span class="sxs-lookup"><span data-stu-id="b8cb4-159">Length (10...100)</span></span>

<span data-ttu-id="b8cb4-160">Sie erstellen eine Konfigurationsbezeichnung, die die folgenden Segmente hat:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-161">Attributwert: Material</span><span class="sxs-lookup"><span data-stu-id="b8cb4-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="b8cb4-162">Textkonstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="b8cb4-163">Attributwert: Länge</span><span class="sxs-lookup"><span data-stu-id="b8cb4-163">Attribute value: Length</span></span>

<span data-ttu-id="b8cb4-164">In diesem Fall ist die Konfigurationskennung für Holzmaterial mit einer Länge von 78 WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="b8cb4-165">Dimensionsbasierte Konfigurationsbezeichnung</span><span class="sxs-lookup"><span data-stu-id="b8cb4-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="b8cb4-166">Für dimensionsbasierte Konfigurationen können Sie eine dedizierte Bezeichnung für die Konfigurationsproduktdimension erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="b8cb4-167">Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="b8cb4-168">Nummernkreiswert</span><span class="sxs-lookup"><span data-stu-id="b8cb4-168">Number sequence value</span></span>
-   <span data-ttu-id="b8cb4-169">Textkonstante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-169">Text constant</span></span>
-   <span data-ttu-id="b8cb4-170">Konfigurationsgruppenartikel</span><span class="sxs-lookup"><span data-stu-id="b8cb4-170">Configuration group item</span></span>

<span data-ttu-id="b8cb4-171">Sie können eine Konfigurationsbezeichnung für eine Stückliste (BOM) definieren.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="b8cb4-172">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8cb4-172">Example</span></span>

<span data-ttu-id="b8cb4-173">Eine Stückliste besitzt vier Stücklistenpositionen, die in zwei Variantengruppen unterteilt sind:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="b8cb4-174">Stücklistenposition: M0007, Standardgehäuse</span><span class="sxs-lookup"><span data-stu-id="b8cb4-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="b8cb4-175">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="b8cb4-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="b8cb4-176">Stücklistenposition: M0008, Spitzengehäuse</span><span class="sxs-lookup"><span data-stu-id="b8cb4-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="b8cb4-177">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="b8cb4-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="b8cb4-178">Stücklistenposition: M0021, Vordergrill Tuch</span><span class="sxs-lookup"><span data-stu-id="b8cb4-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="b8cb4-179">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="b8cb4-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="b8cb4-180">Stücklistenposition: M0022, Vordergrill Metall</span><span class="sxs-lookup"><span data-stu-id="b8cb4-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="b8cb4-181">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="b8cb4-181">Configuration group: Front grill</span></span>

<span data-ttu-id="b8cb4-182">Sie erstellen eine Konfigurationsbezeichnung, die die folgenden Segmente hat:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-183">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="b8cb4-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="b8cb4-184">Textkonstante: "&"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="b8cb4-185">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="b8cb4-185">Configuration group: Front grill</span></span>

<span data-ttu-id="b8cb4-186">In diesem Fall lautet die Konfigurationskennung für ein Standardgehäuse mit Tuchvordergrill M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="b8cb4-187">Bezeichnung für eine Kombination mit Produktvarianten und Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="b8cb4-188">Wenn Sie entweder die einschränkungsbasierte Konfigurationstechnologie oder die dimensionsbasierte Konfigurationstechnologie verwenden, um Produktvarianten für einen Produktmaster zu konfigurieren, können die Produktvariantennummern der Produktvarianten die Bezeichnung aus der Konfigurationsdimension umfassen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="b8cb4-189">Folgen Sie diesen Schritten, um Varianten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="b8cb4-190">Definieren Sie auf der Seite **Produktbezeichnung** eine Produktvarianten-Nummernbezeichnung, die die Konfigurationsdimension umfasst.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="b8cb4-191">Weisen Sie die Bezeichnung einer Produktdimensionsgruppe zu, die die Konfigurationsdimension besitzt.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="b8cb4-192">Definieren Sie eine Konfigurationsbezeichnung für die Komponenten oder die Stücklisten, die für das Konfigurieren von Produktvarianten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="b8cb4-193">Sie können auch eine Bezeichnungen für die Produktvariantennamen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="b8cb4-194">Die Produktvariantennamen können konfiguriert werden, um die Konfigurationskennung oder den Namen zu umfassen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="b8cb4-195">Beispiele für einschränkungsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="b8cb4-196">Für dieses Beispiel können Sie eine Produktvarianten-Nummernbezeichnung verwenden, die aus den folgenden Segmenten besteht:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-197">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="b8cb4-197">Product master number</span></span>
2.  <span data-ttu-id="b8cb4-198">Textkonstante "\_"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="b8cb4-199">Variante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-199">Configuration</span></span>

<span data-ttu-id="b8cb4-200">Die Konfigurationsbezeichnung besteht aus den folgenden Segmenten:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-201">Attributwert: Material</span><span class="sxs-lookup"><span data-stu-id="b8cb4-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="b8cb4-202">Textkonstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="b8cb4-203">Attributwert: Länge</span><span class="sxs-lookup"><span data-stu-id="b8cb4-203">Attribute value: Length</span></span>

<span data-ttu-id="b8cb4-204">Sie geben die folgenden Werte für Segmente ein:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="b8cb4-205">Produktmasternummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="b8cb4-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="b8cb4-206">Material = **Plastik**</span><span class="sxs-lookup"><span data-stu-id="b8cb4-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="b8cb4-207">Länge = **12**</span><span class="sxs-lookup"><span data-stu-id="b8cb4-207">Length = **12**</span></span>

<span data-ttu-id="b8cb4-208">In diesem Fall wird die Produktvariantennummer M0099\_PlasticAAA12 lauten.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="b8cb4-209">Beispiele für einschränkungsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="b8cb4-210">Für dieses Beispiel können Sie eine Produktvarianten-Nummernbezeichnung verwenden, die aus den folgenden Segmenten besteht:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-211">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="b8cb4-211">Product master number</span></span>
2.  <span data-ttu-id="b8cb4-212">Textkonstante "//"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-212">Text constant "//"</span></span>
3.  <span data-ttu-id="b8cb4-213">Variante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-213">Configuration</span></span>

<span data-ttu-id="b8cb4-214">Die Konfigurationsbezeichnung besteht aus den folgenden Segmenten:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="b8cb4-215">Konfigurationsgruppe: Gehäuse</span><span class="sxs-lookup"><span data-stu-id="b8cb4-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="b8cb4-216">Textkonstante: "&"</span><span class="sxs-lookup"><span data-stu-id="b8cb4-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="b8cb4-217">Konfigurationsgruppe: Vordergrill</span><span class="sxs-lookup"><span data-stu-id="b8cb4-217">Configuration group: Front grill</span></span>

<span data-ttu-id="b8cb4-218">Sie geben die folgenden Werte für Segmente ein:</span><span class="sxs-lookup"><span data-stu-id="b8cb4-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="b8cb4-219">Produktmasternummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="b8cb4-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="b8cb4-220">Gehäuse = **M0008**</span><span class="sxs-lookup"><span data-stu-id="b8cb4-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="b8cb4-221">Vordergrill = **M0022**</span><span class="sxs-lookup"><span data-stu-id="b8cb4-221">Front grill = **M0022**</span></span>

<span data-ttu-id="b8cb4-222">In diesem Fall wird die Produktvariantennummer D0123//M0008&M0022 lauten.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="b8cb4-223">Anzahl von Konflikten</span><span class="sxs-lookup"><span data-stu-id="b8cb4-223">Numbering conflicts</span></span>
<span data-ttu-id="b8cb4-224">In einigen Fällen erzeugt eine Produktvarianten-Nummernbezeichnung, die Sie eingerichtet haben, möglicherweise keine eindeutigen Produktvariantennummern.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="b8cb4-225">Die Produktvariantennummern sind beispielsweise nicht eindeutig, wenn eine aktive Produktdimension nicht in der Bezeichnung für einen Produktmaster enthalten ist, der die vordefinierte Technologie für Variantenkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="b8cb4-226">Die Art, wie Sie Konflikte handhaben, ist je nach Konfigurationstechnik unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="b8cb4-227">Vordefinierte Variante</span><span class="sxs-lookup"><span data-stu-id="b8cb4-227">Predefined variants</span></span>

<span data-ttu-id="b8cb4-228">Ein Fehler tritt auf, wenn Sie manuell oder automatisch versuchen, Produktvarianten zu erstellen, bzw. zu generieren, und mehr als eine Produktvariante letztendlich dieselbe Produktvariantennummer besitzt.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="b8cb4-229">Um dieses Szenarios zu vermeiden, sollten Sie alle aktiven Produktdimensionen in der Produktdimensionsgruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="b8cb4-230">Alternativ beziehen Sie einen Nummernkreis ein, um sicherzustellen, dass die Produktvariantennummern eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="b8cb4-231">Einschränkungsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-231">Constraint-based configurations</span></span>

<span data-ttu-id="b8cb4-232">Abhängig von der Bezeichung versucht das System möglicherweise, eine nicht eindeutige Produktvariantennummer zu einer Konfiguration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="b8cb4-233">In diesem Fall verwendet das System stattdessen den Nummernkreis für die Konfigurationsdimension als Produktvariantennummer, und Sie erhalten eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="b8cb4-234">Um dieses Szenarios zu vermeiden, sollten Sie genügend Attribute in die Bezeichnung einbeziehen, um eindeutige Produktvariantennummern zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="b8cb4-235">Sie sollten auch sicherstellen, dass die Option **Wiederverwenden** für die Komponente eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="b8cb4-236">Dimensionsbasierte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-236">Dimension-based configurations</span></span>

<span data-ttu-id="b8cb4-237">Während eines Schritts im Konfigurationsprozess schlägt das System einen Konfigurationswert gemäß der Bezeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="b8cb4-238">In diesem Schritt können Sie den Konfigurationswert manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="b8cb4-239">Wenn Sie die Konfiguration speichern, überprüft das System, dass der Konfigurationswert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="b8cb4-240">Wenn der Wert, den Sie eingegeben haben, nicht eindeutig ist, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="b8cb4-241">Um die Konfiguration zu speichern, müssen Sie einen eindeutigen Konfigurationswert eingeben.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b8cb4-242">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-242">Additional resources</span></span>
--------

[<span data-ttu-id="b8cb4-243">Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="b8cb4-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="b8cb4-244">Erstellen einer Produktnummerenbezeichnung für konfigurierte Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="b8cb4-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


---
title: Maßeinheitsumrechnungen für Produktvarianten
description: In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen für Produktvarianten eingerichtet werden können. Zudem enthält es ein Beispiel für die Einstellung.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ddb6c614ede98e46e46ff284a1a16669bbaaaf66
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258046"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="c1d68-104">Maßeinheitsumrechnungen für Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="c1d68-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1d68-105">In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen für verschiedene Produktvarianten eingerichtet werden können.</span><span class="sxs-lookup"><span data-stu-id="c1d68-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="c1d68-106">Sie können Produktvarianten verwenden, um Variationen eines einzelnen Produkts zu erstellen, anstatt mehrere einzelne Produkte zu erstellen, die verwaltet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c1d68-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="c1d68-107">Eine Produktvariante kann beispielsweise ein T-Shirt einer bestimmten Größe und Farbe sein.</span><span class="sxs-lookup"><span data-stu-id="c1d68-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="c1d68-108">Bisher konnten Einheitenumrechnungen nur im Produktmaster eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d68-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="c1d68-109">Daher hatten alle Produktvarianten die gleichen Regeln für die Einheitenumrechnung.</span><span class="sxs-lookup"><span data-stu-id="c1d68-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="c1d68-110">Wenn jedoch die Funktion *Umrechnung von Maßeinheiten für Produktvarianten* aktiviert ist, Ihre T-Shirts in Kartons verkauft werden, und die Anzahl der T-Shirts, die in einem Karton verpackt werden können, von der Größe der T-Shirts abhängt, können Sie jetzt Einheitenumrechnungen zwischen den verschiedenen Shirtgrößen und den Kartons, die für die Verpackung verwendet werden, einrichten.</span><span class="sxs-lookup"><span data-stu-id="c1d68-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="c1d68-111">Funktion in Ihrem System aktivieren</span><span class="sxs-lookup"><span data-stu-id="c1d68-111">Turn on the feature in your system</span></span>

<span data-ttu-id="c1d68-112">Wenn Sie diese Funktion in Ihrem System noch nicht sehen, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), und aktivieren Sie die Funktion *Umrechnung von Maßeinheiten für Produktvarianten*.</span><span class="sxs-lookup"><span data-stu-id="c1d68-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="c1d68-113">Einrichten eines Produkts für Einheitenumrechnung pro Variante</span><span class="sxs-lookup"><span data-stu-id="c1d68-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="c1d68-114">Protuktvarianten können nur für Produkte des Typs Produktmaster erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c1d68-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="c1d68-115">Weitere Informationen finden Sie unter [Erstellen eines Produktmasters](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="c1d68-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="c1d68-116">Die Funktion *Umrechnung von Maßeinheiten für Produktvarianten* ist nicht für Produkte verfügbar, die für Artikelgewichtsprozesse eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="c1d68-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="c1d68-117">Führen Sie die folgenden Schritte aus, um einen Produktmaster für die Unterstützung der Einheitenumrechnung pro Variante zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c1d68-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="c1d68-118">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**.</span><span class="sxs-lookup"><span data-stu-id="c1d68-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="c1d68-119">Erstellen oder öffnen Sie einen Produktmaster, um zur Seite **Produktdetails** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c1d68-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="c1d68-120">Setzen Sie die Option auf **Konvertierung von Maßeinheiten aktivieren** auf *Ja*.</span><span class="sxs-lookup"><span data-stu-id="c1d68-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="c1d68-121">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Einheitenumrechnung**.</span><span class="sxs-lookup"><span data-stu-id="c1d68-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="c1d68-122">Die Seite **Einheitenumrechnungen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c1d68-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="c1d68-123">Wählen Sie eine der folgenden Registerkarten aus:</span><span class="sxs-lookup"><span data-stu-id="c1d68-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="c1d68-124">**Klasseninterne Umrechnungen** – Wählen Sie diese Registerkarte aus, um zwischen Einheiten zu konvertieren, die zur gleichen Einheitenklasse gehören.</span><span class="sxs-lookup"><span data-stu-id="c1d68-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="c1d68-125">**Klassenübergreifende Umrechnungen** – Wählen Sie diese Registerkarte aus, um zwischen Einheiten zu konvertieren, die zu verschiedenen Einheitenklassen gehören.</span><span class="sxs-lookup"><span data-stu-id="c1d68-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="c1d68-126">Klicken Sie zum Hinzufügen einer neuen Einheitsumrechnung auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c1d68-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="c1d68-127">Setzen Sie das Feld **Konvertierung erstellen für** auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c1d68-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="c1d68-128">**Produkt** – Wenn Sie diesen Wert auswählen, kann eine Einheitenumrechnung für den Produktmaster eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d68-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="c1d68-129">Diese Einheitenumrechnung wird als Fallback für alle Produktvarianten verwendet, für die keine Einheitenumrechnung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c1d68-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="c1d68-130">**Produktvariante** – Wenn Sie diesen Wert auswählen, kann eine Einheitenumrechnung für eine spezifische Produktvariante eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d68-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="c1d68-131">Verwenden Sie das Feld **Produktvariante** zur Auswahl der Variante.</span><span class="sxs-lookup"><span data-stu-id="c1d68-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="c1d68-132">![Hinzufügen einer neuen Einheitenumrechnung](media/uom-new-conversion.png "Hinzufügen einer neuen Einheitenumrechnung")</span><span class="sxs-lookup"><span data-stu-id="c1d68-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="c1d68-133">Verwenden Sie die anderen verfügbaren Felder, um Ihre Einheitenumrechnung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c1d68-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="c1d68-134">Wählen Sie **OK**, um die neue Einheitenumrechnung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c1d68-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="c1d68-135">Sie können die Seite **Einheitenumrechnungen** für ein Produkt oder eine Produktvariante von einer der folgenden Seiten öffnen:</span><span class="sxs-lookup"><span data-stu-id="c1d68-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="c1d68-136">Produktdetails</span><span class="sxs-lookup"><span data-stu-id="c1d68-136">Product details</span></span>
> - <span data-ttu-id="c1d68-137">Details für freigegebene Produkte</span><span class="sxs-lookup"><span data-stu-id="c1d68-137">Released products details</span></span>
> - <span data-ttu-id="c1d68-138">Freigegebene Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="c1d68-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c1d68-139">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="c1d68-139">Example scenario</span></span>

<span data-ttu-id="c1d68-140">In diesem Szenarion verkauft ein Unternehmen die T-Shirts in kleinen, mittig großen und extra-großen Größen.</span><span class="sxs-lookup"><span data-stu-id="c1d68-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="c1d68-141">Das T-Shirt wird als Produkt definiert, und die verschiedenen Größen werden als Varianten dieses Produkts definiert.</span><span class="sxs-lookup"><span data-stu-id="c1d68-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="c1d68-142">Die Shirts sind in Kartons verpackt.</span><span class="sxs-lookup"><span data-stu-id="c1d68-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="c1d68-143">Für kleine, mittlere und große Größen können fünf Shirts in jeder Box enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c1d68-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="c1d68-144">Bei der Größe „extra-groß“ ist jedoch nur Platz für vier Shirts in jeder Schachtel.</span><span class="sxs-lookup"><span data-stu-id="c1d68-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="c1d68-145">Das Unternehmen möchte die verschiedenen Varianten in der Einheit *Stücke* nachverfolgen, aber verkauft die T-Shirts in der Einheit *Kartons*.</span><span class="sxs-lookup"><span data-stu-id="c1d68-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="c1d68-146">Für kleine, mittlere und große Größen beträgt die Umrechnung zwischen der Inventareinheit und der Verkaufseinheit 1 Karton = 5 Stück.</span><span class="sxs-lookup"><span data-stu-id="c1d68-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="c1d68-147">Für die extra große Größe beträgt die Umrechnung 1 Karton = 4 Stück.</span><span class="sxs-lookup"><span data-stu-id="c1d68-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="c1d68-148">Öffnen Sie auf der Seite **Freigegebene Produktdetails** für das Produkt **T-Shirt** die Seite **Einheitenumrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="c1d68-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="c1d68-149">Auf der Seite **Einheitenumrechnungen** richten Sie die folgende Einheitenumrechnung für die **X-große** Freigabenproduktvariante ein.</span><span class="sxs-lookup"><span data-stu-id="c1d68-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="c1d68-150">Feld</span><span class="sxs-lookup"><span data-stu-id="c1d68-150">Field</span></span>                 | <span data-ttu-id="c1d68-151">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c1d68-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="c1d68-152">Konvertierung erstellen für</span><span class="sxs-lookup"><span data-stu-id="c1d68-152">Create conversion for</span></span> | <span data-ttu-id="c1d68-153">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="c1d68-153">Product variant</span></span>         |
    | <span data-ttu-id="c1d68-154">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="c1d68-154">Product variant</span></span>       | <span data-ttu-id="c1d68-155">T-Shirt: : X-groß : :</span><span class="sxs-lookup"><span data-stu-id="c1d68-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="c1d68-156">Von Einheit</span><span class="sxs-lookup"><span data-stu-id="c1d68-156">From unit</span></span>             | <span data-ttu-id="c1d68-157">Schachteln</span><span class="sxs-lookup"><span data-stu-id="c1d68-157">Boxes</span></span>                   |
    | <span data-ttu-id="c1d68-158">Faktor</span><span class="sxs-lookup"><span data-stu-id="c1d68-158">Factor</span></span>                | <span data-ttu-id="c1d68-159">4</span><span class="sxs-lookup"><span data-stu-id="c1d68-159">4</span></span>                       |
    | <span data-ttu-id="c1d68-160">In Einheit</span><span class="sxs-lookup"><span data-stu-id="c1d68-160">To Unit</span></span>               | <span data-ttu-id="c1d68-161">Stückzahl</span><span class="sxs-lookup"><span data-stu-id="c1d68-161">Pieces</span></span>                  |

1. <span data-ttu-id="c1d68-162">Die freigegebenen Produktvarianten **klein**, **mittel** und **groß** haben dieselbe Einheitenumrechnung zwischen dem Feld *Karton* und *Stück*, was bedeutet, dass Sie die Einheitenumrechnung für sie im Produktmaster definieren können.</span><span class="sxs-lookup"><span data-stu-id="c1d68-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="c1d68-163">Feld</span><span class="sxs-lookup"><span data-stu-id="c1d68-163">Field</span></span>                 | <span data-ttu-id="c1d68-164">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c1d68-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="c1d68-165">Konvertierung erstellen für</span><span class="sxs-lookup"><span data-stu-id="c1d68-165">Create conversion for</span></span> | <span data-ttu-id="c1d68-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="c1d68-166">Product</span></span> |
    | <span data-ttu-id="c1d68-167">Produkt</span><span class="sxs-lookup"><span data-stu-id="c1d68-167">Product</span></span>               | <span data-ttu-id="c1d68-168">T-Shirt</span><span class="sxs-lookup"><span data-stu-id="c1d68-168">T-Shirt</span></span> |
    | <span data-ttu-id="c1d68-169">Von Einheit</span><span class="sxs-lookup"><span data-stu-id="c1d68-169">From unit</span></span>             | <span data-ttu-id="c1d68-170">Schachteln</span><span class="sxs-lookup"><span data-stu-id="c1d68-170">Boxes</span></span>   |
    | <span data-ttu-id="c1d68-171">Faktor</span><span class="sxs-lookup"><span data-stu-id="c1d68-171">Factor</span></span>                | <span data-ttu-id="c1d68-172">5</span><span class="sxs-lookup"><span data-stu-id="c1d68-172">5</span></span>       |
    | <span data-ttu-id="c1d68-173">In Einheit</span><span class="sxs-lookup"><span data-stu-id="c1d68-173">To Unit</span></span>               | <span data-ttu-id="c1d68-174">Stücke</span><span class="sxs-lookup"><span data-stu-id="c1d68-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="c1d68-175">Excel verwenden, um die Einheitenumrechnungen zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c1d68-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="c1d68-176">Wenn ein Produkt viele Produktvarianten mit unterschiedlichen Einheitenumrechnungen hat, ist es eine gute Idee, die Einheitenumrechnungen in eine Microsoft Excel-Arbeitsmappe zu exportieren, zu aktualisieren und sie dann wieder in Dynamics 365 Supply Chain Management zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c1d68-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c1d68-177">Um Einheitenumrechnungen nach Excel zu exportieren, klicken Sie auf der Seite **Einheitenumrechnungen** im Aktionsbereich auf **In Microsoft Office öffnen**.</span><span class="sxs-lookup"><span data-stu-id="c1d68-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1d68-178">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c1d68-178">Additional resources</span></span>

[<span data-ttu-id="c1d68-179">Maßeinheit verwalten</span><span class="sxs-lookup"><span data-stu-id="c1d68-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
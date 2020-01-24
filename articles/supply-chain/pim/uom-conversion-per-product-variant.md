---
title: Maßeinheitsumrechnungen für Produktvarianten
description: In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935098"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="e7de6-103">Maßeinheitsumrechnungen für Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="e7de6-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7de6-104">In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können.</span><span class="sxs-lookup"><span data-stu-id="e7de6-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="e7de6-105">Zudem enthält es ein Beispiel für die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e7de6-105">It includes an example of the setup.</span></span>

<span data-ttu-id="e7de6-106">Diese Funktion ermöglicht den Austausch, damit Unternehmen verschiedene Einheitenumrechnung zwischen den Varianten desselben Produkts definieren.</span><span class="sxs-lookup"><span data-stu-id="e7de6-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="e7de6-107">Das folgende Beispiel wird in diesem Thema verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7de6-107">The following example is used in this topic.</span></span> <span data-ttu-id="e7de6-108">Ein Unternehmen verkauft die T-Shirts in kleinen, mittig großen und extra-großen Größen.</span><span class="sxs-lookup"><span data-stu-id="e7de6-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="e7de6-109">Das T-Shirt wird als Produkt definiert, und die verschiedenen Größen werden als Varianten des Produkts definiert.</span><span class="sxs-lookup"><span data-stu-id="e7de6-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="e7de6-110">Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt.</span><span class="sxs-lookup"><span data-stu-id="e7de6-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="e7de6-111">Das Unternehmen möchte die verschiedenen Varianten der T-Shirts in der Einheit **Stücke** nachverfolgen aber verkauft die T-Shirts in der Einheit **Schachteln**.</span><span class="sxs-lookup"><span data-stu-id="e7de6-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="e7de6-112">Die Umrechnung zwischen der Lagereinheit und der Verkaufseinheit ist eine Schachtel = 5, außer für die extra-großen, bei denen 1 Schachtel = 4 Stück ist.</span><span class="sxs-lookup"><span data-stu-id="e7de6-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="e7de6-113">Einrichten eines Produkts für Einheitenumrechnung pro Variante</span><span class="sxs-lookup"><span data-stu-id="e7de6-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="e7de6-114">ProtukVarianten können nur für Produkte von **Produkt-Untertyp** **Produktmaster** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e7de6-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="e7de6-115">Weitere Informationen finden Sie unter [Erstellen eines Produktmasters](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="e7de6-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="e7de6-116">Die Funktion ist nicht für Produkte aktiviert, die für Artikelgewichtsprozesse eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="e7de6-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="e7de6-117">Wenn der Produktmaster mit freigegebenen Produkten erstellt wird, können pro Einheitenumrechnungen Varianten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="e7de6-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="e7de6-118">Sie können für die Menüoption das Öffnen der Einheitenumrechnungsseite im Kontext eines Produkts oder die Produktvariante auf den folgenden Seiten finden.</span><span class="sxs-lookup"><span data-stu-id="e7de6-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="e7de6-119">Seite **Produktdetails**</span><span class="sxs-lookup"><span data-stu-id="e7de6-119">**Product details** page</span></span>
-   <span data-ttu-id="e7de6-120">Seite **Details für freigegebene Produkte**</span><span class="sxs-lookup"><span data-stu-id="e7de6-120">**Released products details** page</span></span>
-   <span data-ttu-id="e7de6-121">Seite **Varianten für freigegebenes Produkt**</span><span class="sxs-lookup"><span data-stu-id="e7de6-121">**Released product variants** page</span></span>

<span data-ttu-id="e7de6-122">Wenn Sie die Detailebene **Einheitenumrechnung** Seite im Kontext eines Untertyps "Produktmaster" oder Produktvariante öffnen, können Sie auswählen, wenn Sie die Einheitenumrechnung für das Produkt oder eine ausgewählte Produktvariante einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="e7de6-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="e7de6-123">Sie gehen follgendermaßen vor, indem Sie entweder **Produktvariante** oder **Produkt** im Feld **Erstellen Sie für Umwandlungen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="e7de6-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="e7de6-124">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="e7de6-124">Product variant</span></span>

<span data-ttu-id="e7de6-125">Wenn Sie **Produktvariante,** wählen, können Sie auswählen, für welche Artikelvariante Sie die Einheitenumrechnung im Feld **Produktvariante** eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7de6-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="e7de6-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="e7de6-126">Product</span></span>

<span data-ttu-id="e7de6-127">Wenn Sie **Produkt** auswählen, kann eine Einheitenumrechnung für den Produktmaster eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="e7de6-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="e7de6-128">Diese Einheitenumrechnung gilt für alle Produktvarianten ohne definierte Einheitenumrechnung.</span><span class="sxs-lookup"><span data-stu-id="e7de6-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="e7de6-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7de6-129">Example</span></span>

<span data-ttu-id="e7de6-130">Ein Produktmaster, **T-Shirt**, besitzt vier kleine, mittlere, große, und X-große Varianten "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="e7de6-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="e7de6-131">Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt.</span><span class="sxs-lookup"><span data-stu-id="e7de6-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="e7de6-132">Hiermit öffnen Sie die Seite **Einheitenumrechnung** von der Freigabenproduktdetailseite für **T-Shirt.**</span><span class="sxs-lookup"><span data-stu-id="e7de6-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="e7de6-133">Auf der Seite **Einheitenumrechnung** richten Sie die Einheitenumrechnung für die X-große Freigabenproduktvariante ein.</span><span class="sxs-lookup"><span data-stu-id="e7de6-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="e7de6-134">**Feld**</span><span class="sxs-lookup"><span data-stu-id="e7de6-134">**Field**</span></span>             | <span data-ttu-id="e7de6-135">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="e7de6-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="e7de6-136">Konvertierung erstellen für</span><span class="sxs-lookup"><span data-stu-id="e7de6-136">Create conversion for</span></span> | <span data-ttu-id="e7de6-137">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="e7de6-137">Product variant</span></span>         |
| <span data-ttu-id="e7de6-138">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="e7de6-138">Product variant</span></span>       | <span data-ttu-id="e7de6-139">T-Shirt: : X-groß : :</span><span class="sxs-lookup"><span data-stu-id="e7de6-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="e7de6-140">Von Einheit</span><span class="sxs-lookup"><span data-stu-id="e7de6-140">From unit</span></span>             | <span data-ttu-id="e7de6-141">Schachteln</span><span class="sxs-lookup"><span data-stu-id="e7de6-141">Boxes</span></span>                   |
| <span data-ttu-id="e7de6-142">Faktor</span><span class="sxs-lookup"><span data-stu-id="e7de6-142">Factor</span></span>                | <span data-ttu-id="e7de6-143">4</span><span class="sxs-lookup"><span data-stu-id="e7de6-143">4</span></span>                       |
| <span data-ttu-id="e7de6-144">In Einheit</span><span class="sxs-lookup"><span data-stu-id="e7de6-144">To Unit</span></span>               | <span data-ttu-id="e7de6-145">Stücke</span><span class="sxs-lookup"><span data-stu-id="e7de6-145">Pieces</span></span>                  |

<span data-ttu-id="e7de6-146">Die freigegebenen Produktvarianten klein, mittel und groß haben dieselbe Einheitenumrechnung zwischen dem Feld Einheit und Stück, was bedeutet, dass Sie die Einheitenumrechnung für die Produktvarianten im Produktmaster definieren können.</span><span class="sxs-lookup"><span data-stu-id="e7de6-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="e7de6-147">**Feld**</span><span class="sxs-lookup"><span data-stu-id="e7de6-147">**Field**</span></span>             | <span data-ttu-id="e7de6-148">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="e7de6-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="e7de6-149">Konvertierung erstellen für</span><span class="sxs-lookup"><span data-stu-id="e7de6-149">Create conversion for</span></span> | <span data-ttu-id="e7de6-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="e7de6-150">Product</span></span>     |
| <span data-ttu-id="e7de6-151">Produkt</span><span class="sxs-lookup"><span data-stu-id="e7de6-151">Product</span></span>               | <span data-ttu-id="e7de6-152">T-Shirt</span><span class="sxs-lookup"><span data-stu-id="e7de6-152">T-Shirt</span></span>     |
| <span data-ttu-id="e7de6-153">Von Einheit</span><span class="sxs-lookup"><span data-stu-id="e7de6-153">From unit</span></span>             | <span data-ttu-id="e7de6-154">Schachteln</span><span class="sxs-lookup"><span data-stu-id="e7de6-154">Boxes</span></span>       |
| <span data-ttu-id="e7de6-155">Faktor</span><span class="sxs-lookup"><span data-stu-id="e7de6-155">Factor</span></span>                | <span data-ttu-id="e7de6-156">5</span><span class="sxs-lookup"><span data-stu-id="e7de6-156">5</span></span>           |
| <span data-ttu-id="e7de6-157">In Einheit</span><span class="sxs-lookup"><span data-stu-id="e7de6-157">To Unit</span></span>               | <span data-ttu-id="e7de6-158">Stücke</span><span class="sxs-lookup"><span data-stu-id="e7de6-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="e7de6-159">Excel verwenden, um die Einheitenumrechnungen zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e7de6-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="e7de6-160">Wenn ein Produkt Produktvarianten mit viele unterschiedliche Einheitenumrechnungen hat, wird empfohlen, die Seite **Einheitenumrechnung** in ein Excel-Arbeitsblatt zu exportieren, die Umrechnung zu aktualisieren und diese dann anschließend wieder in Supply Chain Mangement zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e7de6-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="e7de6-161">Die Option in Excel zu exportieren und die Bearbeitung wieder zurück zu Supply Chain Mangement zu exportieren, wird aktiviert im Menü **Öffnen in Microsoft Office** im Aktivitätsbereich auf der Seite **Einheitenumrechnung**.</span><span class="sxs-lookup"><span data-stu-id="e7de6-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>

---
title: "Maßeinheitsumrechnungen für Produktvarianten"
description: "In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können."
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="86020-103">Maßeinheitsumrechnungen für Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="86020-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="86020-104">In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können.</span><span class="sxs-lookup"><span data-stu-id="86020-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="86020-105">Zudem enthält es ein Beispiel für die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="86020-105">It includes an example of the setup.</span></span>

<span data-ttu-id="86020-106">Diese Funktion ermöglicht den Austausch, damit Unternehmen verschiedene Einheitenumrechnung zwischen den Varianten desselben Produkts definieren.</span><span class="sxs-lookup"><span data-stu-id="86020-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="86020-107">Das folgende Beispiel wird in diesem Thema verwendet.</span><span class="sxs-lookup"><span data-stu-id="86020-107">The following example is used in this topic.</span></span> <span data-ttu-id="86020-108">Ein Unternehmen verkauft die T-Shirts in kleinen, mittig großen und extra-großen Größen.</span><span class="sxs-lookup"><span data-stu-id="86020-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="86020-109">Das T-Shirt wird als Produkt definiert, und die verschiedenen Größen werden als Varianten des Produkts definiert.</span><span class="sxs-lookup"><span data-stu-id="86020-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="86020-110">Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt.</span><span class="sxs-lookup"><span data-stu-id="86020-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="86020-111">Das Unternehmen möchte die verschiedenen Varianten der T-Shirts in der Einheit **Stücke** nachverfolgen aber verkauft die T-Shirts in der Einheit **Schachteln**.</span><span class="sxs-lookup"><span data-stu-id="86020-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="86020-112">Die Umrechnung zwischen der Lagereinheit und der Verkaufseinheit ist eine Schachtel = 5, außer für die extra-großen, bei denen 1 Schachtel = 4 Stück ist.</span><span class="sxs-lookup"><span data-stu-id="86020-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="86020-113">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="86020-113">Setup</span></span>

<span data-ttu-id="86020-114">Sie können die Parameter für die Verwendung der Funktion für die Produkte festlegen, die für **Alle Prozesse** oder nur für das Produkt aktiviert werden, das für **Lagerortprozesse** aktiviert ist, indem Sie die Option **Aktivieren Sie Maßeinheits-Unterhaltungen** auf der Seite **Produktinformationsparameter** nutzen.</span><span class="sxs-lookup"><span data-stu-id="86020-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="86020-115">Einrichten eines Produkts für Einheitenumrechnung pro Variante</span><span class="sxs-lookup"><span data-stu-id="86020-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="86020-116">ProtukVarianten können nur für Produkte von **Produkt-Untertyp** **Produktmaster** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="86020-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="86020-117">Weitere Informationen finden Sie unter [Erstellen eines Produktmasters](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="86020-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="86020-118">Die Funktion ist nicht für Produkte aktiviert, die für Artikelgewichtsprozesse eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="86020-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="86020-119">Während der Erstellung eines Produktmasters aktivieren Sie Maßeinheitsumrechnung, indem Sie die **Aktivieren Sie Maßeinheitsumrechnungen** auf der Seite **Produktdetails** nutzen.</span><span class="sxs-lookup"><span data-stu-id="86020-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="86020-120">Wenn der Produktmaster mit freigegebenen Produkten erstellt wird, können pro Einheitenumrechnungen Varianten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="86020-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="86020-121">Sie können für die Menüoption das Öffnen der Einheitenumrechnungsseite im Kontext eines Produkts oder die Produktvariante auf den folgenden Seiten finden.</span><span class="sxs-lookup"><span data-stu-id="86020-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="86020-122">Seite **Produktdetails**</span><span class="sxs-lookup"><span data-stu-id="86020-122">**Product details** page</span></span>
-   <span data-ttu-id="86020-123">Seite **Details für freigegebene Produkte**</span><span class="sxs-lookup"><span data-stu-id="86020-123">**Released products details** page</span></span>
-   <span data-ttu-id="86020-124">Seite **Varianten für freigegebenes Produkt**</span><span class="sxs-lookup"><span data-stu-id="86020-124">**Released product variants** page</span></span>

<span data-ttu-id="86020-125">Wenn Sie die Detailebene **Einheitenumrechnung** Seite im Kontext eines Untertyps "Produktmaster" oder Produktvariante öffnen, können Sie auswählen, wenn Sie die Einheitenumrechnung für das Produkt oder eine ausgewählte Produktvariante einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="86020-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="86020-126">Sie gehen follgendermaßen vor, indem Sie entweder **Produktvariante** oder **Produkt** im Feld **Erstellen Sie für Umwandlungen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="86020-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="86020-127">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="86020-127">Product variant</span></span>

<span data-ttu-id="86020-128">Wenn Sie **Produktvariante,** wählen, können Sie auswählen, für welche Artikelvariante Sie die Einheitenumrechnung im Feld **Produktvariante** eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86020-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="86020-129">Produkt</span><span class="sxs-lookup"><span data-stu-id="86020-129">Product</span></span>

<span data-ttu-id="86020-130">Wenn Sie **Produkt** auswählen, kann eine Einheitenumrechnung für den Produktmaster eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="86020-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="86020-131">Diese Einheitenumrechnung gilt für alle Produktvarianten ohne definierte Einheitenumrechnung.</span><span class="sxs-lookup"><span data-stu-id="86020-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="86020-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="86020-132">Example</span></span>

<span data-ttu-id="86020-133">Ein Produktmaster, **T-Shirt**, besitzt vier kleine, mittlere, große, und X-große Varianten "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="86020-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="86020-134">Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt.</span><span class="sxs-lookup"><span data-stu-id="86020-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="86020-135">Hiermit öffnen Sie die Seite **Einheitenumrechnung** von der Freigabenproduktdetailseite für **T-Shirt.**</span><span class="sxs-lookup"><span data-stu-id="86020-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="86020-136">Auf der Seite **Einheitenumrechnung** richten Sie die Einheitenumrechnung für die X-große Freigabenproduktvariante ein.</span><span class="sxs-lookup"><span data-stu-id="86020-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="86020-137">**Feld**</span><span class="sxs-lookup"><span data-stu-id="86020-137">**Field**</span></span>             | <span data-ttu-id="86020-138">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="86020-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="86020-139">Konvertierung erstellen für</span><span class="sxs-lookup"><span data-stu-id="86020-139">Create conversion for</span></span> | <span data-ttu-id="86020-140">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="86020-140">Product variant</span></span>         |
| <span data-ttu-id="86020-141">Produktvariante</span><span class="sxs-lookup"><span data-stu-id="86020-141">Product variant</span></span>       | <span data-ttu-id="86020-142">T-Shirt: : X-groß::</span><span class="sxs-lookup"><span data-stu-id="86020-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="86020-143">Von Einheit</span><span class="sxs-lookup"><span data-stu-id="86020-143">From unit</span></span>             | <span data-ttu-id="86020-144">Schachteln</span><span class="sxs-lookup"><span data-stu-id="86020-144">Boxes</span></span>                   |
| <span data-ttu-id="86020-145">Faktor</span><span class="sxs-lookup"><span data-stu-id="86020-145">Factor</span></span>                | <span data-ttu-id="86020-146">4</span><span class="sxs-lookup"><span data-stu-id="86020-146">4</span></span>                       |
| <span data-ttu-id="86020-147">In Einheit</span><span class="sxs-lookup"><span data-stu-id="86020-147">To Unit</span></span>               | <span data-ttu-id="86020-148">Stücke</span><span class="sxs-lookup"><span data-stu-id="86020-148">Pieces</span></span>                  |

<span data-ttu-id="86020-149">Die freigegebenen Produktvarianten klein, mittel und groß haben dieselbe Einheitenumrechnung zwischen dem Feld Einheit und Stück, was bedeutet, dass Sie die Einheitenumrechnung für die Produktvarianten im Produktmaster definieren können.</span><span class="sxs-lookup"><span data-stu-id="86020-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="86020-150">**Feld**</span><span class="sxs-lookup"><span data-stu-id="86020-150">**Field**</span></span>             | <span data-ttu-id="86020-151">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="86020-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="86020-152">Konvertierung erstellen für</span><span class="sxs-lookup"><span data-stu-id="86020-152">Create conversion for</span></span> | <span data-ttu-id="86020-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="86020-153">Product</span></span>     |
| <span data-ttu-id="86020-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="86020-154">Product</span></span>               | <span data-ttu-id="86020-155">T-Shirt</span><span class="sxs-lookup"><span data-stu-id="86020-155">T-Shirt</span></span>     |
| <span data-ttu-id="86020-156">Von Einheit</span><span class="sxs-lookup"><span data-stu-id="86020-156">From unit</span></span>             | <span data-ttu-id="86020-157">Schachteln</span><span class="sxs-lookup"><span data-stu-id="86020-157">Boxes</span></span>       |
| <span data-ttu-id="86020-158">Faktor</span><span class="sxs-lookup"><span data-stu-id="86020-158">Factor</span></span>                | <span data-ttu-id="86020-159">5</span><span class="sxs-lookup"><span data-stu-id="86020-159">5</span></span>           |
| <span data-ttu-id="86020-160">In Einheit</span><span class="sxs-lookup"><span data-stu-id="86020-160">To Unit</span></span>               | <span data-ttu-id="86020-161">Stücke</span><span class="sxs-lookup"><span data-stu-id="86020-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="86020-162">Excel verwenden, um die Einheitenumrechnungen zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="86020-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="86020-163">Wenn ein Produkt Produktvarianten mit viele unterschiedliche Einheitenumrechnungen hat, wird empfohlen, die Seite **Einheitenumrechnung** in ein Excel-Arbeitsblatt zu exportieren, die Umrechnung zu aktualisieren und diese dann anschließend wieder in Finance and Operations zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="86020-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="86020-164">Die Option in Excel zu exportieren und die Bearbeitung wieder zurück zu Finance and Operations zu exportieren, wird aktiviert im Menü **Öffnen in Microsoft Office** im Aktivitätsbereich auf der Seite **Einheitenumrechnung**.</span><span class="sxs-lookup"><span data-stu-id="86020-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>


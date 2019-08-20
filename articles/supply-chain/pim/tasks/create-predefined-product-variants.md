---
title: Vordefinierte Produktvarianten erstellen
description: Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf1e41d0071a4c78d2a0f43548e44ae9d426580
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844776"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="fd3e9-103">Vordefinierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="fd3e9-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd3e9-104">Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="fd3e9-105">Das Demounternehmen für diese Prozedur ist USMF.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="fd3e9-106">Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="fd3e9-106">Create a product master</span></span>
1. <span data-ttu-id="fd3e9-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Produktmaster".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="fd3e9-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-108">Click New.</span></span>
3. <span data-ttu-id="fd3e9-109">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="fd3e9-110">Eine Produktnummer manuell einzugeben ist nur erforderlich, wenn kein Nummernkreis für das Produktnummernfeld eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="fd3e9-111">In anderen Worten, überspringen Sie den Schritt, wenn ein Nummernkreis für das Feld festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="fd3e9-112">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="fd3e9-113">Geben Sie im Feld "Produktdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="fd3e9-114">Wählen Sie die Produktdimensionsgruppe "SizeCol" (Größe und Farbe) aus.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="fd3e9-115">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="fd3e9-116">Klicken Sie auf "Produktdimensionen hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-116">Add product dimensions</span></span>
1. <span data-ttu-id="fd3e9-117">Klicken Sie auf "Produktdimensionen".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="fd3e9-118">Dieses Beispiel zeigt, wie Produktdimensionenen manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="fd3e9-119">Sie können auch wählen, eine Größe, Farbe oder Stilgruppe auszuwählen, die die Produktdimensionswerte umfasst, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="fd3e9-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-120">Click New.</span></span>
3. <span data-ttu-id="fd3e9-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fd3e9-122">Geben Sie im Feld "Größe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="fd3e9-123">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="fd3e9-124">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-124">Click New.</span></span>
7. <span data-ttu-id="fd3e9-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fd3e9-126">Geben Sie im Feld "Größe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="fd3e9-127">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="fd3e9-128">Klicken Sie auf die Registerkarte "Farben".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="fd3e9-129">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-129">Click New.</span></span>
12. <span data-ttu-id="fd3e9-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fd3e9-131">Geben Sie im Feld "Farbe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="fd3e9-132">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="fd3e9-133">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-133">Click New.</span></span>
16. <span data-ttu-id="fd3e9-134">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="fd3e9-135">Geben Sie im Feld "Farbe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="fd3e9-136">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="fd3e9-137">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-137">Click Save.</span></span>
20. <span data-ttu-id="fd3e9-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="fd3e9-139">Generieren Sie Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="fd3e9-139">Generate product variants</span></span>
1. <span data-ttu-id="fd3e9-140">Klicken Sie auf "Produktvarianten".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-140">Click Product variants.</span></span>
2. <span data-ttu-id="fd3e9-141">Klicken Sie auf "Variantenvorschläge".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="fd3e9-142">Klicken Sie auf "Alles auswählen".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-142">Click Select all.</span></span>
    * <span data-ttu-id="fd3e9-143">In diesem Beispiel werden alle möglichen Varianten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="fd3e9-144">Wenn nur eine Teilmenge der möglichen Produktdimensionskombinationen verwendet wird, um Varianten zu erstellen, können Sie die einzelnen Einträge auswählen.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="fd3e9-145">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-145">Click Create.</span></span>
    * <span data-ttu-id="fd3e9-146">Sie können Beschreibungen für alle Ihre Varianten anhand der Kombination von Produktdimensionswerten generieren.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="fd3e9-147">Die Beschreibungen sind optional.</span><span class="sxs-lookup"><span data-stu-id="fd3e9-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="fd3e9-148">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fd3e9-148">Click Save.</span></span>


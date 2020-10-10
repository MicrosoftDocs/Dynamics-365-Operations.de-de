---
title: Vordefinierte Produktvarianten erstellen
description: Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6009f6de76155ea7c2982b28fe4505232447c9c8
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895304"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="96c62-103">Vordefinierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="96c62-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96c62-104">Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen.</span><span class="sxs-lookup"><span data-stu-id="96c62-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="96c62-105">Das Demounternehmen für diese Prozedur ist USMF.</span><span class="sxs-lookup"><span data-stu-id="96c62-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="96c62-106">Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="96c62-106">Create a product master</span></span>
1. <span data-ttu-id="96c62-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Produktmaster".</span><span class="sxs-lookup"><span data-stu-id="96c62-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="96c62-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="96c62-108">Click New.</span></span>
3. <span data-ttu-id="96c62-109">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96c62-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="96c62-110">Eine Produktnummer manuell einzugeben ist nur erforderlich, wenn kein Nummernkreis für das Produktnummernfeld eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="96c62-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="96c62-111">In anderen Worten, überspringen Sie den Schritt, wenn ein Nummernkreis für das Feld festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="96c62-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="96c62-112">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96c62-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="96c62-113">Geben Sie im Feld "Produktdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96c62-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="96c62-114">Wählen Sie die Produktdimensionsgruppe "SizeCol" (Größe und Farbe) aus.</span><span class="sxs-lookup"><span data-stu-id="96c62-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="96c62-115">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="96c62-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="96c62-116">Klicken Sie auf "Produktdimensionen hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="96c62-116">Add product dimensions</span></span>
1. <span data-ttu-id="96c62-117">Klicken Sie auf "Produktdimensionen".</span><span class="sxs-lookup"><span data-stu-id="96c62-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="96c62-118">Dieses Beispiel zeigt, wie Produktdimensionenen manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96c62-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="96c62-119">Sie können auch wählen, eine Größe, Farbe oder Stilgruppe auszuwählen, die die Produktdimensionswerte umfasst, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="96c62-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="96c62-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="96c62-120">Click New.</span></span>
3. <span data-ttu-id="96c62-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="96c62-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="96c62-122">Geben Sie im Feld "Größe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96c62-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="96c62-123">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96c62-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="96c62-124">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="96c62-124">Click New.</span></span>
7. <span data-ttu-id="96c62-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="96c62-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="96c62-126">Geben Sie im Feld "Größe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96c62-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="96c62-127">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96c62-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="96c62-128">Klicken Sie auf die Registerkarte "Farben".</span><span class="sxs-lookup"><span data-stu-id="96c62-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="96c62-129">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="96c62-129">Click New.</span></span>
12. <span data-ttu-id="96c62-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="96c62-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="96c62-131">Geben Sie im Feld "Farbe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96c62-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="96c62-132">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96c62-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="96c62-133">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="96c62-133">Click New.</span></span>
16. <span data-ttu-id="96c62-134">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="96c62-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="96c62-135">Geben Sie im Feld "Farbe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96c62-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="96c62-136">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96c62-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="96c62-137">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="96c62-137">Click Save.</span></span>
20. <span data-ttu-id="96c62-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="96c62-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="96c62-139">Generieren Sie Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="96c62-139">Generate product variants</span></span>
1. <span data-ttu-id="96c62-140">Klicken Sie auf "Produktvarianten".</span><span class="sxs-lookup"><span data-stu-id="96c62-140">Click Product variants.</span></span>
2. <span data-ttu-id="96c62-141">Klicken Sie auf "Variantenvorschläge".</span><span class="sxs-lookup"><span data-stu-id="96c62-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="96c62-142">Klicken Sie auf "Alles auswählen".</span><span class="sxs-lookup"><span data-stu-id="96c62-142">Click Select all.</span></span>
    * <span data-ttu-id="96c62-143">In diesem Beispiel werden alle möglichen Varianten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="96c62-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="96c62-144">Wenn nur eine Teilmenge der möglichen Produktdimensionskombinationen verwendet wird, um Varianten zu erstellen, können Sie die einzelnen Einträge auswählen.</span><span class="sxs-lookup"><span data-stu-id="96c62-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="96c62-145">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="96c62-145">Click Create.</span></span>
    * <span data-ttu-id="96c62-146">Sie können Beschreibungen für alle Ihre Varianten anhand der Kombination von Produktdimensionswerten generieren.</span><span class="sxs-lookup"><span data-stu-id="96c62-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="96c62-147">Die Beschreibungen sind optional.</span><span class="sxs-lookup"><span data-stu-id="96c62-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="96c62-148">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="96c62-148">Click Save.</span></span>


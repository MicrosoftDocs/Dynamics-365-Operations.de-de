---
title: Eine Variantengruppe erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Größen-, Stil- oder Farbvariantengruppe für ein Produkt in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799540"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="17cfa-103">Eine Variantengruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="17cfa-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="17cfa-104">In diesem Thema wird beschrieben, wie Sie eine Größen-, Stil- oder Farbvariantengruppe für ein Produkt in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="17cfa-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="17cfa-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="17cfa-105">Overview</span></span>

<span data-ttu-id="17cfa-106">Dynamics 365 Commerce unterstützt mehrere Varianten für Produkte.</span><span class="sxs-lookup"><span data-stu-id="17cfa-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="17cfa-107">Es ist ideal, Variantengruppen für verschiedene Produktkategorien einzurichten.</span><span class="sxs-lookup"><span data-stu-id="17cfa-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="17cfa-108">Beispielsweise kann eine Größengruppe für T-Shirts mit besonders kleinen, mittleren, großen und besonders großen Größen erstellt werden, oder es kann eine Farbgruppe erstellt werden, die alle verfügbaren Farben eines Produkts enthält.</span><span class="sxs-lookup"><span data-stu-id="17cfa-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="17cfa-109">Variantengruppen sollten hinzugefügt werden, bevor Produkte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="17cfa-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="17cfa-110">In diesem Thema wird eine Größengruppe erstellt und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="17cfa-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="17cfa-111">Ähnliche Verfahren können zum Hinzufügen und Konfigurieren von Stilgruppen und Farbgruppen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17cfa-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="17cfa-112">Eine Größengruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="17cfa-112">Create a size group</span></span>

<span data-ttu-id="17cfa-113">Gehen Sie folgendermaßen vor, um eine Größengruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="17cfa-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="17cfa-114">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Variantengruppen \>. Größengruppen**.</span><span class="sxs-lookup"><span data-stu-id="17cfa-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="17cfa-115">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="17cfa-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="17cfa-116">Geben Sie im Feld **Größengruppe** einen Namen für die Größengruppe ein.</span><span class="sxs-lookup"><span data-stu-id="17cfa-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="17cfa-117">Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="17cfa-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="17cfa-118">Wählen Sie im Aktivitätsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="17cfa-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="17cfa-119">Der Größengruppe Attribute hinzufügen</span><span class="sxs-lookup"><span data-stu-id="17cfa-119">Add attributes to the size group</span></span>

<span data-ttu-id="17cfa-120">Um Attribute zu einer Größengruppe hinzuzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="17cfa-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="17cfa-121">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Variantengruppen \> Größengruppen**.</span><span class="sxs-lookup"><span data-stu-id="17cfa-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="17cfa-122">Wählen Sie im Navigationsbereich eine Größengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="17cfa-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="17cfa-123">Wählen Sie unter **Größengruppenlinien** die Option **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="17cfa-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="17cfa-124">Geben Sie im Feld **Größe** eine Zeichenfolge für die Größe ein (zum Beispiel „XL”).</span><span class="sxs-lookup"><span data-stu-id="17cfa-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="17cfa-125">Geben Sie in das Feld **Größenbezeichnung** einen Namen für die Größe ein (z. B. „Extra groß”).</span><span class="sxs-lookup"><span data-stu-id="17cfa-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="17cfa-126">Geben Sie im Feld **Auffüllungsgewicht** eine Zahl ein, die das Auffüllungsgewicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="17cfa-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="17cfa-127">Geben Sie in das Feld **Nummer in Strichcode** eine Zahl ein, die den Strichcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="17cfa-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="17cfa-128">Geben Sie im Feld **Anzeigereihenfolge** eine Nummer ein, die die Anzeigereihenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="17cfa-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="17cfa-129">Wenn Sie mit dem Hinzufügen von Größen fertig sind, wählen Sie **Speichern** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="17cfa-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="17cfa-130">Die folgende Abbildung zeigt ein Beispiel für die Größengruppe für „lässige Shirtgrößen”</span><span class="sxs-lookup"><span data-stu-id="17cfa-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Größengruppe erstellen](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="17cfa-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17cfa-132">Additional resources</span></span>

[<span data-ttu-id="17cfa-133">Produktinformationsübersicht</span><span class="sxs-lookup"><span data-stu-id="17cfa-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="17cfa-134">Einzelhandelsprodukte einrichten</span><span class="sxs-lookup"><span data-stu-id="17cfa-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="17cfa-135">Produktdimensionen</span><span class="sxs-lookup"><span data-stu-id="17cfa-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Neues Produkt erstellen
description: In diesem Thema wird beschrieben, wie Sie ein neues Produkt in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001966"
---
# <a name="create-a-new-product"></a><span data-ttu-id="773e2-103">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="773e2-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="773e2-104">In diesem Thema wird beschrieben, wie Sie ein neues Produkt in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="773e2-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="773e2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="773e2-105">Overview</span></span>

<span data-ttu-id="773e2-106">Ein Produkt wird hauptsächlich durch eine Produktnummer, einen Namen und eine Beschreibung definiert.</span><span class="sxs-lookup"><span data-stu-id="773e2-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="773e2-107">Es sind jedoch auch andere Daten erforderlich, ein Produkt oder einen Service zu beschreiben:</span><span class="sxs-lookup"><span data-stu-id="773e2-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="773e2-108">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="773e2-108">Create a new product</span></span>

1. <span data-ttu-id="773e2-109">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="773e2-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="773e2-110">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="773e2-111">Wählen Sie in der Dropdownliste **Produktart** entweder **Artikel**oder **Dienstleistung** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="773e2-112">Wählen Sie in der Dropdownliste **Produktuntertyp** entweder **Produkt** (wenn das Produkt keine Varianten hat) oder **Produktmaster** (wenn das Produktvarianten haben wird) aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="773e2-113">Geben Sie in das Feld **Produktnummer** eine Produktnummer ein, falls diese noch nicht vorbelegt ist.</span><span class="sxs-lookup"><span data-stu-id="773e2-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="773e2-114">Geben Sie in das Feld **Produktname** einen Produktnamen ein.</span><span class="sxs-lookup"><span data-stu-id="773e2-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="773e2-115">Geben Sie in das Feld **Suchbegriff** einen Suchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="773e2-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="773e2-116">Wählen Sie in der Dropdownliste **Einzelhandelskategorie** eine entsprechende Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="773e2-117">Wenn das Produkt ein Set ist, wählen Sie **Ja** für **Produktset**.</span><span class="sxs-lookup"><span data-stu-id="773e2-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="773e2-118">Wenn der Produktuntertyp Produktmaster ist, legen Sie die **Produktdimensionsgruppe** fest, um die unterstützten Varianten einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="773e2-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="773e2-119">Zu den Optionen zählen **Farbe**, **Größe**, **Stil** und **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="773e2-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="773e2-120">Bei Bedarf müssen Sie möglicherweise zusätzliche Produktdimensionsgruppen erstellen.</span><span class="sxs-lookup"><span data-stu-id="773e2-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="773e2-121">Wählen Sie in der Dropdownliste **Konfigurationstechnologie** eine entsprechende Option aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="773e2-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="773e2-122">Select **OK**.</span></span>

<span data-ttu-id="773e2-123">Das folgende Bild zeigt das Beispiel eines hinzugefügten Produkts.</span><span class="sxs-lookup"><span data-stu-id="773e2-123">The following image shows an example product being added.</span></span>

![Ein Produkt erstellen](media/create-new-product.png)

<span data-ttu-id="773e2-125">Sobald ein Produkt hinzugefügt wurde, können zusätzliche Daten dafür festgelegt werden, zum Beispiel **Produktbeschreibung**, **Variantengruppen**, **Dimensionsgruppen**, **Produkteigenschaften** und **Verwandte Produkte**.</span><span class="sxs-lookup"><span data-stu-id="773e2-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="773e2-126">Das folgende Bild zeigt die zusätzlichen Details eines Produkts.</span><span class="sxs-lookup"><span data-stu-id="773e2-126">The following image shows a product's additional details.</span></span>

![Produktdetails](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="773e2-128">Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="773e2-128">Create product variants</span></span>

<span data-ttu-id="773e2-129">Wenn der Produktuntertyp **Produktmaster** ist, müssen bestimmte Varianten angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="773e2-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="773e2-130">Gehen Sie folgendermaßen vor, um ein Produktvarianten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="773e2-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="773e2-131">Wählen Sie im Aktivitätsbereich **Produktvarianten**.</span><span class="sxs-lookup"><span data-stu-id="773e2-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="773e2-132">Wenn im Aktionsbereich Variantengruppen ausgewählt wurden, wählen Sie \**Variantenvorschläge*.</span><span class="sxs-lookup"><span data-stu-id="773e2-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="773e2-133">Wählen Sie die Varianten aus, die Sie für das Produkt unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="773e2-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="773e2-134">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="773e2-135">Freigeben eines Produkts</span><span class="sxs-lookup"><span data-stu-id="773e2-135">Release a product</span></span>

<span data-ttu-id="773e2-136">Um ein Produkt zu verkaufen, muss es zunächst an eine juristische Person freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="773e2-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="773e2-137">Wählen Sie auf der Produktseite **Produkte freigeben**.</span><span class="sxs-lookup"><span data-stu-id="773e2-137">From the product page, select **Release products**.</span></span>

    ![Produkt freigeben](media/create-new-product-3.png)

1. <span data-ttu-id="773e2-139">Wählen Sie das freizugebende Produkt und anschließend **Nächste** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-139">Select the product to release, and then select **Next**.</span></span>

    ![Freizugebendes Produkt auswählen](media/create-new-product-4.png)

1. <span data-ttu-id="773e2-141">Wählen Sie die freizugebende Produktsatzvarianten und anschließend **Nächste** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Freizugebende Varianten auswählen](media/create-new-product-5.png)

1. <span data-ttu-id="773e2-143">Wählen Sie die juristische Person und dann **Nächste** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-143">Select the legal entity, and then select **Next**.</span></span>

    ![Juristische Person auswählen](media/create-new-product-6.png)

1. <span data-ttu-id="773e2-145">Wählen Sie **Fertig stellen** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-145">Select **Finish**.</span></span>

    ![Produktfreigabe abschließen](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="773e2-147">Ein freigegebenes Produkt konfigurieren</span><span class="sxs-lookup"><span data-stu-id="773e2-147">Configure a released product</span></span>

<span data-ttu-id="773e2-148">Sobald ein Produkt freigegeben ist, ist eine weitere Konfiguration erforderlich, die das Hinzufügen eines Preises zum Produkt umfasst.</span><span class="sxs-lookup"><span data-stu-id="773e2-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="773e2-149">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="773e2-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="773e2-150">Wählen Sie den Produktkategorieknoten für das freigegebene Produkt aus und wählen Sie das Produkt aus der Produktliste aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="773e2-151">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="773e2-152">Konfigurieren Sie im Abschnitt **Kauf** alle erforderlichen Eigenschaften, einschließlich **Einheit**, **Preis** und **Menge**.</span><span class="sxs-lookup"><span data-stu-id="773e2-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="773e2-153">Wählen Sie im Aktionsbereich **Bestätigen**, um sicherzustellen, dass für fehlende Felder keine Fehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="773e2-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="773e2-154">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="773e2-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="773e2-155">Das folgende Bild zeigt eine Beispielkonfiguration für ein freigegebenes Produkt.</span><span class="sxs-lookup"><span data-stu-id="773e2-155">The following image shows an example configuration for a released product.</span></span>

![Freigegebenes Produkt konfigurieren](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="773e2-157">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="773e2-157">Additional resources</span></span>

[<span data-ttu-id="773e2-158">Erstellen juristischer Personen</span><span class="sxs-lookup"><span data-stu-id="773e2-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="773e2-159">Eine Variantengruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="773e2-159">Create a variant group</span></span>](create-variant-group.md) 

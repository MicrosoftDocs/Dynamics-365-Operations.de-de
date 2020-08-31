---
title: Auftragsdetailmodul
description: In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661171"
---
# <a name="order-details-module"></a><span data-ttu-id="06ab4-103">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="06ab4-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06ab4-104">In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="06ab4-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="06ab4-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="06ab4-105">Overview</span></span>

<span data-ttu-id="06ab4-106">Nachdem eine Bestellung aufgegeben wurde, kann das Bestelldetailmodul verwendet werden, um die Bestätigungsdetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="06ab4-107">Hier werden die Bestellbestätigungs-ID, die Bestellkontaktinformationen und andere Bestelldetails angezeigt, z. B. die gekauften Artikel, die Zahlungsinformationen und die Versandmethode.</span><span class="sxs-lookup"><span data-stu-id="06ab4-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="06ab4-108">Details der Eigenschaften des Auftragsbestätigungsmoduls</span><span class="sxs-lookup"><span data-stu-id="06ab4-108">Order details module properties</span></span>

| <span data-ttu-id="06ab4-109">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="06ab4-109">Property name</span></span>  | <span data-ttu-id="06ab4-110">Werte</span><span class="sxs-lookup"><span data-stu-id="06ab4-110">Values</span></span> | <span data-ttu-id="06ab4-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06ab4-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="06ab4-112">Überschrift</span><span class="sxs-lookup"><span data-stu-id="06ab4-112">Heading</span></span>        | <span data-ttu-id="06ab4-113">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="06ab4-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="06ab4-114">Das Auftragsdetailmodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="06ab4-114">The order details module can have a heading.</span></span> <span data-ttu-id="06ab4-115">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="06ab4-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="06ab4-116">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="06ab4-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="06ab4-117">Contact number</span></span> | <span data-ttu-id="06ab4-118">Text</span><span class="sxs-lookup"><span data-stu-id="06ab4-118">Text</span></span> | <span data-ttu-id="06ab4-119">Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06ab4-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="06ab4-120">Module, die in einem Modul einer Auftragsdetailseite verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="06ab4-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="06ab4-121">Wenn Sie eine Bestelldetailseite erstellen, können Sie zusätzlich zum Bestelldetail-Modul weitere relevante Module hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="06ab4-122">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="06ab4-122">Here are some examples:</span></span>

- <span data-ttu-id="06ab4-123">**Empfehlungsmodule** – Das Empfehlungsmodul kann auf der Auftragsbestätigungsseite platziert werden, um dem Kunden andere Produkte vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="06ab4-124">**Marketing-Module** – Zur Seite mit den Bestelldetails kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="06ab4-125">Ein Auftragsdetailmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="06ab4-125">Add an order details module to a page</span></span>

<span data-ttu-id="06ab4-126">Um ein Auftragsdetailmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="06ab4-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="06ab4-127">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="06ab4-128">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die **Auftragsdetailvorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="06ab4-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="06ab4-129">Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="06ab4-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06ab4-130">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="06ab4-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06ab4-131">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="06ab4-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06ab4-132">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auftragsdetails** an und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="06ab4-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06ab4-133">Wählen Sie **Speichern** und dann **Vorschau** aus, um eine Vorlage in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="06ab4-134">Das Auftragsdetailmodul soll nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.</span><span class="sxs-lookup"><span data-stu-id="06ab4-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="06ab4-135">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="06ab4-136">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="06ab4-137">In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Auftragsdetails-Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="06ab4-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="06ab4-138">Unter **Seitenname** geben Sie **Auftragsdetailseite** ein und wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="06ab4-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="06ab4-139">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="06ab4-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06ab4-140">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auftragsdetails** an und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="06ab4-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06ab4-141">Wählen Sie im Eigenschaftenbereich der Auftragsdetails die Option **Überschrift** neben dem Stiftsymbol.</span><span class="sxs-lookup"><span data-stu-id="06ab4-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="06ab4-142">In dem **Überschriftstext** Feld des Dialogfelds **Überschrift** geben Sie den Überschriftentext ein und wählen dann **Bestelldetails** aus und dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="06ab4-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="06ab4-143">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="06ab4-144">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="06ab4-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06ab4-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="06ab4-145">Additional resources</span></span>

[<span data-ttu-id="06ab4-146">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="06ab4-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="06ab4-147">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="06ab4-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="06ab4-148">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="06ab4-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="06ab4-149">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="06ab4-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="06ab4-150">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="06ab4-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="06ab4-151">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="06ab4-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="06ab4-152">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="06ab4-152">Gift card module</span></span>](add-giftcard.md)

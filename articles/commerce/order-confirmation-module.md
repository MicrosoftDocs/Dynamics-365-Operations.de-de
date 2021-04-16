---
title: Auftragsbestätigungsmodul
description: In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804576"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="a8a40-103">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8a40-104">In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8a40-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a8a40-105">Nachdem ein Auftrag erteilt wurde, werden mit dem Auftragsbestätigungsmodul Auftragsbestätigungsdetails angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8a40-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="a8a40-106">Es werden Auftragsbestätigungs-ID, Auftragskontaktinformationen und andere Auftragsdetails angezeigt, wie z. B. erworbene Artikel, Zahlungsinformationen, Abholoptionen und Liefermethode.</span><span class="sxs-lookup"><span data-stu-id="a8a40-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="a8a40-107">Eigenschaften des Auftragsbestätigungsmoduls</span><span class="sxs-lookup"><span data-stu-id="a8a40-107">Order confirmation module properties</span></span>

| <span data-ttu-id="a8a40-108">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="a8a40-108">Property name</span></span>  | <span data-ttu-id="a8a40-109">Werte</span><span class="sxs-lookup"><span data-stu-id="a8a40-109">Values</span></span> | <span data-ttu-id="a8a40-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8a40-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="a8a40-111">Überschrift</span><span class="sxs-lookup"><span data-stu-id="a8a40-111">Heading</span></span>        | <span data-ttu-id="a8a40-112">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="a8a40-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a8a40-113">Das Auftragsbestätigungsmodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="a8a40-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="a8a40-114">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8a40-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="a8a40-115">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a8a40-116">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="a8a40-116">Contact number</span></span> | <span data-ttu-id="a8a40-117">Text</span><span class="sxs-lookup"><span data-stu-id="a8a40-117">Text</span></span> | <span data-ttu-id="a8a40-118">Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8a40-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="a8a40-119">Informationen zum Abholzeitfenster anzeigen</span><span class="sxs-lookup"><span data-stu-id="a8a40-119">Show pickup timeslot information</span></span> | <span data-ttu-id="a8a40-120">True oder False</span><span class="sxs-lookup"><span data-stu-id="a8a40-120">True or False</span></span> | <span data-ttu-id="a8a40-121">Diese Eigenschaft ist verfügbar in Dynamics 365 Commerce 10.0.15 und höher.</span><span class="sxs-lookup"><span data-stu-id="a8a40-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="a8a40-122">Wenn true, werden die Informationen zum Abholzeitfenster angezeigt, sofern diese für einen Abholartikel bereitgestellt wurden</span><span class="sxs-lookup"><span data-stu-id="a8a40-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="a8a40-123">Module, die auf einer Auftragsbestätigungsseite verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="a8a40-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="a8a40-124">Wenn Sie eine Auftragsbestätigungsseite erstellen, können Sie zusätzlich zum Auftragsbestätigungsmodul weitere relevante Module hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="a8a40-125">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="a8a40-125">Here are some examples:</span></span>

- <span data-ttu-id="a8a40-126">**Empfehlungsmodul** – Das Empfehlungsmodul kann zur Auftragsbestätigungsseite hinzugefügt werden, um dem Kunden andere Produkte vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="a8a40-127">**Marketing-Module** – Zur Auftragsbestätigungsseite kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="a8a40-128">Ein Auftragsbestätigungsmodul zu einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a8a40-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="a8a40-129">Um ein Auftragsbestätigungsmodul zu einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a8a40-130">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="a8a40-131">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie den Namen **Auftragsbestätigungsvorlage** ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8a40-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a8a40-132">Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a8a40-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a8a40-133">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a8a40-134">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a8a40-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a8a40-135">Wählen Sie im Dialogfeld **Modul hinzufügen** aus, wählen Sie die **Auftragsbestätigung** aus, und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a8a40-136">Wählen Sie **Speichern** und dann **Vorschau** aus, um eine Vorlage in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="a8a40-137">Das Auftragsbestätigungsmodul wird nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.</span><span class="sxs-lookup"><span data-stu-id="a8a40-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="a8a40-138">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="a8a40-139">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="a8a40-140">In dem Dialogfeld **Vorlage auswählen** wählen Sie **Auftragsbestätigungsvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="a8a40-141">Unter **Seitenname** geben Sie **Auftragsbestätigungsseite** ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8a40-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="a8a40-142">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a8a40-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a8a40-143">Wählen Sie im Dialogfeld **Modul hinzufügen** aus, wählen Sie die **Auftragsbestätigung** aus, und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a8a40-144">Wählen Sie im Eigenschaftenbereich für das Auftragsbestätigungsmodul die Option **Überschrift** neben dem Stiftsymbol aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="a8a40-145">Im Feld **Überschriftstext** des Dialogfelds **Überschrift** geben Sie den Überschriftentext **Auftragsbestätigung** ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a8a40-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="a8a40-146">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="a8a40-147">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a8a40-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8a40-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8a40-148">Additional resources</span></span>

[<span data-ttu-id="a8a40-149">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a8a40-150">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="a8a40-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a8a40-151">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="a8a40-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a8a40-152">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a8a40-153">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a8a40-154">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a8a40-155">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a8a40-156">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="a8a40-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
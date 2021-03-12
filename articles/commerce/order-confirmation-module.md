---
title: Auftragsbestätigungsmodul
description: In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972741"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="10ce6-103">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10ce6-104">In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="10ce6-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10ce6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="10ce6-105">Overview</span></span>

<span data-ttu-id="10ce6-106">Nachdem ein Auftrag erteilt wurde, werden mit dem Auftragsbestätigungsmodul Auftragsbestätigungsdetails angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10ce6-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="10ce6-107">Es werden Auftragsbestätigungs-ID, Auftragskontaktinformationen und andere Auftragsdetails angezeigt, wie z. B. erworbene Artikel, Zahlungsinformationen, Abholoptionen und Liefermethode.</span><span class="sxs-lookup"><span data-stu-id="10ce6-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="10ce6-108">Eigenschaften des Auftragsbestätigungsmoduls</span><span class="sxs-lookup"><span data-stu-id="10ce6-108">Order confirmation module properties</span></span>

| <span data-ttu-id="10ce6-109">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10ce6-109">Property name</span></span>  | <span data-ttu-id="10ce6-110">Werte</span><span class="sxs-lookup"><span data-stu-id="10ce6-110">Values</span></span> | <span data-ttu-id="10ce6-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10ce6-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="10ce6-112">Überschrift</span><span class="sxs-lookup"><span data-stu-id="10ce6-112">Heading</span></span>        | <span data-ttu-id="10ce6-113">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="10ce6-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="10ce6-114">Das Auftragsbestätigungsmodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="10ce6-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="10ce6-115">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="10ce6-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="10ce6-116">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="10ce6-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="10ce6-117">Contact number</span></span> | <span data-ttu-id="10ce6-118">Text</span><span class="sxs-lookup"><span data-stu-id="10ce6-118">Text</span></span> | <span data-ttu-id="10ce6-119">Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10ce6-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="10ce6-120">Informationen zum Abholzeitfenster anzeigen</span><span class="sxs-lookup"><span data-stu-id="10ce6-120">Show pickup timeslot information</span></span> | <span data-ttu-id="10ce6-121">True oder False</span><span class="sxs-lookup"><span data-stu-id="10ce6-121">True or False</span></span> | <span data-ttu-id="10ce6-122">Diese Eigenschaft ist verfügbar in Dynamics 365 Commerce 10.0.15 und höher.</span><span class="sxs-lookup"><span data-stu-id="10ce6-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="10ce6-123">Wenn true, werden die Informationen zum Abholzeitfenster angezeigt, sofern diese für einen Abholartikel bereitgestellt wurden</span><span class="sxs-lookup"><span data-stu-id="10ce6-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="10ce6-124">Module, die auf einer Auftragsbestätigungsseite verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="10ce6-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="10ce6-125">Wenn Sie eine Auftragsbestätigungsseite erstellen, können Sie zusätzlich zum Auftragsbestätigungsmodul weitere relevante Module hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="10ce6-126">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="10ce6-126">Here are some examples:</span></span>

- <span data-ttu-id="10ce6-127">**Empfehlungsmodul** – Das Empfehlungsmodul kann zur Auftragsbestätigungsseite hinzugefügt werden, um dem Kunden andere Produkte vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="10ce6-128">**Marketing-Module** – Zur Auftragsbestätigungsseite kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="10ce6-129">Ein Auftragsbestätigungsmodul zu einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="10ce6-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="10ce6-130">Um ein Auftragsbestätigungsmodul zu einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="10ce6-131">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="10ce6-132">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie den Namen **Auftragsbestätigungsvorlage** ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="10ce6-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="10ce6-133">Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="10ce6-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="10ce6-134">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="10ce6-135">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="10ce6-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="10ce6-136">Wählen Sie im Dialogfeld **Modul hinzufügen** aus, wählen Sie die **Auftragsbestätigung** aus, und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="10ce6-137">Wählen Sie **Speichern** und dann **Vorschau** aus, um eine Vorlage in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="10ce6-138">Das Auftragsbestätigungsmodul wird nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.</span><span class="sxs-lookup"><span data-stu-id="10ce6-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="10ce6-139">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="10ce6-140">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="10ce6-141">In dem Dialogfeld **Vorlage auswählen** wählen Sie **Auftragsbestätigungsvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="10ce6-142">Unter **Seitenname** geben Sie **Auftragsbestätigungsseite** ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="10ce6-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="10ce6-143">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="10ce6-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="10ce6-144">Wählen Sie im Dialogfeld **Modul hinzufügen** aus, wählen Sie die **Auftragsbestätigung** aus, und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="10ce6-145">Wählen Sie im Eigenschaftenbereich für das Auftragsbestätigungsmodul die Option **Überschrift** neben dem Stiftsymbol aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="10ce6-146">Im Feld **Überschriftstext** des Dialogfelds **Überschrift** geben Sie den Überschriftentext **Auftragsbestätigung** ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="10ce6-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="10ce6-147">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="10ce6-148">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="10ce6-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10ce6-149">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="10ce6-149">Additional resources</span></span>

[<span data-ttu-id="10ce6-150">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="10ce6-151">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="10ce6-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="10ce6-152">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="10ce6-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="10ce6-153">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="10ce6-154">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="10ce6-155">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="10ce6-156">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="10ce6-157">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="10ce6-157">Gift card module</span></span>](add-giftcard.md)

---
title: Versandadressmodul
description: Dieses Thema behandelt das Versandadressenmodul und erläutert, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234412"
---
# <a name="shipping-address-module"></a><span data-ttu-id="711de-103">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="711de-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="711de-104">Dieses Thema behandelt das Versandadressmodul und erläutert, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="711de-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="711de-105">Das Versandadressmodul ermöglicht Debitoren die Versandadresse für einen Auftrag während des Checkout-Flows hinzuzufügen oder auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="711de-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="711de-106">Wenn der Debitor angemeldet ist, werden alle zuvor gespeicherten Adressen für diesen Debitor angezeigt, und der Debitor kann zwischen diesen auswählen.</span><span class="sxs-lookup"><span data-stu-id="711de-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="711de-107">Der Debitor kann auch eine neue Adresse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="711de-107">The customer can also add a new address.</span></span> <span data-ttu-id="711de-108">Die Versandadressmodul wird für alle Artikel in einem Auftrag verwendet, die Versand erfordern.</span><span class="sxs-lookup"><span data-stu-id="711de-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="711de-109">Versandadressformate können in der Commerce-Zentrale für jedes Land oder jede Region definiert werden, und das Versandadressmodul setzt dann länderspezifische Regeln durch.</span><span class="sxs-lookup"><span data-stu-id="711de-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="711de-110">Wenn Debitoren während des Bestellvorgangs eine Versandadresse eingeben, haben sie die Möglichkeit, die Adresse als primäre Adresse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="711de-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="711de-111">Diese Option wird nur angezeigt, wenn ein Debitor angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="711de-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="711de-112">Obwohl das Versandadressmodul keine Adressüberprüfung bereitstellt, kann diese Funktion über die Anpassung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="711de-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="711de-113">Die folgende Abbildung zeigt ein Beispiel eines neuen Versandadressenmoduls auf einer Checkout-Seite.</span><span class="sxs-lookup"><span data-stu-id="711de-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Beispiel eines Versandadressenmoduls auf einer Checkout-Seite](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="711de-115">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="711de-115">Module properties</span></span>

| <span data-ttu-id="711de-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="711de-116">Property name</span></span> | <span data-ttu-id="711de-117">Werte</span><span class="sxs-lookup"><span data-stu-id="711de-117">Values</span></span> | <span data-ttu-id="711de-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="711de-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="711de-119">Überschrift</span><span class="sxs-lookup"><span data-stu-id="711de-119">Heading</span></span> | <span data-ttu-id="711de-120">Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="711de-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="711de-121">Eine optionale Überschrift für das Versandadressmodul.</span><span class="sxs-lookup"><span data-stu-id="711de-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="711de-122">Adresstyp anzeigen</span><span class="sxs-lookup"><span data-stu-id="711de-122">Show address type</span></span> | <span data-ttu-id="711de-123">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="711de-123">**True** or **False**</span></span> | <span data-ttu-id="711de-124">Wenn diese optionale Eigenschaft auf **True** gesetzt ist, wird ein Adresstyp, wie z. B. **Start** oder **Unternehmen**, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="711de-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="711de-125">Wenn kein Adresstyp angegeben ist, wird die Adresse automatisch als **Art**=**Sonstige** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="711de-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="711de-126">Automatisches Vorschlagen aktivieren</span><span class="sxs-lookup"><span data-stu-id="711de-126">Enable auto suggestion</span></span>| <span data-ttu-id="711de-127">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="711de-127">**True** or **False**</span></span> | <span data-ttu-id="711de-128">Wenn diese optionale Eigenschaft auf **True** gesetzt ist, werden automatische Adressvorschläge bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="711de-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="711de-129">Diese Vorschläge werden von Bing Maps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="711de-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="711de-130">Informationen zum Einrichten der Bing Maps-Integration auf Ihrer Website finden Sie unter [Shopauswahlmodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="711de-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="711de-131">Diese Funktion ist ab der Commerce-Version 10.0.15 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="711de-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="711de-132">Optionen für automatisches Vorschlagen</span><span class="sxs-lookup"><span data-stu-id="711de-132">Auto suggest options</span></span>| <span data-ttu-id="711de-133">Eine Anzahl</span><span class="sxs-lookup"><span data-stu-id="711de-133">A number</span></span>| <span data-ttu-id="711de-134">Wenn automatische Adressvorschläge aktiviert sind, können Sie zusätzliche Optionen angeben, z. B. die maximale Anzahl von Vorschlägen, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="711de-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="711de-135">Ein Versandadressmodul in eine Checkout-Seite hinzufügen und die erforderlichen Eigenschaften bestimmen</span><span class="sxs-lookup"><span data-stu-id="711de-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="711de-136">Ein Versandadressmodul kann nur zu einem Checkout-Modul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="711de-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="711de-137">Weitere Informationen zum Konfigurieren des Versandadressmoduls und zum Hinzufügen zu einer Checkout-Seite finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="711de-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="711de-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="711de-138">Additional resources</span></span>

[<span data-ttu-id="711de-139">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="711de-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="711de-140">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="711de-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="711de-141">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="711de-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="711de-142">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="711de-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="711de-143">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="711de-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="711de-144">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="711de-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="711de-145">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="711de-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="711de-146">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="711de-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="711de-147">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="711de-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
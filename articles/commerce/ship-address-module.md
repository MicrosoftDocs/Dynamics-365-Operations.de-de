---
title: Versandadressmodul
description: In diesem Thema wird das Versandadressmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 380d268ec0ba64367f090c31408eac1c54d0ff17
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661440"
---
# <a name="shipping-address-module"></a><span data-ttu-id="e02a2-103">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="e02a2-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e02a2-104">In diesem Thema wird das Versandadressmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="e02a2-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e02a2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e02a2-105">Overview</span></span>

<span data-ttu-id="e02a2-106">Das Versandadressmodul ermöglicht Debitoren die Versandadresse für einen Auftrag während des Checkout-Flows hinzuzufügen oder auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e02a2-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="e02a2-107">Wenn der Debitor angemeldet ist, werden alle zuvor gespeicherten Adressen für diesen Debitor angezeigt, und der Debitor kann zwischen diesen auswählen.</span><span class="sxs-lookup"><span data-stu-id="e02a2-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="e02a2-108">Der Debitor kann auch eine neue Adresse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e02a2-108">The customer can also add a new address.</span></span> <span data-ttu-id="e02a2-109">Die Versandadressmodul wird für alle Artikel in einem Auftrag verwendet, die Versand erfordern.</span><span class="sxs-lookup"><span data-stu-id="e02a2-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="e02a2-110">Versandadressformate können in der Commerce-Zentrale für jedes Land oder jede Region definiert werden, und das Versandadressmodul setzt dann länderspezifische Regeln durch.</span><span class="sxs-lookup"><span data-stu-id="e02a2-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="e02a2-111">Wenn Debitoren während des Bestellvorgangs eine Versandadresse eingeben, haben sie die Möglichkeit, die Adresse als primäre Adresse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e02a2-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="e02a2-112">Diese Option wird nur angezeigt, wenn ein Debitor angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="e02a2-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="e02a2-113">Obwohl das Versandadressmodul keine Adressüberprüfung bereitstellt, kann diese Funktion über die Anpassung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e02a2-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="e02a2-114">Die folgende Abbildung zeigt ein Beispiel eines neuen Versandadressenmoduls auf einer Checkout-Seite.</span><span class="sxs-lookup"><span data-stu-id="e02a2-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Beispiel eines Versandadressenmoduls auf einer Checkout-Seite](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="e02a2-116">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="e02a2-116">Module properties</span></span>

| <span data-ttu-id="e02a2-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="e02a2-117">Property name</span></span> | <span data-ttu-id="e02a2-118">Werte</span><span class="sxs-lookup"><span data-stu-id="e02a2-118">Values</span></span> | <span data-ttu-id="e02a2-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e02a2-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e02a2-120">Überschrift</span><span class="sxs-lookup"><span data-stu-id="e02a2-120">Heading</span></span> | <span data-ttu-id="e02a2-121">Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="e02a2-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e02a2-122">Eine optionale Überschrift für das Versandadressmodul.</span><span class="sxs-lookup"><span data-stu-id="e02a2-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="e02a2-123">Adresstyp anzeigen</span><span class="sxs-lookup"><span data-stu-id="e02a2-123">Show address type</span></span> | <span data-ttu-id="e02a2-124">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="e02a2-124">**True** or **False**</span></span> | <span data-ttu-id="e02a2-125">Wenn diese optionale Eigenschaft auf **True** gesetzt ist, wird ein Adresstyp, wie z. B. **Start** oder **Unternehmen**, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e02a2-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="e02a2-126">Wenn kein Adresstyp angegeben ist, wird die Adresse automatisch als **Art**=**Sonstige** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e02a2-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="e02a2-127">Ein Versandadressmodul in eine Checkout-Seite hinzufügen und die erforderlichen Eigenschaften bestimmen</span><span class="sxs-lookup"><span data-stu-id="e02a2-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="e02a2-128">Ein Versandadressmodul kann nur zu einem Checkout-Modul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e02a2-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="e02a2-129">Weitere Informationen zum Konfigurieren des Versandadressmoduls und zum Hinzufügen zu einer Checkout-Seite finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e02a2-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e02a2-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e02a2-130">Additional resources</span></span>

[<span data-ttu-id="e02a2-131">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="e02a2-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e02a2-132">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="e02a2-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e02a2-133">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="e02a2-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e02a2-134">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="e02a2-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e02a2-135">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="e02a2-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e02a2-136">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="e02a2-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e02a2-137">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="e02a2-137">Gift card module</span></span>](add-giftcard.md)

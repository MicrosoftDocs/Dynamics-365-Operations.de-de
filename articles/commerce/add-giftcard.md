---
title: Geschenkkartenmodul
description: Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761080"
---
# <a name="gift-card-module"></a><span data-ttu-id="e2190-103">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="e2190-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e2190-104">Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e2190-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e2190-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e2190-105">Overview</span></span>

<span data-ttu-id="e2190-106">Geschenkkartenmodule können in Checkout-Modulen verwendet werden, um Geschenkkarten zu akzeptieren, eine übliche Zahlungsmethode, die für E-Commerce-Transaktionen genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="e2190-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="e2190-107">Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="e2190-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="e2190-108">SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst.</span><span class="sxs-lookup"><span data-stu-id="e2190-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="e2190-109">Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="e2190-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="e2190-110">Es stehen zwei Geschenkkartenmodule zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="e2190-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="e2190-111">**Geschenkkarte** – Dieses Modul kann auf einer Checkout-Seite verwendet werden, um eine Geschenkkarte als Zahlungsmittel einzulösen.</span><span class="sxs-lookup"><span data-stu-id="e2190-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="e2190-112">**Guthabenüberprüfung der Geschenkkarte** – Dieses Modul kann auf jeder Seite verwendet werden, um den Kontostand auf einer Geschenkkarte zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e2190-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="e2190-113">Dieses Modul ist in Commerce Version 10.0.14 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2190-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="e2190-114">Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2190-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Beispiel eines Geschenkkarten-Moduls](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="e2190-116">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2190-116">Module properties</span></span>

- <span data-ttu-id="e2190-117">**Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder für Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2190-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="e2190-118">Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums.</span><span class="sxs-lookup"><span data-stu-id="e2190-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="e2190-119">Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e2190-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="e2190-120">Unterstützte Werte:</span><span class="sxs-lookup"><span data-stu-id="e2190-120">Supported values:</span></span>
-   <span data-ttu-id="e2190-121">PIN</span><span class="sxs-lookup"><span data-stu-id="e2190-121">PIN</span></span>
-   <span data-ttu-id="e2190-122">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="e2190-122">Expiration date</span></span>
-   <span data-ttu-id="e2190-123">Pin und Ablaufdatum festlegen</span><span class="sxs-lookup"><span data-stu-id="e2190-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="e2190-124">Keiner</span><span class="sxs-lookup"><span data-stu-id="e2190-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="e2190-125">Site-Einstellungen für Geschenkkartenmodule</span><span class="sxs-lookup"><span data-stu-id="e2190-125">Site settings for gift card modules</span></span>

<span data-ttu-id="e2190-126">Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**.</span><span class="sxs-lookup"><span data-stu-id="e2190-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="e2190-127">Diese Einstellung unterstützt drei Werte:</span><span class="sxs-lookup"><span data-stu-id="e2190-127">This setting supports three values:</span></span>
- <span data-ttu-id="e2190-128">**Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="e2190-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="e2190-129">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2190-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="e2190-130">**SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Givex und SVS Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="e2190-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="e2190-131">Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2190-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="e2190-132">**Dynamics 365, SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="e2190-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="e2190-133">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2190-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="e2190-134">Hinzufügen eines Geschenkkartenmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="e2190-134">Add a gift card module to a page</span></span>

<span data-ttu-id="e2190-135">Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e2190-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2190-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2190-136">Additional resources</span></span>

[<span data-ttu-id="e2190-137">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="e2190-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e2190-138">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="e2190-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e2190-139">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="e2190-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e2190-140">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="e2190-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e2190-141">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="e2190-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e2190-142">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="e2190-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e2190-143">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="e2190-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e2190-144">Unterstützung für externe Geschenkgutscheine</span><span class="sxs-lookup"><span data-stu-id="e2190-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

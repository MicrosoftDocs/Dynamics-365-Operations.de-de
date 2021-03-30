---
title: Geschenkkartenmodul
description: Dieses Thema behandelt Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206294"
---
# <a name="gift-card-module"></a><span data-ttu-id="12d49-103">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12d49-104">Dieses Thema behandelt Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="12d49-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="12d49-105">Geschenkkartenmodule können in Checkout-Modulen verwendet werden, um Geschenkkarten zu akzeptieren, eine übliche Zahlungsmethode, die für E-Commerce-Transaktionen genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="12d49-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="12d49-106">Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="12d49-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="12d49-107">SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst.</span><span class="sxs-lookup"><span data-stu-id="12d49-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="12d49-108">Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="12d49-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="12d49-109">Hilfe für das Einlösen von SVS- und Givex-Geschenkkarten während des Checkout-Flows finden Sie in Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="12d49-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="12d49-110">Es stehen zwei Geschenkkartenmodule zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="12d49-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="12d49-111">**Geschenkkarte** – Dieses Modul kann auf einer Checkout-Seite verwendet werden, um eine Geschenkkarte als Zahlungsmittel einzulösen.</span><span class="sxs-lookup"><span data-stu-id="12d49-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="12d49-112">**Guthabenüberprüfung der Geschenkkarte** – Dieses Modul kann auf jeder Seite verwendet werden, um den Kontostand auf einer Geschenkkarte zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="12d49-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="12d49-113">Dieses Modul ist in Commerce Version 10.0.14 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12d49-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="12d49-114">Hilfe für das Modul „Guthabenüberprüfung der Geschenkkarte“ finden Sie in Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="12d49-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="12d49-115">Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12d49-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Beispiel eines Geschenkkarten-Moduls](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="12d49-117">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="12d49-117">Module properties</span></span>

- <span data-ttu-id="12d49-118">**Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder für Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="12d49-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="12d49-119">Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums.</span><span class="sxs-lookup"><span data-stu-id="12d49-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="12d49-120">Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="12d49-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="12d49-121">Unterstützte Werte:</span><span class="sxs-lookup"><span data-stu-id="12d49-121">Supported values:</span></span>
-   <span data-ttu-id="12d49-122">PIN</span><span class="sxs-lookup"><span data-stu-id="12d49-122">PIN</span></span>
-   <span data-ttu-id="12d49-123">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="12d49-123">Expiration date</span></span>
-   <span data-ttu-id="12d49-124">Pin und Ablaufdatum festlegen</span><span class="sxs-lookup"><span data-stu-id="12d49-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="12d49-125">Keiner</span><span class="sxs-lookup"><span data-stu-id="12d49-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="12d49-126">Site-Einstellungen für Geschenkkartenmodule</span><span class="sxs-lookup"><span data-stu-id="12d49-126">Site settings for gift card modules</span></span>

<span data-ttu-id="12d49-127">Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**.</span><span class="sxs-lookup"><span data-stu-id="12d49-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="12d49-128">Diese Einstellung unterstützt drei Werte:</span><span class="sxs-lookup"><span data-stu-id="12d49-128">This setting supports three values:</span></span>
- <span data-ttu-id="12d49-129">**Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="12d49-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="12d49-130">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12d49-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="12d49-131">**SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Givex und SVS Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="12d49-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="12d49-132">Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12d49-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="12d49-133">**Dynamics 365, SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="12d49-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="12d49-134">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12d49-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12d49-135">Diese Einstellungen sind in Dynamics 365 Commerce 10.0.11 verfügbar und sind nur erforderlich, wenn Sie Hilfe für SVS- oder Givex-Geschenkkarten benötigen.</span><span class="sxs-lookup"><span data-stu-id="12d49-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="12d49-136">Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12d49-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="12d49-137">Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="12d49-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="12d49-138">Hinzufügen eines Geschenkkartenmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="12d49-138">Add a gift card module to a page</span></span>

<span data-ttu-id="12d49-139">Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="12d49-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12d49-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="12d49-140">Additional resources</span></span>

[<span data-ttu-id="12d49-141">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="12d49-142">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="12d49-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="12d49-143">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="12d49-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="12d49-144">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="12d49-145">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="12d49-146">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="12d49-147">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="12d49-148">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="12d49-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="12d49-149">Unterstützung für externe Geschenkgutscheine</span><span class="sxs-lookup"><span data-stu-id="12d49-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="12d49-150">SDK- und Modulbibliothekupdates</span><span class="sxs-lookup"><span data-stu-id="12d49-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Geschenkkartenmodul
description: Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980381"
---
# <a name="gift-card-module"></a><span data-ttu-id="a675b-103">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a675b-104">Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a675b-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a675b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a675b-105">Overview</span></span>

<span data-ttu-id="a675b-106">Geschenkkartenmodule können in Checkout-Modulen verwendet werden, um Geschenkkarten zu akzeptieren, eine übliche Zahlungsmethode, die für E-Commerce-Transaktionen genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="a675b-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="a675b-107">Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="a675b-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="a675b-108">SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst.</span><span class="sxs-lookup"><span data-stu-id="a675b-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="a675b-109">Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="a675b-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a675b-110">Hilfe für das Einlösen von SVS- und Givex-Geschenkkarten während des Checkout-Flows finden Sie in Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="a675b-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="a675b-111">Es stehen zwei Geschenkkartenmodule zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="a675b-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="a675b-112">**Geschenkkarte** – Dieses Modul kann auf einer Checkout-Seite verwendet werden, um eine Geschenkkarte als Zahlungsmittel einzulösen.</span><span class="sxs-lookup"><span data-stu-id="a675b-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="a675b-113">**Guthabenüberprüfung der Geschenkkarte** – Dieses Modul kann auf jeder Seite verwendet werden, um den Kontostand auf einer Geschenkkarte zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a675b-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="a675b-114">Dieses Modul ist in Commerce Version 10.0.14 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a675b-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="a675b-115">Hilfe für das Modul „Guthabenüberprüfung der Geschenkkarte“ finden Sie in Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="a675b-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="a675b-116">Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a675b-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Beispiel eines Geschenkkarten-Moduls](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="a675b-118">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="a675b-118">Module properties</span></span>

- <span data-ttu-id="a675b-119">**Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder für Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a675b-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="a675b-120">Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums.</span><span class="sxs-lookup"><span data-stu-id="a675b-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="a675b-121">Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a675b-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="a675b-122">Unterstützte Werte:</span><span class="sxs-lookup"><span data-stu-id="a675b-122">Supported values:</span></span>
-   <span data-ttu-id="a675b-123">PIN</span><span class="sxs-lookup"><span data-stu-id="a675b-123">PIN</span></span>
-   <span data-ttu-id="a675b-124">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="a675b-124">Expiration date</span></span>
-   <span data-ttu-id="a675b-125">Pin und Ablaufdatum festlegen</span><span class="sxs-lookup"><span data-stu-id="a675b-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="a675b-126">Keiner</span><span class="sxs-lookup"><span data-stu-id="a675b-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="a675b-127">Site-Einstellungen für Geschenkkartenmodule</span><span class="sxs-lookup"><span data-stu-id="a675b-127">Site settings for gift card modules</span></span>

<span data-ttu-id="a675b-128">Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**.</span><span class="sxs-lookup"><span data-stu-id="a675b-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="a675b-129">Diese Einstellung unterstützt drei Werte:</span><span class="sxs-lookup"><span data-stu-id="a675b-129">This setting supports three values:</span></span>
- <span data-ttu-id="a675b-130">**Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="a675b-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="a675b-131">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a675b-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="a675b-132">**SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Givex und SVS Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="a675b-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="a675b-133">Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a675b-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="a675b-134">**Dynamics 365, SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="a675b-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="a675b-135">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a675b-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a675b-136">Diese Einstellungen sind in Dynamics 365 Commerce 10.0.11 verfügbar und sind nur erforderlich, wenn Sie Hilfe für SVS- oder Givex-Geschenkkarten benötigen.</span><span class="sxs-lookup"><span data-stu-id="a675b-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="a675b-137">Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a675b-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a675b-138">Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="a675b-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="a675b-139">Hinzufügen eines Geschenkkartenmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="a675b-139">Add a gift card module to a page</span></span>

<span data-ttu-id="a675b-140">Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="a675b-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a675b-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a675b-141">Additional resources</span></span>

[<span data-ttu-id="a675b-142">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a675b-143">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="a675b-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a675b-144">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="a675b-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a675b-145">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a675b-146">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a675b-147">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a675b-148">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a675b-149">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="a675b-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a675b-150">Unterstützung für externe Geschenkgutscheine</span><span class="sxs-lookup"><span data-stu-id="a675b-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="a675b-151">SDK- und Modulbibliothekupdates</span><span class="sxs-lookup"><span data-stu-id="a675b-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

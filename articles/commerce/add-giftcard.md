---
title: Geschenkkartenmodul
description: Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a8428963e105e422dcd048863c17df0926a409ac
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411111"
---
# <a name="gift-card-module"></a><span data-ttu-id="b4b41-103">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="b4b41-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4b41-104">Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b4b41-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4b41-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b4b41-105">Overview</span></span>

<span data-ttu-id="b4b41-106">Geschenkkarten sind eine übliche Zahlungsmethode, und das Geschenkkartenmodul kann in einem Checkout-Modul zum Akzeptieren von Geschenkkarten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4b41-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="b4b41-107">Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="b4b41-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b4b41-108">SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst.</span><span class="sxs-lookup"><span data-stu-id="b4b41-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="b4b41-109">Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="b4b41-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="b4b41-110">Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4b41-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Beispiel eines Geschenkkarten-Moduls](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b4b41-112">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4b41-112">Module properties</span></span>

- <span data-ttu-id="b4b41-113">**Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder für Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b4b41-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b4b41-114">Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums.</span><span class="sxs-lookup"><span data-stu-id="b4b41-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b4b41-115">Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b4b41-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b4b41-116">Unterstützte Werte:</span><span class="sxs-lookup"><span data-stu-id="b4b41-116">Supported values:</span></span>
-   <span data-ttu-id="b4b41-117">PIN</span><span class="sxs-lookup"><span data-stu-id="b4b41-117">PIN</span></span>
-   <span data-ttu-id="b4b41-118">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b4b41-118">Expiration date</span></span>
-   <span data-ttu-id="b4b41-119">Pin und Ablaufdatum festlegen</span><span class="sxs-lookup"><span data-stu-id="b4b41-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="b4b41-120">Keiner</span><span class="sxs-lookup"><span data-stu-id="b4b41-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b4b41-121">Site-Einstellungen für Geschenkkartenmodule</span><span class="sxs-lookup"><span data-stu-id="b4b41-121">Site settings for gift card modules</span></span>

<span data-ttu-id="b4b41-122">Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**.</span><span class="sxs-lookup"><span data-stu-id="b4b41-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b4b41-123">Diese Einstellung unterstützt drei Werte:</span><span class="sxs-lookup"><span data-stu-id="b4b41-123">This setting supports three values:</span></span>
- <span data-ttu-id="b4b41-124">**Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="b4b41-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b4b41-125">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4b41-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b4b41-126">**SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Givex und SVS Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="b4b41-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b4b41-127">Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4b41-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b4b41-128">**Dynamics 365, SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="b4b41-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b4b41-129">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4b41-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b4b41-130">Hinzufügen eines Geschenkkartenmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="b4b41-130">Add a gift card module to a page</span></span>

<span data-ttu-id="b4b41-131">Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b4b41-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4b41-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4b41-132">Additional resources</span></span>

[<span data-ttu-id="b4b41-133">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="b4b41-133">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b4b41-134">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="b4b41-134">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b4b41-135">Unterstützung für externe Geschenkgutscheine</span><span class="sxs-lookup"><span data-stu-id="b4b41-135">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

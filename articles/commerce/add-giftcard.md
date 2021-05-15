---
title: Geschenkkartenmodul
description: Dieses Thema behandelt Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962762"
---
# <a name="gift-card-module"></a><span data-ttu-id="b8a2f-103">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8a2f-104">Dieses Thema behandelt Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b8a2f-105">Geschenkkartenmodule können in Checkout-Modulen verwendet werden, um Geschenkkarten zu akzeptieren, eine übliche Zahlungsmethode, die für E-Commerce-Transaktionen genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b8a2f-106">Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b8a2f-107">SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b8a2f-108">Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8a2f-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b8a2f-109">Hilfe für das Einlösen von SVS- und Givex-Geschenkkarten während des Checkout-Flows finden Sie in Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="b8a2f-110">Es stehen zwei Geschenkkartenmodule zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="b8a2f-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="b8a2f-111">**Geschenkkarte** – Dieses Modul kann auf einer Kassenseite verwendet werden, um eine Geschenkkarte als Angebot einzulösen.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b8a2f-112">**Überprüfung des Guthabens einer Geschenkkarte** – Dieses Modul kann auf jeder Seite verwendet werden, um den Saldo einer Geschenkkarte zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b8a2f-113">Dieses Modul ist in Commerce Version 10.0.14 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="b8a2f-114">Hilfe für das Modul „Guthabenüberprüfung der Geschenkkarte“ finden Sie in Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="b8a2f-115">Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Beispiel eines Geschenkkarten-Moduls](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b8a2f-117">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8a2f-117">Module properties</span></span>

- <span data-ttu-id="b8a2f-118">**Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder bei Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b8a2f-119">Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b8a2f-120">Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b8a2f-121">Unterstützte Werte:</span><span class="sxs-lookup"><span data-stu-id="b8a2f-121">Supported values:</span></span>
-   <span data-ttu-id="b8a2f-122">PIN</span><span class="sxs-lookup"><span data-stu-id="b8a2f-122">PIN</span></span>
-   <span data-ttu-id="b8a2f-123">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b8a2f-123">Expiration date</span></span>
-   <span data-ttu-id="b8a2f-124">Pin und Ablaufdatum festlegen</span><span class="sxs-lookup"><span data-stu-id="b8a2f-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="b8a2f-125">Keiner</span><span class="sxs-lookup"><span data-stu-id="b8a2f-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b8a2f-126">Site-Einstellungen für Geschenkkartenmodule</span><span class="sxs-lookup"><span data-stu-id="b8a2f-126">Site settings for gift card modules</span></span>

<span data-ttu-id="b8a2f-127">Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b8a2f-128">Diese Einstellung unterstützt drei Werte:</span><span class="sxs-lookup"><span data-stu-id="b8a2f-128">This setting supports three values:</span></span>
- <span data-ttu-id="b8a2f-129">**Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, lässt das Geschenkkartenmodul nur die Einlösung von Dynamics 365 Geschenkkarten zu.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b8a2f-130">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b8a2f-131">**SVS- und Givex-Geschenkkarten** – Wenn diese Einstellung angewendet wird, lässt das Geschenkkarten-Modul nur das Einlösen von Givex- und SVS-Geschenkkarten zu.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b8a2f-132">Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b8a2f-133">**Dynamics 365-, SVS- und Givex-Geschenkkarten** – Wenn diese Einstellung angewendet wird, lässt das Geschenkkartenmodul das Einlösen von Dynamics 365-, Givex- und SVS-Geschenkkarten zu.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b8a2f-134">Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8a2f-135">Diese Einstellungen sind in Dynamics 365 Commerce 10.0.11 verfügbar und sind nur erforderlich, wenn Sie Hilfe für SVS- oder Givex-Geschenkkarten benötigen.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="b8a2f-136">Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b8a2f-137">Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="b8a2f-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="b8a2f-138">Erweitern Sie interne Geschenkkarten für die Verwendung in E-Commerce-Storefronts</span><span class="sxs-lookup"><span data-stu-id="b8a2f-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="b8a2f-139">Standardmäßig sind interne Geschenkkarten nicht für die Verwendung in E-Commerce-Storefronts optimiert.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="b8a2f-140">Bevor Sie also die Verwendung von internen Geschenkkarten zur Zahlung zulassen, sollten Sie diese mit Erweiterungen konfigurieren, die sie sicherer machen.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="b8a2f-141">Hier sind die Geschenkkartenbereiche, die Sie erweitern sollten, bevor Sie die Verwendung interner Geschenkkarten in der Produktion zulassen:</span><span class="sxs-lookup"><span data-stu-id="b8a2f-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="b8a2f-142">**Geschenkkartennummer** – Nummernkreise werden verwendet, um Geschenkkartennummern für interne Geschenkkarten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="b8a2f-143">Da Nummernkreise leicht vorhergesagt werden können, sollten Sie die Generierung von Geschenkkartennummern so erweitern, dass zufällige, kryptografisch sichere Zeichenfolgen für die ausgegebenen Geschenkkartennummern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="b8a2f-144">**GetBalance** – Die **GetBalance** API wird verwendet, um den Kontostand von Geschenkkarten nachzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="b8a2f-145">Standardmäßig ist diese API öffentlich.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-145">By default, this API public.</span></span> <span data-ttu-id="b8a2f-146">Wenn für die Abfrage von Geschenkkarten-Salden keine PIN erforderlich ist, besteht das Risiko, dass Brute-Force-Angriffe die **GetBalance**-API verwenden, um zu versuchen, Geschenkkarten-Nummern abzufragen, die Salden haben.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="b8a2f-147">Durch die Implementierung von PIN-Anforderungen für interne Geschenkkarten und API-Drosselung können Sie das Risiko beheben.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="b8a2f-148">**PIN** – Standardmäßig unterstützen die internen Geschenkkarten keine PINs.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="b8a2f-149">Sie sollten interne Geschenkkarten so erweitern, dass eine PIN erforderlich ist, um den Kontostand abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="b8a2f-150">Diese Funktionalität kann auch verwendet werden, um Geschenkkarten nach aufeinanderfolgenden falschen Versuchen, die PIN einzugeben, zu sperren.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="b8a2f-151">Aktivieren von Geschenkkarten-Zahlungen für das Einchecken von Gästen</span><span class="sxs-lookup"><span data-stu-id="b8a2f-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="b8a2f-152">Standardmäßig sind Geschenkkarten-Zahlungen für die (anonyme) Gast-Kasse nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="b8a2f-153">Um sie zu aktivieren, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="b8a2f-154">Gehen Sie in der Commerce-Zentrale zu **Retail und Commerce \> Kanal einrichten \> POS einrichten \> POS \> POS Vorgänge**.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="b8a2f-155">Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) die Kopfzeile des Rasters und wählen Sie dann **Spalten einfügen**.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="b8a2f-156">Aktivieren Sie in der Dialogbox **Spalten einfügen** das Kontrollkästchen **Anonymen Zugriff zulassen**.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="b8a2f-157">Wählen Sie **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-157">Select **Update**.</span></span>
1. <span data-ttu-id="b8a2f-158">Legen Sie für die Vorgänge **520** (Geschenkkarten-Saldo) und **214** den Wert **AllowAnonymousAccess** auf **1** fest.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="b8a2f-159">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-159">Select **Save**.</span></span>
1. <span data-ttu-id="b8a2f-160">Führen Sie den Job **1090** aus, um Änderungen mit der Kanaldatenbank zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b8a2f-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b8a2f-161">Hinzufügen eines Geschenkkartenmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="b8a2f-161">Add a gift card module to a page</span></span>

<span data-ttu-id="b8a2f-162">Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b8a2f-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8a2f-163">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b8a2f-163">Additional resources</span></span>

[<span data-ttu-id="b8a2f-164">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b8a2f-165">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="b8a2f-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b8a2f-166">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b8a2f-167">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b8a2f-168">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b8a2f-169">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b8a2f-170">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b8a2f-171">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="b8a2f-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b8a2f-172">Unterstützung für externe Geschenkgutscheine</span><span class="sxs-lookup"><span data-stu-id="b8a2f-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="b8a2f-173">SDK- und Modulbibliothekupdates</span><span class="sxs-lookup"><span data-stu-id="b8a2f-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

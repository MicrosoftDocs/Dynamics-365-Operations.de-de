---
title: Zahlungsmodul
description: In diesem Thema wird das Zahlungsmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
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
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661205"
---
# <a name="payment-module"></a><span data-ttu-id="b9fc6-103">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-103">Payment module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b9fc6-104">In diesem Thema wird das Zahlungsmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b9fc6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b9fc6-105">Overview</span></span>

<span data-ttu-id="b9fc6-106">Das Zahlungsmodul ermöglicht es Debitoren, für eine Bestellung mit Kredit‑ oder Debitkarten zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="b9fc6-107">Die Zahlungsintegration für dieses Modul wird vom Zahlungskonnektor von Dynamics 365 für Adyen gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="b9fc6-108">Weitere Informationen darüber, wie der Zahlungskonnektor für konfiguriert und eingerichtet wird, finden Sie unter [Zahlungskonnektor von Dynamics 365 für Adyen](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="b9fc6-109">Das Zahlungsmodul hostet die Zahlungsinformationen, die über Adyen bereitgestellt werden, in einem HTML-Inlineframe (iFrame).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="b9fc6-110">Das Zahlungsmodul interagiert mit der Commerce Scale Unit, um die Adyen-Zahlungsinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="b9fc6-111">Im Rahmen der Commerce Scale Unit-Interaktion kann das Zahlungsmodul die Bereitstellung von Rechnungsadressinformationen entweder im iFrame oder als separates Modul ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="b9fc6-112">Im Fabrikam-Design wird die Rechnungsadresse in einem separaten Modul angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="b9fc6-113">Dieser Ansatz ermöglicht eine größere Flexibilität bei der Formatierung, da die Adresszeilen so gerendert werden können, dass sie den Zeilen der Lieferadresse ähneln.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="b9fc6-114">Mit dem Zahlungsmodul können angemeldete Debitoren auch ihre Zahlungsinformationen speichern.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="b9fc6-115">Die Zahlungsinformationen und die Rechnungsadresse werden über den Adyen-Zahlungskonnektor gespeichert und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="b9fc6-116">Das Zahlungsmodul deckt alle Auftragszuschläge ab, die nicht bereits durch Treuepunkte oder eine Geschenkkarte gedeckt sind.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="b9fc6-117">Wenn der Gesamtbetrag einer Bestellung vollständig durch Treuepunkte oder Gutschriften für Geschenkkarten gedeckt ist, wird das Zahlungsmodul ausgeblendet und der Debitor kann die Bestellung ohne diese aufgeben.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="b9fc6-118">Der Adyen-Zahlungskonnektor unterstützt auch Starke Kundenauthentifizierung (SCA).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="b9fc6-119">Ein Teil der Richtlinie über Zahlungsdienste der Europäischen Union (EU) 2.0 (PSD2.0) verlangt, dass Online-Käufer außerhalb ihres Online-Einkaufserlebnisses authentifiziert werden, wenn sie eine elektronische Zahlungsmethode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="b9fc6-120">Während des Checkout-Flows werden Debitoren zur Website ihrer Bank weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="b9fc6-121">Nach der Authentifizierung werden sie dann zurück zum Commerce-Checkout-Flow umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="b9fc6-122">Während dieser Umleitung bleiben die Informationen, die ein Debitor in den Checkout-Flow eingegeben hat (z. B. Versandadresse, Lieferoptionen, Geschenkkarteninformationen und Treueinformationen), erhalten.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="b9fc6-123">Bevor Sie diese Funktion aktivieren können, muss der Zahlungskonnektor für SCA in der Commerce-Zentrale konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="b9fc6-124">Weitere Informationen finden Sie unter [Starke Kundenauthentifizierung mit Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="b9fc6-125">Die folgende Abbildung zeigt ein Beispiel für Geschenkkarten‑, Treuepunkt‑, Zahlungsmodule auf einer Checkout-Seite.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Beispiel für Geschenkkarten‑, Treuepunkt‑ und Zahlungsmodule auf einer Checkout-Seite](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="b9fc6-127">Zahlungsmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9fc6-127">Payment module properties</span></span>

| <span data-ttu-id="b9fc6-128">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="b9fc6-128">Property name</span></span> | <span data-ttu-id="b9fc6-129">Werte</span><span class="sxs-lookup"><span data-stu-id="b9fc6-129">Values</span></span> | <span data-ttu-id="b9fc6-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9fc6-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b9fc6-131">Überschrift</span><span class="sxs-lookup"><span data-stu-id="b9fc6-131">Heading</span></span> | <span data-ttu-id="b9fc6-132">Überschriftentext</span><span class="sxs-lookup"><span data-stu-id="b9fc6-132">Heading text</span></span> | <span data-ttu-id="b9fc6-133">Eine optionale Überschrift für das Zahlungsmodul.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="b9fc6-134">Höhe des iFrame</span><span class="sxs-lookup"><span data-stu-id="b9fc6-134">Height of the iframe</span></span> | <span data-ttu-id="b9fc6-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="b9fc6-135">Pixels</span></span> | <span data-ttu-id="b9fc6-136">Die iFrame-Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-136">The iframe height, in pixels.</span></span> <span data-ttu-id="b9fc6-137">Die Höhe kann nach Bedarf geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="b9fc6-138">Rechnungsadresse anzeigen</span><span class="sxs-lookup"><span data-stu-id="b9fc6-138">Show billing address</span></span> | <span data-ttu-id="b9fc6-139">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="b9fc6-139">**True** or **False**</span></span> | <span data-ttu-id="b9fc6-140">Wenn diese Eigenschaft auf **True** gesetzt ist, wird die Rechnungsadresse von Adyen im Zahlungsmodul iFrame bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="b9fc6-141">Wenn sie auf **False** eingestellt ist, wird die Rechnungsadresse nicht von Adyen bereitgestellt, und ein Commerce-Benutzer muss ein Modul konfigurieren, um die Rechnungsadresse auf der Checkout-Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="b9fc6-142">Zahlungsstil überschreiben</span><span class="sxs-lookup"><span data-stu-id="b9fc6-142">Payment style override</span></span> | <span data-ttu-id="b9fc6-143">Cascading Style Sheets (CSS)-Code</span><span class="sxs-lookup"><span data-stu-id="b9fc6-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="b9fc6-144">Da das Zahlungsmodul in einem IFrame gehostet wird, sind die Styling-Funktionen eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="b9fc6-145">Mit dieser Eigenschaft können Sie ein gewisses Maß an Styling erzielen.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="b9fc6-146">Um Site-Stile zu überschreiben, müssen Sie den CSS-Code als Wert dieser Eigenschaft einfügen.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="b9fc6-147">Site Builder CSS-Überschreibungen und Stile gelten nicht für dieses Modul.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="b9fc6-148">Rechnungsadresse</span><span class="sxs-lookup"><span data-stu-id="b9fc6-148">Billing address</span></span>

<span data-ttu-id="b9fc6-149">Mit dem Zahlungsmodul können Debitoren eine Rechnungsadresse für ihre Zahlungsinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="b9fc6-150">Außerdem können sie ihre Lieferadresse als Rechnungsadresse verwenden, um den Checkout-Flow einfacher und schneller zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="b9fc6-151">Wenn die Eigenschaft **Rechnungsadresse anzeigen** auf **False** gesetzt ist, sollte das Zahlungsmodul auf der Checkout-Seite konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="b9fc6-152">Einer Checkout-Seite ein Zahlungsmodul hinzufügen, und die benötigten Eigenschaften einrichten</span><span class="sxs-lookup"><span data-stu-id="b9fc6-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="b9fc6-153">Ein Zahlungsmodul kann nur zu einem Checkout-Modul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="b9fc6-154">Weitere Informationen zum Konfigurieren eines Zahlungsmoduls für eine Checkout-Seite erhalten Sie unter [Checkout-Modul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9fc6-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9fc6-155">Additional resources</span></span>

[<span data-ttu-id="b9fc6-156">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b9fc6-157">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="b9fc6-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b9fc6-158">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b9fc6-159">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b9fc6-160">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b9fc6-161">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b9fc6-162">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="b9fc6-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b9fc6-163">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="b9fc6-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="b9fc6-164">Starke Kundenauthentifizierung mit dem Adyen-Konnektor</span><span class="sxs-lookup"><span data-stu-id="b9fc6-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)

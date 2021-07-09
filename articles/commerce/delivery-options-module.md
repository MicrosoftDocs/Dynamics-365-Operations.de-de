---
title: Lieferoptionsmodul
description: Dieses Thema enthält Beschreibungen der Lieferoptionsmodule und Erklärungen zu ihrer Konfiguration in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 8342afefa6eeda3a53decb39caddb62d1e4e1963
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270860"
---
# <a name="delivery-options-module"></a><span data-ttu-id="e67b3-103">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e67b3-104">Dieses Thema enthält Beschreibungen der Lieferoptionsmodule und Erklärungen zu ihrer Konfiguration in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e67b3-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e67b3-105">Mit den Versandoptionsmodulen können Kunden eine Versandart auswählen, z. B. Versand oder Abholung für ihre Online-Bestellung.</span><span class="sxs-lookup"><span data-stu-id="e67b3-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="e67b3-106">Eine Lieferadresse ist erforderlich, um die Lieferart zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e67b3-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="e67b3-107">Wenn sich die Versandadresse ändert, müssen die Lieferoptionen erneut abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e67b3-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="e67b3-108">Wenn ein Auftrag nur Artikel enthält, die in einem Shop abgeholt werden, wird dieses Modul automatisch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e67b3-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="e67b3-109">Informationen zum Konfigurieren der Lieferarten finden Sie unter [Online-Kanaleinrichtung ](channel-setup-online.md)und [Zustellungsmodi einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="e67b3-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="e67b3-110">Den einzelnen Lieferarten können jeweils Gebühren zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="e67b3-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="e67b3-111">Weitere Informationen zum Konfigurieren von Gebühren für einen Online-Shop finden Sie unter [Erweiterte automatische Omni-Channel-Belastungen](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="e67b3-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="e67b3-112">In der Commerce Version 10.0.13 wurde das Lieferoptionsmodul aktualisiert, damit es die Funktionen **Kopfzuschläge ohne Verrechnung** und **Versand als Positionsbelastung** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e67b3-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="e67b3-113">Wenn Verrechnung deaktiviert ist, wird erwartet, dass der E-Commerce-Workflow keine gemischte Lieferart für die Artikel im Warenkorb zulässt (d. h. einige Artikel werden für den Versand ausgewählt, andere für die Abholung).</span><span class="sxs-lookup"><span data-stu-id="e67b3-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="e67b3-114">Die Funktion **Kopfkosten ohne Aufschlag** erfordert, dass das Flag **Konsistente Lieferartbehandlung im Kanal aktivieren** in der Commerce-Zentrale eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="e67b3-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="e67b3-115">Wenn die Funktion Flag eingeschaltet ist, werden die Versandkosten entweder auf Kopf- oder auf Zeilenebene angewendet, je nach Konfiguration in der Commerce-Zentrale.</span><span class="sxs-lookup"><span data-stu-id="e67b3-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="e67b3-116">Das Fabrikam-Design unterstützt eine gemischte Lieferart, bei der einige Artikel für den Versand ausgewählt werden, andere jedoch für die Abholung.</span><span class="sxs-lookup"><span data-stu-id="e67b3-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="e67b3-117">In diesem Modus werden die Versandkosten für alle Artikel anteilig berechnet, die für die Lieferart ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="e67b3-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="e67b3-118">Damit eine gemischte Lieferart funktioniert, müssen Sie zuerst die Funktion **Kopfzuschläge ohne Verrechnung** in der Commerce-Zentralverwaltung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e67b3-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="e67b3-119">Weitere Informationen zu dieser Konfiguration finden Sie unter [Kopfbelastungen auf übereinstimmende Verkaufspositionen aufteilen](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="e67b3-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="e67b3-120">Wenn für Positionen Versandkosten anfallen, können diese für jeden Artikel in der Warenkorbposition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e67b3-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="e67b3-121">Diese Funktionalität erfordert, dass die Eigenschaft **Versandkosten für Positionen anzeigen** für das Warenkorbmodul und das Checkout-Modul aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e67b3-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="e67b3-122">Weitere Informationen finden Sie unter [Einkaufswagenmodul ](add-cart-module.md)und [Checkout-Modul ](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e67b3-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="e67b3-123">Das folgende Bild zeigt ein Beispiel eines Lieferoptionsmoduls auf einer Checkout-Seite.</span><span class="sxs-lookup"><span data-stu-id="e67b3-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Beispiel eines Lieferoptionsmoduls auf einer Checkout-Seite](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="e67b3-125">Lieferoptionsmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="e67b3-125">Delivery options module properties</span></span>

| <span data-ttu-id="e67b3-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e67b3-126">Property</span></span> | <span data-ttu-id="e67b3-127">Werte</span><span class="sxs-lookup"><span data-stu-id="e67b3-127">Values</span></span> | <span data-ttu-id="e67b3-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e67b3-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="e67b3-129">Überschrift</span><span class="sxs-lookup"><span data-stu-id="e67b3-129">Heading</span></span> | <span data-ttu-id="e67b3-130">Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="e67b3-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e67b3-131">Eine optionale Überschrift für das Lieferoptionsmodul.</span><span class="sxs-lookup"><span data-stu-id="e67b3-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="e67b3-132">Benutzerdefinierter CSS-Klassenname</span><span class="sxs-lookup"><span data-stu-id="e67b3-132">Custom CSS class name</span></span> | <span data-ttu-id="e67b3-133">Text</span><span class="sxs-lookup"><span data-stu-id="e67b3-133">Text</span></span> | <span data-ttu-id="e67b3-134">Ein benutzerdefinierter CSS-Klassenname (Cascading Style Sheets), der gegebenenfalls zum Rendern dieses Moduls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e67b3-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="e67b3-135">Liefermodusoption filtern</span><span class="sxs-lookup"><span data-stu-id="e67b3-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="e67b3-136">**Nicht filtern** oder **Nicht-Versand-Modi**</span><span class="sxs-lookup"><span data-stu-id="e67b3-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="e67b3-137">Ein Wert, der angibt, ob das Lieferoptionsmodul alle Nicht-Versand-Modi herausfiltern soll.</span><span class="sxs-lookup"><span data-stu-id="e67b3-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="e67b3-138">Automatisch eine Lieferoption auswählen</span><span class="sxs-lookup"><span data-stu-id="e67b3-138">Auto select a delivery option</span></span> | <span data-ttu-id="e67b3-139">**Nicht filtern**, **Lieferoption automatisch auswählen und Zusammenfassung anzeigen**, oder **Lieferoption automatisch auswählen und Zusammenfassung nicht anzeigen**</span><span class="sxs-lookup"><span data-stu-id="e67b3-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="e67b3-140">Diese Eigenschaft wendet automatisch die erste verfügbare Lieferoption auf die Kasse an, ohne dass der Benutzer diese auswählen muss.</span><span class="sxs-lookup"><span data-stu-id="e67b3-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="e67b3-141">Es sollte nur verwendet werden, wenn es eine verfügbare Lieferoption gibt.</span><span class="sxs-lookup"><span data-stu-id="e67b3-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="e67b3-142">Diese Eigenschaft wird ab der Commerce-Version 10.0.19 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e67b3-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="e67b3-143">Fürgen Sie ein Lieferoptionsmodul in eine Checkout-Seite ein und bestimmen Sie die erforderlichen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e67b3-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="e67b3-144">Ein Lieferoptionsmodul kann nur zu einem Auschecken-Modul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e67b3-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="e67b3-145">Weitere Informationen zum Konfigurieren des Lieferoptionsmoduls und zum Hinzufügen zu einer Checkout-Seite finden Sie unter [Checkout-Modul ](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e67b3-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e67b3-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e67b3-146">Additional resources</span></span>

[<span data-ttu-id="e67b3-147">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e67b3-148">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="e67b3-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e67b3-149">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e67b3-150">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e67b3-151">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="e67b3-152">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e67b3-153">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="e67b3-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="e67b3-154">Online-Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="e67b3-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="e67b3-155">Erweiterte automatische Omni-Channel-Belastungen</span><span class="sxs-lookup"><span data-stu-id="e67b3-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="e67b3-156">Kopfbelastungen abgeglichen mit Verkaufspositionen aufteilen</span><span class="sxs-lookup"><span data-stu-id="e67b3-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="e67b3-157">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="e67b3-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

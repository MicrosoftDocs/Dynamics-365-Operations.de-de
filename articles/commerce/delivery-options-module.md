---
title: Lieferoptionsmodul
description: Dieses Thema enthält Beschreibungen der Lieferoptionsmodule und Erklärungen zu ihrer Konfiguration in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 60449e9492c8e831b4ec6b2896f1ab471ef9d499
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661204"
---
# <a name="delivery-options-module"></a><span data-ttu-id="d9b63-103">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="d9b63-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d9b63-104">Dieses Thema enthält Beschreibungen der Lieferoptionsmodule und Erklärungen zu ihrer Konfiguration in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9b63-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d9b63-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d9b63-105">Overview</span></span>

<span data-ttu-id="d9b63-106">Mit den Versandoptionsmodulen können Kunden eine Versandart auswählen, z. B. Versand oder Abholung für ihre Online-Bestellung.</span><span class="sxs-lookup"><span data-stu-id="d9b63-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="d9b63-107">Eine Lieferadresse ist erforderlich, um die Lieferart zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d9b63-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="d9b63-108">Wenn sich die Versandadresse ändert, müssen die Lieferoptionen erneut abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d9b63-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="d9b63-109">Wenn ein Auftrag nur Artikel enthält, die in einem Shop abgeholt werden, wird dieses Modul automatisch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d9b63-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="d9b63-110">Informationen zum Konfigurieren der Lieferarten finden Sie unter [Online-Kanaleinrichtung ](channel-setup-online.md)und [Zustellungsmodi einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="d9b63-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="d9b63-111">Den einzelnen Lieferarten können jeweils Gebühren zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="d9b63-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="d9b63-112">Weitere Informationen zum Konfigurieren von Gebühren für einen Online-Shop finden Sie unter [Erweiterte automatische Omni-Channel-Belastungen](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="d9b63-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="d9b63-113">In der Commerce Version 10.0.13 wurde das Lieferoptionsmodul aktualisiert, damit es die Funktionen **Kopfzuschläge ohne Verrechnung** und **Versand als Positionsbelastung** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9b63-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="d9b63-114">Wenn Verrechnung deaktiviert ist, wird erwartet, dass der E-Commerce-Workflow keine gemischte Lieferart für die Artikel im Warenkorb zulässt (d. h. einige Artikel werden für den Versand ausgewählt, andere für die Abholung).</span><span class="sxs-lookup"><span data-stu-id="d9b63-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="d9b63-115">Die Funktion **Kopfzuschläge ohne Verrechnung** erfordert, dass das Flag **Einheitlicher Umgang mit der Lieferart im Kanal** in der Commerce-Zentralverwaltung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d9b63-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="d9b63-116">Wenn das Flag aktiviert ist, werden entsprechend der Konfiguration in der Commerce-Zentralverwaltung Versandkosten auf Kopf- oder Positionsebene fällig.</span><span class="sxs-lookup"><span data-stu-id="d9b63-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="d9b63-117">Das Fabrikam-Design unterstützt eine gemischte Lieferart, bei der einige Artikel für den Versand ausgewählt werden, andere jedoch für die Abholung.</span><span class="sxs-lookup"><span data-stu-id="d9b63-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="d9b63-118">In diesem Modus werden die Versandkosten für alle Artikel anteilig berechnet, die für die Lieferart ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="d9b63-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="d9b63-119">Damit eine gemischte Lieferart funktioniert, müssen Sie zuerst die Funktion **Kopfzuschläge ohne Verrechnung** in der Commerce-Zentralverwaltung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d9b63-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="d9b63-120">Weitere Informationen zu dieser Konfiguration finden Sie unter [Kopfbelastungen auf übereinstimmende Verkaufspositionen aufteilen](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="d9b63-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="d9b63-121">Wenn für Positionen Versandkosten anfallen, können diese für jeden Artikel in der Warenkorbposition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d9b63-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="d9b63-122">Diese Funktionalität erfordert, dass die Eigenschaft **Versandkosten für Positionen anzeigen** für das Warenkorbmodul und das Checkout-Modul aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d9b63-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="d9b63-123">Weitere Informationen finden Sie unter [Einkaufswagenmodul ](add-cart-module.md)und [Checkout-Modul ](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d9b63-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="d9b63-124">Das folgende Bild zeigt ein Beispiel eines Lieferoptionsmoduls auf einer Checkout-Seite.</span><span class="sxs-lookup"><span data-stu-id="d9b63-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Beispiel eines Lieferoptionsmoduls auf einer Checkout-Seite](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="d9b63-126">Lieferoptionsmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="d9b63-126">Delivery options module properties</span></span>

| <span data-ttu-id="d9b63-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9b63-127">Property</span></span> | <span data-ttu-id="d9b63-128">Werte</span><span class="sxs-lookup"><span data-stu-id="d9b63-128">Values</span></span> | <span data-ttu-id="d9b63-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9b63-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="d9b63-130">Überschrift</span><span class="sxs-lookup"><span data-stu-id="d9b63-130">Heading</span></span> | <span data-ttu-id="d9b63-131">Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="d9b63-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d9b63-132">Eine optionale Überschrift für das Lieferoptionsmodul.</span><span class="sxs-lookup"><span data-stu-id="d9b63-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="d9b63-133">Benutzerdefinierter CSS-Klassenname</span><span class="sxs-lookup"><span data-stu-id="d9b63-133">Custom CSS class name</span></span> | <span data-ttu-id="d9b63-134">Text</span><span class="sxs-lookup"><span data-stu-id="d9b63-134">Text</span></span> | <span data-ttu-id="d9b63-135">Ein benutzerdefinierter CSS-Klassenname (Cascading Style Sheets), der gegebenenfalls zum Rendern dieses Moduls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9b63-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="d9b63-136">Liefermodusoption filtern</span><span class="sxs-lookup"><span data-stu-id="d9b63-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="d9b63-137">**Nicht filtern** oder **Nicht-Versand-Modi**</span><span class="sxs-lookup"><span data-stu-id="d9b63-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="d9b63-138">Ein Wert, der angibt, ob das Lieferoptionsmodul alle Nicht-Versand-Modi herausfiltern soll.</span><span class="sxs-lookup"><span data-stu-id="d9b63-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="d9b63-139">Fürgen Sie ein Lieferoptionsmodul in eine Checkout-Seite ein und bestimmen Sie die erforderlichen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d9b63-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="d9b63-140">Ein Lieferoptionsmodul kann nur zu einem Auschecken-Modul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d9b63-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="d9b63-141">Weitere Informationen zum Konfigurieren des Lieferoptionsmoduls und zum Hinzufügen zu einer Checkout-Seite finden Sie unter [Checkout-Modul ](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d9b63-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9b63-142">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d9b63-142">Additional resources</span></span>

[<span data-ttu-id="d9b63-143">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="d9b63-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d9b63-144">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="d9b63-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d9b63-145">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="d9b63-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d9b63-146">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="d9b63-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d9b63-147">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="d9b63-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d9b63-148">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="d9b63-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="d9b63-149">Online-Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="d9b63-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="d9b63-150">Erweiterte automatische Omni-Channel-Belastungen</span><span class="sxs-lookup"><span data-stu-id="d9b63-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="d9b63-151">Kopfbelastungen abgeglichen mit Verkaufspositionen aufteilen</span><span class="sxs-lookup"><span data-stu-id="d9b63-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="d9b63-152">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="d9b63-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

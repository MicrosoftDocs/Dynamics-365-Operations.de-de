---
title: Die Abholoption wird nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Option für die Shop-Abholung nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt wird.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46eeed18bb547035603d7e9a01e8f131a2393f01
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801626"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="6a4d8-103">Die Option „Abholung“ wird nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt</span><span class="sxs-lookup"><span data-stu-id="6a4d8-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a4d8-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Option für die Shop-Abholung nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="6a4d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a4d8-105">Description</span></span>

<span data-ttu-id="6a4d8-106">Die Schaltfläche **Abholung** wird nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="6a4d8-107">Die folgende Abbildung zeigt ein Beispiel für eine Seite, die über die Schaltfläche **Abholung** verfügt.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![„Abholung“-Schaltfläche](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="6a4d8-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="6a4d8-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="6a4d8-110">BOPIS-Erweiterung im Commerce-Website-Generator aktivieren</span><span class="sxs-lookup"><span data-stu-id="6a4d8-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="6a4d8-111">Führen Sie die folgenden Schritte aus, um die Erweiterung „Online kaufen, im Shop abholen“ (Buy Online, Pick Up In Store, BOPIS) im Commerce-Website-Generator zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6a4d8-112">Wählen Sie die Website aus.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-112">Select your site.</span></span>
1. <span data-ttu-id="6a4d8-113">Wählen Sie **Site-Einstellungen** und anschließend **Erweiterungen** aus.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="6a4d8-114">Vergewissern Sie sich, dass die Option **BOPIS deaktivieren** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="6a4d8-115">Lieferarten in der Commerce-Zentralverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6a4d8-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="6a4d8-116">Befolgen Sie diese Schritte, um die Lieferarten in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6a4d8-117">Rufen Sie **Beschaffung \> Einrichtung \> Lieferarten** auf.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="6a4d8-118">Stellen Sie sicher, dass die Lieferart **Debitorenabholung** erstellt ist und ihr Produkte und Adressen zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="6a4d8-119">Rufen Sie **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter** auf.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="6a4d8-120">Wählen Sie im linken Navigationsbereich die Option **Debitorenaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="6a4d8-121">Vergewissern Sie sich, dass **Abhollieferart** richtig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="6a4d8-122">Zahlungen für Debitorenaufträge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6a4d8-122">Configure customer orders payments</span></span>

<span data-ttu-id="6a4d8-123">Befolgen Sie diese Schritte, um Zahlungen für Debitorenaufträge in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6a4d8-124">Rufen Sie **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter** auf.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="6a4d8-125">Wählen Sie im linken Navigationsbereich die Option **Debitorenaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="6a4d8-126">Überprüfen Sie, ob im Inforegister **Zahlungen** die Felder **Zahlungsbedingungen** und **Zahlungsart** korrekt eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="6a4d8-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a4d8-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a4d8-127">Additional resources</span></span>

[<span data-ttu-id="6a4d8-128">BOPIS konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6a4d8-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="6a4d8-129">Mehrere Lieferarten zur Abholung für Kundenaufträge</span><span class="sxs-lookup"><span data-stu-id="6a4d8-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="6a4d8-130">Omnichannel-Commerce-Auftragszahlungen</span><span class="sxs-lookup"><span data-stu-id="6a4d8-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="6a4d8-131">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="6a4d8-131">Store selector module</span></span>](../store-selector.md)

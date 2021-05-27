---
title: Einstellungen für die Maßeinheit festlegen
description: Dieses Thema behandelt die Einstellungen der Maßeinheit und beschreibt, wie sie auf Microsoft Dynamics 365 Commerce festgelegt werden.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022373"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="83bd7-103">Einstellungen für die Maßeinheit festlegen</span><span class="sxs-lookup"><span data-stu-id="83bd7-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="83bd7-104">Dieses Thema behandelt die Einstellungen der Maßeinheit und beschreibt, wie sie auf Microsoft Dynamics 365 Commerce festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="83bd7-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="83bd7-105">Ein Produkt kann in verschiedenen Einheiten verkauft werden, z. B. „pro Stück“, „Paar“ und „Dutzend“.</span><span class="sxs-lookup"><span data-stu-id="83bd7-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="83bd7-106">In der Commerce-Zentrale kann die verkaufte Maßeinheit für ein Produkt definiert werden und auf einer E-Commerce-Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="83bd7-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="83bd7-107">Wenn zum Beispiel ein Einzelhändler ein Produkt sowohl einzeln als auch in Dutzenden verkauft, können die verfügbaren Maßeinheiten zusammen mit anderen Produktinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="83bd7-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="83bd7-108">Im Beispiel in der folgenden Abbildung wurde für ein Produkt in der Commerce-Zentrale eine Maßeinheit **ea** (pro Stück) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="83bd7-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Beispiel für ein Produkt, das mit einer Maßeinheit in der Commerce-Zentrale konfiguriert ist](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="83bd7-110">Unterstützung für die Anwendung und Anzeige der Maßeinheit ist ab der Commerce-Version 10.0.19 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83bd7-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="83bd7-111">Einstellungen für die Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="83bd7-111">Unit of measure settings</span></span>

<span data-ttu-id="83bd7-112">Die Einstellungen für die Anzeige von Maßeinheiten werden im Commerce Site Builder festgelegt, und zwar unter **Site-Einstellungen \> Erweiterungen \> Anzeige der Maßeinheit für Produkte**.</span><span class="sxs-lookup"><span data-stu-id="83bd7-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="83bd7-113">Es gibt drei unterstützte Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="83bd7-113">There are three supported settings:</span></span>

- <span data-ttu-id="83bd7-114">**Nicht anzeigen** – Wenn diese Einstellung festgelegt ist, wird auf der E-Commerce-Seite die Maßeinheit für das Produkt nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83bd7-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="83bd7-115">Dieses Verhalten ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="83bd7-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="83bd7-116">**Anzeigen in der Produkt-Kauferfahrung** – Wenn diese Einstellung festgelegt ist, wird die Maßeinheit auf den Produkt-Detailseiten, im Warenkorb, an der Kasse, in der Bestellhistorie und auf den Bestelldetailseiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83bd7-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="83bd7-117">**Anzeige in der Produktübersicht und beim Kauf** – Wenn diese Einstellung festgelegt ist, wird die Maßeinheit auf den Seiten der Produktübersicht und auch während der Produktübersicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83bd7-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="83bd7-118">Als Teil dieses Verhaltens werden Maßeinheiten in den Suchergebnissen und den Modulen der Produktsammlung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83bd7-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83bd7-119">Die Einstellungen für die Anzeige von Maßeinheiten sind ab der Commerce-Version 10.0.19 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83bd7-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="83bd7-120">Wenn Sie ein Update von einer älteren Version von Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="83bd7-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="83bd7-121">Anweisungen finden Sie unter [SDK- und Modulbibliotheks-Updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="83bd7-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="83bd7-122">Module, die die Einstellungen für die Maßeinheit verwenden</span><span class="sxs-lookup"><span data-stu-id="83bd7-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="83bd7-123">Zu den Modulen, die die Einstellungen für die Maßeinheit verwenden, gehören die Module „Kaufbox“, „Wunschliste“, „Warenkorb“, „Warenkorb-Symbol“, „Suchergebnis-Container“, „Produktsammlung“, „Kasse“ und „Bestelldetails“.</span><span class="sxs-lookup"><span data-stu-id="83bd7-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="83bd7-124">Im Beispiel in der folgenden Abbildung zeigt eine Produkt-Detailseite (PDP) die Maßeinheit (**ea**) für ein Produkt an.</span><span class="sxs-lookup"><span data-stu-id="83bd7-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Beispiel für ein PDP, das die Maßeinheit anzeigt](./media/Productunit-PDP.png)

<span data-ttu-id="83bd7-126">In dem Beispiel in der folgenden Abbildung zeigt ein Produktsammlungsmodul die Maßeinheit (**ea**) für ein Produkt an.</span><span class="sxs-lookup"><span data-stu-id="83bd7-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Beispiel eines Produktsammlung-Moduls, das die Maßeinheit anzeigt](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="83bd7-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83bd7-128">Additional resources</span></span>

[<span data-ttu-id="83bd7-129">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="83bd7-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="83bd7-130">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="83bd7-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="83bd7-131">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="83bd7-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="83bd7-132">Seiten und Module zur Kontenverwaltung</span><span class="sxs-lookup"><span data-stu-id="83bd7-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="83bd7-133">SDK- und Modulbibliotheksupdates</span><span class="sxs-lookup"><span data-stu-id="83bd7-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

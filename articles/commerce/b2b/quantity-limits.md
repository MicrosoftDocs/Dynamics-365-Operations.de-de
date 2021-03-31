---
title: Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites
description: In diesem Thema wird beschrieben, wie Sie Produktmengenbeschränkungen für B2B-E-Commerce-Websites (Business-to-Business) einrichten.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211176"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="79f27-103">Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites</span><span class="sxs-lookup"><span data-stu-id="79f27-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79f27-104">In diesem Thema wird beschrieben, wie Sie Produktmengenbeschränkungen für B2B-E-Commerce-Websites (Business-to-Business) einrichten.</span><span class="sxs-lookup"><span data-stu-id="79f27-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="79f27-105">Die meisten Produkte haben eine Maßeinheit, die ihre Gruppierung definiert.</span><span class="sxs-lookup"><span data-stu-id="79f27-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="79f27-106">Die Gruppierung beeinflusst, wie die Produkte verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="79f27-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="79f27-107">Einige Produkte haben möglicherweise eine zusätzliche Gruppierung für Mengen.</span><span class="sxs-lookup"><span data-stu-id="79f27-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="79f27-108">Diese Gruppierung bestimmt, ob die Produkte als einzelne Einheiten oder als Vielfache verkauft werden können und ob ein Mindest- oder Höchstbestellmengenlimit eingehalten werden muss.</span><span class="sxs-lookup"><span data-stu-id="79f27-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="79f27-109">Die Mengenbegrenzungsfunktion stellt sicher, dass die Mindest-, Höchst-, Mehrfach- und Standardmengen, die in Microsoft Dynamics 365 Commerce konfiguriert sind (in den Standardeinstellungen für Bestellungen oder in den Site-Einstellungen für den Commerce-Website-Generator). auf Kundenbestellungen angewendet werden, die auf einer E-Commerce-Site aufgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="79f27-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="79f27-110">Produktmengenbeschränkungen werden derzeit für Point of Sale (POS) und Call Center nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79f27-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="79f27-111">Viele Einzelhändler bieten die Option der Debitorenaufträge (auch Sonderaufträge), um die verschiedenen Produkt- und Erfüllungsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="79f27-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="79f27-112">Nachfolgend sind einige typische Szenarios:</span><span class="sxs-lookup"><span data-stu-id="79f27-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="79f27-113">Ein Kunde möchte, dass Produkte bestimmter Varianten in Vielfachen von wenigen Artikeln verkauft werden.</span><span class="sxs-lookup"><span data-stu-id="79f27-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="79f27-114">Ein Debitor möchte Produkte von einem Shop oder einem Lagerplatz aufheben, der aus Filiale oder vom Lagerplatz abweicht, an dem der Debitor die Produkte gekauft hat.</span><span class="sxs-lookup"><span data-stu-id="79f27-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="79f27-115">Die Verpackungsstandards für die Geschäfte unterscheiden sich jedoch von den Verpackungsstandards für den Online-Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="79f27-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="79f27-116">Ein Kunde möchte ein Produkt in limitierter Auflage kaufen, das ein maximales Mengenlimit für Artikel hat, die gekauft werden können.</span><span class="sxs-lookup"><span data-stu-id="79f27-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="79f27-117">Die Funktion für Standardbestelleinstellung in der Commerce-Zentralverwaltung aktivieren</span><span class="sxs-lookup"><span data-stu-id="79f27-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="79f27-118">Bevor Sie Produktmengenlimits festlegen können, muss die Standardfunktion für Bestelleinstellungen in der Commerce-Zentralverwaltung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="79f27-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="79f27-119">Führen Sie diese Schritte aus, um die Funktion Standardbestelleinstellungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="79f27-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="79f27-120">Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="79f27-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="79f27-121">Suchen Sie die **Die Einstellungen für Website und Standardbestellung in der Kundenbestellung unterstützen** Funktion und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="79f27-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="79f27-122">Wählen Sie unten im rechten Bereich die Option **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="79f27-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="79f27-123">Mengeneinstellungen festlegen</span><span class="sxs-lookup"><span data-stu-id="79f27-123">Define quantity settings</span></span> 

<span data-ttu-id="79f27-124">Sie können die Mengeneinstellungen auf der Seite **Standardauftragseinstellungen** definieren.</span><span class="sxs-lookup"><span data-stu-id="79f27-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="79f27-125">Gehen Sie zum Festlegen der Mengeneinstellungen folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="79f27-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="79f27-126">Navigieren Sie zu Produkt **Einzelhandel und Handel \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="79f27-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="79f27-127">Wählen Sie ein freigegebenes Produkt.</span><span class="sxs-lookup"><span data-stu-id="79f27-127">Select a released product.</span></span>
1. <span data-ttu-id="79f27-128">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Auftragseinstellungen** die Option **Standardauftragseinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="79f27-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="79f27-129">Legen Sie auf der **Standardbestelleinstellungen**-Seite, im Inforegister **Auftrag** im **Verkaufsmenge**-Abschnitt die Produktverkaufsmengen fest:</span><span class="sxs-lookup"><span data-stu-id="79f27-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="79f27-130">**Mehrere** – die Menge, in deren Vielfachen das Produkt gekauft werden kann.</span><span class="sxs-lookup"><span data-stu-id="79f27-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="79f27-131">**Mindestbestellmenge** – die Mindestanzahl der Produkte, die gekauft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="79f27-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="79f27-132">**Maximalbestellmenge** – die Maximalanzahl der Produkte, die gekauft werden kann.</span><span class="sxs-lookup"><span data-stu-id="79f27-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="79f27-133">**Standardbestellmenge** – die Standardmenge, die bei Auswahl des Produkts automatisch eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79f27-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="79f27-134">Aktivieren Sie die Funktion für B2B-Bestellmengenbeschränkungen im Commerce-Website-Generator</span><span class="sxs-lookup"><span data-stu-id="79f27-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="79f27-135">Führen Sie diese Schritte aus, um die Funktion für B2B-Bestellmengenbeschränkungen im Commerce-Website-Generator zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="79f27-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="79f27-136">Gehen Sie zu **Site-Einstellungen \> Erweiterungen**</span><span class="sxs-lookup"><span data-stu-id="79f27-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="79f27-137">Unter **Bestellmengenlimits aktivieren** wählen Sie im Dropdown-Menü **Für B2B-Kunden aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="79f27-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="79f27-138">Aktualisierte Einstellungen für den Site Builder werden erst wirksam, nachdem die Datei App.settings.json aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="79f27-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="79f27-139">Weitere Informationen finden Sie unter [SDK- und Modulbibliothek-Updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="79f27-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79f27-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="79f27-140">Additional resources</span></span>

[<span data-ttu-id="79f27-141">Eine B2B-E-Commerce-Website einrichten</span><span class="sxs-lookup"><span data-stu-id="79f27-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="79f27-142">Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen</span><span class="sxs-lookup"><span data-stu-id="79f27-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="79f27-143">Benutzer von Geschäftspartnern auf Websites für B2B-E-Commerce verwalten</span><span class="sxs-lookup"><span data-stu-id="79f27-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="79f27-144">Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites</span><span class="sxs-lookup"><span data-stu-id="79f27-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
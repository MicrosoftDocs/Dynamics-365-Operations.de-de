---
title: Ändern Sie die Sortierreihenfolge für Verkaufsentitäten
description: In diesem Thema werden die Konzepte erläutert, die zum Steuern der Anzeigereihenfolge für verschiedene verkaufsbezogene Entitäten in Dynamics 365 Commerce zugeordnet werden.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 67807c53a6ffc6dd09cc6f0e48218e2ee2de559f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207774"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="5dfe3-103">Ändern Sie die Sortierreihenfolge für Verkaufsentitäten</span><span class="sxs-lookup"><span data-stu-id="5dfe3-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5dfe3-104">Einzelhändler erachten die Produkterfassung als ein primäres Tool für Debitoreninteraktionen über alle Kanäle hinweg.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="5dfe3-105">Verschiedene Funktionen können Debitoren helfen, Produkte einfacher zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="5dfe3-106">So können sie Kategorien, Suchen und Filter durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="5dfe3-107">In diesem Thema werden die Konzepte erläutert, die zum Steuern der Anzeigereihenfolge für verschiedene verkaufsbezogene Entitäten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="5dfe3-108">Es wird auch erklärt, wie Sie die Sortierreihenfolge ändern.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="5dfe3-109">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5dfe3-109">Overview</span></span>

<span data-ttu-id="5dfe3-110">Die Unterstützung zur Sortierung von verschiedenen verkaufsbezogenen Entitäten wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="5dfe3-111">Diese Unterstützung ist nun besser auf Szenarien mit Bestandskunden ausgerichtet, die zuvor Erweiterungen von Implementierungspartnern erforderlich machten.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="5dfe3-112">In Retail-Versionen vor Version 10.0.5 war die Sortierreihenfolge für Kategorien in der Navigationshierarchie alphabetisch.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="5dfe3-113">Mit den neuen benutzerdefinierten Sortierreihenfolgenfunktionen können Verkaufsmanager die Sortierreihenfolge für verschiedene verkaufsbezogene Entitäten für alle Endbenutzerkunden konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="5dfe3-114">Diese Kunden umfassen Headquarters (HQ) und Callcenter.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="5dfe3-115">Konfigurieren der Anzeigereihenfolge für Kategorien in der Produkthierarchie</span><span class="sxs-lookup"><span data-stu-id="5dfe3-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="5dfe3-116">Bevor Sie dieses Verfahren ausführen können, müssen Demodaten in Ihrer Umgebung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="5dfe3-117">Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Commerce-Produkthierarchie**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="5dfe3-118">Klicken Sie auf **Kategoriehierarchie bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="5dfe3-119">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-119">Click **Edit**.</span></span>
4. <span data-ttu-id="5dfe3-120">Erweitern Sie in der Struktur **ALLE \> Aktivität Sport**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="5dfe3-121">Erweitern Sie in der Struktur **ALLE \> Team-Sport**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="5dfe3-122">Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="5dfe3-123">(Die Zahl kann negativ sein.)</span><span class="sxs-lookup"><span data-stu-id="5dfe3-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="5dfe3-124">Wiederholen Sie die Schritte 4 bis 6 für zusätzliche Kategorien, für die Sie die Reihenfolge ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="5dfe3-125">Der Anzeigereihenfolge für die Kanalnavigationshierarchie wird in HQ für die Produkthierarchie und freigegebene Produkte nach Kategorie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Produkthierarchie: Benutzerdefinierte Sortierung mit negativen Werten](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Freigegebene Produkte nach Kategorie: Benutzerdefinierte Sortierung auf Basis der Produkthierarchie](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="5dfe3-128">Konfigurieren der Anzeigereihenfolge für Kategorien in der Kanalnavigationshierarchie</span><span class="sxs-lookup"><span data-stu-id="5dfe3-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="5dfe3-129">Bevor Sie dieses Verfahren ausführen können, müssen Demodaten in Ihrer Umgebung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="5dfe3-130">Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Kanalnavigationskategorien**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="5dfe3-131">Wählen Sie in der Liste die **Modenavigation**-Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="5dfe3-132">Klicken Sie auf **Kategoriehierarchie bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="5dfe3-133">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-133">Click **Edit**.</span></span>
5. <span data-ttu-id="5dfe3-134">In der Struktur wählen Sie **Mode \> Damenmode \> Damenschuhe** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="5dfe3-135">Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="5dfe3-136">In der Struktur wählen Sie **Mode \> Damenmode \> Oberteile** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="5dfe3-137">Ebenso können Sie die Sortierreihenfolge für die Unterkategorien definieren.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="5dfe3-138">In der Struktur wählen Sie **Mode \> Herrenmode \> Freizeithemden** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="5dfe3-139">Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="5dfe3-140">In der Struktur wählen Sie **Mode \> Herrenmode \> Mäntel & Jacken** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="5dfe3-141">Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="5dfe3-142">Wiederholen Sie dies für alle weiteren Kategorien, für die Sie die Reihenfolge ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="5dfe3-143">Der Anzeigereihenfolge für die Kanalnavigationshierarchie wird in HQ, im Katalog und in Kanälen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Kanalnavigationshierarchie: Benutzerdefinierte Sortierung](./media/ChannelNavCustomSorted.png)

![Katalognavigationshierarchie: Benutzerdefinierte Sortierung auf Basis der Kanalnavigationshierarchie](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS mit benutzerdefiniert sortierten Kategorien](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="5dfe3-147">Standardmäßig ist die Funktion für die benutzerdefinierte Sortierreihenfolge deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5dfe3-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="5dfe3-148">Um zu erfahren, wie Sie diese Funktion und andere Funktionen aktivieren können, siehe [Funktionsverwaltung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="5dfe3-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
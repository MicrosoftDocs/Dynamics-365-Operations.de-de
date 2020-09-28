---
title: Navigationsmenümodul
description: Dieses Thema enthält Navigationsmenümodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761391"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="8bb4b-103">Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="8bb4b-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="8bb4b-104">Dieses Thema enthält Navigationsmenümodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8bb4b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8bb4b-105">Overview</span></span>

<span data-ttu-id="8bb4b-106">Der Hauptzweck von Navigationsmenümodulen besteht darin, Website-Benutzern das Durchsuchen von Produkten und Website-Seiten gemäß der in Dynamics 365 Commerce-Zentralverwaltung definierten Kanalnavigationshierarchie zu ermöglichen .</span><span class="sxs-lookup"><span data-stu-id="8bb4b-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="8bb4b-107">In einem Navigationsmenümodul konfigurierte Elemente werden als Website-Header-Navigation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="8bb4b-108">Navigationsmenümodule unterstützen auch statische Menüelemente, die auf andere Seiten einer E-Commerce-Wensite verweisen.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="8bb4b-109">Das Navigationsmenümodul kann dem Header-Modul einer Seite hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="8bb4b-110">Im Fabrikam-Design werden im Navigationsmenü standardmäßig zwei Ebenen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="8bb4b-111">Im Starter-Design werden im Navigationsmenü standardmäßig drei Ebenen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="8bb4b-112">Um die Anzahl der Ebenen zu ändern, ist eine Ansichtserweiterung für das Design erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="8bb4b-113">Die folgende Abbildung zeigt ein Beispiel für ein Navigationsmenü für die Fabrikam-Website mit zwei Ebenen der Kategoriehierarchie und einigen statischen Menüelementen.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="8bb4b-114">![Beispiel eines Navigationsmenümoduls](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="8bb4b-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="8bb4b-115">Eigenschaften des Navigationsmenümoduls</span><span class="sxs-lookup"><span data-stu-id="8bb4b-115">Navigation menu module properties</span></span>

| <span data-ttu-id="8bb4b-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="8bb4b-116">Property name</span></span>             | <span data-ttu-id="8bb4b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8bb4b-117">Value</span></span>                 | <span data-ttu-id="8bb4b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bb4b-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8bb4b-119">Grundlage</span><span class="sxs-lookup"><span data-stu-id="8bb4b-119">Source</span></span>                  | <span data-ttu-id="8bb4b-120">**Retail**, **Manuelle Dokumenterstellung**, **Retail und manuelle Dokumenterstellung**</span><span class="sxs-lookup"><span data-stu-id="8bb4b-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="8bb4b-121">Der **Retail**-Wert ermöglicht der Kanalnavigationshierarchie der Commerce-Zentralverwaltung im Navigationsmenü angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="8bb4b-122">Der Wert **Manuelle Dokumenterstellung** ermöglicht das Kuratieren statische Menüelemente.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="8bb4b-123">Der Wert **Retail und manuelle Dokumenterstellung** ermöglicht eine Mischung aus beiden.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="8bb4b-124">Kategoriebilder anzeigen</span><span class="sxs-lookup"><span data-stu-id="8bb4b-124">Show category images</span></span> | <span data-ttu-id="8bb4b-125">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="8bb4b-125">**True** or **False**</span></span>    | <span data-ttu-id="8bb4b-126">Wenn diese Eigenschaft aktiviert ist, werden Kategoriebilder so im Navigationsmenü angezeigt, wie Sie in der Commerce-Zentralverwaltung für jede Kategorie definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="8bb4b-127">Hinzugefügt in Commerce-Version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="8bb4b-128">Statisches Menüelement</span><span class="sxs-lookup"><span data-stu-id="8bb4b-128">Static menu item</span></span>| <span data-ttu-id="8bb4b-129">Wertearray</span><span class="sxs-lookup"><span data-stu-id="8bb4b-129">Array of values</span></span>| <span data-ttu-id="8bb4b-130">Statische Menüelemente, die einen Menüelementnamen mit einem Link zu einer statischen Website-Seite verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="8bb4b-131">Sie können Menüelemente unter anderen Menüelementen erstellen.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="8bb4b-132">Standardmäßig werden statische Menüs auf der Stammebene angezeigt und an die Kanalnavigationshierarchie angehängt, falls diese vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="8bb4b-133">Die folgende Abbildung zeigt ein Beispiel für ein Kategoriebild, das im Navigationsmenü für die Fabrikam-Website angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8bb4b-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="8bb4b-134">![Beispiel eines Navigationsmoduls mit Kategoriebildern](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="8bb4b-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="8bb4b-135">Hinzufügen eines Header-Moduls zu einem Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="8bb4b-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="8bb4b-136">Ausführliche Informationen zum Hinzufügen eines Navigationsmenümoduls zu einem Header-Modul finden Sie unter [Header-Modul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="8bb4b-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8bb4b-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8bb4b-137">Additional resources</span></span>

[<span data-ttu-id="8bb4b-138">Überblick über das Starterkit</span><span class="sxs-lookup"><span data-stu-id="8bb4b-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8bb4b-139">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="8bb4b-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8bb4b-140">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="8bb4b-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="8bb4b-141">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="8bb4b-141">Header module</span></span>](author-header-module.md)

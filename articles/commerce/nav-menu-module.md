---
title: Navigationsmenümodul
description: Dieses Thema enthält Navigationsmenümodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4412701"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="7a064-103">Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="7a064-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a064-104">Dieses Thema enthält Navigationsmenümodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7a064-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7a064-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7a064-105">Overview</span></span>

<span data-ttu-id="7a064-106">Der Hauptzweck von Navigationsmenümodulen besteht darin, Website-Benutzern das Durchsuchen von Produkten und Website-Seiten gemäß der in Dynamics 365 Commerce-Zentralverwaltung definierten Kanalnavigationshierarchie zu ermöglichen .</span><span class="sxs-lookup"><span data-stu-id="7a064-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="7a064-107">In einem Navigationsmenümodul konfigurierte Elemente werden als Website-Header-Navigation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a064-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="7a064-108">Navigationsmenümodule unterstützen auch statische Menüelemente, die auf andere Seiten einer E-Commerce-Wensite verweisen.</span><span class="sxs-lookup"><span data-stu-id="7a064-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="7a064-109">Das Navigationsmenümodul kann dem Header-Modul einer Seite hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7a064-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="7a064-110">Im Fabrikam-Design werden im Navigationsmenü standardmäßig zwei Ebenen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a064-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="7a064-111">Im Starter-Design werden im Navigationsmenü standardmäßig drei Ebenen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a064-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="7a064-112">Um die Anzahl der Ebenen zu ändern, ist eine Ansichtserweiterung für das Design erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a064-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="7a064-113">Die folgende Abbildung zeigt ein Beispiel für ein Navigationsmenü für die Fabrikam-Website mit zwei Ebenen der Kategoriehierarchie und einigen statischen Menüelementen.</span><span class="sxs-lookup"><span data-stu-id="7a064-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="7a064-114">![Beispiel eines Navigationsmenümoduls](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="7a064-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="7a064-115">Eigenschaften des Navigationsmenümoduls</span><span class="sxs-lookup"><span data-stu-id="7a064-115">Navigation menu module properties</span></span>

| <span data-ttu-id="7a064-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="7a064-116">Property name</span></span>             | <span data-ttu-id="7a064-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7a064-117">Value</span></span>                 | <span data-ttu-id="7a064-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a064-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="7a064-119">Grundlage</span><span class="sxs-lookup"><span data-stu-id="7a064-119">Source</span></span>                  | <span data-ttu-id="7a064-120">**Retail**, **Manuelle Dokumenterstellung**, **Retail und manuelle Dokumenterstellung**</span><span class="sxs-lookup"><span data-stu-id="7a064-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="7a064-121">Der **Retail**-Wert ermöglicht der Kanalnavigationshierarchie der Commerce-Zentralverwaltung im Navigationsmenü angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="7a064-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="7a064-122">Der Wert **Manuelle Dokumenterstellung** ermöglicht das Kuratieren statische Menüelemente.</span><span class="sxs-lookup"><span data-stu-id="7a064-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="7a064-123">Der Wert **Retail und manuelle Dokumenterstellung** ermöglicht eine Mischung aus beiden.</span><span class="sxs-lookup"><span data-stu-id="7a064-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="7a064-124">Kategoriebilder anzeigen</span><span class="sxs-lookup"><span data-stu-id="7a064-124">Show category images</span></span> | <span data-ttu-id="7a064-125">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="7a064-125">**True** or **False**</span></span>    | <span data-ttu-id="7a064-126">Wenn diese Eigenschaft aktiviert ist, werden Kategoriebilder so im Navigationsmenü angezeigt, wie Sie in der Commerce-Zentralverwaltung für jede Kategorie definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7a064-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="7a064-127">Hinzugefügt in Commerce-Version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="7a064-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="7a064-128">Aktivieren Sie das mehrstufige Navigationsmenü</span><span class="sxs-lookup"><span data-stu-id="7a064-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="7a064-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="7a064-129">**True** or **False**</span></span> | <span data-ttu-id="7a064-130">Wenn diese Eigenschaft aktiviert ist, kann das Navigationsmenü mehrere Ebenen der Navigationshierarchie anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a064-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="7a064-131">Diese Funktion ist nur in Dynamics 365 Commerce, Release 10.0.15 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a064-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="7a064-132">Anzahl der Ebenen</span><span class="sxs-lookup"><span data-stu-id="7a064-132">Number of levels</span></span> | <span data-ttu-id="7a064-133">Integer</span><span class="sxs-lookup"><span data-stu-id="7a064-133">integer</span></span> | <span data-ttu-id="7a064-134">Diese Eigenschaft definiert die Anzahl der Ebenen, die angezeigt werden sollen, wenn die Eigenschaft **Aktivieren Sie das mehrstufige Navigationsmenü** auf **Wahr** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7a064-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="7a064-135">Statisches Menüelement</span><span class="sxs-lookup"><span data-stu-id="7a064-135">Static menu item</span></span>| <span data-ttu-id="7a064-136">Wertearray</span><span class="sxs-lookup"><span data-stu-id="7a064-136">Array of values</span></span>| <span data-ttu-id="7a064-137">Statische Menüelemente, die einen Menüelementnamen mit einem Link zu einer statischen Website-Seite verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7a064-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="7a064-138">Sie können Menüelemente unter anderen Menüelementen erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a064-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="7a064-139">Standardmäßig werden statische Menüs auf der Stammebene angezeigt und an die Kanalnavigationshierarchie angehängt, falls diese vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7a064-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="7a064-140">Stamm-Menü anzeigen</span><span class="sxs-lookup"><span data-stu-id="7a064-140">Show root menu</span></span> | <span data-ttu-id="7a064-141">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="7a064-141">**True** or **False**</span></span> | <span data-ttu-id="7a064-142">Wenn diese Eigenschaft aktiviert ist, kann das Navigationsmenü unter einem benutzerdefinierten Stamm definiert werden (z. B. **Jetzt einkaufen**).</span><span class="sxs-lookup"><span data-stu-id="7a064-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="7a064-143">Diese Funktion ist nur in Dynamics 365 Commerce, Release 10.0.15 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a064-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="7a064-144">Stamm-Menü</span><span class="sxs-lookup"><span data-stu-id="7a064-144">Root menu</span></span> | <span data-ttu-id="7a064-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7a064-145">string</span></span> | <span data-ttu-id="7a064-146">Diese Eigenschaft kann verwendet werden, um Text für einen benutzerdefinierten Stamm zu definieren, wenn die **Stamm-Menü anzeigen** Eigenschaft ist auf **Wahr** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7a064-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="7a064-147">Die folgende Abbildung zeigt ein Beispiel für ein Kategoriebild, das im Navigationsmenü für die Fabrikam-Website angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7a064-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="7a064-148">![Beispiel eines Navigationsmoduls mit Kategoriebildern](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="7a064-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="7a064-149">Hinzufügen eines Header-Moduls zu einem Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="7a064-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="7a064-150">Ausführliche Informationen zum Hinzufügen eines Navigationsmenümoduls zu einem Header-Modul finden Sie unter [Header-Modul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="7a064-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a064-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a064-151">Additional resources</span></span>

[<span data-ttu-id="7a064-152">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="7a064-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7a064-153">Breadcrumb-Modul</span><span class="sxs-lookup"><span data-stu-id="7a064-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="7a064-154">Siteauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="7a064-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="7a064-155">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="7a064-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7a064-156">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="7a064-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="7a064-157">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="7a064-157">Header module</span></span>](author-header-module.md)

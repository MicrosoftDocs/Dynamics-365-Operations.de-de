---
title: Anpassen der Sitenavigation
description: In diesem Thema wird beschrieben, wie Sie eine benutzerdefinierte Online-Navigationshierarchie erstellen, um die Produkte für das Durchsuchen auf Ihrer Microsoft Dynamics 365 Commerce-Site zu organisieren.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cfd0a9559eb2b596adb822b228929e6855711bb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222608"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="4a977-103">Navigation auf der Website anpassen</span><span class="sxs-lookup"><span data-stu-id="4a977-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4a977-104">In diesem Thema wird beschrieben, wie Sie eine benutzerdefinierte Online-Navigationshierarchie erstellen, um die Produkte für das Durchsuchen auf Ihrer Microsoft Dynamics 365 Commerce-Site zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="4a977-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="4a977-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4a977-105">Overview</span></span>

<span data-ttu-id="4a977-106">Online-Schaufenster ermöglichen es Debitoren, Produkte zu entdecken und zu suchen, indem sie durch Produktkategorien navigieren.</span><span class="sxs-lookup"><span data-stu-id="4a977-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="4a977-107">Diese Funktion wird normalerweise von den Registerkarten am oberen Seitenrand oder auf einer Navigationsleiste links bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4a977-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="4a977-108">In Dynamics 365 Commerce können Sie die hierarchische Struktur der Kategorienavigation und der Produkte erstellen und verwalten, die in den unterschiedlichen Kategorien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4a977-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="4a977-109">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="4a977-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="4a977-110">Um eine Kanalnavigationshierarchie zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="4a977-111">Navigieren Sie zu **Retail and Commerce \> Produkte und Kategorien \> Kategorie- und Produktverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="4a977-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="4a977-112">Wählen Sie **Kategoriehierarchien** und **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="4a977-113">Der Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a977-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4a977-114">Die oberste Kategorie, die Sie erstellen, ist der Stammkategorieknoten.</span><span class="sxs-lookup"><span data-stu-id="4a977-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="4a977-115">Sie wird nicht auf dem Standort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a977-115">It won't be shown on your site.</span></span> <span data-ttu-id="4a977-116">Um eine Kategoriehierarchie zu erstellen, in der ein einzelner oberste Knoten auf dem Standort angezeigt wird, erstellen und benennen Sie die Kategorie als untergeordnetes Element der Stammkategorie.</span><span class="sxs-lookup"><span data-stu-id="4a977-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="4a977-117">Wählen Sie **Neuer Kategorieknoten** und benennen Sie die Kategorie.</span><span class="sxs-lookup"><span data-stu-id="4a977-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="4a977-118">Fahren Sie fort, um gleichgeordnete und untergeordnete Kategorien nach Bedarf zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a977-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="4a977-119">Sie können Produkte nun jeder Kategorie zuweisen, die Sie unter der obersten Ebene erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a977-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="4a977-120">Passen Sie die Reihenfolge der Kategorien an</span><span class="sxs-lookup"><span data-stu-id="4a977-120">Customize the order of categories</span></span>

<span data-ttu-id="4a977-121">Standardmäßig werden die Kategorien, die Sie festlegen, in alphabetischer Reihenfolge auf der Site angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a977-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="4a977-122">Allerdings können Sie die Anzeigereihenfolge der Kategorien auch anpassen.</span><span class="sxs-lookup"><span data-stu-id="4a977-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="4a977-123">Zuweisen eines Kategoriehierarchietyps</span><span class="sxs-lookup"><span data-stu-id="4a977-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="4a977-124">Navigieren Sie zu **Retail and Commerce \> Produkte und Kategorien \> Kategorie- und Produktverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="4a977-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="4a977-125">Wählen Sie **Kategoriehierarchien**.</span><span class="sxs-lookup"><span data-stu-id="4a977-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="4a977-126">Klicken Sie im Aktivitätsbereich auf der Registerkarte auf **Kategoriehierarchie** in der Gruppe **Einrichten** und wählen Sie **Hierarchietyp zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="4a977-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="4a977-127">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-127">Select **New**.</span></span>
1. <span data-ttu-id="4a977-128">Wählen Sie im Feld **Kategoriehierarchietyp** die **Kanalnavigationshierarchie** aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="4a977-129">Wählen Sie im Feld **Kategoriehierarchie** die Kanalnavigationshierarchie aus, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a977-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="4a977-130">Veröffentlichen Sie die neuen oder aktualisierten Navigationshierarchien</span><span class="sxs-lookup"><span data-stu-id="4a977-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="4a977-131">Um Ihre Navigationshierarchie im Online Schaufenster verfügbar zu machen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="4a977-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="4a977-132">Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.</span><span class="sxs-lookup"><span data-stu-id="4a977-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="4a977-133">In der Struktur auf der linken Seite wählen Sie den Onlineshop aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="4a977-134">Wählen Sie **Kanalupdates veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="4a977-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="4a977-135">Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="4a977-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="4a977-136">Wählen Sie **Job 1040** suchen und auswählen.</span><span class="sxs-lookup"><span data-stu-id="4a977-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="4a977-137">Wählen Sie **Jetzt ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-137">Select **Run now**.</span></span>
1. <span data-ttu-id="4a977-138">Wiederholen Sie die Schritte 5 und 6 für Job 1070 und 1150.</span><span class="sxs-lookup"><span data-stu-id="4a977-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="4a977-139">Anzeigen der Kategorien auf der Site</span><span class="sxs-lookup"><span data-stu-id="4a977-139">Show categories on your site</span></span>

<span data-ttu-id="4a977-140">Um Ihre Kategoriehierarchie in Ihrem Online-Schaufenster anzuzeigen, müssen Sie das Navigationsmenümodul am geeigneten Speicherort in einer Vorlage oder Fragment hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a977-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="4a977-141">Das Navigationsmenümodul wird dann in der Navigationshierarchie angezeigt, vorausgesetzt, die Navigationshierarchie wurde im Kanal veröffentlicht, mit dem Ihre Site verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4a977-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="4a977-142">Mit dem Navigationsmenümodul, das in der Modulbibliothek enthalten ist, können Benutzer nur zu Kategorien navigieren, die keine Unterkategorien umfassen.</span><span class="sxs-lookup"><span data-stu-id="4a977-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="4a977-143">Wenn Ihre Debitoren nicht in der Lage sind, zu der Kategorien zu navigieren, die Unterkategorien umfassen, müssen Sie das Navigationsmenümodul anpassen.</span><span class="sxs-lookup"><span data-stu-id="4a977-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="4a977-144">Fügen Sie benutzerdefinierte Navigationsoptionen hinzu</span><span class="sxs-lookup"><span data-stu-id="4a977-144">Add custom navigation options</span></span>

<span data-ttu-id="4a977-145">Auf dem Navigationsmenü können Sie Navigationsoptionen hinzufügen, die nicht Teil der Hierarchie Ihrer Produktkategorie sind.</span><span class="sxs-lookup"><span data-stu-id="4a977-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="4a977-146">Zum Beispiel am Ende der Liste der Produktkategorien können Sie ein Element **Kontaktieren Sie uns** hinzufügen, das auf die Kontaktseite verweist, die Sie für Ihren Standort erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a977-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="4a977-147">Um benutzerdefinierte Navigationsoptionen Ihrem Navigationsmenü hinzuzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="4a977-148">In der Vorlage oder im Fragment, das Sie anpassen möchten, wählen Sie das Navigationsmenümodul aus.</span><span class="sxs-lookup"><span data-stu-id="4a977-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="4a977-149">Im Eigenschaftenbereich auf der Registerkarte **Daten**, wählen Sie **Artikel hinzufügen**, um einen neuen Navigationsartikel des Content Management-Systems (CMS) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a977-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="4a977-150">Geben Sie Hyperlinktext und eine URL ein.</span><span class="sxs-lookup"><span data-stu-id="4a977-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="4a977-151">Wiederholen Sie die Schritte 2 und 3, um kundenspezifischere Navigationsoptionen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a977-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="4a977-152">Wenn Sie fertig sind, wählen Sie **Speichern**, um die Vorlage oder das Fragment zu speichern, und wählen Sie dann **Bearbeitung beenden**, um diese einzuchecken.</span><span class="sxs-lookup"><span data-stu-id="4a977-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a977-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a977-153">Additional resources</span></span>

[<span data-ttu-id="4a977-154">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="4a977-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4a977-155">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="4a977-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="4a977-156">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="4a977-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="4a977-157">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="4a977-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="4a977-158">Arbeiten mit Modulen</span><span class="sxs-lookup"><span data-stu-id="4a977-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="4a977-159">Erstellen einer Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="4a977-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="4a977-160">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="4a977-160">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
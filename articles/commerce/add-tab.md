---
title: Registerkartenmodul
description: Dieses Thema behandelt Registerkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: c865d5e055e3fadf2dda225b49f13a163974768f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797454"
---
# <a name="tab-module"></a><span data-ttu-id="aac50-103">Registerkartenmodul</span><span class="sxs-lookup"><span data-stu-id="aac50-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aac50-104">Dieses Thema behandelt Registerkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aac50-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aac50-105">Registerkartenmodule sind containerähnliche Module, mit denen die Informationen auf einer Site-Seite auf Registerkarten organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="aac50-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="aac50-106">Sie können auf jeder Seite verwendet werden, auf der Informationen auf Registerkarten angezeigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="aac50-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="aac50-107">In jedem Registerkartenmodul kann ein oder mehrere Registerkartenelemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aac50-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="aac50-108">Jedes Registerkartenelementmodul repräsentiert eine einzelne Registerkarte. In jedem Registerkartenelementmodul können ein oder mehrere Module hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aac50-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="aac50-109">Es gibt keine Einschränkungen hinsichtlich der Modultypen, die einem Registerkartenelementmodul hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="aac50-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="aac50-110">Das folgende Bild zeigt ein Beispiel eines Registerkartenmoduls, das auf einer Homepage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aac50-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="aac50-111">In diesem Beispiel ist die **Versand** Registerkarte ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="aac50-111">In this example, the **Shipping** tab selected.</span></span>

![Beispiel eines Registerkarten-Moduls](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="aac50-113">Registerkartenmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="aac50-113">Tab module properties</span></span>

| <span data-ttu-id="aac50-114">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="aac50-114">Property name</span></span> | <span data-ttu-id="aac50-115">Werte</span><span class="sxs-lookup"><span data-stu-id="aac50-115">Values</span></span> | <span data-ttu-id="aac50-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aac50-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="aac50-117">Überschrift</span><span class="sxs-lookup"><span data-stu-id="aac50-117">Heading</span></span> | <span data-ttu-id="aac50-118">Text</span><span class="sxs-lookup"><span data-stu-id="aac50-118">Text</span></span> | <span data-ttu-id="aac50-119">Diese Eigenschaft gibt eine optionale Textüberschrift für das Registerkartenmodul an.</span><span class="sxs-lookup"><span data-stu-id="aac50-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="aac50-120">Aktiver Registerkartenindex</span><span class="sxs-lookup"><span data-stu-id="aac50-120">Active Tab Index</span></span> | <span data-ttu-id="aac50-121">Nummer</span><span class="sxs-lookup"><span data-stu-id="aac50-121">Number</span></span> | <span data-ttu-id="aac50-122">Diese Eigenschaft gibt die Registerkarte an, die beim Laden einer Seite standardmäßig aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="aac50-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="aac50-123">Wenn kein Wert angegeben wird, ist das erste Registerkartenelement standardmäßig aktiv.</span><span class="sxs-lookup"><span data-stu-id="aac50-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="aac50-124">Registerkartenelementmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="aac50-124">Tab item module properties</span></span>

| <span data-ttu-id="aac50-125">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="aac50-125">Property name</span></span> | <span data-ttu-id="aac50-126">Werte</span><span class="sxs-lookup"><span data-stu-id="aac50-126">Values</span></span> | <span data-ttu-id="aac50-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aac50-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="aac50-128">Titel</span><span class="sxs-lookup"><span data-stu-id="aac50-128">Title</span></span> | <span data-ttu-id="aac50-129">Text</span><span class="sxs-lookup"><span data-stu-id="aac50-129">Text</span></span> | <span data-ttu-id="aac50-130">Diese Eigenschaft gibt die Textüberschrift für das Registerkartenelementmodul an.</span><span class="sxs-lookup"><span data-stu-id="aac50-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="aac50-131">Ein Registerkartenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="aac50-131">Add a tab module to a page</span></span>

<span data-ttu-id="aac50-132">Um ein Registerkartenmodul einer Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="aac50-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="aac50-133">Verwenden Sie die Fabrikam-Marketingvorlage (oder eine Vorlage ohne Einschränkungen), um eine neue Seite mit dem Namen **Richtlinienseite speichern** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aac50-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="aac50-134">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="aac50-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aac50-135">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="aac50-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aac50-136">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="aac50-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aac50-137">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Registerkarte** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="aac50-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aac50-138">Wählen Sie im Eigenschaftenbereich des Registerkartenmoduls die Option **Überschrift** neben dem Stiftsymbol.</span><span class="sxs-lookup"><span data-stu-id="aac50-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="aac50-139">In dem **Überschrift** Dialogfeld unter **Überschriftstext** geben Sie den Überschriftentext ein (z. B. **Richtlinien**).</span><span class="sxs-lookup"><span data-stu-id="aac50-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="aac50-140">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="aac50-140">Then select **OK**.</span></span>
1. <span data-ttu-id="aac50-141">Wählen Sie im Slot **Registerkarte** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="aac50-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aac50-142">Im Dialogfeld **Modul hinzufügen** wählen Sie das **Registerkartenelement**-Modul und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="aac50-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aac50-143">Im Eigenschaftenbereich des Registerkartenelementmoduls unter **Titel** geben Sie den Titeltext ein (z. B. **Lieferung**).</span><span class="sxs-lookup"><span data-stu-id="aac50-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="aac50-144">Wählen Sie im Slot **Registerkartenelement** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="aac50-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aac50-145">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Textblock** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="aac50-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aac50-146">Fügen Sie im Eigenschaftenbereich des Textblockmoduls unter **Rich Text** einen Textabschnitt hinzu.</span><span class="sxs-lookup"><span data-stu-id="aac50-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="aac50-147">Im Slot **Registerkarte** fügen Sie einige weitere Registerkartenelementmodule mit Titeln hinzu.</span><span class="sxs-lookup"><span data-stu-id="aac50-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="aac50-148">Fügen Sie in jedem Registerkartenelementmodul ein Textblockmodul mit Inhalt hinzu.</span><span class="sxs-lookup"><span data-stu-id="aac50-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="aac50-149">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aac50-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="aac50-150">Auf der Seite wird ein Registerkartenmodul angezeigt, das Registerkartenelementmodule enthält, deren Inhalt Sie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="aac50-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="aac50-151">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="aac50-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aac50-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aac50-152">Additional resources</span></span>

[<span data-ttu-id="aac50-153">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="aac50-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aac50-154">Containermodul</span><span class="sxs-lookup"><span data-stu-id="aac50-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="aac50-155">Akkordeonmodul</span><span class="sxs-lookup"><span data-stu-id="aac50-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="aac50-156">Textblockmodul</span><span class="sxs-lookup"><span data-stu-id="aac50-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Akkordeon Modul
description: Dieses Thema enthält Akkordeonmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417253"
---
# <a name="accordion-module"></a><span data-ttu-id="a494a-103">Akkordeon Modul</span><span class="sxs-lookup"><span data-stu-id="a494a-103">Accordion module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a494a-104">Dieses Thema enthält Akkordeonmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a494a-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a494a-105">Overview</span></span>

<span data-ttu-id="a494a-106">Akkordeonmodule sind containerähnliche Module, mit denen die Informationen oder Module auf einer Seite organisiert werden, indem eine zusammenklappbare schubladenähnliche Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a494a-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="a494a-107">Ein Akkordeonmodul kann auf jeder Seite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="a494a-108">In jedem Akkordeonmodul können ein oder mehrere Akkordeongegenstandsmodule hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="a494a-109">Jedes Akkordeonelementsmodul repräsentiert eine reduzierbare Schublade.</span><span class="sxs-lookup"><span data-stu-id="a494a-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="a494a-110">edem Akkordeonmodul können ein oder mehrere Akkordeonartikelmodule hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="a494a-111">Es gibt keine Einschränkungen hinsichtlich der Modultypen, die einem Akkordeonartikeltmodul hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="a494a-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="a494a-112">Das folgende Bild zeigt ein Beispiel eines Akkordeonmoduls, mit dem Informationen auf der Seite mit häufig gestellten Fragen (FAQ) eines Geschäfts organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Beispiel eines Akkordeonmoduls](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="a494a-114">Eigenschaften des Akkordeonmoduls</span><span class="sxs-lookup"><span data-stu-id="a494a-114">Accordion module properties</span></span>

| <span data-ttu-id="a494a-115">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="a494a-115">Property name</span></span> | <span data-ttu-id="a494a-116">Werte</span><span class="sxs-lookup"><span data-stu-id="a494a-116">Values</span></span> | <span data-ttu-id="a494a-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a494a-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="a494a-118">Überschrift</span><span class="sxs-lookup"><span data-stu-id="a494a-118">Heading</span></span> | <span data-ttu-id="a494a-119">Text</span><span class="sxs-lookup"><span data-stu-id="a494a-119">Text</span></span> | <span data-ttu-id="a494a-120">Diese Eigenschaft gibt eine optionale Textüberschrift für das Akkordeonmodul an.</span><span class="sxs-lookup"><span data-stu-id="a494a-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="a494a-121">Alle Ebenen erweitern</span><span class="sxs-lookup"><span data-stu-id="a494a-121">Expand All</span></span> | <span data-ttu-id="a494a-122">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="a494a-122">**True** or **False**</span></span> | <span data-ttu-id="a494a-123">Wenn der Wert auf **Wahr** eingestellt ist, ist die Funktion zum Erweitern/Reduzieren aktiviert, sodass alle Elemente im Akkordeonmodul erweitert und reduziert werden können.</span><span class="sxs-lookup"><span data-stu-id="a494a-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="a494a-124">Interaktionsstil</span><span class="sxs-lookup"><span data-stu-id="a494a-124">Interaction Style</span></span> | <span data-ttu-id="a494a-125">**Unabhängig** oder **Nur ein Artikel erweitern**</span><span class="sxs-lookup"><span data-stu-id="a494a-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="a494a-126">Diese Eigenschaft definiert den Interaktionsstil für Akkordeonelemente.</span><span class="sxs-lookup"><span data-stu-id="a494a-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="a494a-127">Wenn der Wert auf **Unabhängig** eingestellt ist, kann jeder Akkordeonartikel unabhängig erweitert oder reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="a494a-128">Wenn der Wert auf **Erweitern Sie nur einen Artikel** eingestellt ist, kann jeweils nur ein Artikel erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="a494a-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="a494a-129">Wenn Elemente erweitert werden, werden zuvor erweiterte Artikel reduziert.</span><span class="sxs-lookup"><span data-stu-id="a494a-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="a494a-130">Eigenschaften des Akkordeonartikelmoduls</span><span class="sxs-lookup"><span data-stu-id="a494a-130">Accordion item module properties</span></span>

| <span data-ttu-id="a494a-131">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="a494a-131">Property name</span></span> | <span data-ttu-id="a494a-132">Werte</span><span class="sxs-lookup"><span data-stu-id="a494a-132">Values</span></span> | <span data-ttu-id="a494a-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a494a-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="a494a-134">Titel</span><span class="sxs-lookup"><span data-stu-id="a494a-134">Title</span></span> | <span data-ttu-id="a494a-135">Text</span><span class="sxs-lookup"><span data-stu-id="a494a-135">Text</span></span> | <span data-ttu-id="a494a-136">Diese Eigenschaft gibt die Textüberschrift für das Akkordeonelementmodul an.</span><span class="sxs-lookup"><span data-stu-id="a494a-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="a494a-137">Durch Auswahl des Titelbereichs können Benutzer den Abschnitt erweitern oder reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a494a-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="a494a-138">Standardmäßig erweitern</span><span class="sxs-lookup"><span data-stu-id="a494a-138">Expand by default</span></span> | <span data-ttu-id="a494a-139">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="a494a-139">**True** or **False**</span></span> | <span data-ttu-id="a494a-140">Wenn der Wert auf **Wahr** eingestellt ist, wird das Akkordeonelement beim Laden der Seite standardmäßig erweitert.</span><span class="sxs-lookup"><span data-stu-id="a494a-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="a494a-141">Ein Akkordeonmodul einer FAQ-Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a494a-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="a494a-142">Um ein Akkordeonmodul einer FAQ-Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="a494a-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="a494a-143">Gehen Sie zu **Seiten** und verwenden Sie die Fabrikam-Marketingvorlage (oder eine Vorlage ohne Einschränkungen), um eine neue Seite mit dem Namen **FAQ speichern** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a494a-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="a494a-144">Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a494a-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a494a-145">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a494a-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a494a-146">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a494a-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a494a-147">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Akkordeon** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a494a-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a494a-148">Wählen Sie im Eigenschaftenbereich des Akkordeonmoduls die Option **Überschrift** neben dem Stiftsymbol.</span><span class="sxs-lookup"><span data-stu-id="a494a-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="a494a-149">In dem **Überschrift** Dialogfeld unter **Überschriftstex** geben Sie **Häufig gestellte Fragen** ein.</span><span class="sxs-lookup"><span data-stu-id="a494a-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="a494a-150">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a494a-150">Then select **OK**.</span></span>
1. <span data-ttu-id="a494a-151">Wählen Sie im Eigenschaftenbereich des Akkordeonmoduls das Kontrollkästchen **alle erweitern anzeigen** und dann im Feld **Interaktionsstil** **Unabhängig**.</span><span class="sxs-lookup"><span data-stu-id="a494a-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="a494a-152">Wählen Sie im Slot **Akkordeon** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a494a-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a494a-153">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Akkordeonelement** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a494a-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a494a-154">Im Eigenschaftenbereich des Akkordeonelementmoduls unter **Titel** geben Sie den Titeltext ein (z. B. **Wie funktionieren Retouren?**).</span><span class="sxs-lookup"><span data-stu-id="a494a-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="a494a-155">Wählen Sie im Slot **Akkordeonelement** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a494a-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a494a-156">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Textblock** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a494a-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a494a-157">Geben Sie im Eigenschaftenbereich des Textblockmoduls einen Textabsatz ein (z. B. **Rücksendungen müssen über das Call Center bearbeitet werden. Wenden Sie sich für Rücksendungen an 1-800-FABRIKAM. Produkte haben ein 30-tägiges Rückgaberecht. Rückgaben müssen innerhalb dieses Zeitraums eingeleitet werden.**).</span><span class="sxs-lookup"><span data-stu-id="a494a-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="a494a-158">In dem **Akkordeon** Slot fügen Sie ein paar weitere Akkordeonelementmodule hinzu.</span><span class="sxs-lookup"><span data-stu-id="a494a-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="a494a-159">Fügen Sie in jedem Akkordeonelementmodul ein Textblockmodul mit Inhalt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a494a-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="a494a-160">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a494a-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="a494a-161">Auf der Seite wird ein Akkordeonmodul angezeigt, das den von Ihnen hinzugefügten Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="a494a-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="a494a-162">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a494a-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a494a-163">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a494a-163">Additional resources</span></span>

[<span data-ttu-id="a494a-164">Überblick über Starterkit</span><span class="sxs-lookup"><span data-stu-id="a494a-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a494a-165">Containermodul</span><span class="sxs-lookup"><span data-stu-id="a494a-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a494a-166">Registerkartenmodul</span><span class="sxs-lookup"><span data-stu-id="a494a-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="a494a-167">Textblockmodul</span><span class="sxs-lookup"><span data-stu-id="a494a-167">Text block module</span></span>](add-content-rich-block.md)

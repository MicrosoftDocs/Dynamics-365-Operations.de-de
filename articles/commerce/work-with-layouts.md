---
title: Arbeiten mit Voreinstellungslayouts
description: In diesem Thema wird beschrieben, wie Sie in Microsoft Dynamics 365 Commerce mit vordefinierten Layouts arbeiten.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793920"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="62ee8-103">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="62ee8-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62ee8-104">In diesem Thema wird beschrieben, wie Sie in Microsoft Dynamics 365 Commerce mit vordefinierten Layouts arbeiten.</span><span class="sxs-lookup"><span data-stu-id="62ee8-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="62ee8-105">Bevor Sie die Prozeduren in diesem Thema abschließen, lesen Sie unbedingt [Vordefinierte und benutzerdefinierte Layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="62ee8-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="62ee8-106">Einen allgemeinen Überblick erhalten Sie in [Übersicht über Vorlagen und Layouts](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="62ee8-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="62ee8-107">Ein neues vordefiniertes Layout erstellen</span><span class="sxs-lookup"><span data-stu-id="62ee8-107">Create a new preset layout</span></span>

<span data-ttu-id="62ee8-108">Es gibt zwei Methoden zum Erstellen eines vordefinierten Layouts.</span><span class="sxs-lookup"><span data-stu-id="62ee8-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="62ee8-109">Sie können ein vorhandenes benutzerdefiniertes Layout als neues vordefiniertes Layout speichern oder ein vordefiniertes Layout von Grund auf neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="62ee8-110">Erstellen eines vordefinierten Layouts aus einem vorhandenen benutzerdefinierten Layout</span><span class="sxs-lookup"><span data-stu-id="62ee8-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="62ee8-111">Gehen Sie folgendermaßen vor, um ein vordefiniertes Layout aus einem vorhandenen benutzerdefinierten Layout zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="62ee8-112">Öffnen Sie eine vorhandene Seite, die derzeit kein vordefiniertes Layout verwendet und deren Modulstruktur Sie für andere Seiten Ihrer Site wiederverwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="62ee8-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="62ee8-113">Wählen Sie **Bearbeiten** aus, um die Seite auszuchecken.</span><span class="sxs-lookup"><span data-stu-id="62ee8-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="62ee8-114">Wählen Sie **Als neues Layout speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-114">Select **Save as new layout**.</span></span> <span data-ttu-id="62ee8-115">Das Dialogfeld **Als neues Layout speichern** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="62ee8-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="62ee8-116">Geben Sie einen Namen und eine Beschreibung für Ihr vordefiniertes Layout ein.</span><span class="sxs-lookup"><span data-stu-id="62ee8-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="62ee8-117">Die von Ihnen eingegebenen Werte werden anderen Autoren angezeigt, wenn sie neue Seiten aus Ihrem Layout erstellen oder zu diesem wechseln.</span><span class="sxs-lookup"><span data-stu-id="62ee8-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="62ee8-118">Geben Sie daher Werte ein, die für Seitenautoren hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="62ee8-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="62ee8-119">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="62ee8-119">Select **OK**.</span></span>

<span data-ttu-id="62ee8-120">Das vordefinierte Layout ist jetzt verfügbar, wenn Sie neue Seiten erstellen oder ein anderes Layout für eine Seite in derselben Vorlagenhierarchie auswählen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="62ee8-121">Um schnell festzustellen, ob eine bestimmte Seite derzeit an ein vordefiniertes Layout gebunden ist, wählen Sie die Seite in der Seitenlistenansicht aus und überprüfen Sie die Layout-Metadaten im Eigenschaftsfenster auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="62ee8-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="62ee8-122">Ein neues vordefiniertes Layout erstellen</span><span class="sxs-lookup"><span data-stu-id="62ee8-122">Create a new preset layout</span></span>

<span data-ttu-id="62ee8-123">Gehen Sie folgendermaßen vor, um ein vordefiniertes Layout von Grund auf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="62ee8-124">Wählen Sie im linken Navigationsbereich **Layouts** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="62ee8-125">Wählen Sie **Neues Layout** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-125">Select **New Layout**.</span></span> <span data-ttu-id="62ee8-126">Das Dialogfeld **Neues Layout** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="62ee8-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="62ee8-127">Wählen Sie die Vorlage aus, die für Ihr vordefiniertes Layout verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62ee8-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="62ee8-128">Geben Sie einen Namen und eine Beschreibung für Ihr vordefiniertes Layout ein.</span><span class="sxs-lookup"><span data-stu-id="62ee8-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="62ee8-129">Die von Ihnen eingegebenen Werte werden anderen Autoren angezeigt, wenn sie neue Seiten aus Ihrem Layout erstellen oder zu diesem wechseln.</span><span class="sxs-lookup"><span data-stu-id="62ee8-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="62ee8-130">Geben Sie daher Werte ein, die für Seitenautoren hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="62ee8-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="62ee8-131">Wählen Sie **OK** aus, um das neue vordefinierte Layout zu erstellen und den Layout-Editor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="62ee8-132">Fügen Sie im Layout-Editor Module hinzu und konfigurieren Sie sie mithilfe der Gliederungsstruktur links und des Eigenschaftsfensters rechts.</span><span class="sxs-lookup"><span data-stu-id="62ee8-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="62ee8-133">(Der Vorgang ähnelt dem Vorgang zum Hinzufügen und Konfigurieren von Modulen für eine Vorlage im Vorlageneditor.) Die Anordnung der Module und die gesperrten Standardeinstellungen werden zur zentralen Modulkonfiguration für alle Seiten, die dieses vordefinierte Layout verwenden.</span><span class="sxs-lookup"><span data-stu-id="62ee8-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="62ee8-134">Ändern eines vordefinierten Layouts</span><span class="sxs-lookup"><span data-stu-id="62ee8-134">Modify a preset layout</span></span>

<span data-ttu-id="62ee8-135">Führen Sie folgende Schritte aus, um ein vordefiniertes Layout zu ändern.</span><span class="sxs-lookup"><span data-stu-id="62ee8-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="62ee8-136">Wählen Sie im linken Navigationsbereich **Layouts** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="62ee8-137">Wählen Sie im Layout-Editor links in der Gliederungsstruktur das zu ändernde Modul aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="62ee8-138">Befolgen Sie dann einen dieser Schritte:</span><span class="sxs-lookup"><span data-stu-id="62ee8-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="62ee8-139">Um ein Modul innerhalb seines übergeordneten Moduls nach oben oder unten zu verschieben, wählen Sie die Ellipsen-Schaltfläche (**...**) für das Modul und dann **Nach oben verschieben** oder **Nach unten verschieben** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="62ee8-140">Um die Standardeinstellungen eines Moduls zu ändern, geben Sie im Eigenschaftenbereich Standardwerte ein und sperren Sie diese optional für alle nachgeordneten Seiten.</span><span class="sxs-lookup"><span data-stu-id="62ee8-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="62ee8-141">Um neue Module oder Fragmente zu Containermodulen hinzuzufügen, klicken Sie auf die Ellipsen-Schaltfläche und dann auf **Modul hinzufügen** oder **Fragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="62ee8-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="62ee8-142">Um ein Modul aus dem Layout zu entfernen, wählen Sie die Ellipsen-Schaltfläche und anschließend **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="62ee8-143">Ändern eines vordefinierten Layoutdesigns</span><span class="sxs-lookup"><span data-stu-id="62ee8-143">Change a preset layout theme</span></span>

<span data-ttu-id="62ee8-144">In der Regel wird für alle Seiten, die ein vordefiniertes Layout verwenden, ein Standarddesign festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62ee8-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="62ee8-145">Gehen Sie folgendermaßen vor, um das Design für alle untergeordneten Seiten festzulegen oder zu ändern, die Ihr vordefiniertes Layout verwenden.</span><span class="sxs-lookup"><span data-stu-id="62ee8-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="62ee8-146">Wählen Sie im Layout-Editor in der linken Gliederungsstruktur das Seitencontainer-Modul aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="62ee8-147">(In der Regel ist dieses Modul der zweite Knoten und heißt **Standardseite**.)</span><span class="sxs-lookup"><span data-stu-id="62ee8-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="62ee8-148">Wählen Sie im Eigenschaftenbereich rechts im Feld **Design** ein Design aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="62ee8-149">Speichern, Einchecken, Anzeigen einer Vorschau und Veröffentlichen eines vordefinierten Layouts</span><span class="sxs-lookup"><span data-stu-id="62ee8-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="62ee8-150">Gehen Sie folgendermaßen vor, um Ihr vordefiniertes Layout zu speichern und einzuchecken.</span><span class="sxs-lookup"><span data-stu-id="62ee8-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="62ee8-151">Wählen Sie **Speichern** oben im Layouteditor aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="62ee8-152">Gespeicherte Änderungen wirken sich erst beim Einchecken auf nachfolgende Seiten aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="62ee8-153">Wählen Sie **Beenden Sie die Bearbeitung**.</span><span class="sxs-lookup"><span data-stu-id="62ee8-153">Select **Finish editing**.</span></span> <span data-ttu-id="62ee8-154">Ihre Änderungen sind jetzt für nachfolgende Workflows erkennbar.</span><span class="sxs-lookup"><span data-stu-id="62ee8-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="62ee8-155">Um eine Vorschau Ihrer Änderungen anzuzeigen, öffnen Sie entweder eine vorhandene Seite, die das vordefinierte Layout verwendet, oder erstellen Sie eine neue Seite aus dem Layout.</span><span class="sxs-lookup"><span data-stu-id="62ee8-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="62ee8-156">Führen Sie einen der folgenden Schritte aus, um das Layout auf Ihrer Live-Site zu veröffentlichen, nachdem Sie eine Vorschau der Änderungen an Ihrem vordefinierten Layout angezeigt haben:</span><span class="sxs-lookup"><span data-stu-id="62ee8-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="62ee8-157">Navigieren Sie zu **Layouts**, wählen Sie das Layout und dann **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="62ee8-158">Wählen Sie den Layoutnamen aus, um den Layout-Editor zu öffnen, und wählen Sie anschließend **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="62ee8-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="62ee8-159">Veröffentlichen Sie eine Seite, die auf das unveröffentlichte Layout verweist.</span><span class="sxs-lookup"><span data-stu-id="62ee8-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="62ee8-160">Das Layout wird automatisch veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="62ee8-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="62ee8-161">Vordefinierte Layouts können von mehreren Seiten referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="62ee8-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="62ee8-162">Beachten Sie beim Veröffentlichen eines vordefinierten Layouts, dass sich dies möglicherweise auf das Layout mehrerer Seiten auswirkt.</span><span class="sxs-lookup"><span data-stu-id="62ee8-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62ee8-163">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="62ee8-163">Additional resources</span></span>

[<span data-ttu-id="62ee8-164">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="62ee8-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="62ee8-165">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="62ee8-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

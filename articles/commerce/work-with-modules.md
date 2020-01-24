---
title: Arbeiten mit Modulen
description: In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914793"
---
# <a name="work-with-modules"></a><span data-ttu-id="e6b80-103">Arbeiten mit Modulen</span><span class="sxs-lookup"><span data-stu-id="e6b80-103">Work with modules</span></span>

<span data-ttu-id="e6b80-104">In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6b80-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e6b80-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e6b80-105">Overview</span></span>

<span data-ttu-id="e6b80-106">Module sind logische Bausteine, aus denen sich Ihre Seitenstruktur zusammensetzt. Sie dienen verschiedenen Zwecken und Bereichen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="e6b80-107">Einige Module sind übergeordnete Container, und ihr einziger Zweck besteht darin, andere Module (untergeordnete Module) zu speichern und zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="e6b80-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="e6b80-108">Andere Module, z. B. ein einfaches Bildplatzierungsmodul, haben einen ganz bestimmten Zweck.</span><span class="sxs-lookup"><span data-stu-id="e6b80-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="e6b80-109">Weitere Module, z. B. ein Karussellmodul, lassen sich irgendwo zwischen diesen beiden Kategorien einordnen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="e6b80-110">Standardmäßig enthält Ihre Dynamics 365 Commerce-Site eine Starter-Kit-Modulbibliothek, mit der Sie die grundlegendsten E-Commerce-Szenarien erstellen können.</span><span class="sxs-lookup"><span data-stu-id="e6b80-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="e6b80-111">Sie sollten in der Lage sein, eine End-to-End-E-Commerce-Site zu erstellen, indem Sie diese Module verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6b80-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="e6b80-112">Sie können diese Module jedoch auch anpassen oder neue, benutzerdefinierte Module für bestimmte Anforderungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="e6b80-113">Wenn Sie benutzerdefinierte Module erstellen möchten, steht ein SDK (Module Design Software Development Kit) zur Verfügung, mit dem Sie eine benutzerdefinierte Modulbibliothek erstellen können.</span><span class="sxs-lookup"><span data-stu-id="e6b80-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="e6b80-114">Containermodule und -Slots</span><span class="sxs-lookup"><span data-stu-id="e6b80-114">Container modules and slots</span></span>

<span data-ttu-id="e6b80-115">Wie bereits erwähnt, enthalten einige Module untergeordnete Module.</span><span class="sxs-lookup"><span data-stu-id="e6b80-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="e6b80-116">Diese Module sind als *Container* bekannt und sie ermöglichen Hierarchien geschachtelter Module.</span><span class="sxs-lookup"><span data-stu-id="e6b80-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="e6b80-117">Containermodule enthalten *Slots*.</span><span class="sxs-lookup"><span data-stu-id="e6b80-117">Container modules include *slots*.</span></span> <span data-ttu-id="e6b80-118">Slots werden verwendet, um das Layout und den Zweck von untergeordneten Modulen im Container zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e6b80-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="e6b80-119">Ein Beispiel ist ein grundlegendes Seitencontainermodul (ein übergeordnetes Modul für jede Seite), das mehrere wichtige Slots definiert:</span><span class="sxs-lookup"><span data-stu-id="e6b80-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="e6b80-120">Ein Kopfzeilen-Slot</span><span class="sxs-lookup"><span data-stu-id="e6b80-120">A header slot</span></span>
- <span data-ttu-id="e6b80-121">Ein Text-Slot</span><span class="sxs-lookup"><span data-stu-id="e6b80-121">A body slot</span></span>
- <span data-ttu-id="e6b80-122">Ein Fußzeilen-Slot</span><span class="sxs-lookup"><span data-stu-id="e6b80-122">A footer slot</span></span>

<span data-ttu-id="e6b80-123">Der Modulentwickler definiert diese Slots und legt fest, welche untergeordneten Module und wie viele untergeordnete Module direkt darin platziert werden können.</span><span class="sxs-lookup"><span data-stu-id="e6b80-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="e6b80-124">Beispielsweise unterstützt der Kopfzeilen-Slot möglicherweise nur einen Typ des **Kopfzeilen-Moduls**, wohingegen der Text-Slot eine unbegrenzte Anzahl an Modulen jedes Typs unterstützt (mit Ausnahme andere Seitencontainermodule).</span><span class="sxs-lookup"><span data-stu-id="e6b80-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="e6b80-125">In den Erstellungstools müssen Seitenautoren nicht im Voraus wissen, welche Module in die einzelnen Slots eingefügt werden können und welche nicht.</span><span class="sxs-lookup"><span data-stu-id="e6b80-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="e6b80-126">Wenn Seitenautoren einen Slot auswählen und dann versuchen, ein Modul zum Hinzufügen auszuwählen, wird eine gefilterte Ansicht der Modultypen angezeigt, die für diesen Slot unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e6b80-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="e6b80-127">Inhaltsmodule</span><span class="sxs-lookup"><span data-stu-id="e6b80-127">Content modules</span></span>

<span data-ttu-id="e6b80-128">Inhaltsmodule enthalten Inhalts- und Medienelemente wie Text (z. B. Überschriften, Absätze und Links) oder Ressourcenverweise (z. B. Bilder, Videos und PDFs).</span><span class="sxs-lookup"><span data-stu-id="e6b80-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="e6b80-129">Zu den Beispielen typischer Inhaltsmodultypen zählen **Hero**, **Funktion** und **Banner**.</span><span class="sxs-lookup"><span data-stu-id="e6b80-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="e6b80-130">Module dieser drei Typen können Text oder Medien enthalten und erfordern keine untergeordneten Module, um etwas auf einer Seite sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="e6b80-131">Die Mehrzahl der typischen täglichen Seiten- und Inhaltserstellungsaktivitäten umfasst Inhaltsmodule, hauptsächlich weil diese Module den tatsächlichen Inhalt definieren, der in ihren übergeordneten Containermodulen gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="e6b80-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="e6b80-132">Es sind viele Inhaltsmodule verfügbar, und diese Module sind normalerweise die letzten Elemente, die Sie der Hierarchie der verschachtelten Module einer Seite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="e6b80-133">Die folgende Abbildung zeigt, wie Module in übergeordneten Containermodul-Slots verschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="e6b80-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Verschachteln von Modulen](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="e6b80-135">Module hinzufügen oder entfernen</span><span class="sxs-lookup"><span data-stu-id="e6b80-135">Add or remove modules</span></span>

<span data-ttu-id="e6b80-136">Die folgenden Prozeduren beschreiben das Hinzufügen und Entfernen von Modulen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="e6b80-137">Ein Modul hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e6b80-137">Add a module</span></span>

<span data-ttu-id="e6b80-138">Gehen Sie folgendermaßen vor, um ein Modul aus einem Slot oder Container auf einer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6b80-139">Wählen Sie links im Gliederungsfenster einen Container oder Slot aus, dem ein untergeordnetes Modul hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6b80-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6b80-140">Der Moduldesigner definiert die Liste der Modultypen, die einem bestimmten Modul-Slot hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="e6b80-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="e6b80-141">Vorlagenautoren können dann die zulässigen Moduloptionen verfeinern, um eine konsistente Suchmaschinenoptimierung (SEO) und Autoreneffizienz für alle Seiten sicherzustellen, die aus einer bestimmten Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e6b80-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="e6b80-142">Wählen Sie die Ellipsen-Schaltfläche (**...**) für das Modul aus und dann **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e6b80-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="e6b80-143">Das Dialogfeld **Modul hinzufügen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6b80-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="e6b80-144">Dieses Dialogfeld wird automatisch gefiltert, sodass nur Module angezeigt werden, die im ausgewählten Container oder Slot unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e6b80-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="e6b80-145">Die Liste der Module wird durch die Seitenvorlage oder die Containermoduldefinition bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e6b80-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6b80-146">Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Modul hinzufügen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6b80-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="e6b80-147">Suchen Sie im Dialogfeld nach einem Modul und wählen Sie es aus, um es Ihrer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="e6b80-148">**Funktion** und **Hero** sind hilfreiche Modultypen, mit denen Anfänger arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="e6b80-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="e6b80-149">Wählen Sie **OK** aus, um das ausgewählte Modul dem ausgewählten Container oder Slot auf Ihrer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="e6b80-150">Ein Modul entfernen</span><span class="sxs-lookup"><span data-stu-id="e6b80-150">Remove a module</span></span>

<span data-ttu-id="e6b80-151">Gehen Sie folgendermaßen vor, um ein Moduls aus einem Slot oder Container auf einer Seite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e6b80-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6b80-152">Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des zu entfernenden Moduls und anschließend die Schaltfläche mit dem Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="e6b80-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="e6b80-153">Wenn Sie aufgefordert werden, das Entfernen des Moduls zu bestätigen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e6b80-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="e6b80-154">Module konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e6b80-154">Configure modules</span></span>

<span data-ttu-id="e6b80-155">In den folgenden Prozeduren wird beschrieben, wie Sie Inhalts- und Containermodule konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e6b80-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="e6b80-156">Ein Inhaltsmodul konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e6b80-156">Configure a content module</span></span>

<span data-ttu-id="e6b80-157">Um ein Inhaltsmodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="e6b80-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6b80-158">Wählen Sie im Gliederungsbereich links einen Inhaltsmodultyp (z. B. **Feature**, **Hero** oder **Banner**) aus.</span><span class="sxs-lookup"><span data-stu-id="e6b80-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="e6b80-159">Erweitern Sie im Eigenschaftenbereich rechts die verschachtelten Steuerelemente, indem Sie die Überschriften auswählen, und legen Sie die erforderlichen Steuerelementwerte fest.</span><span class="sxs-lookup"><span data-stu-id="e6b80-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="e6b80-160">Falls der Eigenschaftenbereich den Abschnitt **Datenkonfiguration** enthält, wählen Sie ihn aus, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e6b80-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="e6b80-161">Fahren Sie andernfalls mit Schritt 5 fort.</span><span class="sxs-lookup"><span data-stu-id="e6b80-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="e6b80-162">Falls die Schaltfläche **Datenquelle hinzufügen** vorhanden ist, wählen Sie diese und dann die hinzuzufügenden Inhaltselemente aus.</span><span class="sxs-lookup"><span data-stu-id="e6b80-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="e6b80-163">Geben Sie Einstellungen für erforderliche oder gewünschte Modulsteuerungen ein.</span><span class="sxs-lookup"><span data-stu-id="e6b80-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="e6b80-164">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e6b80-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="e6b80-165">Ein Containermodul konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e6b80-165">Configure a container module</span></span>

<span data-ttu-id="e6b80-166">Um ein Containermodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="e6b80-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6b80-167">Wählen Sie ein Containermodul auf Ihrer Seite aus (z. B. ein Karussell oder ein flüssiges Containermodul).</span><span class="sxs-lookup"><span data-stu-id="e6b80-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="e6b80-168">Erweitern Sie im Eigenschaftenbereich rechts die verschachtelten Steuerelemente, indem Sie die Überschriften auswählen, und legen Sie die erforderlichen Steuerelementwerte fest.</span><span class="sxs-lookup"><span data-stu-id="e6b80-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="e6b80-169">Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des Containers oder von Slots im Container und dann **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="e6b80-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="e6b80-170">Fügen Sie dann dem ausgewählten Container untergeordnete Module hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6b80-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="e6b80-171">Weitere Informationen erhalten Sie in der Prozedur [Modul hinzufügen](#add-a-module), die am Anfang dieses Themas beschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="e6b80-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="e6b80-172">Wenn mehrere untergeordnete Module als gleichgeordnete Elemente in einem übergeordneten Container vorhanden sind, können Sie deren Anzeigereihenfolge im übergeordneten Container ändern.</span><span class="sxs-lookup"><span data-stu-id="e6b80-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="e6b80-173">Wählen Sie die Auslassungsschaltfläche für ein Modul aus und verwenden Sie dann die Aufwärts- und Abwärtspfeiltasten.</span><span class="sxs-lookup"><span data-stu-id="e6b80-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6b80-174">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6b80-174">Additional resources</span></span>

[<span data-ttu-id="e6b80-175">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="e6b80-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e6b80-176">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="e6b80-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="e6b80-177">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="e6b80-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="e6b80-178">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="e6b80-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="e6b80-179">Ein Containermodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e6b80-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="e6b80-180">Einer Seite Inhaltsplatzierungsmodule hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e6b80-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e6b80-181">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="e6b80-181">Work with publish groups</span></span>](publish-groups.md)


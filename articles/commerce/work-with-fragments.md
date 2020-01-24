---
title: Arbeiten mit Fragmenten
description: In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.
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
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914699"
---
# <a name="work-with-fragments"></a><span data-ttu-id="b5cc6-103">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="b5cc6-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b5cc6-104">In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5cc6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b5cc6-105">Overview</span></span>

<span data-ttu-id="b5cc6-106">Fragmente ermöglichen ein zentrales Authoring für Modulkonfigurationen, die auf Ihrer Website wiederverwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="b5cc6-107">Beispielsweise werden Kopf- und Fußzeilen sowie Banner häufig als Fragmente konfiguriert, da sie auf mehreren Seiten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="b5cc6-108">Sie können sich Fragmente als Miniaturwebseiten vorstellen, die in andere Seiten Ihrer Site eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="b5cc6-109">Fragmente haben ihren eigenen Lebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="b5cc6-110">Mit anderen Worten, sie werden als unabhängige Entitäten in den Authoring-Tools erstellt, referenziert, aktualisiert und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="b5cc6-111">Nachdem Fragmente konfiguriert wurden, können sie überall dort verwendet werden, wo Module in Ihrer Site-Struktur verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="b5cc6-112">Fragmente können auf Seiten, in Layouts, in Vorlagen und in anderen Fragmenten referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="b5cc6-113">Fragmente können bis zu sieben Ebenen tief in anderen Fragmenten verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="b5cc6-114">Wenn Sie beispielsweise eine saisonale Veranstaltung über mehrere Seiten auf unserer Website bewerben möchten, können Sie ein Fragment verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="b5cc6-115">Der erste Schritt beim Erstellen eines neuen Fragments ist die Auswahl des Modultyps, von dem aus Sie beginnen möchten.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="b5cc6-116">In diesem Beispiel können Sie das Fragment aus einem Hero-Modul erstellen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="b5cc6-117">Fragmente können aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="b5cc6-118">Sie können dann das Hero-Fragment mit Ihrem spezifischen Werbeinhalt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="b5cc6-119">Sie können es auch nach Bedarf lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-119">You can also localize it as you require.</span></span> <span data-ttu-id="b5cc6-120">Das neue eigenständige Hero-Fragment kann dann als vorkonfiguriertes Modul auf Ihrer Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="b5cc6-121">Sie können es einfach Vorlagen, bestimmten Seiten oder anderen Fragmenten hinzufügen, die Hero-Module enthalten können.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="b5cc6-122">Alle Stellen, an denen das Fragment hinzugefügt wird, verweisen auf das von Ihnen erstellte zentrale Hero-Fragment.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="b5cc6-123">Wenn Sie Änderungen am Fragment veröffentlichen, wirken sich diese Änderungen sofort auf alle Stellen aus, auf die das Fragment auf der Site verweist.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="b5cc6-124">Daher bieten Fragmente eine leistungsstarke und effiziente Möglichkeit, Modulkonfigurationen auf einer Site wiederzuverwenden und zentral zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="b5cc6-125">Indem Sie sie effektiv einsetzen, können Sie die Flexibilität erheblich steigern und die Kosten für die Verwaltung des Websiteinhalts senken.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="b5cc6-126">Die folgende Abbildung zeigt, wie Fragmente verwendet werden können, um das Authoring gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site zu zentralisieren.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Eine Abbildung, die zeigt, wie Fragmente zum Zentralisieren des Erstellens gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site verwendet werden können](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="b5cc6-128">Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-128">Create a fragment</span></span>

<span data-ttu-id="b5cc6-129">Sie können entweder ein neues Fragment erstellen oder eine vorhandene Modulkonfiguration als Fragment speichern.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="b5cc6-130">Ein neues Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-130">Create a new fragment</span></span>

<span data-ttu-id="b5cc6-131">Um ein neues Fragment zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="b5cc6-132">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="b5cc6-133">Wählen Sie **Neues Seitenfragment** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="b5cc6-134">Ein Dialogfeld mit allen verfügbaren Modultypen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="b5cc6-135">Wie bereits erwähnt, können Fragmente aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="b5cc6-136">Wählen Sie einen Modultyp für Ihr Fragment und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="b5cc6-137">Durch Auswahl eines generischen Containermodultyps erhalten Sie die größte Flexibilität, wenn Sie Ihr Fragment später aktualisieren und konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="b5cc6-138">Speichern einer vorhandenen Modulkonfiguration als Fragment</span><span class="sxs-lookup"><span data-stu-id="b5cc6-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="b5cc6-139">Gehen Sie folgendermaßen vor, um ein zuvor konfiguriertes Modul in ein wiederverwendbares Fragment zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="b5cc6-140">Öffnen Sie eine Seite oder Vorlage, die das Modul enthält, das Sie in ein Fragment konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="b5cc6-141">Wählen Sie im Gliederungsbereich links die Ellipsen-Schaltfläche (**...**) neben dem Namen des Moduls und dann **Als Fragment speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="b5cc6-142">Ein Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-142">A dialog box appears.</span></span>
1. <span data-ttu-id="b5cc6-143">Geben Sie einen Namen und Metadaten für das Fragment ein.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="b5cc6-144">Wählen Sie **OK** aus, um die Modulkonfiguration als Fragment zu speichern, das anderen Seiten hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="b5cc6-145">Hinzufügen, Entfernen oder Bearbeiten von Fragmenten auf einer Seite</span><span class="sxs-lookup"><span data-stu-id="b5cc6-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="b5cc6-146">Die folgenden Prozeduren beschreiben das Hinzufügen, Entfernen und Bearbeiten von Fragmenten.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="b5cc6-147">Fragment hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-147">Add a fragment</span></span>

<span data-ttu-id="b5cc6-148">Gehen Sie folgendermaßen vor, um einer Seite ein Fragment hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="b5cc6-149">Wählen Sie links im Gliederungsfenster einen Container oder Steckplatz aus, zu dem untergeordnete Module hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="b5cc6-150">Wählen Sie die Ellipsen-Schaltfläche neben dem Namen des Containers oder Slots und dann **Fragment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="b5cc6-151">Ein Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5cc6-152">Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Fragment hinzufügen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="b5cc6-153">Suchen Sie im Dialogfeld nach einem Fragment, das Sie hinzufügen möchten, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="b5cc6-154">Wenn keine verfügbaren Fragmente aufgelistet sind, müssen Sie möglicherweise zuerst ein Fragment aus einem Modultyp erstellen, den der ausgewählte Container oder Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="b5cc6-155">Wählen Sie **OK** aus, um das ausgewählte Fragment dem ausgewählten Container oder Slot auf Ihrer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="b5cc6-156">Die Module, die in einem Container oder Slot zulässig sind, werden durch die Seitenvorlage oder die eigenen Definitionen der Module definiert.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="b5cc6-157">Ein Fragment entfernen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-157">Remove a fragment</span></span>

<span data-ttu-id="b5cc6-158">Gehen Sie folgendermaßen vor, um ein Fragment aus einem Slot oder Container auf einer Seite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="b5cc6-159">Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des zu entfernenden Fragments und anschließend die Schaltfläche mit dem Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="b5cc6-160">Wenn Sie aufgefordert werden, das Entfernen des Fragments zu bestätigen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="b5cc6-161">Wenn Sie ein Fragment von einer Seite entfernen, entfernen Sie einfach den Verweis darauf von dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="b5cc6-162">Sie löschen das Fragment **nicht** von Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="b5cc6-163">Um Fragmente von Ihrer Site zu löschen, müssen Sie die Benutzeroberfläche des Fragmentinspektors verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="b5cc6-164">Sie können Fragmente nur dann von einer Site löschen, wenn derzeit keine Seiten, Vorlagen oder anderen Fragmente auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="b5cc6-165">Fragment bearbeiten</span><span class="sxs-lookup"><span data-stu-id="b5cc6-165">Edit a fragment</span></span>

<span data-ttu-id="b5cc6-166">Um Fragmente zu bearbeiten, müssen Sie die Benutzeroberfläche des Fragmenteditors verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="b5cc6-167">Diese Beschränkung ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-167">This restriction is by design.</span></span> <span data-ttu-id="b5cc6-168">Es hilft, sicherzustellen, dass Autoren den Prozess der Bearbeitung der Module für eine bestimmte Seite nicht mit dem Prozess der Bearbeitung von Fragmenten verwechseln, die möglicherweise auf mehreren Seiten geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="b5cc6-169">Um ein neues Fragment zu bearbeiten, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="b5cc6-170">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="b5cc6-171">Wählen Sie unter **Fragmente** das zu bearbeitende Fragment aus.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="b5cc6-172">Bearbeiten Sie die Moduleigenschaften und die Struktur des Fragments nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="b5cc6-173">Der Vorgang ähnelt dem Vorgang zum Bearbeiten von Modulen, die in der Seiteneditoransicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="b5cc6-174">Sie können ein Fragment auch bearbeiten, indem Sie es auf einer Seite, in einer Vorlage oder in einem übergeordneten Fragment auswählen und dann **Fragment bearbeiten** im Eigenschaftenbereich rechts.</span><span class="sxs-lookup"><span data-stu-id="b5cc6-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5cc6-175">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-175">Additional resources</span></span>

[<span data-ttu-id="b5cc6-176">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="b5cc6-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b5cc6-177">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="b5cc6-178">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="b5cc6-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="b5cc6-179">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="b5cc6-179">Work with publish groups</span></span>](publish-groups.md)

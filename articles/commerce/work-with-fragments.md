---
title: Arbeiten mit Fragmenten
description: In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124358"
---
# <a name="work-with-fragments"></a><span data-ttu-id="f0ec5-103">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="f0ec5-103">Work with fragments</span></span> 


[!include [banner](includes/banner.md)]

<span data-ttu-id="f0ec5-104">In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f0ec5-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f0ec5-105">Overview</span></span>

<span data-ttu-id="f0ec5-106">Fragmente ermöglichen ein zentrales Authoring für Modulkonfigurationen, die auf Ihrer Website wiederverwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="f0ec5-107">Beispielsweise werden Kopf- und Fußzeilen sowie Banner häufig als Fragmente konfiguriert, da sie auf mehreren Seiten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="f0ec5-108">Sie können sich Fragmente als Miniaturwebseiten vorstellen, die in andere Seiten Ihrer Site eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="f0ec5-109">Fragmente haben ihren eigenen Lebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="f0ec5-110">Mit anderen Worten, sie werden als unabhängige Entitäten in den Authoring-Tools erstellt, referenziert, aktualisiert und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="f0ec5-111">Nachdem Fragmente konfiguriert wurden, können sie überall dort verwendet werden, wo Module in Ihrer Site-Struktur verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="f0ec5-112">Fragmente können auf Seiten, in Layouts, in Vorlagen und in anderen Fragmenten referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="f0ec5-113">Fragmente können bis zu sieben Ebenen tief in anderen Fragmenten verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="f0ec5-114">Wenn Sie beispielsweise eine saisonale Veranstaltung über mehrere Seiten auf unserer Website bewerben möchten, können Sie ein Fragment verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="f0ec5-115">Der erste Schritt beim Erstellen eines neuen Fragments ist die Auswahl des Modultyps, von dem aus Sie beginnen möchten.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="f0ec5-116">In diesem Beispiel können Sie das Fragment aus einem Hero-Modul erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="f0ec5-117">Fragmente können aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="f0ec5-118">Sie können dann das Hero-Fragment mit Ihrem spezifischen Werbeinhalt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="f0ec5-119">Sie können es auch nach Bedarf lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-119">You can also localize it as you require.</span></span> <span data-ttu-id="f0ec5-120">Das neue eigenständige Hero-Fragment kann dann als vorkonfiguriertes Modul auf Ihrer Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="f0ec5-121">Sie können es einfach Vorlagen, bestimmten Seiten oder anderen Fragmenten hinzufügen, die Hero-Module enthalten können.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="f0ec5-122">Alle Stellen, an denen das Fragment hinzugefügt wird, verweisen auf das von Ihnen erstellte zentrale Hero-Fragment.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="f0ec5-123">Wenn Sie Änderungen am Fragment veröffentlichen, wirken sich diese Änderungen sofort auf alle Stellen aus, auf die das Fragment auf der Site verweist.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="f0ec5-124">Daher bieten Fragmente eine leistungsstarke und effiziente Möglichkeit, Modulkonfigurationen auf einer Site wiederzuverwenden und zentral zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="f0ec5-125">Indem Sie sie effektiv einsetzen, können Sie die Flexibilität erheblich steigern und die Kosten für die Verwaltung des Websiteinhalts senken.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="f0ec5-126">Die folgende Abbildung zeigt, wie Fragmente verwendet werden können, um das Authoring gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site zu zentralisieren.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Eine Abbildung, die zeigt, wie Fragmente zum Zentralisieren des Erstellens gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site verwendet werden können](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="f0ec5-128">Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-128">Create a fragment</span></span>

<span data-ttu-id="f0ec5-129">Sie können entweder ein neues Fragment erstellen oder eine vorhandene Modulkonfiguration als Fragment speichern.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="f0ec5-130">Speichern einer vorhandenen Modulkonfiguration als Fragment</span><span class="sxs-lookup"><span data-stu-id="f0ec5-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="f0ec5-131">Gehen Sie folgendermaßen vor, um ein zuvor konfiguriertes Modul in ein wiederverwendbares Fragment zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="f0ec5-132">Öffnen Sie eine Seite oder Vorlage, die das Modul enthält, das Sie in ein Fragment konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="f0ec5-133">Wählen Sie links im Gliederungsfenster die Ellipsen-Schaltfläche (**...**) neben dem Namen des Moduls.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-133">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module.</span></span> 
1. <span data-ttu-id="f0ec5-134">Wählen Sie **Als Fragment teilen**.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-134">Select **Share as Fragment**.</span></span> 
1. <span data-ttu-id="f0ec5-135">Ein Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-135">A dialog box appears.</span></span> <span data-ttu-id="f0ec5-136">Geben Sie einen Namen und Metadaten für das Fragment ein.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-136">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="f0ec5-137">Wählen Sie **OK** aus, um die Modulkonfiguration als Fragment zu speichern, das anderen Seiten hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="f0ec5-138">Das folgende Bild zeigt, wie Sie eine Modulkonfiguration als Fragment speichern.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Ein Screenshot, wie eine Modulkonfiguration als Fragment gespeichert wird](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="f0ec5-140">Ein neues Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-140">Create a new fragment</span></span>

<span data-ttu-id="f0ec5-141">Um ein neues Fragment zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="f0ec5-142">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="f0ec5-143">Wählen Sie **Neues Seitenfragment** aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="f0ec5-144">Ein Dialogfeld mit allen verfügbaren Modultypen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="f0ec5-145">Wie bereits erwähnt, können Fragmente aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="f0ec5-146">Wählen Sie einen Modultyp für Ihr Fragment.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="f0ec5-147">Das folgende Bild zeigt, wo ein neues Fragment erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-147">The following image shows where to create a new fragment.</span></span>

![Ein Screenshot, wo ein neues Fragment erstellt werden soll](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="f0ec5-149">Durch Auswahl eines generischen Containermodultyps erhalten Sie die größte Flexibilität, wenn Sie Ihr Fragment später aktualisieren und konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="f0ec5-150">Hinzufügen, Entfernen oder Bearbeiten von Fragmenten auf einer Seite</span><span class="sxs-lookup"><span data-stu-id="f0ec5-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="f0ec5-151">Die folgenden Prozeduren beschreiben das Hinzufügen, Entfernen und Bearbeiten von Fragmenten.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="f0ec5-152">Fragment hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-152">Add a fragment</span></span>

<span data-ttu-id="f0ec5-153">Gehen Sie folgendermaßen vor, um einer Seite ein Fragment hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="f0ec5-154">Wählen Sie links im Gliederungsfenster einen Container oder Steckplatz aus, zu dem untergeordnete Module hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-154">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="f0ec5-155">Wählen Sie die Ellipsen-Schaltfläche neben dem Namen des Containers oder Slots und dann **Fragment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-155">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="f0ec5-156">Ein Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-156">A dialog box appears.</span></span>

    ![Ein Screenshot, in dem gezeigt wird, wie einem Slot oder Container ein vorhandenes Fragment hinzugefügt wird](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="f0ec5-158">Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Fragment hinzufügen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-158">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="f0ec5-159">Suchen Sie im Dialogfeld nach einem Fragment, das Sie hinzufügen möchten, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-159">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="f0ec5-160">Wenn keine verfügbaren Fragmente aufgelistet sind, müssen Sie möglicherweise zuerst ein Fragment aus einem Modultyp erstellen, den der ausgewählte Container oder Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-160">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="f0ec5-161">Wählen Sie Ihr gewünschtes Fragment aus, das dem Container oder Slot auf Ihrer Seite hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-161">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Ein Screenshot des modalen Fensters der Fragmentauswahl](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="f0ec5-163">Die Module, die in einem Container oder Slot zulässig sind, werden durch die Seitenvorlage oder die eigenen Definitionen der Module definiert.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-163">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="f0ec5-164">Ein Fragment entfernen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-164">Remove a fragment</span></span>

<span data-ttu-id="f0ec5-165">Gehen Sie folgendermaßen vor, um ein Fragment aus einem Slot oder Container auf einer Seite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-165">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="f0ec5-166">Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des zu entfernenden Fragments und anschließend die Schaltfläche mit dem Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-166">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="f0ec5-167">Wenn Sie aufgefordert werden, das Entfernen des Fragments zu bestätigen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-167">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="f0ec5-168">Wenn Sie ein Fragment von einer Seite entfernen, entfernen Sie einfach den Verweis darauf von dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-168">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="f0ec5-169">Sie löschen das Fragment **nicht** von Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-169">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="f0ec5-170">Um Fragmente von Ihrer Site zu löschen, müssen Sie die Benutzeroberfläche des Fragmentinspektors verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-170">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="f0ec5-171">Sie können Fragmente nur dann von einer Site löschen, wenn derzeit keine Seiten, Vorlagen oder anderen Fragmente auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-171">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="f0ec5-172">Fragment bearbeiten</span><span class="sxs-lookup"><span data-stu-id="f0ec5-172">Edit a fragment</span></span>

<span data-ttu-id="f0ec5-173">Um Fragmente zu bearbeiten, müssen Sie die Benutzeroberfläche des Fragmenteditors verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-173">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="f0ec5-174">Diese Beschränkung ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-174">This restriction is by design.</span></span> <span data-ttu-id="f0ec5-175">Es hilft, sicherzustellen, dass Autoren den Prozess der Bearbeitung der Module für eine bestimmte Seite nicht mit dem Prozess der Bearbeitung von Fragmenten verwechseln, die möglicherweise auf mehreren Seiten geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-175">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="f0ec5-176">Um ein neues Fragment zu bearbeiten, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-176">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="f0ec5-177">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-177">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="f0ec5-178">Wählen Sie unter **Fragmente** das zu bearbeitende Fragment aus.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-178">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="f0ec5-179">Bearbeiten Sie die Moduleigenschaften und die Struktur des Fragments nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-179">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="f0ec5-180">Der Vorgang ähnelt dem Vorgang zum Bearbeiten von Modulen, die in der Seiteneditoransicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-180">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="f0ec5-181">Sie können ein Fragment auch bearbeiten, indem Sie es auf einer Seite, in einer Vorlage oder in einem übergeordneten Fragment auswählen und dann **Fragment bearbeiten** im Eigenschaftenbereich rechts.</span><span class="sxs-lookup"><span data-stu-id="f0ec5-181">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0ec5-182">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-182">Additional resources</span></span>

[<span data-ttu-id="f0ec5-183">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="f0ec5-183">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f0ec5-184">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-184">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f0ec5-185">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="f0ec5-185">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="f0ec5-186">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="f0ec5-186">Work with publish groups</span></span>](publish-groups.md)

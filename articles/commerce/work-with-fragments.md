---
title: Arbeiten mit Fragmenten
description: In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793944"
---
# <a name="work-with-fragments"></a><span data-ttu-id="6f38d-103">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="6f38d-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f38d-104">In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6f38d-105">Fragmente ermöglichen ein zentrales Authoring für Modulkonfigurationen, die auf Ihrer Website wiederverwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="6f38d-106">Beispielsweise werden Kopf- und Fußzeilen sowie Banner häufig als Fragmente konfiguriert, da sie auf mehreren Seiten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="6f38d-107">Sie können sich Fragmente als Miniaturwebseiten vorstellen, die in andere Seiten Ihrer Site eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6f38d-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="6f38d-108">Fragmente haben ihren eigenen Lebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="6f38d-109">Mit anderen Worten, sie werden als unabhängige Entitäten in den Authoring-Tools erstellt, referenziert, aktualisiert und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f38d-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="6f38d-110">Nachdem Fragmente konfiguriert wurden, können sie überall dort verwendet werden, wo Module in Ihrer Site-Struktur verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6f38d-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="6f38d-111">Fragmente können auf Seiten, in Layouts, in Vorlagen und in anderen Fragmenten referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="6f38d-112">Fragmente können bis zu sieben Ebenen tief in anderen Fragmenten verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="6f38d-113">Wenn Sie beispielsweise eine saisonale Veranstaltung über mehrere Seiten auf unserer Website bewerben möchten, können Sie ein Fragment verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="6f38d-114">Der erste Schritt beim Erstellen eines neuen Fragments ist die Auswahl des Modultyps, von dem aus Sie beginnen möchten.</span><span class="sxs-lookup"><span data-stu-id="6f38d-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="6f38d-115">In diesem Beispiel können Sie das Fragment aus einem Hero-Modul erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="6f38d-116">Fragmente können aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="6f38d-117">Sie können dann das Hero-Fragment mit Ihrem spezifischen Werbeinhalt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6f38d-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="6f38d-118">Sie können es auch nach Bedarf lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="6f38d-118">You can also localize it as you require.</span></span> <span data-ttu-id="6f38d-119">Das neue eigenständige Hero-Fragment kann dann als vorkonfiguriertes Modul auf Ihrer Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="6f38d-120">Sie können es einfach Vorlagen, bestimmten Seiten oder anderen Fragmenten hinzufügen, die Hero-Module enthalten können.</span><span class="sxs-lookup"><span data-stu-id="6f38d-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="6f38d-121">Alle Stellen, an denen das Fragment hinzugefügt wird, verweisen auf das von Ihnen erstellte zentrale Hero-Fragment.</span><span class="sxs-lookup"><span data-stu-id="6f38d-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="6f38d-122">Wenn Sie Änderungen am Fragment veröffentlichen, wirken sich diese Änderungen sofort auf alle Stellen aus, auf die das Fragment auf der Site verweist.</span><span class="sxs-lookup"><span data-stu-id="6f38d-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="6f38d-123">Daher bieten Fragmente eine leistungsstarke und effiziente Möglichkeit, Modulkonfigurationen auf einer Site wiederzuverwenden und zentral zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6f38d-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="6f38d-124">Indem Sie sie effektiv einsetzen, können Sie die Flexibilität erheblich steigern und die Kosten für die Verwaltung des Websiteinhalts senken.</span><span class="sxs-lookup"><span data-stu-id="6f38d-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="6f38d-125">Die folgende Abbildung zeigt, wie Fragmente verwendet werden können, um das Authoring gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site zu zentralisieren.</span><span class="sxs-lookup"><span data-stu-id="6f38d-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Eine Abbildung, die zeigt, wie Fragmente zum Zentralisieren des Erstellens gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site verwendet werden können](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="6f38d-127">Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="6f38d-127">Create a fragment</span></span>

<span data-ttu-id="6f38d-128">Sie können entweder ein neues Fragment erstellen oder eine vorhandene Modulkonfiguration als Fragment speichern.</span><span class="sxs-lookup"><span data-stu-id="6f38d-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="6f38d-129">Speichern einer vorhandenen Modulkonfiguration als Fragment</span><span class="sxs-lookup"><span data-stu-id="6f38d-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="6f38d-130">Gehen Sie folgendermaßen vor, um ein zuvor konfiguriertes Modul in ein wiederverwendbares Fragment im Commerce Site Builder zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6f38d-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f38d-131">Öffnen Sie eine Seite oder Vorlage, die das Modul enthält, das Sie in ein Fragment konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6f38d-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="6f38d-132">Wählen Sie im Gliederungsbereich links oder direkt in Visual Page Builder das zuvor konfigurierte Modul aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="6f38d-133">Wählen Sie die Auslassungspunkte (**...**) neben dem Namen des Moduls im Gliederungsbereich oder in der Symbolleiste des ausgewählten Moduls im Visual Page Builder aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="6f38d-134">Wählen Sie **Als Fragment teilen**.</span><span class="sxs-lookup"><span data-stu-id="6f38d-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="6f38d-135">Geben Sie im Dialogfeld **Als Fragment speichern** einen Namen für das Fragment ein.</span><span class="sxs-lookup"><span data-stu-id="6f38d-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="6f38d-136">Wählen Sie **OK** aus, um die Modulkonfiguration als Fragment zu speichern, das anderen Seiten hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6f38d-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="6f38d-137">Neues Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="6f38d-137">Create a new fragment</span></span>

<span data-ttu-id="6f38d-138">Führen Sie die folgenden Schritte aus, um ein neues Fragmente im Commerce Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f38d-139">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="6f38d-140">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-140">Select **New**.</span></span> <span data-ttu-id="6f38d-141">Ein Dialogfeld **Neues Fragment** mit allen verfügbaren Modultypen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6f38d-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="6f38d-142">Wie bereits erwähnt, können Fragmente aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="6f38d-143">Wählen Sie einen Modultyp für Ihr Fragment.</span><span class="sxs-lookup"><span data-stu-id="6f38d-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="6f38d-144">Durch Auswahl eines generischen Containermodultyps erhalten Sie die größte Flexibilität, wenn Sie Ihr Fragment später aktualisieren und konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="6f38d-145">Hinzufügen, Entfernen oder Bearbeiten von Fragmenten auf einer Seite</span><span class="sxs-lookup"><span data-stu-id="6f38d-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="6f38d-146">Die folgenden Prozeduren beschreiben das Hinzufügen, Entfernen und Bearbeiten von Fragmenten.</span><span class="sxs-lookup"><span data-stu-id="6f38d-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="6f38d-147">Fragment hinzufügen</span><span class="sxs-lookup"><span data-stu-id="6f38d-147">Add a fragment</span></span>

<span data-ttu-id="6f38d-148">Führen Sie die folgenden Schritte aus, um ein Fragmente im Commerce Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f38d-149">Wählen Sie im Gliederungsbereich links oder direkt im Visual Page Builder einen Container oder Slot aus, zu dem untergeordnete Module hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6f38d-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="6f38d-150">Wählen Sie die Auslassungspunkte (**...**) neben dem Namen des Containers oder Slots aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="6f38d-151">Wenn Sie alternativ Visual Page Builder verwenden, wählen Sie das Pluszeichen (**+**) aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="6f38d-152">Wählen Sie **Fragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6f38d-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="6f38d-153">Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Fragment hinzufügen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f38d-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="6f38d-154">Suchen Sie im Dialogfeld **Fragment auswählen** nach einem Fragment, das Sie hinzufügen möchten, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="6f38d-155">Wenn keine verfügbaren Fragmente aufgelistet sind, müssen Sie möglicherweise zuerst ein Fragment aus einem Modultyp erstellen, den der ausgewählte Container oder Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f38d-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="6f38d-156">Wählen Sie Ihr gewünschtes Fragment aus, das dem Container oder Slot auf Ihrer Seite hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f38d-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="6f38d-157">Die Module, die in einem Container oder Slot zulässig sind, werden durch die Seitenvorlage oder die eigenen Definitionen der Module definiert.</span><span class="sxs-lookup"><span data-stu-id="6f38d-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="6f38d-158">Ein Fragment entfernen</span><span class="sxs-lookup"><span data-stu-id="6f38d-158">Remove a fragment</span></span>

<span data-ttu-id="6f38d-159">Führen Sie die folgenden Schritte aus, um ein Fragment aus einem Slot oder Container auf einer Seite im Commerce Site Builder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f38d-160">Wählen Sie links im Gliederungsbereich die Auslassungspunkte (**...**) neben dem Namen des zu entfernenden Fragments und anschließend das Papierkorbsymbol aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="6f38d-161">Alternativ können Sie das Fragment in Visual Page Builder und das Papierkorbsymbol in der Symbolleiste des Fragments auswählen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="6f38d-162">Wenn Sie aufgefordert werden, das Entfernen des Fragments zu bestätigen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="6f38d-163">Wenn Sie ein Fragment von einer Seite entfernen, entfernen Sie einfach den Verweis darauf von dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="6f38d-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="6f38d-164">Sie löschen das Fragment **nicht** von Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="6f38d-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="6f38d-165">Um Fragmente von Ihrer Site zu löschen, müssen Sie die Benutzeroberfläche des Fragmentinspektors verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="6f38d-166">Sie können Fragmente nur dann von einer Site löschen, wenn derzeit keine Seiten, Vorlagen oder anderen Fragmente auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="6f38d-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="6f38d-167">Fragment bearbeiten</span><span class="sxs-lookup"><span data-stu-id="6f38d-167">Edit a fragment</span></span>

<span data-ttu-id="6f38d-168">Um Fragmente zu bearbeiten, müssen Sie die Benutzeroberfläche des Fragmenteditors verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="6f38d-169">Diese Beschränkung ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="6f38d-169">This restriction is by design.</span></span> <span data-ttu-id="6f38d-170">Es hilft, sicherzustellen, dass Autoren den Prozess der Bearbeitung der Module für eine bestimmte Seite nicht mit dem Prozess der Bearbeitung von Fragmenten verwechseln, die möglicherweise auf mehreren Seiten geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="6f38d-171">Führen Sie die folgenden Schritte aus, um ein neues Fragmente im Commerce Site Builder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f38d-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f38d-172">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="6f38d-173">Wählen Sie unter **Fragmente** das zu bearbeitende Fragment aus.</span><span class="sxs-lookup"><span data-stu-id="6f38d-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="6f38d-174">Bearbeiten Sie die Moduleigenschaften und die Struktur des Fragments nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="6f38d-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="6f38d-175">Der Vorgang ähnelt dem Vorgang zum Bearbeiten von Modulen, die in der Seiteneditoransicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6f38d-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="6f38d-176">Sie können ein Fragment auch bearbeiten, indem Sie es auf einer Seite, in einer Vorlage oder in einem übergeordneten Fragment auswählen und dann **Fragment bearbeiten** im Eigenschaftenbereich rechts.</span><span class="sxs-lookup"><span data-stu-id="6f38d-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f38d-177">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6f38d-177">Additional resources</span></span>

[<span data-ttu-id="6f38d-178">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="6f38d-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="6f38d-179">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="6f38d-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="6f38d-180">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="6f38d-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="6f38d-181">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6f38d-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

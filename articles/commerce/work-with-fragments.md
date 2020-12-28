---
title: Arbeiten mit Fragmenten
description: In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f1525610fb16edd5ff9ccefe0194f6f27b797b62
ms.sourcegitcommit: 1a12b42cc17f004a981c716aed3da6cf538475a5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4412693"
---
# <a name="work-with-fragments"></a><span data-ttu-id="d4e32-103">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="d4e32-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4e32-104">In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d4e32-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d4e32-105">Overview</span></span>

<span data-ttu-id="d4e32-106">Fragmente ermöglichen ein zentrales Authoring für Modulkonfigurationen, die auf Ihrer Website wiederverwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="d4e32-107">Beispielsweise werden Kopf- und Fußzeilen sowie Banner häufig als Fragmente konfiguriert, da sie auf mehreren Seiten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="d4e32-108">Sie können sich Fragmente als Miniaturwebseiten vorstellen, die in andere Seiten Ihrer Site eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="d4e32-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="d4e32-109">Fragmente haben ihren eigenen Lebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="d4e32-110">Mit anderen Worten, sie werden als unabhängige Entitäten in den Authoring-Tools erstellt, referenziert, aktualisiert und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d4e32-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="d4e32-111">Nachdem Fragmente konfiguriert wurden, können sie überall dort verwendet werden, wo Module in Ihrer Site-Struktur verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d4e32-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="d4e32-112">Fragmente können auf Seiten, in Layouts, in Vorlagen und in anderen Fragmenten referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="d4e32-113">Fragmente können bis zu sieben Ebenen tief in anderen Fragmenten verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="d4e32-114">Wenn Sie beispielsweise eine saisonale Veranstaltung über mehrere Seiten auf unserer Website bewerben möchten, können Sie ein Fragment verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="d4e32-115">Der erste Schritt beim Erstellen eines neuen Fragments ist die Auswahl des Modultyps, von dem aus Sie beginnen möchten.</span><span class="sxs-lookup"><span data-stu-id="d4e32-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="d4e32-116">In diesem Beispiel können Sie das Fragment aus einem Hero-Modul erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="d4e32-117">Fragmente können aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="d4e32-118">Sie können dann das Hero-Fragment mit Ihrem spezifischen Werbeinhalt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d4e32-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="d4e32-119">Sie können es auch nach Bedarf lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="d4e32-119">You can also localize it as you require.</span></span> <span data-ttu-id="d4e32-120">Das neue eigenständige Hero-Fragment kann dann als vorkonfiguriertes Modul auf Ihrer Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="d4e32-121">Sie können es einfach Vorlagen, bestimmten Seiten oder anderen Fragmenten hinzufügen, die Hero-Module enthalten können.</span><span class="sxs-lookup"><span data-stu-id="d4e32-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="d4e32-122">Alle Stellen, an denen das Fragment hinzugefügt wird, verweisen auf das von Ihnen erstellte zentrale Hero-Fragment.</span><span class="sxs-lookup"><span data-stu-id="d4e32-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="d4e32-123">Wenn Sie Änderungen am Fragment veröffentlichen, wirken sich diese Änderungen sofort auf alle Stellen aus, auf die das Fragment auf der Site verweist.</span><span class="sxs-lookup"><span data-stu-id="d4e32-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="d4e32-124">Daher bieten Fragmente eine leistungsstarke und effiziente Möglichkeit, Modulkonfigurationen auf einer Site wiederzuverwenden und zentral zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d4e32-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="d4e32-125">Indem Sie sie effektiv einsetzen, können Sie die Flexibilität erheblich steigern und die Kosten für die Verwaltung des Websiteinhalts senken.</span><span class="sxs-lookup"><span data-stu-id="d4e32-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="d4e32-126">Die folgende Abbildung zeigt, wie Fragmente verwendet werden können, um das Authoring gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site zu zentralisieren.</span><span class="sxs-lookup"><span data-stu-id="d4e32-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Eine Abbildung, die zeigt, wie Fragmente zum Zentralisieren des Erstellens gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site verwendet werden können](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="d4e32-128">Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="d4e32-128">Create a fragment</span></span>

<span data-ttu-id="d4e32-129">Sie können entweder ein neues Fragment erstellen oder eine vorhandene Modulkonfiguration als Fragment speichern.</span><span class="sxs-lookup"><span data-stu-id="d4e32-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="d4e32-130">Speichern einer vorhandenen Modulkonfiguration als Fragment</span><span class="sxs-lookup"><span data-stu-id="d4e32-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="d4e32-131">Gehen Sie folgendermaßen vor, um ein zuvor konfiguriertes Modul in ein wiederverwendbares Fragment im Commerce Site Builder zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d4e32-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d4e32-132">Öffnen Sie eine Seite oder Vorlage, die das Modul enthält, das Sie in ein Fragment konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d4e32-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="d4e32-133">Wählen Sie im Gliederungsbereich links oder direkt in Visual Page Builder das zuvor konfigurierte Modul aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="d4e32-134">Wählen Sie die Auslassungspunkte (**...**) neben dem Namen des Moduls im Gliederungsbereich oder in der Symbolleiste des ausgewählten Moduls im Visual Page Builder aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="d4e32-135">Wählen Sie **Als Fragment teilen**.</span><span class="sxs-lookup"><span data-stu-id="d4e32-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="d4e32-136">Geben Sie im Dialogfeld **Als Fragment speichern** einen Namen für das Fragment ein.</span><span class="sxs-lookup"><span data-stu-id="d4e32-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="d4e32-137">Wählen Sie **OK** aus, um die Modulkonfiguration als Fragment zu speichern, das anderen Seiten hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4e32-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="d4e32-138">Neues Fragment erstellen</span><span class="sxs-lookup"><span data-stu-id="d4e32-138">Create a new fragment</span></span>

<span data-ttu-id="d4e32-139">Führen Sie die folgenden Schritte aus, um ein neues Fragmente im Commerce Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d4e32-140">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="d4e32-141">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-141">Select **New**.</span></span> <span data-ttu-id="d4e32-142">Ein Dialogfeld **Neues Fragment** mit allen verfügbaren Modultypen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4e32-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="d4e32-143">Wie bereits erwähnt, können Fragmente aus jedem Modultyp erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="d4e32-144">Wählen Sie einen Modultyp für Ihr Fragment.</span><span class="sxs-lookup"><span data-stu-id="d4e32-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="d4e32-145">Durch Auswahl eines generischen Containermodultyps erhalten Sie die größte Flexibilität, wenn Sie Ihr Fragment später aktualisieren und konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="d4e32-146">Hinzufügen, Entfernen oder Bearbeiten von Fragmenten auf einer Seite</span><span class="sxs-lookup"><span data-stu-id="d4e32-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="d4e32-147">Die folgenden Prozeduren beschreiben das Hinzufügen, Entfernen und Bearbeiten von Fragmenten.</span><span class="sxs-lookup"><span data-stu-id="d4e32-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="d4e32-148">Fragment hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d4e32-148">Add a fragment</span></span>

<span data-ttu-id="d4e32-149">Führen Sie die folgenden Schritte aus, um ein Fragmente im Commerce Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d4e32-150">Wählen Sie im Gliederungsbereich links oder direkt im Visual Page Builder einen Container oder Slot aus, zu dem untergeordnete Module hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="d4e32-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="d4e32-151">Wählen Sie die Auslassungspunkte (**...**) neben dem Namen des Containers oder Slots aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="d4e32-152">Wenn Sie alternativ Visual Page Builder verwenden, wählen Sie das Pluszeichen (**+**) aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="d4e32-153">Wählen Sie **Fragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d4e32-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="d4e32-154">Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Fragment hinzufügen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4e32-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="d4e32-155">Suchen Sie im Dialogfeld **Fragment auswählen** nach einem Fragment, das Sie hinzufügen möchten, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="d4e32-156">Wenn keine verfügbaren Fragmente aufgelistet sind, müssen Sie möglicherweise zuerst ein Fragment aus einem Modultyp erstellen, den der ausgewählte Container oder Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4e32-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="d4e32-157">Wählen Sie Ihr gewünschtes Fragment aus, das dem Container oder Slot auf Ihrer Seite hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4e32-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="d4e32-158">Die Module, die in einem Container oder Slot zulässig sind, werden durch die Seitenvorlage oder die eigenen Definitionen der Module definiert.</span><span class="sxs-lookup"><span data-stu-id="d4e32-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="d4e32-159">Ein Fragment entfernen</span><span class="sxs-lookup"><span data-stu-id="d4e32-159">Remove a fragment</span></span>

<span data-ttu-id="d4e32-160">Führen Sie die folgenden Schritte aus, um ein Fragment aus einem Slot oder Container auf einer Seite im Commerce Site Builder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d4e32-161">Wählen Sie links im Gliederungsbereich die Auslassungspunkte (**...**) neben dem Namen des zu entfernenden Fragments und anschließend das Papierkorbsymbol aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="d4e32-162">Alternativ können Sie das Fragment in Visual Page Builder und das Papierkorbsymbol in der Symbolleiste des Fragments auswählen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="d4e32-163">Wenn Sie aufgefordert werden, das Entfernen des Fragments zu bestätigen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d4e32-164">Wenn Sie ein Fragment von einer Seite entfernen, entfernen Sie einfach den Verweis darauf von dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="d4e32-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="d4e32-165">Sie löschen das Fragment **nicht** von Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="d4e32-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="d4e32-166">Um Fragmente von Ihrer Site zu löschen, müssen Sie die Benutzeroberfläche des Fragmentinspektors verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="d4e32-167">Sie können Fragmente nur dann von einer Site löschen, wenn derzeit keine Seiten, Vorlagen oder anderen Fragmente auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="d4e32-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="d4e32-168">Fragment bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d4e32-168">Edit a fragment</span></span>

<span data-ttu-id="d4e32-169">Um Fragmente zu bearbeiten, müssen Sie die Benutzeroberfläche des Fragmenteditors verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="d4e32-170">Diese Beschränkung ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="d4e32-170">This restriction is by design.</span></span> <span data-ttu-id="d4e32-171">Es hilft, sicherzustellen, dass Autoren den Prozess der Bearbeitung der Module für eine bestimmte Seite nicht mit dem Prozess der Bearbeitung von Fragmenten verwechseln, die möglicherweise auf mehreren Seiten geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="d4e32-172">Führen Sie die folgenden Schritte aus, um ein neues Fragmente im Commerce Site Builder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4e32-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d4e32-173">Wählen Sie im linken Navigationsbereich **Fragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="d4e32-174">Wählen Sie unter **Fragmente** das zu bearbeitende Fragment aus.</span><span class="sxs-lookup"><span data-stu-id="d4e32-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="d4e32-175">Bearbeiten Sie die Moduleigenschaften und die Struktur des Fragments nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d4e32-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="d4e32-176">Der Vorgang ähnelt dem Vorgang zum Bearbeiten von Modulen, die in der Seiteneditoransicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d4e32-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="d4e32-177">Sie können ein Fragment auch bearbeiten, indem Sie es auf einer Seite, in einer Vorlage oder in einem übergeordneten Fragment auswählen und dann **Fragment bearbeiten** im Eigenschaftenbereich rechts.</span><span class="sxs-lookup"><span data-stu-id="d4e32-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4e32-178">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d4e32-178">Additional resources</span></span>

[<span data-ttu-id="d4e32-179">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="d4e32-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d4e32-180">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="d4e32-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d4e32-181">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="d4e32-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="d4e32-182">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="d4e32-182">Work with publish groups</span></span>](publish-groups.md)

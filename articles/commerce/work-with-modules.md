---
title: Arbeiten mit Modulen
description: In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 89d95814e892e3afcb6514ab0d0219f7b08b9c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000458"
---
# <a name="work-with-modules"></a><span data-ttu-id="5f3d4-103">Arbeiten mit Modulen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5f3d4-104">In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f3d4-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5f3d4-105">Overview</span></span>

<span data-ttu-id="5f3d4-106">Module sind logische Bausteine, aus denen sich Ihre Seitenstruktur zusammensetzt. Sie dienen verschiedenen Zwecken und Bereichen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="5f3d4-107">Einige Module sind übergeordnete Container, und ihr einziger Zweck besteht darin, andere Module (untergeordnete Module) zu speichern und zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="5f3d4-108">Andere Module, z. B. ein einfaches Bildplatzierungsmodul, haben einen ganz bestimmten Zweck.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="5f3d4-109">Weitere Module, z. B. ein Karussellmodul, lassen sich irgendwo zwischen diesen beiden Kategorien einordnen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="5f3d4-110">Standardmäßig enthält Ihre Dynamics 365 Commerce-Site eine Modulbibliothek, mit der Sie die grundlegendsten E-Commerce-Szenarien erstellen können.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="5f3d4-111">Sie sollten in der Lage sein, eine End-to-End-E-Commerce-Site zu erstellen, indem Sie diese Module verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="5f3d4-112">Sie können diese Module jedoch auch anpassen oder neue, benutzerdefinierte Module für bestimmte Anforderungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="5f3d4-113">Wenn Sie benutzerdefinierte Module erstellen möchten, steht ein SDK (Module Design Software Development Kit) zur Verfügung, mit dem Sie eine benutzerdefinierte Modulbibliothek erstellen können.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="5f3d4-114">Containermodule und -Slots</span><span class="sxs-lookup"><span data-stu-id="5f3d4-114">Container modules and slots</span></span>

<span data-ttu-id="5f3d4-115">Wie bereits erwähnt, enthalten einige Module untergeordnete Module.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="5f3d4-116">Diese Module sind als *Container* bekannt und sie ermöglichen Hierarchien geschachtelter Module.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="5f3d4-117">Containermodule enthalten *Slots*.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-117">Container modules include *slots*.</span></span> <span data-ttu-id="5f3d4-118">Slots werden verwendet, um das Layout und den Zweck von untergeordneten Modulen im Container zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="5f3d4-119">Ein Beispiel ist ein grundlegendes Seitencontainermodul (ein übergeordnetes Modul für jede Seite), das mehrere wichtige Slots definiert:</span><span class="sxs-lookup"><span data-stu-id="5f3d4-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="5f3d4-120">Ein Kopfzeilen-Slot</span><span class="sxs-lookup"><span data-stu-id="5f3d4-120">A header slot</span></span>
- <span data-ttu-id="5f3d4-121">Ein Unterkopfzeilen-Slot</span><span class="sxs-lookup"><span data-stu-id="5f3d4-121">A sub-header slot</span></span>
- <span data-ttu-id="5f3d4-122">Ein Haupt-Slot</span><span class="sxs-lookup"><span data-stu-id="5f3d4-122">A main slot</span></span>
- <span data-ttu-id="5f3d4-123">Ein Fußzeilen-Slot</span><span class="sxs-lookup"><span data-stu-id="5f3d4-123">A footer slot</span></span>
- <span data-ttu-id="5f3d4-124">Ein Unterfußzeilen-Slot</span><span class="sxs-lookup"><span data-stu-id="5f3d4-124">A sub-footer slot</span></span>

<span data-ttu-id="5f3d4-125">Der Modulentwickler definiert diese Slots und legt fest, welche untergeordneten Module und wie viele untergeordnete Module direkt darin platziert werden können.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="5f3d4-126">Beispielsweise unterstützt der Kopfzeilen-Slot möglicherweise nur einen Typ des **Kopfzeilen-Moduls**, wohingegen der Text-Slot eine unbegrenzte Anzahl an Modulen jedes Typs unterstützt (mit Ausnahme andere Seitencontainermodule).</span><span class="sxs-lookup"><span data-stu-id="5f3d4-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="5f3d4-127">In den Erstellungstools müssen Seitenautoren nicht im Voraus wissen, welche Module in die einzelnen Slots eingefügt werden können und welche nicht.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="5f3d4-128">Wenn Seitenautoren einen Slot auswählen und dann versuchen, ein Modul zum Hinzufügen auszuwählen, wird eine gefilterte Ansicht der Modultypen angezeigt, die für diesen Slot unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="5f3d4-129">Inhaltsmodule</span><span class="sxs-lookup"><span data-stu-id="5f3d4-129">Content modules</span></span>

<span data-ttu-id="5f3d4-130">Inhaltsmodule enthalten Inhalts- und Medienelemente wie Text (z. B. Überschriften, Absätze und Links) oder Ressourcenverweise (z. B. Bilder, Videos und PDFs).</span><span class="sxs-lookup"><span data-stu-id="5f3d4-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="5f3d4-131">Typische Inhaltsmodultypen umfassen Inhaltsblock-, Textblock- und Promobannermodule.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="5f3d4-132">Module dieser drei Typen können Text oder Medien enthalten und erfordern keine untergeordneten Module, um etwas auf einer Seite sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="5f3d4-133">Die Mehrzahl der typischen täglichen Seiten- und Inhaltserstellungsaktivitäten umfasst Inhaltsmodule, hauptsächlich weil diese Module den tatsächlichen Inhalt definieren, der in ihren übergeordneten Containermodulen gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="5f3d4-134">Es sind viele Inhaltsmodule verfügbar, und diese Module sind normalerweise die letzten Elemente, die Sie der Hierarchie der verschachtelten Module einer Seite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="5f3d4-135">Die folgende Abbildung zeigt, wie Module in übergeordneten Containermodul-Slots verschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Verschachteln von Modulen](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="5f3d4-137">Module hinzufügen oder entfernen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-137">Add or remove modules</span></span>

<span data-ttu-id="5f3d4-138">Die folgenden Prozeduren beschreiben das Hinzufügen und Entfernen von Modulen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="5f3d4-139">Ein Modul hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-139">Add a module</span></span>

<span data-ttu-id="5f3d4-140">Gehen Sie folgendermaßen vor, um ein Modul aus einem Slot oder Container auf einer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-141">Wählen Sie im Gliederungsbereich links oder direkt auf der Haupt-Canvas einen Container oder Slot aus, zu dem ein untergeordnetes Modul hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f3d4-142">Der Moduldesigner definiert die Liste der Modultypen, die einem bestimmten Modul-Slot hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="5f3d4-143">Vorlagenautoren können dann die zulässigen Moduloptionen verfeinern, um eine konsistente Suchmaschinenoptimierung (SEO) und Autoreneffizienz für alle Seiten sicherzustellen, die aus einer bestimmten Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="5f3d4-144">Wenn Sie einem Slot ein Modul hinzufügen, wird das Dialogfeld **Modul hinzufügen** automatisch gefiltert, sodass nur Module angezeigt werden, die im ausgewählten Container oder Slot unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="5f3d4-145">Die Liste der zulässigen Module wird durch die Seitenvorlage oder die Containermoduldefinition bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="5f3d4-146">Wenn Sie den Gliederungsbereich verwenden, wählen Sie die Auslassungspunkte (**...**) neben dem Modulnamen und dann **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="5f3d4-147">Wenn Sie die Steuerelemente direkt auf der Canvas verwenden, wählen Sie das Pluszeichen (**+**) in einem leeren Slot oder neben dem aktuell ausgewählten Modul und dann **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f3d4-148">Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Modul hinzufügen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="5f3d4-149">Wählen Sie im Dialogfeld **Modul hinzufügen** ein Modul aus, um es Ihrer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="5f3d4-150">**Inhaltsblock** ist ein guter Modultyp für Anfänger.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="5f3d4-151">Wählen Sie **OK** aus, um das ausgewählte Modul dem ausgewählten Container oder Slot auf Ihrer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="5f3d4-152">Ein Modul entfernen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-152">Remove a module</span></span>

<span data-ttu-id="5f3d4-153">Gehen Sie folgendermaßen vor, um ein Moduls aus einem Slot oder Container auf einer Seite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-154">Wählen Sie links im Gliederungsbereich die Auslassungspunkte (**...**) neben dem Namen des zu entfernenden Moduls und anschließend das Papierkorbsymbol aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="5f3d4-155">Alternativ können Sie auf der Haupt-Canvas das Papierkorbsymbol in der Symbolleiste eines ausgewählten Moduls auswählen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="5f3d4-156">Wenn Sie aufgefordert werden, das Entfernen des Moduls zu bestätigen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="5f3d4-157">Ein Modul an eine neue Position verschieben</span><span class="sxs-lookup"><span data-stu-id="5f3d4-157">Move a module to a new position</span></span>

<span data-ttu-id="5f3d4-158">Verwenden Sie eine der folgenden Methoden, um ein Modul an eine neue Position auf Ihrer Seite zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="5f3d4-159">Ein Modul mithilfe des Gliederungsbereichs verschieben</span><span class="sxs-lookup"><span data-stu-id="5f3d4-159">Move a module using the outline pane</span></span>

<span data-ttu-id="5f3d4-160">Führen Sie die folgenden Schritte aus, um ein Modul mithilfe des Gliederungsbereichs zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-161">Wählen und halten Sie das Modul, das Sie verschieben möchten, im Gliederungsbereich, und ziehen Sie das Modul an eine neue Position in der Gliederung.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="5f3d4-162">Die blaue Linie in der Gliederung und auf der Canvas zeigt an, wo das Modul platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="5f3d4-163">Lassen Sie das Modul los, um es in der neuen Position abzulegen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="5f3d4-164">Ein Modul direkt auf der Canvas verschieben</span><span class="sxs-lookup"><span data-stu-id="5f3d4-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="5f3d4-165">Führen Sie die folgenden Schritte aus, um ein Modul direkt auf der Canvas zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-166">Wählen Sie das Modul aus, das Sie auf der Canvas verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="5f3d4-167">Wählen Sie in der Symbolleiste des Moduls entweder ein nach oben oder nach unten zeigendes Pfeilsymbol aus, und ziehen Sie den Pfeil an eine neue Position auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="5f3d4-168">Die blaue Linie auf der Canvas und in der Gliederung zeigt an, wo das Modul platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="5f3d4-169">Wenn ein Modul nicht nach oben oder unten verschoben werden kann, ist dieses Pfeilsymbol ausgegraut.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="5f3d4-170">Lassen Sie das Modul los, um es in der neuen Position abzulegen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="5f3d4-171">Ein Modul mithilfe des Auslassungsmenüs verschieben</span><span class="sxs-lookup"><span data-stu-id="5f3d4-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="5f3d4-172">Führen Sie die folgenden Schritte aus, um ein Modul mithilfe des Auslassungsmenüs zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-173">Wählen Sie ein Modul entweder in der Gliederung oder auf der Canvas aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="5f3d4-174">Wählen Sie die Auslassungspunkte (**...**) neben dem Namen des Moduls im Gliederungsbereich oder in der Symbolleiste des ausgewählten Moduls auf der Canvas aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="5f3d4-175">Wenn das Modul innerhalb des Containers oder Slots nach oben oder unten verschoben werden kann, werden Optionen für **Nach oben** oder **Nach unten** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="5f3d4-176">Wählen Sie die gewünschte Verschiebungsoption aus, um das Modul relativ zu seinen gleichgeordneten Elementen nach oben oder unten zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="5f3d4-177">Module konfigurieren</span><span class="sxs-lookup"><span data-stu-id="5f3d4-177">Configure modules</span></span>

<span data-ttu-id="5f3d4-178">In den folgenden Prozeduren wird beschrieben, wie Sie Inhalts- und Containermodule konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="5f3d4-179">Ein Inhaltsmodul konfigurieren</span><span class="sxs-lookup"><span data-stu-id="5f3d4-179">Configure a content module</span></span>

<span data-ttu-id="5f3d4-180">Um ein Inhaltsmodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-181">Erweitern Sie die Baumstruktur im Gliederungsbereich links, und wählen Sie einen beliebigen Inhaltsmodultyp (z. B. **Inhaltsblock**) aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="5f3d4-182">Alternativ können Sie das Modul auf der Haupt-Canvas auswählen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="5f3d4-183">Geben Sie im Moduleigenschaftsbereich auf der rechten Seite Eigenschaften für alle gewünschten Modulsteuerelemente ein.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="5f3d4-184">Wählen Sie in der Befehlsleiste **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="5f3d4-185">Dadurch wird auch der Vorschau-Canvas aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="5f3d4-186">Modultexteigenschaften bearbeiten</span><span class="sxs-lookup"><span data-stu-id="5f3d4-186">Edit module text properties</span></span>

<span data-ttu-id="5f3d4-187">Modultexteigenschaften, die nicht schreibgeschützt sind, können direkt auf der Canvas bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="5f3d4-188">Führen Sie die folgenden Schritte aus, um die Modultexteigenschaften zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-189">Wählen Sie das Textsteuerelement auf der Canvas aus, und platzieren Sie den Cursor an der Stelle, an der Sie Text bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="5f3d4-190">Geben Sie Ihren Textinhalt ein.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-190">Enter your text content.</span></span>
1. <span data-ttu-id="5f3d4-191">Wählen Sie eine beliebige Stelle außerhalb des Textinhalts aus, um weitere Inhalte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="5f3d4-192">Inline-Bildauswahl</span><span class="sxs-lookup"><span data-stu-id="5f3d4-192">Inline image selection</span></span>

<span data-ttu-id="5f3d4-193">Modulbilder, die nicht schreibgeschützt sind, können direkt über die Canvas geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="5f3d4-194">Führen Sie die folgenden Schritte aus, um ein neues Bild für ein Inhaltsmodul auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-195">Doppelklicken Sie auf der Canvas auf das Bild.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="5f3d4-196">Dadurch wird das Medienauswahlfenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="5f3d4-197">Suchen Sie ein neues Bild, das Sie verwenden möchten, und wählen Sie es aus. Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="5f3d4-198">Das neue Bild wird jetzt auf der Canvas gerendert.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="5f3d4-199">Ein Containermodul konfigurieren</span><span class="sxs-lookup"><span data-stu-id="5f3d4-199">Configure a container module</span></span>

<span data-ttu-id="5f3d4-200">Um ein Containermodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="5f3d4-201">Wählen Sie ein Containermodul auf Ihrer Seite aus (z. B. ein Karussell oder ein flüssiges Containermodul).</span><span class="sxs-lookup"><span data-stu-id="5f3d4-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="5f3d4-202">Erweitern Sie im Eigenschaftenbereich rechts die verschachtelten Steuerelemente, indem Sie die Überschriften auswählen, und legen Sie die erforderlichen Steuerelementwerte fest.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="5f3d4-203">Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des Containers oder von Slots im Container und dann **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="5f3d4-204">Fügen Sie dann dem ausgewählten Container untergeordnete Module hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="5f3d4-205">Weitere Informationen erhalten Sie im Abschnitt [Mit Modulen arbeiten](#add-a-module) am Anfang dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="5f3d4-206">Wenn mehrere untergeordnete Module als gleichgeordnete Elemente in einem übergeordneten Container vorhanden sind, können Sie deren Anzeigereihenfolge im übergeordneten Container ändern.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="5f3d4-207">Wählen Sie die Auslassungsschaltfläche für ein Modul aus und verwenden Sie dann die Aufwärts- und Abwärtspfeiltasten.</span><span class="sxs-lookup"><span data-stu-id="5f3d4-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f3d4-208">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-208">Additional resources</span></span>

[<span data-ttu-id="5f3d4-209">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="5f3d4-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="5f3d4-210">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="5f3d4-211">Arbeiten mit Voreinstellungslayouts</span><span class="sxs-lookup"><span data-stu-id="5f3d4-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="5f3d4-212">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="5f3d4-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="5f3d4-213">Ein Containermodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="5f3d4-214">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="5f3d4-214">Work with publish groups</span></span>](publish-groups.md)


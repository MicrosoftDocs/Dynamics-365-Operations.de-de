---
title: IFrame-Modul
description: Dieses Thema behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665395"
---
# <a name="iframe-module"></a><span data-ttu-id="6a58c-103">IFrame-Modul</span><span class="sxs-lookup"><span data-stu-id="6a58c-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a58c-104">Dieses Thema behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6a58c-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a58c-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6a58c-105">Overview</span></span>

<span data-ttu-id="6a58c-106">Ein iFrame-Modul stellt einen iFrame (Inlineframe) bereit, der externe Inhalte auf einer Website hostet.</span><span class="sxs-lookup"><span data-stu-id="6a58c-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="6a58c-107">Zum Beispiel kann es verwendet werden, um auf einer Webseite ein YouTube-Video oder einen PDF-Datei-Viewer zu hosten.</span><span class="sxs-lookup"><span data-stu-id="6a58c-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="6a58c-108">Ein iFrame-Modul benötigt eine Ziel-URL.</span><span class="sxs-lookup"><span data-stu-id="6a58c-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="6a58c-109">Anschließend wird der Inhalt der Zielseite in einem HTML-**iFrame**-Element gehostet.</span><span class="sxs-lookup"><span data-stu-id="6a58c-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="6a58c-110">Externe URLs müssen auf der Zulassungsliste gemäß der Inhaltssicherheitsrichtlinie (CPS) der Website stehen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="6a58c-111">Für iFrame-Inhalte sollten URLs mithilfe der **frame-ancester**-Richtlinie zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="6a58c-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="6a58c-112">Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="6a58c-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6a58c-113">Das iFrame-Modul ist in der Dynamics 365 Commerce-Version 10.0.13 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a58c-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="6a58c-114">Das folgende Bild zeigt Beispiele für iFrame-Module, die externe Videos auf Webseiten zeigen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Beispiel für iFrame-Module, die externe Videos zeigen](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="6a58c-116">Hinzufügen von iFrame-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a58c-116">Iframe module properties</span></span>

| <span data-ttu-id="6a58c-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6a58c-117">Property name</span></span>             | <span data-ttu-id="6a58c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6a58c-118">Value</span></span>                 | <span data-ttu-id="6a58c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a58c-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6a58c-120">Überschrift</span><span class="sxs-lookup"><span data-stu-id="6a58c-120">Heading</span></span> | <span data-ttu-id="6a58c-121">Text</span><span class="sxs-lookup"><span data-stu-id="6a58c-121">Text</span></span> | <span data-ttu-id="6a58c-122">Die Überschrift für das Modul.</span><span class="sxs-lookup"><span data-stu-id="6a58c-122">The heading for the module.</span></span> |
| <span data-ttu-id="6a58c-123">Ziel-URL</span><span class="sxs-lookup"><span data-stu-id="6a58c-123">Target URL</span></span> | <span data-ttu-id="6a58c-124">URL</span><span class="sxs-lookup"><span data-stu-id="6a58c-124">URL</span></span> | <span data-ttu-id="6a58c-125">Die URL, die im Modul gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="6a58c-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="6a58c-126">Höhe</span><span class="sxs-lookup"><span data-stu-id="6a58c-126">Height</span></span> | <span data-ttu-id="6a58c-127">Anzahl oder Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="6a58c-127">Number or percentage</span></span> | <span data-ttu-id="6a58c-128">Die Höhe des Moduls, in Pixeln oder Prozent.</span><span class="sxs-lookup"><span data-stu-id="6a58c-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="6a58c-129">Zum Beispiel wird der Wert **100** als Anzahl von Pixeln und der Wert **100 %** als Prozentsatz behandelt.</span><span class="sxs-lookup"><span data-stu-id="6a58c-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="6a58c-130">Aria-Label</span><span class="sxs-lookup"><span data-stu-id="6a58c-130">Aria label</span></span> | <span data-ttu-id="6a58c-131">Text</span><span class="sxs-lookup"><span data-stu-id="6a58c-131">Text</span></span> | <span data-ttu-id="6a58c-132">Aus Gründen der Barrierefreiheit kann ein Label von „Accessible Rich Internet Applications“ (ARIA) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6a58c-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="6a58c-133">Ein iFrame-Modul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="6a58c-133">Add an iframe module to a page</span></span>

<span data-ttu-id="6a58c-134">Gehen Sie wie folgt vor, um einer Seite ein iFrame-Modul hinzuzufügen und ein externes Video anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="6a58c-135">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6a58c-136">Im Dialogfeld **Neue Vorlage** geben Sie unter **Vorlagenname** **Containervorlage** ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a58c-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6a58c-137">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6a58c-138">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="6a58c-139">In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Marketingvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="6a58c-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="6a58c-140">Gehen Sie unter **Seitenname** **Marketingseite** ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a58c-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="6a58c-141">Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6a58c-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6a58c-142">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6a58c-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6a58c-143">Legen Sie im Eigenschaftsbereich des Moduls den **Breite**-Wert auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="6a58c-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="6a58c-144">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6a58c-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6a58c-145">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **iFrame** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6a58c-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6a58c-146">Legen Sie im Eigenschaftenbereich des Moduls den Wert der **Ziel-URL** auf eine externe URL für ein Video fest.</span><span class="sxs-lookup"><span data-stu-id="6a58c-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="6a58c-147">Legen Sie weitere benötigte Eigenschaften fest, wie **Überschrift** und **Höhe**.</span><span class="sxs-lookup"><span data-stu-id="6a58c-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="6a58c-148">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6a58c-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6a58c-149">Gehen Sie zur Marketingseite Ihrer Website.</span><span class="sxs-lookup"><span data-stu-id="6a58c-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="6a58c-150">Sie sollten sehen, dass das Video im iFrame-Modul gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="6a58c-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="6a58c-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a58c-151">Additional resources</span></span>

[<span data-ttu-id="6a58c-152">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="6a58c-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6a58c-153">Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) verwalten</span><span class="sxs-lookup"><span data-stu-id="6a58c-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)

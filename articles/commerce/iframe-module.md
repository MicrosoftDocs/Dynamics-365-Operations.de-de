---
title: IFrame-Modul
description: Dieses Thema behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646941"
---
# <a name="iframe-module"></a><span data-ttu-id="39d91-103">IFrame-Modul</span><span class="sxs-lookup"><span data-stu-id="39d91-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="39d91-104">Dieses Thema behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="39d91-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39d91-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="39d91-105">Overview</span></span>

<span data-ttu-id="39d91-106">Ein iFrame-Modul stellt einen iFrame (Inlineframe) bereit, der externe Inhalte auf einer Website hostet.</span><span class="sxs-lookup"><span data-stu-id="39d91-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="39d91-107">Zum Beispiel kann es verwendet werden, um auf einer Webseite ein YouTube-Video oder einen PDF-Datei-Viewer zu hosten.</span><span class="sxs-lookup"><span data-stu-id="39d91-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="39d91-108">Ein iFrame-Modul benötigt eine Ziel-URL.</span><span class="sxs-lookup"><span data-stu-id="39d91-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="39d91-109">Anschließend wird der Inhalt der Zielseite in einem HTML-**iFrame**-Element gehostet.</span><span class="sxs-lookup"><span data-stu-id="39d91-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="39d91-110">Externe URLs müssen auf der Zulassungsliste (der sogenannten „Whitelist“) gemäß der Inhaltssicherheitsrichtlinie (CPS) der Website stehen.</span><span class="sxs-lookup"><span data-stu-id="39d91-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="39d91-111">Für iFrame-Inhalte sollten URLs mithilfe der **frame-ancester**-Richtlinie zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="39d91-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="39d91-112">Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="39d91-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="39d91-113">Das folgende Bild zeigt Beispiele für iFrame-Module, die externe Videos auf Webseiten zeigen.</span><span class="sxs-lookup"><span data-stu-id="39d91-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Beispiel für iFrame-Module, die externe Videos zeigen](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="39d91-115">Hinzufügen von iFrame-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39d91-115">Iframe module properties</span></span>

| <span data-ttu-id="39d91-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="39d91-116">Property name</span></span>             | <span data-ttu-id="39d91-117">Wert</span><span class="sxs-lookup"><span data-stu-id="39d91-117">Value</span></span>                 | <span data-ttu-id="39d91-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39d91-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="39d91-119">Überschrift</span><span class="sxs-lookup"><span data-stu-id="39d91-119">Heading</span></span> | <span data-ttu-id="39d91-120">Text</span><span class="sxs-lookup"><span data-stu-id="39d91-120">Text</span></span> | <span data-ttu-id="39d91-121">Die Überschrift für das Modul.</span><span class="sxs-lookup"><span data-stu-id="39d91-121">The heading for the module.</span></span> |
| <span data-ttu-id="39d91-122">Ziel-URL</span><span class="sxs-lookup"><span data-stu-id="39d91-122">Target URL</span></span> | <span data-ttu-id="39d91-123">URL</span><span class="sxs-lookup"><span data-stu-id="39d91-123">URL</span></span> | <span data-ttu-id="39d91-124">Die URL, die im Modul gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="39d91-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="39d91-125">Höhe</span><span class="sxs-lookup"><span data-stu-id="39d91-125">Height</span></span> | <span data-ttu-id="39d91-126">Anzahl oder Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="39d91-126">Number or percentage</span></span> | <span data-ttu-id="39d91-127">Die Höhe des Moduls, in Pixeln oder Prozent.</span><span class="sxs-lookup"><span data-stu-id="39d91-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="39d91-128">Zum Beispiel wird der Wert **100** als Anzahl von Pixeln und der Wert **100 %** als Prozentsatz behandelt.</span><span class="sxs-lookup"><span data-stu-id="39d91-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="39d91-129">Aria-Label</span><span class="sxs-lookup"><span data-stu-id="39d91-129">Aria label</span></span> | <span data-ttu-id="39d91-130">Text</span><span class="sxs-lookup"><span data-stu-id="39d91-130">Text</span></span> | <span data-ttu-id="39d91-131">Aus Gründen der Barrierefreiheit kann ein Label von „Accessible Rich Internet Applications“ (ARIA) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="39d91-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="39d91-132">Ein iFrame-Modul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="39d91-132">Add an iframe module to a page</span></span>

<span data-ttu-id="39d91-133">Gehen Sie wie folgt vor, um einer Seite ein iFrame-Modul hinzuzufügen und ein externes Video anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39d91-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="39d91-134">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39d91-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="39d91-135">Im Dialogfeld **Neue Vorlage** geben Sie unter **Vorlagenname** **Containervorlage** ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39d91-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="39d91-136">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="39d91-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="39d91-137">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39d91-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="39d91-138">In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Marketingvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="39d91-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="39d91-139">Gehen Sie unter **Seitenname** **Marketingseite** ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="39d91-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="39d91-140">Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39d91-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39d91-141">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="39d91-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39d91-142">Legen Sie im Eigenschaftsbereich des Moduls den **Breite**-Wert auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="39d91-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="39d91-143">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39d91-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39d91-144">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **iFrame** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="39d91-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39d91-145">Legen Sie im Eigenschaftenbereich des Moduls den Wert der **Ziel-URL** auf eine externe URL für ein Video fest.</span><span class="sxs-lookup"><span data-stu-id="39d91-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="39d91-146">Legen Sie weitere benötigte Eigenschaften fest, wie **Überschrift** und **Höhe**.</span><span class="sxs-lookup"><span data-stu-id="39d91-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="39d91-147">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="39d91-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="39d91-148">Gehen Sie zur Marketingseite Ihrer Website.</span><span class="sxs-lookup"><span data-stu-id="39d91-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="39d91-149">Sie sollten sehen, dass das Video im iFrame-Modul gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="39d91-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="39d91-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39d91-150">Additional resources</span></span>

[<span data-ttu-id="39d91-151">Überblick über das Starterkit</span><span class="sxs-lookup"><span data-stu-id="39d91-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="39d91-152">Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) verwalten</span><span class="sxs-lookup"><span data-stu-id="39d91-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)

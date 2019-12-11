---
title: Hero-Modul
description: Dieses Thema enthält Heromodule und es wird beschrieben, wie diese den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785389"
---
# <a name="hero-module"></a><span data-ttu-id="0307e-103">Hero-Modul</span><span class="sxs-lookup"><span data-stu-id="0307e-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0307e-104">Dieses Thema enthält Heromodule und es wird beschrieben, wie diese den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0307e-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0307e-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0307e-105">Overview</span></span>

<span data-ttu-id="0307e-106">Ein Heldmodul wird verwendet, um Produkte oder verkaufsfördernden Maßnahmen über eine Kombination von Bildern und Text zu promoten.</span><span class="sxs-lookup"><span data-stu-id="0307e-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="0307e-107">So kann beispielsweise ein Einzelhändler ein Heldmodul der Startseite einer E-Commerce-Webseite hinzufügen, um ein neues Produkt zu bewerben und die Aufmerksamkeit von Debitoren zu erregen.</span><span class="sxs-lookup"><span data-stu-id="0307e-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="0307e-108">Ein Heromodul wird durch Daten des Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0307e-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="0307e-109">Es ist ein Stand-Alone-Module, das die nicht von Seiteninhalt oder anderen Modulen auf der Seite abhängt.</span><span class="sxs-lookup"><span data-stu-id="0307e-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="0307e-110">Ein Heromodul kann für jede beliebige Siteseite verwendet werden, in der ein Einzelhändler etwas promoten will (beispielsweise Produkte, Verkäufe oder Funktionen).</span><span class="sxs-lookup"><span data-stu-id="0307e-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="0307e-111">Beispiele für Heromodule im E-Commerce</span><span class="sxs-lookup"><span data-stu-id="0307e-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="0307e-112">Ein Heromodul kann auf der Startseite einer E-Commerce-Webseite verwendet werden, um Aktionen und neue Produkte hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="0307e-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="0307e-113">Ein Heromodul kann auf einer Produktdetailseite verwendet werden, um Produktinformationen zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="0307e-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="0307e-114">Mehrere Heromodule können innerhalb eines Karussellmoduls eingelagert werden, um mehrere Produkte oder Promotionen hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="0307e-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="0307e-115">Heromoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="0307e-115">Hero module properties</span></span>

| <span data-ttu-id="0307e-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="0307e-116">Property name</span></span>  | <span data-ttu-id="0307e-117">Werte</span><span class="sxs-lookup"><span data-stu-id="0307e-117">Values</span></span> | <span data-ttu-id="0307e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0307e-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0307e-119">Bild</span><span class="sxs-lookup"><span data-stu-id="0307e-119">Image</span></span>          | <span data-ttu-id="0307e-120">Bilddatei</span><span class="sxs-lookup"><span data-stu-id="0307e-120">Image file</span></span> | <span data-ttu-id="0307e-121">Ein Bild kann verwendet werden, um ein Produkt oder eine verkaufsfördernde Aktion zu machen.</span><span class="sxs-lookup"><span data-stu-id="0307e-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="0307e-122">Ein Bild kann zu der Bildergalerie hochgeladen werden, oder ein vorhandenes Bild kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0307e-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="0307e-123">Überschrift</span><span class="sxs-lookup"><span data-stu-id="0307e-123">Heading</span></span>        | <span data-ttu-id="0307e-124">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="0307e-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0307e-125">Jedes Heromodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="0307e-125">Every hero module can have a heading.</span></span> <span data-ttu-id="0307e-126">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="0307e-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0307e-127">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0307e-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0307e-128">Absatz</span><span class="sxs-lookup"><span data-stu-id="0307e-128">Paragraph</span></span>      | <span data-ttu-id="0307e-129">Absatztext</span><span class="sxs-lookup"><span data-stu-id="0307e-129">Paragraph text</span></span> | <span data-ttu-id="0307e-130">Heromodul unterstützt Absatztext im Rich-Text-Format.</span><span class="sxs-lookup"><span data-stu-id="0307e-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="0307e-131">Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung und Hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="0307e-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="0307e-132">Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0307e-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="0307e-133">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="0307e-133">Link</span></span>           | <span data-ttu-id="0307e-134">Verknüpfen Sie Text, Link-URL, umfangreiche Internet-Anwendungs (ARIA)- Beschriftung und **Öffnen Sie die Verknüpfung in einer neuen Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="0307e-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="0307e-135">Heromodul unterstützt mindestens einen oder mehrere Links „Aufruf zum Handelns“.</span><span class="sxs-lookup"><span data-stu-id="0307e-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="0307e-136">Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0307e-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="0307e-137">ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0307e-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="0307e-138">Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0307e-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="0307e-139">Textplatzierung</span><span class="sxs-lookup"><span data-stu-id="0307e-139">Text placement</span></span> | <span data-ttu-id="0307e-140">**Oben links**, **Oben rechts**, **Oben zentriert**, **Unten links**, **Unten rechts**, **Unten zentriert**, **Mitte links**, **Mitte rechts** oder **Mitte zentriert**</span><span class="sxs-lookup"><span data-stu-id="0307e-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="0307e-141">Diese Eigenschaft definiert die Bildlage relativ zum im Text.</span><span class="sxs-lookup"><span data-stu-id="0307e-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="0307e-142">Wenn beispielsweise **Rechts** aktiviert ist, erscheint das Bild auf der rechten Seite des Texts.</span><span class="sxs-lookup"><span data-stu-id="0307e-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="0307e-143">Textdesign</span><span class="sxs-lookup"><span data-stu-id="0307e-143">Text theme</span></span>     | <span data-ttu-id="0307e-144">**Hell** oder **Dunkel**</span><span class="sxs-lookup"><span data-stu-id="0307e-144">**Light** or **Dark**</span></span> | <span data-ttu-id="0307e-145">Ein Farbschema kann für den Text definiert werden, der auf Grundlage des Hintergrundbilds basiert.</span><span class="sxs-lookup"><span data-stu-id="0307e-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="0307e-146">Wenn beispielsweise das Bild einen dunklen Hintergrund hat, kann ein Lichtthema angewendet werden, damit der Text sichtbarer wird und die Farbenkontrast-Verhältnisse verbessert.</span><span class="sxs-lookup"><span data-stu-id="0307e-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="0307e-147">Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="0307e-147">Gradient</span></span>       | <span data-ttu-id="0307e-148">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="0307e-148">**True** or **False**</span></span> | <span data-ttu-id="0307e-149">Ein Farbverlauf kann für das Bild angewendet werden, um Farbenkontrast-Verhältnisse zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="0307e-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="0307e-150">Ein Heromodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0307e-150">Add a hero module to a new page</span></span>

<span data-ttu-id="0307e-151">Um ein Heromodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="0307e-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0307e-152">Gehen Sie zu **Vorlagen** und erstellen Sie eine Seitenvorlage mit der Bezeichnung **Herovorlage**.</span><span class="sxs-lookup"><span data-stu-id="0307e-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="0307e-153">Im **Haupt-** Slot der Standardseite fügen Sie ein Heromodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="0307e-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="0307e-154">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="0307e-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="0307e-155">Verwenden Sie die Herovorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Heroseite** hat.</span><span class="sxs-lookup"><span data-stu-id="0307e-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="0307e-156">Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="0307e-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0307e-157">Im Dialogfeld **Modul hinzufügen** unter **Modul wählen** wählen Sie das Heromodul, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="0307e-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="0307e-158">In der Gliederungsstruktur im Feld links wählen Sie das Heromodul aus.</span><span class="sxs-lookup"><span data-stu-id="0307e-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="0307e-159">Wählen Sie im Eigenschaftenbereich rechts und wählen Sie **Eine Bild hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0307e-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="0307e-160">Wählen Sie dann ein vorhandenes Bild aus oder laden Sie ein neues Bild hoch.</span><span class="sxs-lookup"><span data-stu-id="0307e-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="0307e-161">Wählen Sie **Kopfzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="0307e-161">Select **Heading**.</span></span>
1. <span data-ttu-id="0307e-162">Im Dialogfeld **Überschrift** fügen Sie den Überschriftentext hinzu, wählen Sie die Überschriftsebene, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0307e-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="0307e-163">Fügen Sie unter **Rich-Text** Text hinzufügen, wie Sie diesen benötigen.</span><span class="sxs-lookup"><span data-stu-id="0307e-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="0307e-164">Wählen Sie **Fügen Sie Aktivitäts-Link hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="0307e-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="0307e-165">Im Dialogfeld **Aktivitäts-Link** fügen Sie Text des Links, eine URL und eine ARIA-Beschriftung hinzu und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="0307e-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="0307e-166">Seite speichern und Ihre Änderungen in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0307e-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="0307e-167">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="0307e-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0307e-168">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0307e-168">Additional resources</span></span>

[<span data-ttu-id="0307e-169">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="0307e-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0307e-170">Warnmmodul</span><span class="sxs-lookup"><span data-stu-id="0307e-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="0307e-171">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="0307e-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="0307e-172">Umfangreiches Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="0307e-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="0307e-173">Inhaltsplatzierungsmodul</span><span class="sxs-lookup"><span data-stu-id="0307e-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="0307e-174">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="0307e-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="0307e-175">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="0307e-175">Video player module</span></span>](add-video-player.md)

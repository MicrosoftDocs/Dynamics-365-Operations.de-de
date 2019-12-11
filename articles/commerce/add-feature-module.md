---
title: Funktionsmodul
description: Dieses Thema enthält Funktionsmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785283"
---
# <a name="feature-module"></a><span data-ttu-id="fdafc-103">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="fdafc-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fdafc-104">Dieses Thema enthält Funktionsmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fdafc-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fdafc-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="fdafc-105">Overview</span></span>

<span data-ttu-id="fdafc-106">Ein Funktionsmodul wird verwendet, um Produkte oder verkaufsfördernden Maßnahmen über eine Kombination von Bildern und Text zu promoten.</span><span class="sxs-lookup"><span data-stu-id="fdafc-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="fdafc-107">So kann beispielsweise ein Einzelhändler ein Funktionsmodul einer Produktdetailseite hinzufügen, um die Funktionen des Produkts hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="fdafc-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="fdafc-108">Ein Funktionsmodul wird durch Daten des Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="fdafc-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="fdafc-109">Es ist ein Stand-Alone-Module, das die nicht von Seiteninhalt oder anderen Modulen auf der Seite abhängt.</span><span class="sxs-lookup"><span data-stu-id="fdafc-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="fdafc-110">Ein Funktionsmodul kann für jede beliebige Siteseite verwendet werden, in der ein Einzelhändler etwas promoten will (beispielsweise Produkte, Verkäufe oder Funktionen).</span><span class="sxs-lookup"><span data-stu-id="fdafc-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="fdafc-111">Beispiele für Funktionsmodule in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="fdafc-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="fdafc-112">Ein Funktionsmodul kann auf den folgenden Seiten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="fdafc-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="fdafc-113">Eine Produktdetailseite, um Produktfunktionen zu zeigen</span><span class="sxs-lookup"><span data-stu-id="fdafc-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="fdafc-114">Die Startseite, um Produkte zu promoten</span><span class="sxs-lookup"><span data-stu-id="fdafc-114">The home page, to promote products</span></span>
- <span data-ttu-id="fdafc-115">Eine Kategorieseite, um eine Produktgruppe zu markieren</span><span class="sxs-lookup"><span data-stu-id="fdafc-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="fdafc-116">Hinzufügen von Funktionseigenschaften</span><span class="sxs-lookup"><span data-stu-id="fdafc-116">Feature module properties</span></span>

| <span data-ttu-id="fdafc-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fdafc-117">Property name</span></span>     | <span data-ttu-id="fdafc-118">Werte</span><span class="sxs-lookup"><span data-stu-id="fdafc-118">Values</span></span> | <span data-ttu-id="fdafc-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdafc-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="fdafc-120">Bild</span><span class="sxs-lookup"><span data-stu-id="fdafc-120">Image</span></span>             | <span data-ttu-id="fdafc-121">Bilddatei</span><span class="sxs-lookup"><span data-stu-id="fdafc-121">Image file</span></span> | <span data-ttu-id="fdafc-122">Ein Bild kann verwendet werden, um ein Produkt oder eine verkaufsfördernde Aktion durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fdafc-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="fdafc-123">Ein Bild kann zu der Bildergalerie hochgeladen werden, oder ein vorhandenes Bild kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdafc-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="fdafc-124">Überschrift</span><span class="sxs-lookup"><span data-stu-id="fdafc-124">Heading</span></span>           | <span data-ttu-id="fdafc-125">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="fdafc-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="fdafc-126">Jedes Funktionsmodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="fdafc-126">Every feature module can have a heading.</span></span> <span data-ttu-id="fdafc-127">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdafc-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="fdafc-128">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="fdafc-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="fdafc-129">Absatz</span><span class="sxs-lookup"><span data-stu-id="fdafc-129">Paragraph</span></span>         | <span data-ttu-id="fdafc-130">Absatztext</span><span class="sxs-lookup"><span data-stu-id="fdafc-130">Paragraph text</span></span> | <span data-ttu-id="fdafc-131">Funktionsmodule unterstützt Absatztext im Rich-Text-Format.</span><span class="sxs-lookup"><span data-stu-id="fdafc-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="fdafc-132">Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung und Hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="fdafc-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="fdafc-133">Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdafc-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="fdafc-134">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="fdafc-134">Link</span></span>              | <span data-ttu-id="fdafc-135">Verknüpfen Sie Text, Link-URL, umfangreiche Internet-Anwendungs (ARIA)- Beschriftung und **Öffnen Sie die Verknüpfung in einer neuen Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="fdafc-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="fdafc-136">Funktionsmomodul unterstützt mindestens einen oder mehrere Links „Aufruf zum Handeln“.</span><span class="sxs-lookup"><span data-stu-id="fdafc-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="fdafc-137">Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fdafc-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="fdafc-138">ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="fdafc-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="fdafc-139">Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="fdafc-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="fdafc-140">Bildplatzierung</span><span class="sxs-lookup"><span data-stu-id="fdafc-140">Image placement</span></span>   | <span data-ttu-id="fdafc-141">**Rechts**, **Links**, **Oben** oder **Unten**</span><span class="sxs-lookup"><span data-stu-id="fdafc-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="fdafc-142">Diese Eigenschaft definiert die Bildlage relativ zum im Text.</span><span class="sxs-lookup"><span data-stu-id="fdafc-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="fdafc-143">Wenn beispielsweise **Rechts** aktiviert ist, erscheint das Bild auf der rechten Seite des Texts.</span><span class="sxs-lookup"><span data-stu-id="fdafc-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="fdafc-144">Bild-Spaltengröße</span><span class="sxs-lookup"><span data-stu-id="fdafc-144">Image column size</span></span> | <span data-ttu-id="fdafc-145">Ein Wert von **1** bis **12**</span><span class="sxs-lookup"><span data-stu-id="fdafc-145">A value from **1** through **12**</span></span> | <span data-ttu-id="fdafc-146">Diese Eigenschaft definiert die Größe des Bildes relativ zum Text.</span><span class="sxs-lookup"><span data-stu-id="fdafc-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="fdafc-147">Größe wird als Anzahl Spalten auf der Seite angegeben.</span><span class="sxs-lookup"><span data-stu-id="fdafc-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="fdafc-148">Es gibt 12 Spalten auf einer Seite.</span><span class="sxs-lookup"><span data-stu-id="fdafc-148">There are 12 columns on a page.</span></span> <span data-ttu-id="fdafc-149">Standardmäßig haben das Bild und der Text die gleiche Größe (je sechs Spalten).</span><span class="sxs-lookup"><span data-stu-id="fdafc-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="fdafc-150">Allerdings kann die Größe nach Bedarf geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fdafc-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="fdafc-151">Ein Funktionsmodul kann einer neuen Seite hinzugefügt werde</span><span class="sxs-lookup"><span data-stu-id="fdafc-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="fdafc-152">Um ein Funktionsmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="fdafc-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fdafc-153">Gehen Sie zu **Vorlagen** und erstellen Sie eine Seitenvorlage mit der Bezeichnung **Funktionsvorlage**.</span><span class="sxs-lookup"><span data-stu-id="fdafc-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="fdafc-154">Im **Haupt-** Slot der Standardseite fügen Sie ein Funktionsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="fdafc-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="fdafc-155">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="fdafc-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="fdafc-156">Verwenden Sie die Funktionsvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Funktionsseite** hat.</span><span class="sxs-lookup"><span data-stu-id="fdafc-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="fdafc-157">Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fdafc-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fdafc-158">Im Dialogfeld **Modul hinzufügen** unter **Modul wählen** wählen Sie das Funktionsmodul, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdafc-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="fdafc-159">In der Gliederungsstruktur im Feld links wählen Sie das Funktionsmodul aus.</span><span class="sxs-lookup"><span data-stu-id="fdafc-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="fdafc-160">Wählen Sie im Eigenschaftenbereich rechts und wählen Sie **Eine Bild hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="fdafc-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="fdafc-161">Wählen Sie dann ein vorhandenes Bild aus oder laden Sie ein neues Bild hoch.</span><span class="sxs-lookup"><span data-stu-id="fdafc-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="fdafc-162">Wählen Sie **Kopfzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="fdafc-162">Select **Heading**.</span></span>
1. <span data-ttu-id="fdafc-163">Im Dialogfeld **Überschrift** fügen Sie den Überschriftentext hinzu, wählen Sie die Überschriftsebene, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fdafc-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="fdafc-164">Fügen Sie unter **Rich-Text** Text hinzufügen, wie Sie diesen benötigen.</span><span class="sxs-lookup"><span data-stu-id="fdafc-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="fdafc-165">Wählen Sie **Fügen Sie Aktivitäts-Link hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="fdafc-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="fdafc-166">Im Dialogfeld **Aktivitäts-Link** fügen Sie Text des Links, eine URL und eine ARIA-Beschriftung hinzu und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdafc-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="fdafc-167">Seite speichern und Ihre Änderungen in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fdafc-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="fdafc-168">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="fdafc-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdafc-169">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fdafc-169">Additional resources</span></span>

[<span data-ttu-id="fdafc-170">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="fdafc-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fdafc-171">Warnmmodul</span><span class="sxs-lookup"><span data-stu-id="fdafc-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="fdafc-172">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="fdafc-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="fdafc-173">Umfangreiches Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="fdafc-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="fdafc-174">Inhaltsplatzierungsmodul</span><span class="sxs-lookup"><span data-stu-id="fdafc-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="fdafc-175">Hero-Modul</span><span class="sxs-lookup"><span data-stu-id="fdafc-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="fdafc-176">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="fdafc-176">Video player module</span></span>](add-video-player.md)

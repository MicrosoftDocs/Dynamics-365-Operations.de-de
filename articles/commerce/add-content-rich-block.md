---
title: Textblock-Modul
description: Dieses Thema behandelt Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797766"
---
# <a name="text-block-module"></a><span data-ttu-id="4b20d-103">Textblockmodul</span><span class="sxs-lookup"><span data-stu-id="4b20d-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b20d-104">Dieses Thema behandelt Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4b20d-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4b20d-105">Ein Textblockmodul ist ein Modul, mit dem Textinhalte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4b20d-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="4b20d-106">Dieser Inhalt kann entweder zu Informations- oder Werbezwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b20d-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="4b20d-107">Textblock-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="4b20d-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="4b20d-108">Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="4b20d-109">Beispiele für Textblockmodule in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="4b20d-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="4b20d-110">Textblockmodule können folgendermaßen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="4b20d-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="4b20d-111">Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="4b20d-112">Für Informationszwecke auf einer beliebigen Seite.</span><span class="sxs-lookup"><span data-stu-id="4b20d-112">For informational purposes on any page.</span></span> <span data-ttu-id="4b20d-113">So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="4b20d-114">Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="4b20d-115">(beispielsweise „kostenloser Versand für Aufträge über $50“).</span><span class="sxs-lookup"><span data-stu-id="4b20d-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="4b20d-116">Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).</span><span class="sxs-lookup"><span data-stu-id="4b20d-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="4b20d-117">Das folgende Bild zeigt ein Beispiel eines Textblockmoduls, das auf einer Homepage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b20d-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Beispiel eines Textblockmoduls](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="4b20d-119">Eigenschaften des Textblock-Moduls</span><span class="sxs-lookup"><span data-stu-id="4b20d-119">Text block module properties</span></span>

| <span data-ttu-id="4b20d-120">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="4b20d-120">Property name</span></span>     | <span data-ttu-id="4b20d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4b20d-121">Value</span></span>                                            | <span data-ttu-id="4b20d-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b20d-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="4b20d-123">Rich-Text</span><span class="sxs-lookup"><span data-stu-id="4b20d-123">Rich text</span></span>         | <span data-ttu-id="4b20d-124">Rich-Text</span><span class="sxs-lookup"><span data-stu-id="4b20d-124">Rich text</span></span>                                        | <span data-ttu-id="4b20d-125">Absatztext.</span><span class="sxs-lookup"><span data-stu-id="4b20d-125">Paragraph text.</span></span> <span data-ttu-id="4b20d-126">Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung.</span><span class="sxs-lookup"><span data-stu-id="4b20d-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="4b20d-127">Benutzerdefinierter Klassenname</span><span class="sxs-lookup"><span data-stu-id="4b20d-127">Custom class name</span></span> | <span data-ttu-id="4b20d-128">Ein Cascading Style Sheets ( CSS) Klassenname</span><span class="sxs-lookup"><span data-stu-id="4b20d-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="4b20d-129">Der Name einer benutzerspezifischen CSS Klasse, die ein Entwickler zum Formatieren dieses Moduls bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4b20d-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="4b20d-130">Der Klassenname sollte im Theme Pack definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b20d-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="4b20d-131">Schriftgröße</span><span class="sxs-lookup"><span data-stu-id="4b20d-131">Font size</span></span>         | <span data-ttu-id="4b20d-132">**Klein**, **Mittel**, **Groß** oder **Sehr groß**</span><span class="sxs-lookup"><span data-stu-id="4b20d-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="4b20d-133">Die Schriftgröße des aktuellen Inhalts.</span><span class="sxs-lookup"><span data-stu-id="4b20d-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="4b20d-134">Hinzufügen eines Textblockmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="4b20d-134">Add a text block module to a page</span></span>

<span data-ttu-id="4b20d-135">Um ein Textblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4b20d-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4b20d-136">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="4b20d-137">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die **Inhaltvorlage** ein und wählen OK.</span><span class="sxs-lookup"><span data-stu-id="4b20d-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="4b20d-138">Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4b20d-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4b20d-139">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4b20d-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4b20d-140">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4b20d-141">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="4b20d-142">In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Inhalt-Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="4b20d-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="4b20d-143">Unter **Seitenname** geben Sie **Inhalt-Seite** ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4b20d-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="4b20d-144">Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4b20d-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4b20d-145">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4b20d-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4b20d-146">Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="4b20d-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="4b20d-147">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4b20d-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4b20d-148">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Textblock** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4b20d-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="4b20d-149">Fügen Sie im Eigenschaftenbereich des Textblockmoduls Text zum Feld **Rich Text** hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b20d-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="4b20d-150">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="4b20d-151">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4b20d-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b20d-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4b20d-152">Additional resources</span></span>

[<span data-ttu-id="4b20d-153">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="4b20d-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4b20d-154">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="4b20d-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="4b20d-155">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="4b20d-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="4b20d-156">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="4b20d-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="4b20d-157">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="4b20d-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
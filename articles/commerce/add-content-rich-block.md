---
title: Textblock-Modul
description: Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cad6a26ea1858d6afac33ef8eab10e16b404035b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980480"
---
# <a name="text-block-module"></a><span data-ttu-id="c5a40-103">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="c5a40-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5a40-104">Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c5a40-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c5a40-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c5a40-105">Overview</span></span>

<span data-ttu-id="c5a40-106">Ein Textblockmodul ist ein Modul, mit dem Textinhalte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c5a40-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="c5a40-107">Dieser Inhalt kann entweder zu Informations- oder Werbezwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5a40-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="c5a40-108">Textblock-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="c5a40-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="c5a40-109">Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="c5a40-110">Beispiele für Textblockmodule in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="c5a40-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="c5a40-111">Textblockmodule können folgendermaßen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="c5a40-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="c5a40-112">Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="c5a40-113">Für Informationszwecke auf einer beliebigen Seite.</span><span class="sxs-lookup"><span data-stu-id="c5a40-113">For informational purposes on any page.</span></span> <span data-ttu-id="c5a40-114">So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="c5a40-115">Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="c5a40-116">(beispielsweise „kostenloser Versand für Aufträge über $50“).</span><span class="sxs-lookup"><span data-stu-id="c5a40-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="c5a40-117">Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).</span><span class="sxs-lookup"><span data-stu-id="c5a40-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="c5a40-118">Das folgende Bild zeigt ein Beispiel eines Textblockmoduls, das auf einer Homepage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5a40-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Beispiel eines Textblockmoduls](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="c5a40-120">Eigenschaften des Textblock-Moduls</span><span class="sxs-lookup"><span data-stu-id="c5a40-120">Text block module properties</span></span>

| <span data-ttu-id="c5a40-121">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="c5a40-121">Property name</span></span>     | <span data-ttu-id="c5a40-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c5a40-122">Value</span></span>                                            | <span data-ttu-id="c5a40-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5a40-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="c5a40-124">Rich-Text</span><span class="sxs-lookup"><span data-stu-id="c5a40-124">Rich text</span></span>         | <span data-ttu-id="c5a40-125">Rich-Text</span><span class="sxs-lookup"><span data-stu-id="c5a40-125">Rich text</span></span>                                        | <span data-ttu-id="c5a40-126">Absatztext.</span><span class="sxs-lookup"><span data-stu-id="c5a40-126">Paragraph text.</span></span> <span data-ttu-id="c5a40-127">Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung.</span><span class="sxs-lookup"><span data-stu-id="c5a40-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="c5a40-128">Benutzerdefinierter Klassenname</span><span class="sxs-lookup"><span data-stu-id="c5a40-128">Custom class name</span></span> | <span data-ttu-id="c5a40-129">Ein Cascading Style Sheets ( CSS) Klassenname</span><span class="sxs-lookup"><span data-stu-id="c5a40-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="c5a40-130">Der Name einer benutzerspezifischen CSS Klasse, die ein Entwickler zum Formatieren dieses Moduls bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c5a40-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="c5a40-131">Der Klassenname sollte im Theme Pack definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5a40-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="c5a40-132">Schriftgröße</span><span class="sxs-lookup"><span data-stu-id="c5a40-132">Font size</span></span>         | <span data-ttu-id="c5a40-133">**Klein**, **Mittel**, **Groß** oder **Sehr groß**</span><span class="sxs-lookup"><span data-stu-id="c5a40-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="c5a40-134">Die Schriftgröße des aktuellen Inhalts.</span><span class="sxs-lookup"><span data-stu-id="c5a40-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="c5a40-135">Hinzufügen eines Textblockmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="c5a40-135">Add a text block module to a page</span></span>

<span data-ttu-id="c5a40-136">Um ein Textblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="c5a40-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c5a40-137">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c5a40-138">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die **Inhaltvorlage** ein und wählen OK.</span><span class="sxs-lookup"><span data-stu-id="c5a40-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="c5a40-139">Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c5a40-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c5a40-140">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c5a40-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c5a40-141">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c5a40-142">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c5a40-143">In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Inhalt-Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="c5a40-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="c5a40-144">Unter **Seitenname** geben Sie **Inhalt-Seite** ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c5a40-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c5a40-145">Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c5a40-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c5a40-146">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c5a40-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c5a40-147">Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="c5a40-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="c5a40-148">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c5a40-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c5a40-149">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Textblock** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c5a40-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="c5a40-150">Fügen Sie im Eigenschaftenbereich des Textblockmoduls Text zum Feld **Rich Text** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c5a40-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="c5a40-151">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="c5a40-152">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c5a40-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5a40-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5a40-153">Additional resources</span></span>

[<span data-ttu-id="c5a40-154">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="c5a40-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c5a40-155">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="c5a40-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="c5a40-156">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="c5a40-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="c5a40-157">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="c5a40-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c5a40-158">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="c5a40-158">Video player module</span></span>](add-video-player.md)


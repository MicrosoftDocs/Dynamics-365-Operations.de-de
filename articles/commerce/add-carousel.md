---
title: Karussellmodul
description: Dieses Thema behandelt Karussellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797886"
---
# <a name="carousel-module"></a><span data-ttu-id="d6bf1-103">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="d6bf1-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6bf1-104">Dieses Thema behandelt Karussellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d6bf1-105">Ein Karussellmodul wird verwendet, um mehrere Werbeartikel (einschließlich Rich-Bilder) in ein rotierenden Karussellbanner einzusetzen, den Debitoren durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="d6bf1-106">So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="d6bf1-107">Sie können Inhaltsblockmodule innerhalb eines Karussellmoduls hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="d6bf1-108">Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="d6bf1-109">Beispiele für Containermodulen in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="d6bf1-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="d6bf1-110">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="d6bf1-111">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="d6bf1-112">Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="d6bf1-113">Das folgende Bild zeigt ein Beispiel eines Karussellmoduls, das auf einer Homepage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="d6bf1-114">Dieses Karussellmodul enthält mehrere Inhaltsblockelemente.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-114">This carousel module contains multiple content block items.</span></span>

![Beispiel eines Karussell-Moduls](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="d6bf1-116">Karussellmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6bf1-116">Carousel module properties</span></span>

| <span data-ttu-id="d6bf1-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="d6bf1-117">Property name</span></span>             | <span data-ttu-id="d6bf1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d6bf1-118">Value</span></span>                 | <span data-ttu-id="d6bf1-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6bf1-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="d6bf1-120">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d6bf1-120">Autoplay</span></span>                  | <span data-ttu-id="d6bf1-121">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="d6bf1-121">**True** or **False**</span></span> | <span data-ttu-id="d6bf1-122">Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="d6bf1-123">Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="d6bf1-124">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="d6bf1-124">Slide transition interval</span></span> | <span data-ttu-id="d6bf1-125">Ein Wert in Sekunden</span><span class="sxs-lookup"><span data-stu-id="d6bf1-125">A value in seconds</span></span>    | <span data-ttu-id="d6bf1-126">Das Intervall für Übergänge zwischen Artikeln.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="d6bf1-127">Übergangstyp</span><span class="sxs-lookup"><span data-stu-id="d6bf1-127">Transition type</span></span>           | <span data-ttu-id="d6bf1-128">**Anzeigen** oder **Ausblenden**</span><span class="sxs-lookup"><span data-stu-id="d6bf1-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="d6bf1-129">Der Übergangseffekt zwischen Elementen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-129">The transition effect between items.</span></span> |
| <span data-ttu-id="d6bf1-130">Karussellflipper ausblenden</span><span class="sxs-lookup"><span data-stu-id="d6bf1-130">Hide carousel flipper</span></span>     | <span data-ttu-id="d6bf1-131">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="d6bf1-131">**True** or **False**</span></span> | <span data-ttu-id="d6bf1-132">Wenn der Wert auf **Wahr** gesetzt ist, sind der Karussellflipper und die Sequenzanzeige ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="d6bf1-133">Karussell ablehnen zulassen</span><span class="sxs-lookup"><span data-stu-id="d6bf1-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="d6bf1-134">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="d6bf1-134">**True** or **False**</span></span> | <span data-ttu-id="d6bf1-135">Wenn der Wert auf **True** gesetzt wird, können Benutzer das Karussell ablehnen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="d6bf1-136">Ein Karussellmodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d6bf1-136">Add a carousel module to a page</span></span>

<span data-ttu-id="d6bf1-137">Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d6bf1-138">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d6bf1-139">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Karussellvorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bf1-140">Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="d6bf1-141">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="d6bf1-142">Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="d6bf1-143">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="d6bf1-144">Stellen Sie im rechten Bereich den Wert **Breite** auf **Bildschirm füllen** ein.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="d6bf1-145">Fügen Sie unter **Seitengliederung** dem Karussellmodul ein Werbebanner-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="d6bf1-146">Fügen Sie dem Karussellmodul ein Inhaltsblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="d6bf1-147">Legen Sie die Eigenschaften des Inhaltsblockmoduls fest, indem Sie **Überschrift**, **Verknüpfung**, **Layout** und andere Eigenschaften bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="d6bf1-148">Fügen Sie ein weiteres Inhaltsblockmodul hinzu und konfigurieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="d6bf1-149">Legen Sie nach Bedarf weitere Eigenschaften für das Karussellmodul fest.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="d6bf1-150">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d6bf1-151">Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="d6bf1-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="d6bf1-152">Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="d6bf1-153">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d6bf1-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6bf1-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d6bf1-154">Additional resources</span></span>

[<span data-ttu-id="d6bf1-155">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="d6bf1-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d6bf1-156">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="d6bf1-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="d6bf1-157">Textblockmodul</span><span class="sxs-lookup"><span data-stu-id="d6bf1-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d6bf1-158">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="d6bf1-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="d6bf1-159">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="d6bf1-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
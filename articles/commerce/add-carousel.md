---
title: Karussellmodul
description: Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 35aaf35419a8c5b83b2a3e1136a02200bf347c6b
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411295"
---
# <a name="carousel-module"></a><span data-ttu-id="a5054-103">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="a5054-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a5054-104">Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a5054-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a5054-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a5054-105">Overview</span></span>

<span data-ttu-id="a5054-106">Ein Karussellmodul wird verwendet, um mehrere Werbeartikel (einschließlich Rich-Bilder) in ein rotierenden Karussellbanner einzusetzen, den Debitoren durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="a5054-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="a5054-107">So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a5054-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="a5054-108">Sie können Inhaltsblockmodule innerhalb eines Karussellmoduls hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a5054-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="a5054-109">Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5054-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="a5054-110">Beispiele für Containermodulen in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="a5054-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="a5054-111">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5054-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="a5054-112">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5054-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="a5054-113">Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.</span><span class="sxs-lookup"><span data-stu-id="a5054-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="a5054-114">Das folgende Bild zeigt ein Beispiel eines Karussellmoduls, das auf einer Homepage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5054-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="a5054-115">Dieses Karussellmodul enthält mehrere Inhaltsblockelemente.</span><span class="sxs-lookup"><span data-stu-id="a5054-115">This carousel module contains multiple content block items.</span></span>

![Beispiel eines Karussell-Moduls](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="a5054-117">Karussellmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5054-117">Carousel module properties</span></span>

| <span data-ttu-id="a5054-118">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="a5054-118">Property name</span></span>             | <span data-ttu-id="a5054-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a5054-119">Value</span></span>                 | <span data-ttu-id="a5054-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5054-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="a5054-121">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="a5054-121">Autoplay</span></span>                  | <span data-ttu-id="a5054-122">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="a5054-122">**True** or **False**</span></span> | <span data-ttu-id="a5054-123">Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch.</span><span class="sxs-lookup"><span data-stu-id="a5054-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="a5054-124">Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen.</span><span class="sxs-lookup"><span data-stu-id="a5054-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="a5054-125">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="a5054-125">Slide transition interval</span></span> | <span data-ttu-id="a5054-126">Ein Wert in Sekunden</span><span class="sxs-lookup"><span data-stu-id="a5054-126">A value in seconds</span></span>    | <span data-ttu-id="a5054-127">Das Intervall für Übergänge zwischen Artikeln.</span><span class="sxs-lookup"><span data-stu-id="a5054-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="a5054-128">Übergangstyp</span><span class="sxs-lookup"><span data-stu-id="a5054-128">Transition type</span></span>           | <span data-ttu-id="a5054-129">**Anzeigen** oder **Ausblenden**</span><span class="sxs-lookup"><span data-stu-id="a5054-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="a5054-130">Der Übergangseffekt zwischen Elementen.</span><span class="sxs-lookup"><span data-stu-id="a5054-130">The transition effect between items.</span></span> |
| <span data-ttu-id="a5054-131">Karussellflipper ausblenden</span><span class="sxs-lookup"><span data-stu-id="a5054-131">Hide carousel flipper</span></span>     | <span data-ttu-id="a5054-132">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="a5054-132">**True** or **False**</span></span> | <span data-ttu-id="a5054-133">Wenn der Wert auf **Wahr** gesetzt ist, sind der Karussellflipper und die Sequenzanzeige ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="a5054-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="a5054-134">Karussell ablehnen zulassen</span><span class="sxs-lookup"><span data-stu-id="a5054-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="a5054-135">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="a5054-135">**True** or **False**</span></span> | <span data-ttu-id="a5054-136">Wenn der Wert auf **True** gesetzt wird, können Benutzer das Karussell ablehnen.</span><span class="sxs-lookup"><span data-stu-id="a5054-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="a5054-137">Ein Karussellmodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a5054-137">Add a carousel module to a page</span></span>

<span data-ttu-id="a5054-138">Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="a5054-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a5054-139">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a5054-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="a5054-140">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Karussellvorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5054-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a5054-141">Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5054-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="a5054-142">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a5054-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="a5054-143">Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.</span><span class="sxs-lookup"><span data-stu-id="a5054-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="a5054-144">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5054-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="a5054-145">Stellen Sie im rechten Bereich den Wert **Breite** auf **Bildschirm füllen** ein.</span><span class="sxs-lookup"><span data-stu-id="a5054-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="a5054-146">Fügen Sie unter **Seitengliederung** dem Karussellmodul ein Werbebanner-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5054-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="a5054-147">Fügen Sie dem Karussellmodul ein Inhaltsblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5054-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="a5054-148">Legen Sie die Eigenschaften des Inhaltsblockmoduls fest, indem Sie **Überschrift**, **Verknüpfung**, **Layout** und andere Eigenschaften bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a5054-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="a5054-149">Fügen Sie ein weiteres Inhaltsblockmodul hinzu und konfigurieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="a5054-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="a5054-150">Legen Sie nach Bedarf weitere Eigenschaften für das Karussellmodul fest.</span><span class="sxs-lookup"><span data-stu-id="a5054-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="a5054-151">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5054-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="a5054-152">Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="a5054-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="a5054-153">Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="a5054-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="a5054-154">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a5054-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5054-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a5054-155">Additional resources</span></span>

[<span data-ttu-id="a5054-156">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="a5054-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a5054-157">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="a5054-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="a5054-158">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="a5054-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a5054-159">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="a5054-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="a5054-160">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="a5054-160">Video player module</span></span>](add-video-player.md)

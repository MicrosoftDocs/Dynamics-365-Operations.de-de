---
title: Karussellmodul
description: Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269727"
---
# <a name="carousel-module"></a><span data-ttu-id="106ef-103">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="106ef-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="106ef-104">Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="106ef-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="106ef-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="106ef-105">Overview</span></span>

<span data-ttu-id="106ef-106">Ein Karussellmodul wird verwendet, um mehrere Werbeartikel (einschließlich Rich-Bilder) in ein rotierenden Karussellbanner einzusetzen, den Debitoren durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="106ef-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="106ef-107">So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="106ef-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="106ef-108">Sie können Inhaltsblockmodule innerhalb eines Karussellmoduls hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="106ef-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="106ef-109">Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="106ef-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="106ef-110">Beispiele für Containermodulen in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="106ef-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="106ef-111">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="106ef-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="106ef-112">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="106ef-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="106ef-113">Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.</span><span class="sxs-lookup"><span data-stu-id="106ef-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="106ef-114">Karussellmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="106ef-114">Carousel module properties</span></span>

| <span data-ttu-id="106ef-115">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="106ef-115">Property name</span></span>             | <span data-ttu-id="106ef-116">Wert</span><span class="sxs-lookup"><span data-stu-id="106ef-116">Value</span></span>                 | <span data-ttu-id="106ef-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="106ef-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="106ef-118">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="106ef-118">Autoplay</span></span>                  | <span data-ttu-id="106ef-119">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="106ef-119">**True** or **False**</span></span> | <span data-ttu-id="106ef-120">Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch.</span><span class="sxs-lookup"><span data-stu-id="106ef-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="106ef-121">Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen.</span><span class="sxs-lookup"><span data-stu-id="106ef-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="106ef-122">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="106ef-122">Slide transition interval</span></span> | <span data-ttu-id="106ef-123">Ein Wert in Sekunden</span><span class="sxs-lookup"><span data-stu-id="106ef-123">A value in seconds</span></span>    | <span data-ttu-id="106ef-124">Das Intervall für Übergänge zwischen Artikeln.</span><span class="sxs-lookup"><span data-stu-id="106ef-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="106ef-125">Übergangstyp</span><span class="sxs-lookup"><span data-stu-id="106ef-125">Transition type</span></span>           | <span data-ttu-id="106ef-126">**Anzeigen** oder **Ausblenden**</span><span class="sxs-lookup"><span data-stu-id="106ef-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="106ef-127">Der Übergangseffekt zwischen Elementen.</span><span class="sxs-lookup"><span data-stu-id="106ef-127">The transition effect between items.</span></span> |
| <span data-ttu-id="106ef-128">Karussellflipper ausblenden</span><span class="sxs-lookup"><span data-stu-id="106ef-128">Hide carousel flipper</span></span>     | <span data-ttu-id="106ef-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="106ef-129">**True** or **False**</span></span> | <span data-ttu-id="106ef-130">Wenn der Wert auf **Wahr** gesetzt ist, sind der Karussellflipper und die Sequenzanzeige ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="106ef-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="106ef-131">Karussell ablehnen zulassen</span><span class="sxs-lookup"><span data-stu-id="106ef-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="106ef-132">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="106ef-132">**True** or **False**</span></span> | <span data-ttu-id="106ef-133">Wenn der Wert auf **True** gesetzt wird, können Benutzer das Karussell ablehnen.</span><span class="sxs-lookup"><span data-stu-id="106ef-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="106ef-134">Ein Karussellmodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="106ef-134">Add a carousel module to a page</span></span>

<span data-ttu-id="106ef-135">Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="106ef-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="106ef-136">Wählen Sie **Neu** aus, um eine Seitenvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="106ef-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="106ef-137">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Karussellvorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="106ef-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="106ef-138">Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.</span><span class="sxs-lookup"><span data-stu-id="106ef-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="106ef-139">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="106ef-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="106ef-140">Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.</span><span class="sxs-lookup"><span data-stu-id="106ef-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="106ef-141">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="106ef-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="106ef-142">Stellen Sie im rechten Bereich den Wert **Breite** auf **Bildschirm füllen** ein.</span><span class="sxs-lookup"><span data-stu-id="106ef-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="106ef-143">Fügen Sie unter **Seitengliederung** dem Karussellmodul ein Werbebanner-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="106ef-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="106ef-144">Fügen Sie dem Karussellmodul ein Inhaltsblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="106ef-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="106ef-145">Legen Sie die Eigenschaften des Inhaltsblockmoduls fest, indem Sie **Überschrift**, **Verknüpfung**, **Layout** und andere Eigenschaften bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="106ef-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="106ef-146">Fügen Sie ein weiteres Inhaltsblockmodul hinzu und konfigurieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="106ef-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="106ef-147">Legen Sie nach Bedarf weitere Eigenschaften für das Karussellmodul fest.</span><span class="sxs-lookup"><span data-stu-id="106ef-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="106ef-148">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="106ef-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="106ef-149">Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="106ef-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="106ef-150">Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="106ef-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="106ef-151">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="106ef-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="106ef-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="106ef-152">Additional resources</span></span>

[<span data-ttu-id="106ef-153">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="106ef-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="106ef-154">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="106ef-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="106ef-155">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="106ef-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="106ef-156">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="106ef-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="106ef-157">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="106ef-157">Video player module</span></span>](add-video-player.md)

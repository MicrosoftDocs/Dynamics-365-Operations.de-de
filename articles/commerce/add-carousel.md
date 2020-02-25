---
title: Karussellmodul
description: Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025780"
---
# <a name="carousel-module"></a><span data-ttu-id="7b3c1-103">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="7b3c1-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7b3c1-104">Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7b3c1-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7b3c1-105">Overview</span></span>

<span data-ttu-id="7b3c1-106">Ein Karussellmodul wird verwendet, um mehrere Werbeartikel (einschließlich Rich-Bilder) in ein rotierenden Karussellbanner einzusetzen, den Debitoren durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="7b3c1-107">So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="7b3c1-108">Sie können Inhaltsblockmodule innerhalb eines Karussellmoduls hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="7b3c1-109">Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="7b3c1-110">Beispiele für Containermodulen in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="7b3c1-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="7b3c1-111">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="7b3c1-112">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="7b3c1-113">Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="7b3c1-114">Karussellmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b3c1-114">Carousel module properties</span></span>

| <span data-ttu-id="7b3c1-115">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="7b3c1-115">Property name</span></span>             | <span data-ttu-id="7b3c1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7b3c1-116">Value</span></span>                 | <span data-ttu-id="7b3c1-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b3c1-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="7b3c1-118">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="7b3c1-118">Autoplay</span></span>                  | <span data-ttu-id="7b3c1-119">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="7b3c1-119">**True** or **False**</span></span> | <span data-ttu-id="7b3c1-120">Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="7b3c1-121">Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="7b3c1-122">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="7b3c1-122">Slide transition interval</span></span> | <span data-ttu-id="7b3c1-123">Ein Wert in Sekunden</span><span class="sxs-lookup"><span data-stu-id="7b3c1-123">A value in seconds</span></span>    | <span data-ttu-id="7b3c1-124">Das Intervall für Übergänge zwischen Artikeln.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="7b3c1-125">Übergangstyp</span><span class="sxs-lookup"><span data-stu-id="7b3c1-125">Transition type</span></span>           | <span data-ttu-id="7b3c1-126">**Anzeigen** oder **Ausblenden**</span><span class="sxs-lookup"><span data-stu-id="7b3c1-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="7b3c1-127">Der Übergangseffekt zwischen Elementen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-127">The transition effect between items.</span></span> |
| <span data-ttu-id="7b3c1-128">Karussellflipper ausblenden</span><span class="sxs-lookup"><span data-stu-id="7b3c1-128">Hide carousel flipper</span></span>     | <span data-ttu-id="7b3c1-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="7b3c1-129">**True** or **False**</span></span> | <span data-ttu-id="7b3c1-130">Wenn der Wert auf **Wahr** gesetzt ist, sind der Karussellflipper und die Sequenzanzeige ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="7b3c1-131">Karussell ablehnen zulassen</span><span class="sxs-lookup"><span data-stu-id="7b3c1-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="7b3c1-132">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="7b3c1-132">**True** or **False**</span></span> | <span data-ttu-id="7b3c1-133">Wenn der Wert auf **True** gesetzt wird, können Benutzer das Karussell ablehnen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="7b3c1-134">Ein Karussellmodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="7b3c1-134">Add a carousel module to a page</span></span>

<span data-ttu-id="7b3c1-135">Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7b3c1-136">Erstellen Sie eine Seitenvorlage, die mit **Karussellvorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="7b3c1-137">Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="7b3c1-138">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="7b3c1-139">Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="7b3c1-140">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="7b3c1-141">Stellen Sie im rechten Bereich den Wert **Breite** auf **Bildschirm füllen** ein.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="7b3c1-142">Fügen Sie unter **Seitengliederung** dem Karussellmodul ein Werbebanner-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="7b3c1-143">Fügen Sie dem Karussellmodul ein Inhaltsblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="7b3c1-144">Legen Sie die Eigenschaften des Inhaltsblockmoduls fest, indem Sie **Überschrift**, **Verknüpfung**, **Layout** und andere Eigenschaften bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="7b3c1-145">Fügen Sie ein weiteres Inhaltsblockmodul hinzu und konfigurieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="7b3c1-146">Legen Sie nach Bedarf weitere Eigenschaften für das Karussellmodul fest.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="7b3c1-147">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-147">Save and preview the page.</span></span> <span data-ttu-id="7b3c1-148">Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="7b3c1-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="7b3c1-149">Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="7b3c1-150">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="7b3c1-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b3c1-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7b3c1-151">Additional resources</span></span>

[<span data-ttu-id="7b3c1-152">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="7b3c1-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7b3c1-153">Werbebanner-Modul</span><span class="sxs-lookup"><span data-stu-id="7b3c1-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="7b3c1-154">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="7b3c1-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="7b3c1-155">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="7b3c1-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="7b3c1-156">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="7b3c1-156">Video player module</span></span>](add-video-player.md)

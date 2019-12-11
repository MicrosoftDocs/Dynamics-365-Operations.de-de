---
title: Karussellmodul
description: Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785236"
---
# <a name="carousel-module"></a><span data-ttu-id="6d2af-103">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="6d2af-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6d2af-104">Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6d2af-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6d2af-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6d2af-105">Overview</span></span>

<span data-ttu-id="6d2af-106">Ein Karussellmodul wird verwendet, um mehrere Werbeartikel in ein Karussell einzusetzen, das Debitoren durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="6d2af-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="6d2af-107">Es handelt sich um einen spezielles Containermodul, das andere Module hostet.</span><span class="sxs-lookup"><span data-stu-id="6d2af-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="6d2af-108">So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="6d2af-109">Sie können Hero- und Funktionsmodule innerhalb eines Karussellmoduls hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="6d2af-110">Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d2af-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="6d2af-111">Beispiele für Containermodulen in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="6d2af-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="6d2af-112">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d2af-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="6d2af-113">Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d2af-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="6d2af-114">Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.</span><span class="sxs-lookup"><span data-stu-id="6d2af-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="6d2af-115">Karussellmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d2af-115">Carousel module properties</span></span>

| <span data-ttu-id="6d2af-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6d2af-116">Property name</span></span>             | <span data-ttu-id="6d2af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6d2af-117">Value</span></span>                                | <span data-ttu-id="6d2af-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d2af-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="6d2af-119">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="6d2af-119">Autoplay</span></span>                  | <span data-ttu-id="6d2af-120">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="6d2af-120">**True** or **False**</span></span>                | <span data-ttu-id="6d2af-121">Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch.</span><span class="sxs-lookup"><span data-stu-id="6d2af-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="6d2af-122">Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="6d2af-123">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="6d2af-123">Slide transition interval</span></span> | <span data-ttu-id="6d2af-124">Ein Wert in Sekunden</span><span class="sxs-lookup"><span data-stu-id="6d2af-124">A value in seconds</span></span>                   | <span data-ttu-id="6d2af-125">Das Intervall für Übergänge zwischen Artikeln.</span><span class="sxs-lookup"><span data-stu-id="6d2af-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="6d2af-126">Übergangsanimation</span><span class="sxs-lookup"><span data-stu-id="6d2af-126">Transition animation</span></span>      | <span data-ttu-id="6d2af-127">**Anzeigen** oder **Ausblenden**</span><span class="sxs-lookup"><span data-stu-id="6d2af-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="6d2af-128">Der Übergangseffekt</span><span class="sxs-lookup"><span data-stu-id="6d2af-128">The transition effect.</span></span> |
| <span data-ttu-id="6d2af-129">Breite</span><span class="sxs-lookup"><span data-stu-id="6d2af-129">Width</span></span>                     | <span data-ttu-id="6d2af-130">**Eingepasster Container** oder **Bildschirm ausfüllen**</span><span class="sxs-lookup"><span data-stu-id="6d2af-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="6d2af-131">Wenn der Wert auf **Eingepasster Container** festgelegt ist, werden die Module im Karussell auf die Breite des Karussells beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6d2af-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="6d2af-132">Wenn der Wert auf **Bildschirm ausfüllen** gesetzt wird, wird das Karussell nicht auf die Karussellbreite eingeschränkt und können den Bildschirm ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="6d2af-133">Sie können den Wert ändern, um das gewünschte Layout zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="6d2af-134">Ein Karussellmodul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="6d2af-134">Add a carousel module to a page</span></span>

<span data-ttu-id="6d2af-135">Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6d2af-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6d2af-136">Erstellen Sie eine Seitenvorlage, die mit **Karussellvorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="6d2af-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="6d2af-137">Im **Haupt-** Slot der Standardseite fügen Sie ein Karussellmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d2af-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="6d2af-138">Hinzufügen eines Heromoduls dem Karussellmodul.</span><span class="sxs-lookup"><span data-stu-id="6d2af-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="6d2af-139">Hinzufügen eines Funktionsmoduls dem Karussellmodul.</span><span class="sxs-lookup"><span data-stu-id="6d2af-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="6d2af-140">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="6d2af-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="6d2af-141">Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.</span><span class="sxs-lookup"><span data-stu-id="6d2af-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="6d2af-142">Im **Haupt-** Slot der neuen Seite fügen Sie ein Karussellmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d2af-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="6d2af-143">Hier können Sie die Eigenschaft **Breite** des Karussellmoduls auf **Bildschirm ausfüllen** festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="6d2af-144">Hier können Sie die Eigenschaft **Übergangsanimation** auf **Folie** festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="6d2af-145">Hinzufügen eines Heromoduls dem Karussellmodul.</span><span class="sxs-lookup"><span data-stu-id="6d2af-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="6d2af-146">Im Heromodul fügen Sie ein Bild und eine Kurzbeschreibung hinzu und wählen Sie dann **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6d2af-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="6d2af-147">Hinzufügen eines Funktionsmoduls dem Karussellmodul.</span><span class="sxs-lookup"><span data-stu-id="6d2af-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="6d2af-148">Im Funktionsmodul fügen Sie ein Bild, eine Überschrift und einen Absatz des Texts hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d2af-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="6d2af-149">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-149">Save and preview the page.</span></span> <span data-ttu-id="6d2af-150">Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="6d2af-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="6d2af-151">Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="6d2af-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="6d2af-152">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="6d2af-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d2af-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d2af-153">Additional resources</span></span>

[<span data-ttu-id="6d2af-154">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="6d2af-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6d2af-155">Warnmmodul</span><span class="sxs-lookup"><span data-stu-id="6d2af-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="6d2af-156">Umfangreiches Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="6d2af-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6d2af-157">Inhaltsplatzierungsmodul</span><span class="sxs-lookup"><span data-stu-id="6d2af-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="6d2af-158">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="6d2af-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="6d2af-159">Hero-Modul</span><span class="sxs-lookup"><span data-stu-id="6d2af-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="6d2af-160">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="6d2af-160">Video player module</span></span>](add-video-player.md)

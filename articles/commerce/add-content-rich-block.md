---
title: Umfangreiches Inhaltsblockmodul
description: Dieses Thema enthält umfangreiche Inhaltsblockmodule und beschreibt, wie sie den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785420"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="ba5a7-103">Umfangreiches Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ba5a7-104">Dieses Thema enthält umfangreiche Inhaltsblockmodule und beschreibt, wie sie den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ba5a7-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ba5a7-105">Overview</span></span>

<span data-ttu-id="ba5a7-106">Ein umfangreiches Inhaltsblockmodul ist ein spezieller Container, der eines oder mehrere umfangreichen Inhaltsblockmodule aufnimmt.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="ba5a7-107">Umfangreiche Inhaltsblockmodule werden für Textinhalt auf einer Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="ba5a7-108">Dieser Inhalt kann entweder zu Informations- oder Werbezwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="ba5a7-109">Umfangreiche Inhaltsblockmodule werden von Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="ba5a7-110">Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="ba5a7-111">Beispiele für umfangreiche Inhaltsblockmodule in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="ba5a7-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="ba5a7-112">Umfangreiche Inhaltsblockmodule können folgendermaßen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ba5a7-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="ba5a7-113">Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="ba5a7-114">Für Informationszwecke auf einer beliebigen Seite.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-114">For informational purposes on any page.</span></span> <span data-ttu-id="ba5a7-115">So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="ba5a7-116">Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="ba5a7-117">(beispielsweise „kostenloser Versand für Aufträge über $50“).</span><span class="sxs-lookup"><span data-stu-id="ba5a7-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="ba5a7-118">Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).</span><span class="sxs-lookup"><span data-stu-id="ba5a7-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="ba5a7-119">Umfangreiche Inhaltsblockmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba5a7-119">Content rich block module properties</span></span>

| <span data-ttu-id="ba5a7-120">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="ba5a7-120">Property name</span></span>     | <span data-ttu-id="ba5a7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ba5a7-121">Value</span></span>                                 | <span data-ttu-id="ba5a7-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ba5a7-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="ba5a7-123">Spaltenanzahl</span><span class="sxs-lookup"><span data-stu-id="ba5a7-123">Number of columns</span></span> | <span data-ttu-id="ba5a7-124">Eine Nummer aus **1** bis **4**</span><span class="sxs-lookup"><span data-stu-id="ba5a7-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="ba5a7-125">Die Anzahl der Spalten in umfangreichen Inhaltsblockmodulen</span><span class="sxs-lookup"><span data-stu-id="ba5a7-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="ba5a7-126">Es kann bis zu vier Spalten geben.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="ba5a7-127">Breite</span><span class="sxs-lookup"><span data-stu-id="ba5a7-127">Width</span></span>             | <span data-ttu-id="ba5a7-128">**Container ausfüllen** oder **Bildschirm ausfüllen**</span><span class="sxs-lookup"><span data-stu-id="ba5a7-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="ba5a7-129">Wenn der Wert auf **Container ausfüllen** festgelegt ist, wird der Container auf die Breite des Containers beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="ba5a7-130">Wenn der Wert auf **Bildschirm ausfüllen** gesetzt wird, werden die Elemente nicht auf die Containerbreite eingeschränkt und können den Bildschirm ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="ba5a7-131">Sie können den Wert ändern, um das gewünschte Layout zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="ba5a7-132">Umfangreiche Inhaltsblockelementmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba5a7-132">Content rich block item module properties</span></span>

| <span data-ttu-id="ba5a7-133">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="ba5a7-133">Property name</span></span> | <span data-ttu-id="ba5a7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ba5a7-134">Value</span></span>          | <span data-ttu-id="ba5a7-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba5a7-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="ba5a7-136">Absatz</span><span class="sxs-lookup"><span data-stu-id="ba5a7-136">Paragraph</span></span>     | <span data-ttu-id="ba5a7-137">Absatztext</span><span class="sxs-lookup"><span data-stu-id="ba5a7-137">Paragraph text</span></span> | <span data-ttu-id="ba5a7-138">Der Text, der jeden umfangreichen Inhaltsblockmoduls begleiten soll.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="ba5a7-139">Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="ba5a7-140">Hinzufügen eines umfangreichen Inhaltsblockmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="ba5a7-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="ba5a7-141">Um ein umfangreiches Inhaltsblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ba5a7-142">Erstellen Sie eine Seitenvorlage, die mit **Inhaltvorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="ba5a7-143">Im **Haupt-** Slot der Standardseite fügen Sie ein umfangreiches Inhaltsblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="ba5a7-144">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="ba5a7-145">Verwenden Sie die Inhaltvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Inhaltseite** hat.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="ba5a7-146">Im **Haupt-** Slot der neuen Seite fügen Sie ein umfangreiches Inhaltsblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="ba5a7-147">In den Eigenschaften des umfangreichen Inhaltsblockmoduls legen Sie die Zahl der Spalten auf **2** fest.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="ba5a7-148">Im umfangreichen Inhaltsblockmodul wählen Sie **Modul hinzufügen** und fügen ein umfangreiches Inhaltsblockmodulelement hinzu (zum Beispiel **item1**).</span><span class="sxs-lookup"><span data-stu-id="ba5a7-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="ba5a7-149">In einem neuen umfangreiches Inhaltsblockmodul fügen Sie den Absatztext hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="ba5a7-150">Im umfangreichen Inhaltsblockmodul wählen Sie **Modul hinzufügen** und fügen ein umfangreiches Inhaltsblockmodulelement hinzu (zum Beispiel **item2**).</span><span class="sxs-lookup"><span data-stu-id="ba5a7-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="ba5a7-151">In einem neuen umfangreiches Inhaltsblockmodul fügen Sie den Absatztext hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="ba5a7-152">Seite speichern und Änderungen in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="ba5a7-153">Sie sollten zwei Rich-Text-Textblöcke in einer Zwei-Spaltenansicht sehen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="ba5a7-154">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="ba5a7-155">Wenn Sie einen dritten umfangreichen Inhaltsblock hinzufügen, wird er unter den zwei Elementen angeordnet, die Sie zuvor hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="ba5a7-156">Wenn Sie die Anzahl und Artikel im Container ändern, können Sie unterschiedliche Layouts für Textinhalt erreichen.</span><span class="sxs-lookup"><span data-stu-id="ba5a7-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba5a7-157">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba5a7-157">Additional resources</span></span>

[<span data-ttu-id="ba5a7-158">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="ba5a7-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ba5a7-159">Warnmmodul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="ba5a7-160">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="ba5a7-161">Inhaltsplatzierungsmodul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="ba5a7-162">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="ba5a7-163">Hero-Modul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="ba5a7-164">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="ba5a7-164">Video player module</span></span>](add-video-player.md)


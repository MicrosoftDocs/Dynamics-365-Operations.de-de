---
title: Textblock-Modul
description: Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025596"
---
# <a name="text-block-module"></a><span data-ttu-id="2a017-103">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="2a017-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2a017-104">Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2a017-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2a017-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2a017-105">Overview</span></span>

<span data-ttu-id="2a017-106">Ein Textblockmodul ist ein Modul, mit dem Textinhalte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2a017-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="2a017-107">Dieser Inhalt kann entweder zu Informations- oder Werbezwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a017-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="2a017-108">Textblock-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="2a017-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="2a017-109">Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.</span><span class="sxs-lookup"><span data-stu-id="2a017-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="2a017-110">Beispiele für Textblockmodule in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="2a017-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="2a017-111">Textblockmodule können folgendermaßen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="2a017-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="2a017-112">Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="2a017-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="2a017-113">Für Informationszwecke auf einer beliebigen Seite.</span><span class="sxs-lookup"><span data-stu-id="2a017-113">For informational purposes on any page.</span></span> <span data-ttu-id="2a017-114">So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2a017-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="2a017-115">Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2a017-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="2a017-116">(beispielsweise „kostenloser Versand für Aufträge über $50“).</span><span class="sxs-lookup"><span data-stu-id="2a017-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="2a017-117">Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).</span><span class="sxs-lookup"><span data-stu-id="2a017-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="2a017-118">Eigenschaften des Textblock-Moduls</span><span class="sxs-lookup"><span data-stu-id="2a017-118">Text block module properties</span></span>

| <span data-ttu-id="2a017-119">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2a017-119">Property name</span></span>     | <span data-ttu-id="2a017-120">Value</span><span class="sxs-lookup"><span data-stu-id="2a017-120">Value</span></span>                                            | <span data-ttu-id="2a017-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a017-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="2a017-122">Rich-Text</span><span class="sxs-lookup"><span data-stu-id="2a017-122">Rich text</span></span>         | <span data-ttu-id="2a017-123">Rich-Text</span><span class="sxs-lookup"><span data-stu-id="2a017-123">Rich text</span></span>                                        | <span data-ttu-id="2a017-124">Absatztext.</span><span class="sxs-lookup"><span data-stu-id="2a017-124">Paragraph text.</span></span> <span data-ttu-id="2a017-125">Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung.</span><span class="sxs-lookup"><span data-stu-id="2a017-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="2a017-126">Benutzerdefinierter Klassenname</span><span class="sxs-lookup"><span data-stu-id="2a017-126">Custom class name</span></span> | <span data-ttu-id="2a017-127">Ein Cascading Style Sheets ( CSS) Klassenname</span><span class="sxs-lookup"><span data-stu-id="2a017-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="2a017-128">Der Name einer benutzerspezifischen CSS Klasse, die ein Entwickler zum Formatieren dieses Moduls bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2a017-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="2a017-129">Der Klassenname sollte im Theme Pack definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a017-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="2a017-130">Schriftgröße</span><span class="sxs-lookup"><span data-stu-id="2a017-130">Font size</span></span>         | <span data-ttu-id="2a017-131">**Klein**, **Mittel**, **Groß** oder **Sehr groß**</span><span class="sxs-lookup"><span data-stu-id="2a017-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="2a017-132">Die Schriftgröße des aktuellen Inhalts.</span><span class="sxs-lookup"><span data-stu-id="2a017-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="2a017-133">Hinzufügen eines Textblockmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="2a017-133">Add a text block module to a page</span></span>

<span data-ttu-id="2a017-134">Um ein Textblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="2a017-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2a017-135">Erstellen Sie eine Seitenvorlage, die mit **Inhaltvorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="2a017-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="2a017-136">Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a017-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="2a017-137">Beenden Sie die Bearbeitung der Vorlage und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="2a017-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="2a017-138">Verwenden Sie die Inhaltvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Inhaltseite** hat.</span><span class="sxs-lookup"><span data-stu-id="2a017-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="2a017-139">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a017-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="2a017-140">Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="2a017-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2a017-141">Fügen Sie dem Containermodul ein Textblockmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a017-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="2a017-142">Fügen Sie im Eigenschaftenbereich des Textblockmoduls Text zum Feld **Rich Text** hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a017-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="2a017-143">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="2a017-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a017-144">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2a017-144">Additional resources</span></span>

[<span data-ttu-id="2a017-145">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="2a017-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2a017-146">Werbebanner-Modul</span><span class="sxs-lookup"><span data-stu-id="2a017-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2a017-147">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="2a017-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2a017-148">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="2a017-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2a017-149">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="2a017-149">Video player module</span></span>](add-video-player.md)


---
title: Hinzufügen eines Logos
description: In diesem Thema wird beschrieben, wie Sie ein Logo zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5fc0673dcdcc8b761089be2c2d201c8488128865
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025695"
---
# <a name="add-a-logo"></a><span data-ttu-id="57fb3-103">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="57fb3-103">Add a logo</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="57fb3-104">In diesem Thema wird beschrieben, wie Sie ein Logo zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57fb3-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57fb3-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="57fb3-105">Overview</span></span>

<span data-ttu-id="57fb3-106">Wenn Sie Ihre Site erstellen, ist eines der ersten Dinge, die Sie wahrscheinlich tun werden, das Hinzufügen Ihres Firmen- oder Markenlogos zum Header der Site.</span><span class="sxs-lookup"><span data-stu-id="57fb3-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="57fb3-107">Das Dynamics 365 Commerce-Online-Starter-Kit enthält ein Modul, das diese Aufgabe vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="57fb3-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="57fb3-108">Sie können ein Logo direkt zu einer Vorlage, einem Layout oder einer Seite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57fb3-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="57fb3-109">Auf diese Weise können Sie ganz einfach das Logo ändern, das auf bestimmten Seiten oder Seitengruppen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="57fb3-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="57fb3-110">In diesem Thema wird jedoch das häufigste Szenario behandelt, in dem Sie ein Headerfragment mit Ihrem Logo versehen, das auf allen Seiten Ihrer Website wiederverwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="57fb3-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="57fb3-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="57fb3-111">Prerequisites</span></span>

<span data-ttu-id="57fb3-112">Bevor Sie allen Seiten Ihrer Site ein Logo hinzufügen können, müssen Sie diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="57fb3-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="57fb3-113">Laden Sie Ihr Logo in die Medienbibliothek hoch.</span><span class="sxs-lookup"><span data-stu-id="57fb3-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="57fb3-114">Erstellen Sie ein Header-Fragment.</span><span class="sxs-lookup"><span data-stu-id="57fb3-114">Create a header fragment.</span></span> <span data-ttu-id="57fb3-115">Weitere Informationen zum Erstellen und Verwenden von Fragmenten finden Sie unter [Arbeiten mit Fragmenten](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="57fb3-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="57fb3-116">Fügen Sie das Headerfragment in die Vorlage ein, die die Seiten Ihrer Site für ihre Layout- und Moduloptionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="57fb3-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="57fb3-117">Weitere Informationen zu Vorlagen erhalten Sie unter [Arbeiten mit Vorlagen](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="57fb3-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="57fb3-118">Einem Headerfragment ein Logo hinzufügen</span><span class="sxs-lookup"><span data-stu-id="57fb3-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="57fb3-119">Gehen Sie folgendermaßen vor, um dem Headerfragment für Ihre Site ein Logo hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="57fb3-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="57fb3-120">Wählen Sie im linken Navigationsbereich **Seitenfragmente** aus.</span><span class="sxs-lookup"><span data-stu-id="57fb3-120">In the navigation pane on the left, select **Page Fragments**.</span></span>
1. <span data-ttu-id="57fb3-121">Wählen Sie das Headerfragment, das Sie eben erstellt haben, aus und dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="57fb3-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="57fb3-122">Erweitern Sie das Kopfmodul.</span><span class="sxs-lookup"><span data-stu-id="57fb3-122">Expand the header module.</span></span>
1. <span data-ttu-id="57fb3-123">Geben Sie im Eigenschaftenbereich für das Kopfzeilenmodul ein Bild und einen Link für das Logo ein.</span><span class="sxs-lookup"><span data-stu-id="57fb3-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="57fb3-124">Speichern Sie das Headerfragment, beenden Sie die Bearbeitung und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="57fb3-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="57fb3-125">Nachdem Sie das aktualisierte Headerfragment veröffentlicht haben, wird auf allen Websiteseiten, die die Vorlage mit dem Headerfragment verwenden, Ihr Logo angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57fb3-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57fb3-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57fb3-126">Additional resources</span></span>

[<span data-ttu-id="57fb3-127">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="57fb3-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="57fb3-128">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="57fb3-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="57fb3-129">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="57fb3-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="57fb3-130">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="57fb3-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="57fb3-131">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="57fb3-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="57fb3-132">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="57fb3-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="57fb3-133">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="57fb3-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


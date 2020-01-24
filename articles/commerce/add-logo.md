---
title: Hinzufügen eines Logos
description: In diesem Thema wird beschrieben, wie Sie ein Logo zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914619"
---
# <a name="add-a-logo"></a><span data-ttu-id="54a39-103">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="54a39-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="54a39-104">In diesem Thema wird beschrieben, wie Sie ein Logo zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="54a39-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="54a39-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="54a39-105">Overview</span></span>

<span data-ttu-id="54a39-106">Wenn Sie Ihre Site erstellen, ist eines der ersten Dinge, die Sie wahrscheinlich tun werden, das Hinzufügen Ihres Firmen- oder Markenlogos zum Header der Site.</span><span class="sxs-lookup"><span data-stu-id="54a39-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="54a39-107">Das Dynamics 365 Commerce-Online-Starter-Kit enthält ein Modul, das diese Aufgabe vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="54a39-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="54a39-108">Sie können ein Logo direkt zu einer Vorlage, einem Layout oder einer Seite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="54a39-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="54a39-109">Auf diese Weise können Sie ganz einfach das Logo ändern, das auf bestimmten Seiten oder Seitengruppen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="54a39-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="54a39-110">In diesem Thema wird jedoch das häufigste Szenario behandelt, in dem Sie ein Headerfragment mit Ihrem Logo versehen, das auf allen Seiten Ihrer Website wiederverwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="54a39-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="54a39-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="54a39-111">Prerequisites</span></span>

<span data-ttu-id="54a39-112">Bevor Sie allen Seiten Ihrer Site ein Logo hinzufügen können, müssen Sie diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="54a39-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="54a39-113">Laden Sie Ihr Logo in den Digital Asset Manager hoch, auf den Sie über die Seite **Anlagen** zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="54a39-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="54a39-114">Erstellen Sie ein Header-Fragment.</span><span class="sxs-lookup"><span data-stu-id="54a39-114">Create a header fragment.</span></span> <span data-ttu-id="54a39-115">Weitere Informationen zum Erstellen und Verwenden von Fragmenten finden Sie unter [Arbeiten mit Fragmenten](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="54a39-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="54a39-116">Fügen Sie das Headerfragment in die Vorlage ein, die die Seiten Ihrer Site für ihre Layout- und Moduloptionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="54a39-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="54a39-117">Weitere Informationen zu Vorlagen erhalten Sie unter [Arbeiten mit Vorlagen](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="54a39-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="54a39-118">Einem Headerfragment ein Logo hinzufügen</span><span class="sxs-lookup"><span data-stu-id="54a39-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="54a39-119">Gehen Sie folgendermaßen vor, um dem Headerfragment für Ihre Site ein Logo hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="54a39-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="54a39-120">Wählen Sie im Navigationsbereich links **Fragmente** und dann das von Ihnen erstellte Header-Fragment aus.</span><span class="sxs-lookup"><span data-stu-id="54a39-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="54a39-121">Wählen Sie **Auschecken** aus.</span><span class="sxs-lookup"><span data-stu-id="54a39-121">Select **Check out**.</span></span>
3. <span data-ttu-id="54a39-122">Erweitern Sie die Slots **Header** und **Logo**.</span><span class="sxs-lookup"><span data-stu-id="54a39-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="54a39-123">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den Slot **Logo** und dann **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54a39-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="54a39-124">Wählen Sie das Logomodul aus.</span><span class="sxs-lookup"><span data-stu-id="54a39-124">Select the logo module.</span></span>
6. <span data-ttu-id="54a39-125">Im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie das Logomodul so, dass es Ihr Logo anzeigt.</span><span class="sxs-lookup"><span data-stu-id="54a39-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="54a39-126">Speichern Sie das Kopffragment, laden Sie es hoch und veröffentlichen Sie es.</span><span class="sxs-lookup"><span data-stu-id="54a39-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="54a39-127">Nachdem Sie das aktualisierte Headerfragment veröffentlicht haben, wird auf allen Websiteseiten, die die Vorlage mit dem Headerfragment verwenden, Ihr Logo angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54a39-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54a39-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="54a39-128">Additional resources</span></span>

[<span data-ttu-id="54a39-129">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="54a39-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="54a39-130">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="54a39-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="54a39-131">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="54a39-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="54a39-132">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="54a39-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="54a39-133">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="54a39-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="54a39-134">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="54a39-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="54a39-135">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="54a39-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


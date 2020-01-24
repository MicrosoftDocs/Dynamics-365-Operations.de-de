---
title: Hinzufügen eines Urheberrechtshinweises
description: In diesem Thema wird beschrieben, wie eine Urheberrechts-Meldung der E-Comerce Website hinzugefügt wird.
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914569"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="a0861-103">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="a0861-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a0861-104">In diesem Thema wird beschrieben, wie eine Urheberrechts-Meldung der E-Comerce Website hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a0861-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a0861-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a0861-105">Prerequisites</span></span>

<span data-ttu-id="a0861-106">Bevor Sie einen Urheberrechtshinweis Ihrer Site hinzufügen können, müssen Sie die folgenden Artikel haben:</span><span class="sxs-lookup"><span data-stu-id="a0861-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="a0861-107">Eine Vorlage, die freigegebenesFußzeilenfragment enthält.</span><span class="sxs-lookup"><span data-stu-id="a0861-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="a0861-108">Eine Seite, die diese Vorlage verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0861-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="a0861-109">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="a0861-109">Add a copyright notice</span></span>

<span data-ttu-id="a0861-110">Um einen Urheberrechtshinweis am Fuß jeder Seite hinzuzufügen die eine bestimmte Vorlage verwendet, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="a0861-111">Wechseln Sie zu **Fragmente**, und wählen Sie dann **Neues Seiten-Fragment** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="a0861-112">Wählen Sie im Dialogfeld **Fußzeile** das Modul und geben Sie dem Fragment einen Namen.</span><span class="sxs-lookup"><span data-stu-id="a0861-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="a0861-113">Geben Sie zum Beispiel **Fußzeile-Urheberrecht** ein.</span><span class="sxs-lookup"><span data-stu-id="a0861-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="a0861-114">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0861-114">Select **OK**.</span></span>
1. <span data-ttu-id="a0861-115">Im Navigationsbereich wählen Sie die Ellipsis-Schaltfläche (**...**) neben der **Fußzeile** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a0861-116">Wählen Sie im Dialogfeld **Fußzeilenkategorie** und **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="a0861-117">Im Navigationsbereich wählen Sie die Ellipsis-Schaltfläche (...) neben der **Fußzeilenkategorie** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a0861-118">Wählen Sie im Dialogfeld **Umfangreiches Inhaltsblockmodul** und **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="a0861-119">Im Navigationsbereich wählen Sie **Umfangreiches Inhaltsblockmodul** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="a0861-120">Im Eigenschaftenbereich auf der rechten Seite im Feld **Absatz**, fügen Sie die Urheberrechtsnachricht hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0861-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="a0861-121">Geben Sie beispielsweise **(C) Fabrikam 2019** ein.</span><span class="sxs-lookup"><span data-stu-id="a0861-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="a0861-122">Wählen Sie **Speichern** aus, wählen Sie **Einchecken** und **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="a0861-123">Wechseln Sie zu **Vorlagen**, wählen Sie die Vorlage, und wählen Sie dann **Auschecken** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="a0861-124">Erweitern Sie unter **Seiten-Gliederung**, **Text** und erweitern Sie dann **Standardseite**.</span><span class="sxs-lookup"><span data-stu-id="a0861-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="a0861-125">Aktivieren Sie die Schaltfläche neben **Fußzeilen-Slot**, und wählen Sie dann **Fügen Sie Fragment hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="a0861-126">Wählen Sie das Fragment, das Sie eben erstellt haben, und wählen Sie dann **Auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="a0861-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="a0861-127">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="a0861-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="a0861-128">Die Fußzeile, die den Urheberrechtshinweis automatisch enthält, wird im unteren Bereich alle Seiten hinzugefügt, die auf der ausgewählten Vorlage basieren.</span><span class="sxs-lookup"><span data-stu-id="a0861-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0861-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a0861-129">Additional resources</span></span>

[<span data-ttu-id="a0861-130">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="a0861-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="a0861-131">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="a0861-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="a0861-132">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="a0861-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="a0861-133">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="a0861-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="a0861-134">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="a0861-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="a0861-135">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="a0861-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="a0861-136">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="a0861-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


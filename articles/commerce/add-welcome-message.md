---
title: Hinzufügen einer Begrüßungsnachricht
description: In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914515"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="2c372-103">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="2c372-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2c372-104">In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2c372-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="2c372-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2c372-105">Overview</span></span>

<span data-ttu-id="2c372-106">Eine Begrüßungsmeldung auf der E-Commerce-Website kann Besucher über laufende Verkäufe, Siteaktualisierungen oder verfügbaren saisonale Sammlungen informieren.</span><span class="sxs-lookup"><span data-stu-id="2c372-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="2c372-107">Die Begrüßungsmeldung wird festgelegt, indem das Warnungsmodul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c372-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="2c372-108">Das allgemeine Modul muss den **Fehler-/Informationensnachrichten** Slots des Kopffragments hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2c372-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="2c372-109">Mit dem Warnungsmodul können Sie den Text definieren, der angezeigt wird, die Textfarbe und die Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="2c372-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="2c372-110">Es kann auch angeben, ob Besucher der Site die Nachricht ablehnen können.</span><span class="sxs-lookup"><span data-stu-id="2c372-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="2c372-111">Wenn eine Begrüßungsmeldung einem freigegebenen Kopffragment hinzugefügt wird, wir dieses für jede Seite angezeigt, die die Vorlage verwendet, in dem das freigegebene Kopffragment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c372-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="2c372-112">Um eine Begrüßungsmeldung der Site hinzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="2c372-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="2c372-113">In Dynamics 365 Commerce gehen sie zur Site.</span><span class="sxs-lookup"><span data-stu-id="2c372-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="2c372-114">Wählen Sie **Fragmente**.</span><span class="sxs-lookup"><span data-stu-id="2c372-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="2c372-115">Wählen Sie das Kopffragment aus, um die Nachricht hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c372-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="2c372-116">In der Gliederungsstruktur erweitern Sie **Fehler-/Informationensnachrichten**</span><span class="sxs-lookup"><span data-stu-id="2c372-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="2c372-117">Wählen Sie das Warnungsmodul aus.</span><span class="sxs-lookup"><span data-stu-id="2c372-117">Select the alert module.</span></span>

    <span data-ttu-id="2c372-118">Wenn ein Warnungsmodul noch nicht vorhanden ist, wählen Sie die Ellipsen-Schaltfläche (**...**) neben der **Fehler-/Informationensnachricht** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="2c372-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="2c372-119">Wählen Sie das Warnungsmodul aus und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2c372-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="2c372-120">Im Eigenschaftenbereich auf der rechten Seite auf der Registerkarte **Daten** wählen Sie **Fügen Sie Datenquelle hinzu** und **Inhalt** aus.</span><span class="sxs-lookup"><span data-stu-id="2c372-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="2c372-121">Im Feld **Geben Sie Text ein** geben Sie den Text der Begrüßungsmeldung ein.</span><span class="sxs-lookup"><span data-stu-id="2c372-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="2c372-122">Speichern Sie das Kopffragment, laden Sie es hoch und veröffentlichen Sie es.</span><span class="sxs-lookup"><span data-stu-id="2c372-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="2c372-123">Die Begrüßungsmeldung wird nun oben auf jeder Standortsseite angezeigt, das das ausgewählte Kopffragment verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c372-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c372-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2c372-124">Additional resources</span></span>

[<span data-ttu-id="2c372-125">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="2c372-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2c372-126">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="2c372-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2c372-127">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="2c372-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2c372-128">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="2c372-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2c372-129">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="2c372-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2c372-130">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="2c372-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="2c372-131">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="2c372-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


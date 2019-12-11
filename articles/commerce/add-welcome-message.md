---
title: Hinzufügen einer Begrüßungsnachricht
description: In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697381"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="249b3-103">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="249b3-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="249b3-104">In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="249b3-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="249b3-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="249b3-105">Overview</span></span>

<span data-ttu-id="249b3-106">Eine Begrüßungsmeldung auf der E-Commerce-Website kann Besucher über laufende Verkäufe, Siteaktualisierungen oder verfügbaren saisonale Sammlungen informieren.</span><span class="sxs-lookup"><span data-stu-id="249b3-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="249b3-107">Die Begrüßungsmeldung wird festgelegt, indem das Warnungsmodul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="249b3-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="249b3-108">Das allgemeine Modul muss den **Fehler-/Informationensnachrichten** Slots des Kopffragments hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="249b3-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="249b3-109">Mit dem Warnungsmodul können Sie den Text definieren, der angezeigt wird, die Textfarbe und die Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="249b3-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="249b3-110">Es kann auch angeben, ob Besucher der Site die Nachricht ablehnen können.</span><span class="sxs-lookup"><span data-stu-id="249b3-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="249b3-111">Wenn eine Begrüßungsmeldung einem freigegebenen Kopffragment hinzugefügt wird, wir dieses für jede Seite angezeigt, die die Vorlage verwendet, in dem das freigegebene Kopffragment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="249b3-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="249b3-112">Um eine Begrüßungsmeldung der Site hinzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="249b3-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="249b3-113">In Dynamics 365 Commerce gehen sie zur Site.</span><span class="sxs-lookup"><span data-stu-id="249b3-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="249b3-114">Wählen Sie **Fragmente**.</span><span class="sxs-lookup"><span data-stu-id="249b3-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="249b3-115">Wählen Sie das Kopffragment aus, um die Nachricht hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="249b3-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="249b3-116">In der Gliederungsstruktur erweitern Sie **Fehler-/Informationensnachrichten**</span><span class="sxs-lookup"><span data-stu-id="249b3-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="249b3-117">Wählen Sie das Warnungsmodul aus.</span><span class="sxs-lookup"><span data-stu-id="249b3-117">Select the alert module.</span></span>

    <span data-ttu-id="249b3-118">Wenn ein Warnungsmodul noch nicht vorhanden ist, wählen Sie die Ellipsen-Schaltfläche (**...**) neben der **Fehler-/Informationensnachricht** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="249b3-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="249b3-119">Wählen Sie das Warnungsmodul aus und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="249b3-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="249b3-120">Im Eigenschaftenbereich auf der rechten Seite auf der Registerkarte **Daten** wählen Sie **Fügen Sie Datenquelle hinzu** und **Inhalt** aus.</span><span class="sxs-lookup"><span data-stu-id="249b3-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="249b3-121">Im Feld **Geben Sie Text ein** geben Sie den Text der Begrüßungsmeldung ein.</span><span class="sxs-lookup"><span data-stu-id="249b3-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="249b3-122">Speichern Sie das Kopffragment, laden Sie es hoch und veröffentlichen Sie es.</span><span class="sxs-lookup"><span data-stu-id="249b3-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="249b3-123">Die Begrüßungsmeldung wird nun oben auf jeder Standortsseite angezeigt, das das ausgewählte Kopffragment verwendet.</span><span class="sxs-lookup"><span data-stu-id="249b3-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="249b3-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="249b3-124">Additional resources</span></span>

[<span data-ttu-id="249b3-125">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="249b3-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="249b3-126">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="249b3-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="249b3-127">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="249b3-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="249b3-128">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="249b3-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="249b3-129">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="249b3-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="249b3-130">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="249b3-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


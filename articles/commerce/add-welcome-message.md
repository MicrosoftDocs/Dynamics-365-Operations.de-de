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
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001253"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="f788e-103">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="f788e-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f788e-104">In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f788e-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="f788e-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f788e-105">Overview</span></span>

<span data-ttu-id="f788e-106">Eine Begrüßungsmeldung auf der E-Commerce-Website kann Besucher über laufende Verkäufe, Siteaktualisierungen oder verfügbaren saisonale Sammlungen informieren.</span><span class="sxs-lookup"><span data-stu-id="f788e-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="f788e-107">Die Begrüßungsmeldung wird festgelegt, indem das Warnungsmodul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f788e-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="f788e-108">Das allgemeine Modul muss den **Fehler-/Informationensnachrichten** Slots des Kopffragments hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f788e-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="f788e-109">Mit dem Warnungsmodul können Sie den Text definieren, der angezeigt wird, die Textfarbe und die Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="f788e-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="f788e-110">Es kann auch angeben, ob Besucher der Site die Nachricht ablehnen können.</span><span class="sxs-lookup"><span data-stu-id="f788e-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="f788e-111">Wenn eine Begrüßungsmeldung einem freigegebenen Kopffragment hinzugefügt wird, wir dieses für jede Seite angezeigt, die die Vorlage verwendet, in dem das freigegebene Kopffragment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f788e-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="f788e-112">Um eine Begrüßungsmeldung der Site hinzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="f788e-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="f788e-113">In Dynamics 365 Commerce gehen sie zur Site.</span><span class="sxs-lookup"><span data-stu-id="f788e-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="f788e-114">Wählen Sie **Fragmente**.</span><span class="sxs-lookup"><span data-stu-id="f788e-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="f788e-115">Wählen Sie das Kopffragment aus, um die Nachricht hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f788e-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="f788e-116">In der Gliederungsstruktur erweitern Sie **Fehler-/Informationensnachrichten**</span><span class="sxs-lookup"><span data-stu-id="f788e-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="f788e-117">Wählen Sie das Warnungsmodul aus.</span><span class="sxs-lookup"><span data-stu-id="f788e-117">Select the alert module.</span></span>

    <span data-ttu-id="f788e-118">Wenn ein Warnungsmodul noch nicht vorhanden ist, wählen Sie die Ellipsen-Schaltfläche (**...**) neben der **Fehler-/Informationensnachricht** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="f788e-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="f788e-119">Wählen Sie das Warnungsmodul aus und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f788e-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="f788e-120">Im Eigenschaftenbereich auf der rechten Seite auf der Registerkarte **Daten** wählen Sie **Fügen Sie Datenquelle hinzu** und **Inhalt** aus.</span><span class="sxs-lookup"><span data-stu-id="f788e-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="f788e-121">Im Feld **Geben Sie Text ein** geben Sie den Text der Begrüßungsmeldung ein.</span><span class="sxs-lookup"><span data-stu-id="f788e-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="f788e-122">Speichern Sie das Kopffragment, laden Sie es hoch und veröffentlichen Sie es.</span><span class="sxs-lookup"><span data-stu-id="f788e-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="f788e-123">Die Begrüßungsmeldung wird nun oben auf jeder Standortsseite angezeigt, das das ausgewählte Kopffragment verwendet.</span><span class="sxs-lookup"><span data-stu-id="f788e-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f788e-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f788e-124">Additional resources</span></span>

[<span data-ttu-id="f788e-125">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="f788e-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f788e-126">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="f788e-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f788e-127">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="f788e-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f788e-128">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="f788e-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f788e-129">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="f788e-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f788e-130">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="f788e-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f788e-131">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="f788e-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


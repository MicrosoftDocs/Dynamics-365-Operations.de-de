---
title: Hinzufügen einer Begrüßungsnachricht
description: In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce-Website hinzugefügt wird.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797382"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="6ead8-103">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="6ead8-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ead8-104">In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce-Website hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6ead8-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="6ead8-105">Eine Begrüßungsmeldung auf der E-Commerce-Website kann Besucher über laufende Verkäufe, Siteaktualisierungen oder verfügbaren saisonale Sammlungen informieren.</span><span class="sxs-lookup"><span data-stu-id="6ead8-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="6ead8-106">Die Begrüßungsmeldung wird festgelegt, indem das Warnungsmodul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ead8-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="6ead8-107">Das allgemeine Modul muss den **Fehler-/Informationensnachrichten** Slots des Kopffragments hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6ead8-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="6ead8-108">Mit dem Warnungsmodul können Sie den Text definieren, der angezeigt wird, die Textfarbe und die Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="6ead8-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="6ead8-109">Es kann auch angeben, ob Besucher der Site die Nachricht ablehnen können.</span><span class="sxs-lookup"><span data-stu-id="6ead8-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="6ead8-110">Wenn eine Begrüßungsmeldung einem freigegebenen Kopffragment hinzugefügt wird, wir dieses für jede Seite angezeigt, die die Vorlage verwendet, in dem das freigegebene Kopffragment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ead8-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="6ead8-111">Um eine Begrüßungsmeldung der Site hinzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6ead8-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="6ead8-112">Navigieren Sie im Commerce Site Builder zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="6ead8-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="6ead8-113">Wählen Sie **Fragmente**.</span><span class="sxs-lookup"><span data-stu-id="6ead8-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="6ead8-114">Wählen Sie das Kopffragment aus, um die Nachricht hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ead8-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="6ead8-115">In der Gliederungsstruktur erweitern Sie **Fehler-/Informationensnachrichten**</span><span class="sxs-lookup"><span data-stu-id="6ead8-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="6ead8-116">Wählen Sie das Warnungsmodul aus und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6ead8-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="6ead8-117">Wenn ein Warnungsmodul noch nicht vorhanden ist, wählen Sie zunächst die Ellipsen-Schaltfläche (**...**) neben der **Fehler-/Informationensnachricht** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="6ead8-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="6ead8-118">Im Eigenschaftenbereich auf der rechten Seite auf der Registerkarte **Daten** wählen Sie **Fügen Sie Datenquelle hinzu** und **Inhalt** aus.</span><span class="sxs-lookup"><span data-stu-id="6ead8-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="6ead8-119">Im Feld **Geben Sie Text ein** geben Sie den Text der Begrüßungsmeldung ein.</span><span class="sxs-lookup"><span data-stu-id="6ead8-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="6ead8-120">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Kopffragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6ead8-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="6ead8-121">Die Begrüßungsmeldung wird nun oben auf jeder Standortsseite angezeigt, das das ausgewählte Kopffragment verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ead8-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ead8-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ead8-122">Additional resources</span></span>

[<span data-ttu-id="6ead8-123">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="6ead8-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6ead8-124">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="6ead8-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="6ead8-125">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="6ead8-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6ead8-126">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="6ead8-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6ead8-127">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="6ead8-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="6ead8-128">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="6ead8-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6ead8-129">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="6ead8-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

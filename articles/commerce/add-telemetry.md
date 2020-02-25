---
title: Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie
description: In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
manager: annbe
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001276"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="f0d58-103">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="f0d58-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f0d58-104">In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f0d58-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="f0d58-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f0d58-105">Overview</span></span>

<span data-ttu-id="f0d58-106">Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="f0d58-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="f0d58-107">Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="f0d58-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="f0d58-108">Die meisten Internet-Analysepakete erfordern, dass Sie clientseitige Scriptcode im **\<Kopf\>** Element des HTML für alle Seiten Ihrer Site hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f0d58-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="f0d58-109">Die Anweisungen in diesem Thema gelten auch für benutzerdefinierte clientseitige andere Funktionen, die Microsoft Dynamics 365 Commerce System intern nicht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f0d58-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="f0d58-110">Erstellen Sie ein wiederverwendbares Fragment für Ihren Skriptcode</span><span class="sxs-lookup"><span data-stu-id="f0d58-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="f0d58-111">Nachdem Sie ein Fragment für den Skriptcode erstell haben, kann er über alle Seiten auf dem Standort wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0d58-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="f0d58-112">Gehen Sie zu **Fragmente \> Neues Seitenfragment**</span><span class="sxs-lookup"><span data-stu-id="f0d58-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="f0d58-113">Wählen Sie **Externes Skript** aus, geben Sie einen Namen für das Fragment ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f0d58-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="f0d58-114">In der Fragmenthierarchie wählen Sie das untergeordnete Modul **Skript-Injector** des Fragments aus, das Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f0d58-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="f0d58-115">Im Eigenschaftenbereich auf der rechten Seite fügen Sie das Skript clientseitiges hinzu und legen andere Konfigurationsoptionen fest, wie Sie sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="f0d58-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="f0d58-116">Das Fragment den Vorlagen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f0d58-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="f0d58-117">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f0d58-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="f0d58-118">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f0d58-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="f0d58-119">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Fragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f0d58-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="f0d58-120">Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f0d58-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="f0d58-121">Speichern Sie die Vorlage und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="f0d58-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="f0d58-122">Nachdem Sie fertig sind, müssen Sie das Fragment und die Master-Vorlage veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="f0d58-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f0d58-123">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f0d58-123">Additional resources</span></span>

[<span data-ttu-id="f0d58-124">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="f0d58-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f0d58-125">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="f0d58-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f0d58-126">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="f0d58-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f0d58-127">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="f0d58-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f0d58-128">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="f0d58-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f0d58-129">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="f0d58-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f0d58-130">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="f0d58-130">Add languages to your site</span></span>](add-languages-to-site.md)


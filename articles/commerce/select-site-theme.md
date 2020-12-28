---
title: Auswählen eines Sitedesigns
description: In diesem Thema wird beschrieben, wie Sie das Design Ihrer Site in Microsoft Dynamics 365 Commerce festlegen oder ändern.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c54a3e9471fdeb56f27fe7c567c7cd7f0b7fd218
ms.sourcegitcommit: 2ef23dcd4e42362186b9951e675010d97d55c6bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4556428"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="e7ac2-103">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="e7ac2-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7ac2-104">In diesem Thema wird beschrieben, wie Sie das Design Ihrer Site in Microsoft Dynamics 365 Commerce festlegen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7ac2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e7ac2-105">Overview</span></span>

<span data-ttu-id="e7ac2-106">Das Layout und der Stil einer Site (z. B. Schriftarten, Größen und Farben) werden durch das Design definiert, das Sie auswählen und auf die Site anwenden.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="e7ac2-107">Ein Design wird von einem Entwickler in Ihrem Unternehmen erstellt und bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="e7ac2-108">Eine Überblick über die Designs erhalten Sie in [Designüberblick](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="e7ac2-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="e7ac2-109">Weitere Informationen zum Erstellen und Bereitstellen von Designs finden Sie unter [Neues Design erstellen](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="e7ac2-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="e7ac2-110">Wenn Sie eine Site zum ersten Mal erstellen, wird standardmäßig ein Design mit der Bezeichnung **Fabrikam** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="e7ac2-111">Dieses Standarddesign wird als Teil der Commerce-Modulbibliothek bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="e7ac2-112">Nachdem Sie zusätzliche Designs für Ihre Site bereitgestellt haben, können Sie die Site so konfigurieren, dass stattdessen eines davon verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="e7ac2-113">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="e7ac2-113">Select the site theme</span></span>

<span data-ttu-id="e7ac2-114">Gehen Sie folgendermaßen vor, um das Design auszuwählen, das auf Ihre Site angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="e7ac2-115">Wechseln Sie in der Website-Authoring-Umgebung zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="e7ac2-116">Navigieren Sie zu **Siteverwaltung** \> **Erweiterbarkeit**.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="e7ac2-117">Wählen Sie unter **Design** ein Design aus dem Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="e7ac2-118">Um das ausgewählte Design auf Ihre Site anzuwenden, wählen Sie **Speichern und veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="e7ac2-119">Das ausgewählte Design wird auf Ihrer Site veröffentlicht, sobald Sie **Speichern und veröffentlichen** auf der Seite **Erweiterbarkeit** auswählen.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="e7ac2-120">Um eine Vorschau eines Designs auf Ihrer Site anzuzeigen, bevor Sie es anwenden, können Sie Ihre Entwicklungs- oder Sandbox-Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7ac2-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7ac2-121">Additional resources</span></span>

[<span data-ttu-id="e7ac2-122">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="e7ac2-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e7ac2-123">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="e7ac2-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e7ac2-124">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="e7ac2-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e7ac2-125">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="e7ac2-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e7ac2-126">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="e7ac2-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e7ac2-127">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="e7ac2-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e7ac2-128">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="e7ac2-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="e7ac2-129">Designüberblick</span><span class="sxs-lookup"><span data-stu-id="e7ac2-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="e7ac2-130">Neues Design erstellen</span><span class="sxs-lookup"><span data-stu-id="e7ac2-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)


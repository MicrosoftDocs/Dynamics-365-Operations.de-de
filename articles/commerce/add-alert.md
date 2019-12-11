---
title: Warnungsmodul
description: Dieses Thema enthält allgemeine Module und es wird beschrieben, wie diese Standortsseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785351"
---
# <a name="alert-module"></a><span data-ttu-id="95e9a-103">Warnmmodul</span><span class="sxs-lookup"><span data-stu-id="95e9a-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="95e9a-104">Dieses Thema enthält allgemeine Module und es wird beschrieben, wie diese Standortsseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="95e9a-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="95e9a-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="95e9a-105">Overview</span></span>

<span data-ttu-id="95e9a-106">Ein Warnungsmodul wird verwendet, um Informationsmeldungen auf einer Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="95e9a-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="95e9a-107">Warnungsmodule unterstützen Textnachricht und einen Link.</span><span class="sxs-lookup"><span data-stu-id="95e9a-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="95e9a-108">Sie können verwendet werden, um Standort-weite Aktionen anzuzeigen, die auf allen Seiten einer E-Commerce-Webseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95e9a-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="95e9a-109">WModule Wachsame werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="95e9a-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="95e9a-110">Beispiele der Warnungsmodule in E-Commerce</span><span class="sxs-lookup"><span data-stu-id="95e9a-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="95e9a-111">Warnungsmodule können im Sitekopf verwendet werden, um Standort-weite Aktionen oder Nachrichten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="95e9a-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="95e9a-112">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="95e9a-112">Here are some examples:</span></span>

<span data-ttu-id="95e9a-113">„Jahresendverkauf endet in 10 Tagen“</span><span class="sxs-lookup"><span data-stu-id="95e9a-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="95e9a-114">„Mit den Aktionen zum Schulbeginn viel sparen.</span><span class="sxs-lookup"><span data-stu-id="95e9a-114">"Save big with back to school sale.</span></span> <span data-ttu-id="95e9a-115">Jetzt shoppen.“</span><span class="sxs-lookup"><span data-stu-id="95e9a-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="95e9a-116">Warnungsmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="95e9a-116">Alert module properties</span></span>

| <span data-ttu-id="95e9a-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="95e9a-117">Property name</span></span>  | <span data-ttu-id="95e9a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="95e9a-118">Value</span></span>                              | <span data-ttu-id="95e9a-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95e9a-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="95e9a-120">Text</span><span class="sxs-lookup"><span data-stu-id="95e9a-120">Text</span></span>           | <span data-ttu-id="95e9a-121">Text</span><span class="sxs-lookup"><span data-stu-id="95e9a-121">Text</span></span>                               | <span data-ttu-id="95e9a-122">Die Textnachricht erscheint im Warnungsmodul.</span><span class="sxs-lookup"><span data-stu-id="95e9a-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="95e9a-123">Textausrichtung</span><span class="sxs-lookup"><span data-stu-id="95e9a-123">Text alignment</span></span> | <span data-ttu-id="95e9a-124">**Rechts** **Links** **Zentriert**</span><span class="sxs-lookup"><span data-stu-id="95e9a-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="95e9a-125">Ein Wert, der definiert, wie Text im Warnungsmodul dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="95e9a-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="95e9a-126">Warnung verwerfen</span><span class="sxs-lookup"><span data-stu-id="95e9a-126">Dismiss alert</span></span>  | <span data-ttu-id="95e9a-127">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="95e9a-127">**True** or **False**</span></span>              | <span data-ttu-id="95e9a-128">Wenn der Wert auf **True** gesetzt wird, kann der Debitor die Warnung ablehnen.</span><span class="sxs-lookup"><span data-stu-id="95e9a-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="95e9a-129">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="95e9a-129">Link</span></span>           | <span data-ttu-id="95e9a-130">URL</span><span class="sxs-lookup"><span data-stu-id="95e9a-130">URL</span></span>                                | <span data-ttu-id="95e9a-131">Die URL für einen optionalen Link.</span><span class="sxs-lookup"><span data-stu-id="95e9a-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="95e9a-132">Ein Warnungsmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="95e9a-132">Add an alert module to a page</span></span> 

<span data-ttu-id="95e9a-133">Um ein Warnungsmodul einer Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="95e9a-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="95e9a-134">Erstellen Sie eine Seitenvorlage, die mit **Warnungsvorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="95e9a-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="95e9a-135">Im **Haupt-** Slot der Standardseite fügen Sie ein Warnungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="95e9a-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="95e9a-136">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="95e9a-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="95e9a-137">Verwenden Sie die Warnungsvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Warnungsseite** hat.</span><span class="sxs-lookup"><span data-stu-id="95e9a-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="95e9a-138">Im **Haupt-** Slot der neuen Seite fügen Sie ein Warnungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="95e9a-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="95e9a-139">In den Einstellungen für das Warnungsmodul geben Sie den Warnungstext ein.</span><span class="sxs-lookup"><span data-stu-id="95e9a-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="95e9a-140">Sie können die anderen Eigenschaften bearbeiten, wenn Sie das Modul weiter anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="95e9a-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="95e9a-141">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="95e9a-141">Save and preview the page.</span></span> <span data-ttu-id="95e9a-142">Am oberen Rand der Seite können sollten Sie eine Warnung sehen, die den von Ihnen hinzugefügten Text hat.</span><span class="sxs-lookup"><span data-stu-id="95e9a-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="95e9a-143">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="95e9a-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="95e9a-144">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="95e9a-144">Additional resources</span></span>

[<span data-ttu-id="95e9a-145">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="95e9a-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="95e9a-146">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="95e9a-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="95e9a-147">Umfangreiches Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="95e9a-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="95e9a-148">Inhaltsplatzierungsmodul</span><span class="sxs-lookup"><span data-stu-id="95e9a-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="95e9a-149">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="95e9a-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="95e9a-150">Hero-Modul</span><span class="sxs-lookup"><span data-stu-id="95e9a-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="95e9a-151">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="95e9a-151">Video player module</span></span>](add-video-player.md)

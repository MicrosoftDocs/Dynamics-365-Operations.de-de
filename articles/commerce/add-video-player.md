---
title: Video-Player-Modul
description: Dieses Thema enthält Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025646"
---
# <a name="video-player-module"></a><span data-ttu-id="c1777-103">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="c1777-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c1777-104">Dieses Thema enthält Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c1777-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c1777-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c1777-105">Overview</span></span>

<span data-ttu-id="c1777-106">Das Video-Player-Module wird verwendet, um die Videowiedergabe zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c1777-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="c1777-107">Es kann zu jeder Seite hinzugefügt werden, vorausgesetzt, der Videoinhalt wird in das Content Management System (CMS) hochgeladen und ist dort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c1777-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="c1777-108">Das Video-Player-Modul unterstützt den Medientyp .mp4.</span><span class="sxs-lookup"><span data-stu-id="c1777-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="c1777-109">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="c1777-109">Video player module</span></span>

<span data-ttu-id="c1777-110">Das Video-Player-Modul kann verwendet werden, um Videos auf einer E-Commerce-Webseite zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="c1777-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="c1777-111">Es unterstützt alle Wiedergabefunktionen, wie Wiedergabe, Pause, Vollbildmodus, Audiobeschreibungen und Untertitel.</span><span class="sxs-lookup"><span data-stu-id="c1777-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="c1777-112">Das Video-Player-Modul unterstützt außerdem Anpassung von Untertiteln, um Microsoft-Barrierefreiheitsstandards zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c1777-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="c1777-113">So können Sie die Schriftgröße und die Hintergrundfarbe anpassen.</span><span class="sxs-lookup"><span data-stu-id="c1777-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="c1777-114">Das Video-Player-Modul unterstützt auch sekundäre Audiospuren.</span><span class="sxs-lookup"><span data-stu-id="c1777-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="c1777-115">Beim Hochladen eines Videos in das CMS kann auch eine sekundäre Audiospur hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c1777-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="c1777-116">Das Video-Player-Modul kann dann die sekundäre Audiospur wiedergeben, wenn ein Benutzer sie auswählt.</span><span class="sxs-lookup"><span data-stu-id="c1777-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="c1777-117">Beispiele für Ambient-Video-Player-Module im E-Commerce</span><span class="sxs-lookup"><span data-stu-id="c1777-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="c1777-118">Instruktionsvideos auf Produktdetailseiten oder Marketings-Seiten</span><span class="sxs-lookup"><span data-stu-id="c1777-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="c1777-119">Werbespots oder Videos zu Richtlinien auf einer Marketings-Seite</span><span class="sxs-lookup"><span data-stu-id="c1777-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="c1777-120">Marketings-Videos, die Produktfunktionen auf Produktdetailseiten oder Marketings-Seiten markieren</span><span class="sxs-lookup"><span data-stu-id="c1777-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="c1777-121">Video-Player-Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1777-121">Video player module properties</span></span>

| <span data-ttu-id="c1777-122">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="c1777-122">Property name</span></span>         | <span data-ttu-id="c1777-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c1777-123">Value</span></span>                               | <span data-ttu-id="c1777-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1777-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="c1777-125">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="c1777-125">Auto play</span></span>             | <span data-ttu-id="c1777-126">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-126">**True** or **False**</span></span>               | <span data-ttu-id="c1777-127">Wenn der Wert auf **Wahr** gesetzt wird, wird das Video automatisch wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="c1777-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="c1777-128">Stummschalten</span><span class="sxs-lookup"><span data-stu-id="c1777-128">Mute</span></span>                  | <span data-ttu-id="c1777-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-129">**True** or **False**</span></span>               | <span data-ttu-id="c1777-130">Wenn der Wert auf **Wahr** gesetzt wird, wird der Ton abgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="c1777-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="c1777-131">Standardmäßig besitzt das Feld für diesen Player den Wert **False**.</span><span class="sxs-lookup"><span data-stu-id="c1777-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="c1777-132">Im Chrome Browser wird automatische Wiedergabe standardmäßig stumm geschaltet, und die Audiowiedergabe wird nur abgespielt, wenn der Benutzer das Video manuell wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="c1777-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="c1777-133">Schleife</span><span class="sxs-lookup"><span data-stu-id="c1777-133">Loop</span></span>                  | <span data-ttu-id="c1777-134">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-134">**True** or **False**</span></span>               | <span data-ttu-id="c1777-135">Wenn der Wert auf **Wahr** gesetzt wird, wird das Video im Loop wiederholt.</span><span class="sxs-lookup"><span data-stu-id="c1777-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="c1777-136">Medien</span><span class="sxs-lookup"><span data-stu-id="c1777-136">Media</span></span>                 | <span data-ttu-id="c1777-137">Videodateipfad und Name</span><span class="sxs-lookup"><span data-stu-id="c1777-137">Video file path and name</span></span> | <span data-ttu-id="c1777-138">Die Videodatei, die der Video-Player wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="c1777-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="c1777-139">Vollbildmodus</span><span class="sxs-lookup"><span data-stu-id="c1777-139">Play fullscreen</span></span>       | <span data-ttu-id="c1777-140">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-140">**True** or **False**</span></span>               | <span data-ttu-id="c1777-141">Wenn der Wert auf **True** gesetzt wird, wird das Video im Vollbildmodus wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="c1777-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="c1777-142">Trigger für Wiedergabe/Anhalten</span><span class="sxs-lookup"><span data-stu-id="c1777-142">Play pause trigger</span></span>    | <span data-ttu-id="c1777-143">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-143">**True** or **False**</span></span>               | <span data-ttu-id="c1777-144">Wenn der Wert auf **Wahr** gesetzt wird, wird eine Wiedergabe-/Pausenschaltfläche im Video angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1777-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="c1777-145">Videoplayer-Steuerungen</span><span class="sxs-lookup"><span data-stu-id="c1777-145">Video player controls</span></span> | <span data-ttu-id="c1777-146">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-146">**True** or **False**</span></span>               | <span data-ttu-id="c1777-147">Wenn der Wert auf **True** gesetzt wird, werden alle Steuerungen des Video-Players angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1777-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="c1777-148">Zu diesen Steuerelementen gehören Wiedergabe- und Pausenschaltflächen, ein Fortschrittsbalken und Untertiteloptionen.</span><span class="sxs-lookup"><span data-stu-id="c1777-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="c1777-149">Posterbild ausblenden</span><span class="sxs-lookup"><span data-stu-id="c1777-149">Hide poster image</span></span>     | <span data-ttu-id="c1777-150">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="c1777-150">**True** or **False**</span></span>               | <span data-ttu-id="c1777-151">Ein Videodatei kann einen Plakatrahmen haben.</span><span class="sxs-lookup"><span data-stu-id="c1777-151">A video can have a poster frame.</span></span> <span data-ttu-id="c1777-152">Wenn der Wert dieser Eigenschaft auf **Wahr** festgelegt wurde, wird der Plakatrahmen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="c1777-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="c1777-153">Maske festlegen</span><span class="sxs-lookup"><span data-stu-id="c1777-153">Mask level</span></span>            | <span data-ttu-id="c1777-154">Eine Nummer aus **0** bis **100**</span><span class="sxs-lookup"><span data-stu-id="c1777-154">A number from **0** through **100**</span></span> | <span data-ttu-id="c1777-155">Die Maske, die für die Videodatei für die Formatierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1777-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="c1777-156">Hinzufügen eines Video-Player-Moduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="c1777-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="c1777-157">Bevor Sie ein Video-Player-Modul erstellen, müssen Sie zuerst ein Video in die Medienbibliothek hochladen.</span><span class="sxs-lookup"><span data-stu-id="c1777-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="c1777-158">Um ein Video-Player-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="c1777-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c1777-159">Erstellen Sie eine Seitenvorlage, die mit **Video-Player-Vorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1777-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="c1777-160">Im **Haupt-** Slot der Standardseite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1777-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="c1777-161">Im Containermodul fügen Sie Video-Player- und Ambient Video-Player-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1777-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="c1777-162">Beenden Sie die Bearbeitung der Vorlage und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="c1777-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="c1777-163">Verwenden Sie die Video-Player-Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Video-Player-Seite** hat.</span><span class="sxs-lookup"><span data-stu-id="c1777-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="c1777-164">Im **Haupt-** Slot der neuen Seite fügen Sie ein Ambient Video-Player-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1777-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="c1777-165">Wählen Sie im Eigenschaftenfenster für das Videoplayer-Modul **Video hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1777-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="c1777-166">Wählen Sie im Dialogfeld **Medienauswahl** ein Video und anschließend **Neues Medienelement hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1777-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="c1777-167">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c1777-167">Save and preview the page.</span></span> <span data-ttu-id="c1777-168">Sie sollten das Videomodul auf der Seite sehen.</span><span class="sxs-lookup"><span data-stu-id="c1777-168">You should see the video module on the page.</span></span> <span data-ttu-id="c1777-169">Sie können zusätzliche Einstellungen ändern, um das Verhalten des Moduls anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c1777-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="c1777-170">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="c1777-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1777-171">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c1777-171">Additional resources</span></span>

[<span data-ttu-id="c1777-172">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="c1777-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c1777-173">Werbebanner-Modul</span><span class="sxs-lookup"><span data-stu-id="c1777-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="c1777-174">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="c1777-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="c1777-175">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="c1777-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c1777-176">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="c1777-176">Content block module</span></span>](add-hero-module.md)

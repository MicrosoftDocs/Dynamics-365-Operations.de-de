---
title: Videos hochladen
description: In diesem Thema wird beschrieben, wie Sie Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d74e7116d68074bfc917784a8f51f85d5682c5d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213841"
---
# <a name="upload-videos"></a><span data-ttu-id="3b64c-103">Videos hochladen</span><span class="sxs-lookup"><span data-stu-id="3b64c-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b64c-104">In diesem Thema wird beschrieben, wie Sie Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="3b64c-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="3b64c-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="3b64c-105">Overview</span></span>

<span data-ttu-id="3b64c-106">Die Medienbibliothek des Commerce-Site-Builders ermöglicht Ihnen das Hochladen von Videos.</span><span class="sxs-lookup"><span data-stu-id="3b64c-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="3b64c-107">Sie sollten immer die Version eines Videos mit der höchsten Bitrate und Auflösung hochladen, da das Video automatisch so konvertiert wird, dass es für verschiedene Ansichtsfenster und deren Haltepunkte geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3b64c-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="3b64c-108">Beim Hochladen angegebene Videoinformationen</span><span class="sxs-lookup"><span data-stu-id="3b64c-108">Video information specified during upload</span></span>

<span data-ttu-id="3b64c-109">Beim Hochladen eines Videos können die folgenden Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3b64c-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="3b64c-110">**Titel, Beschreibung, Schlüsselwörter**: Metadaten des Videos.</span><span class="sxs-lookup"><span data-stu-id="3b64c-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="3b64c-111">**Automatische Generierung von Untertiteln**: Gibt an, ob Untertitel für das Video automatisch generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b64c-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="3b64c-112">**Untertitel**: Gibt die zu verwendenden Untertitel an.</span><span class="sxs-lookup"><span data-stu-id="3b64c-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="3b64c-113">**Regular Audio**: Gibt die zu verwendende reguläre Tonspur an.</span><span class="sxs-lookup"><span data-stu-id="3b64c-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="3b64c-114">**Miniaturansicht**: Gibt die Miniaturansicht für das Video an.</span><span class="sxs-lookup"><span data-stu-id="3b64c-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="3b64c-115">Wenn nicht angegeben, wird es automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="3b64c-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="3b64c-116">**Beschreibendes Audio**: Gibt die zu verwendende beschreibende Tonspur an.</span><span class="sxs-lookup"><span data-stu-id="3b64c-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="3b64c-117">Ein Video hochladen</span><span class="sxs-lookup"><span data-stu-id="3b64c-117">Upload a video</span></span>

<span data-ttu-id="3b64c-118">Führen Sie die folgenden Schritte aus, um ein Video in Site Builder hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="3b64c-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3b64c-119">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3b64c-120">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="3b64c-121">Navigieren Sie im Fenster Datei-Explorer zu einer oder mehreren hochzuladenden Videodateien und wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="3b64c-122">Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.</span><span class="sxs-lookup"><span data-stu-id="3b64c-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="3b64c-123">Geben Sie eine optionale Beschreibung und Schlüsselwörter ein und wählen Sie eine Kategorie aus, falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="3b64c-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="3b64c-124">Wenn Sie das Bild bzw. die Bilder nach dem sofortigen Hochladen veröffentlichen möchten, wählen Sie das Kontrollkästchen **Medienelemente nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="3b64c-125">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-125">Select **OK**.</span></span>

<span data-ttu-id="3b64c-126">Wenn Sie mehrere Arten von Assets gleichzeitig hochladen (z. B. Bilder und Videos), können Sie im Dialogfeld **Medienelement hochladen** nur Schlüsselwörter angeben, ob die Dateien unmittelbar nach dem Hochladen veröffentlicht werden sollen und ob für Videodateien automatisch Untertitel generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b64c-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="3b64c-127">Alle Assets werden die gleichen Schlüsselwörter verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b64c-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b64c-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3b64c-128">Additional resources</span></span>

[<span data-ttu-id="3b64c-129">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="3b64c-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3b64c-130">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="3b64c-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="3b64c-131">Dateien hochladen</span><span class="sxs-lookup"><span data-stu-id="3b64c-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="3b64c-132">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="3b64c-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3b64c-133">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="3b64c-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="3b64c-134">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="3b64c-134">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
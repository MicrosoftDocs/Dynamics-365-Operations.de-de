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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097021"
---
# <a name="upload-videos"></a><span data-ttu-id="ef3fe-103">Videos hochladen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ef3fe-104">In diesem Thema wird beschrieben, wie Sie Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="ef3fe-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ef3fe-105">Overview</span></span>

<span data-ttu-id="ef3fe-106">Die Medienbibliothek des Commerce-Site-Builders ermöglicht Ihnen das Hochladen von Videos.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="ef3fe-107">Sie sollten immer die Version eines Videos mit der höchsten Bitrate und Auflösung hochladen, da das Video automatisch so konvertiert wird, dass es für verschiedene Ansichtsfenster und deren Haltepunkte geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="ef3fe-108">Beim Hochladen angegebene Videoinformationen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-108">Video information specified during upload</span></span>

<span data-ttu-id="ef3fe-109">Beim Hochladen eines Videos können die folgenden Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="ef3fe-110">**Titel, Beschreibung, Schlüsselwörter**: Metadaten des Videos.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="ef3fe-111">**Automatische Generierung von Untertiteln**: Gibt an, ob Untertitel für das Video automatisch generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="ef3fe-112">**Untertitel**: Gibt die zu verwendenden Untertitel an.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="ef3fe-113">**Regular Audio**: Gibt die zu verwendende reguläre Tonspur an.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="ef3fe-114">**Miniaturansicht**: Gibt die Miniaturansicht für das Video an.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="ef3fe-115">Wenn nicht angegeben, wird es automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="ef3fe-116">**Beschreibendes Audio**: Gibt die zu verwendende beschreibende Tonspur an.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="ef3fe-117">Ein Video hochladen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-117">Upload a video</span></span>

<span data-ttu-id="ef3fe-118">Führen Sie die folgenden Schritte aus, um ein Video in Site Builder hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="ef3fe-119">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="ef3fe-120">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="ef3fe-121">Navigieren Sie im Fenster Datei-Explorer zu einer oder mehreren hochzuladenden Videodateien und wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="ef3fe-122">Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="ef3fe-123">Geben Sie eine optionale Beschreibung und Schlüsselwörter ein und wählen Sie eine Kategorie aus, falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="ef3fe-124">Wenn Sie das Bild bzw. die Bilder nach dem sofortigen Hochladen veröffentlichen möchten, wählen Sie das Kontrollkästchen **Medienelemente nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="ef3fe-125">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-125">Select **OK**.</span></span>

<span data-ttu-id="ef3fe-126">Wenn Sie mehrere Arten von Assets gleichzeitig hochladen (z. B. Bilder und Videos), können Sie im Dialogfeld **Medienelement hochladen** nur Schlüsselwörter angeben, ob die Dateien unmittelbar nach dem Hochladen veröffentlicht werden sollen und ob für Videodateien automatisch Untertitel generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="ef3fe-127">Alle Assets werden die gleichen Schlüsselwörter verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef3fe-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef3fe-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-128">Additional resources</span></span>

[<span data-ttu-id="ef3fe-129">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="ef3fe-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ef3fe-130">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ef3fe-131">Dateien hochladen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="ef3fe-132">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="ef3fe-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="ef3fe-133">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="ef3fe-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

---
title: Hochladen von anderen Dateien als Bildern und Videos
description: In diesem Thema wird beschrieben, wie Sie andere Binärdateien als Bilder und Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799252"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="43c4a-103">Andere Dateien außer Bildern und Videos hochladen</span><span class="sxs-lookup"><span data-stu-id="43c4a-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="43c4a-104">In diesem Thema wird beschrieben, wie Sie andere Dateien als Bilder und Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="43c4a-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="43c4a-105">Die Medienbibliothek des Commerce-Site-Builders unterstützt das Hochladen von anderen Binärdateien als Bildern oder Videos.</span><span class="sxs-lookup"><span data-stu-id="43c4a-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="43c4a-106">Beispielsweise können Sie Microsoft Excel, Microsoft Word, Microsoft PowerPoint oder PDF-Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="43c4a-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="43c4a-107">Die folgenden Dokumenttypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="43c4a-107">The following document types are supported:</span></span>
- <span data-ttu-id="43c4a-108">7Z</span><span class="sxs-lookup"><span data-stu-id="43c4a-108">7Z</span></span>
- <span data-ttu-id="43c4a-109">AVI</span><span class="sxs-lookup"><span data-stu-id="43c4a-109">AVI</span></span>
- <span data-ttu-id="43c4a-110">CS</span><span class="sxs-lookup"><span data-stu-id="43c4a-110">CS</span></span>
- <span data-ttu-id="43c4a-111">CSS</span><span class="sxs-lookup"><span data-stu-id="43c4a-111">CSS</span></span>
- <span data-ttu-id="43c4a-112">DOC</span><span class="sxs-lookup"><span data-stu-id="43c4a-112">DOC</span></span>
- <span data-ttu-id="43c4a-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="43c4a-113">DOCX</span></span>
- <span data-ttu-id="43c4a-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="43c4a-114">EPUB</span></span>
- <span data-ttu-id="43c4a-115">GIF</span><span class="sxs-lookup"><span data-stu-id="43c4a-115">GIF</span></span>
- <span data-ttu-id="43c4a-116">INDD</span><span class="sxs-lookup"><span data-stu-id="43c4a-116">INDD</span></span>
- <span data-ttu-id="43c4a-117">JAR</span><span class="sxs-lookup"><span data-stu-id="43c4a-117">JAR</span></span>
- <span data-ttu-id="43c4a-118">JPG</span><span class="sxs-lookup"><span data-stu-id="43c4a-118">JPG</span></span>
- <span data-ttu-id="43c4a-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="43c4a-119">JPEG</span></span>
- <span data-ttu-id="43c4a-120">JS</span><span class="sxs-lookup"><span data-stu-id="43c4a-120">JS</span></span>
- <span data-ttu-id="43c4a-121">MP3</span><span class="sxs-lookup"><span data-stu-id="43c4a-121">MP3</span></span>
- <span data-ttu-id="43c4a-122">MP4</span><span class="sxs-lookup"><span data-stu-id="43c4a-122">MP4</span></span>
- <span data-ttu-id="43c4a-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="43c4a-123">MPEG</span></span>
- <span data-ttu-id="43c4a-124">MPG</span><span class="sxs-lookup"><span data-stu-id="43c4a-124">MPG</span></span>
- <span data-ttu-id="43c4a-125">ODP</span><span class="sxs-lookup"><span data-stu-id="43c4a-125">ODP</span></span>
- <span data-ttu-id="43c4a-126">ODS</span><span class="sxs-lookup"><span data-stu-id="43c4a-126">ODS</span></span>
- <span data-ttu-id="43c4a-127">ODT</span><span class="sxs-lookup"><span data-stu-id="43c4a-127">ODT</span></span>
- <span data-ttu-id="43c4a-128">PDF</span><span class="sxs-lookup"><span data-stu-id="43c4a-128">PDF</span></span>
- <span data-ttu-id="43c4a-129">PNG</span><span class="sxs-lookup"><span data-stu-id="43c4a-129">PNG</span></span>
- <span data-ttu-id="43c4a-130">PPT</span><span class="sxs-lookup"><span data-stu-id="43c4a-130">PPT</span></span>
- <span data-ttu-id="43c4a-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="43c4a-131">PPTX</span></span>
- <span data-ttu-id="43c4a-132">PS</span><span class="sxs-lookup"><span data-stu-id="43c4a-132">PS</span></span>
- <span data-ttu-id="43c4a-133">QXP</span><span class="sxs-lookup"><span data-stu-id="43c4a-133">QXP</span></span>
- <span data-ttu-id="43c4a-134">RAR</span><span class="sxs-lookup"><span data-stu-id="43c4a-134">RAR</span></span>
- <span data-ttu-id="43c4a-135">RTF</span><span class="sxs-lookup"><span data-stu-id="43c4a-135">RTF</span></span>
- <span data-ttu-id="43c4a-136">SVG</span><span class="sxs-lookup"><span data-stu-id="43c4a-136">SVG</span></span>
- <span data-ttu-id="43c4a-137">TAR</span><span class="sxs-lookup"><span data-stu-id="43c4a-137">TAR</span></span>
- <span data-ttu-id="43c4a-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="43c4a-138">TGZ</span></span>
- <span data-ttu-id="43c4a-139">TXT</span><span class="sxs-lookup"><span data-stu-id="43c4a-139">TXT</span></span>
- <span data-ttu-id="43c4a-140">WMV</span><span class="sxs-lookup"><span data-stu-id="43c4a-140">WMV</span></span>
- <span data-ttu-id="43c4a-141">XLS</span><span class="sxs-lookup"><span data-stu-id="43c4a-141">XLS</span></span>
- <span data-ttu-id="43c4a-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="43c4a-142">XLSX</span></span>
- <span data-ttu-id="43c4a-143">XML</span><span class="sxs-lookup"><span data-stu-id="43c4a-143">XML</span></span>
- <span data-ttu-id="43c4a-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="43c4a-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="43c4a-145">Eine Datei hochladen</span><span class="sxs-lookup"><span data-stu-id="43c4a-145">Upload a file</span></span>

<span data-ttu-id="43c4a-146">Um eine Datei in den Commerce Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="43c4a-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="43c4a-147">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="43c4a-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="43c4a-148">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="43c4a-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="43c4a-149">Wählen Sie im Datei-Explorer eine oder mehrere Dateien aus und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="43c4a-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="43c4a-150">Geben Sie im Dialogfeld **Medienelement hochladen** Titel, Beschreibung und Schlüsselwort-Metadaten nach Bedarf ein.</span><span class="sxs-lookup"><span data-stu-id="43c4a-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="43c4a-151">Um die Datei(en) unmittelbar nach dem Hochladen zu veröffentlichen, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="43c4a-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="43c4a-152">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="43c4a-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43c4a-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43c4a-153">Additional resources</span></span>

[<span data-ttu-id="43c4a-154">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="43c4a-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="43c4a-155">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="43c4a-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="43c4a-156">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="43c4a-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="43c4a-157">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="43c4a-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="43c4a-158">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="43c4a-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="43c4a-159">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="43c4a-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

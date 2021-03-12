---
title: Hochladen von anderen Dateien als Bildern und Videos
description: In diesem Thema wird beschrieben, wie Sie andere Binärdateien als Bilder und Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
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
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995769"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="22b3f-103">Hochladen von anderen Dateien als Bildern und Videos</span><span class="sxs-lookup"><span data-stu-id="22b3f-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22b3f-104">In diesem Thema wird beschrieben, wie Sie andere Dateien als Bilder und Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="22b3f-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="22b3f-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="22b3f-105">Overview</span></span>

<span data-ttu-id="22b3f-106">Die Medienbibliothek des Commerce-Site-Builders unterstützt das Hochladen von anderen Binärdateien als Bildern oder Videos.</span><span class="sxs-lookup"><span data-stu-id="22b3f-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="22b3f-107">Beispielsweise können Sie Microsoft Excel, Microsoft Word, Microsoft PowerPoint oder PDF-Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="22b3f-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="22b3f-108">Die folgenden Dokumenttypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="22b3f-108">The following document types are supported:</span></span>
- <span data-ttu-id="22b3f-109">7Z</span><span class="sxs-lookup"><span data-stu-id="22b3f-109">7Z</span></span>
- <span data-ttu-id="22b3f-110">AVI</span><span class="sxs-lookup"><span data-stu-id="22b3f-110">AVI</span></span>
- <span data-ttu-id="22b3f-111">CS</span><span class="sxs-lookup"><span data-stu-id="22b3f-111">CS</span></span>
- <span data-ttu-id="22b3f-112">CSS</span><span class="sxs-lookup"><span data-stu-id="22b3f-112">CSS</span></span>
- <span data-ttu-id="22b3f-113">DOC</span><span class="sxs-lookup"><span data-stu-id="22b3f-113">DOC</span></span>
- <span data-ttu-id="22b3f-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="22b3f-114">DOCX</span></span>
- <span data-ttu-id="22b3f-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="22b3f-115">EPUB</span></span>
- <span data-ttu-id="22b3f-116">GIF</span><span class="sxs-lookup"><span data-stu-id="22b3f-116">GIF</span></span>
- <span data-ttu-id="22b3f-117">INDD</span><span class="sxs-lookup"><span data-stu-id="22b3f-117">INDD</span></span>
- <span data-ttu-id="22b3f-118">JAR</span><span class="sxs-lookup"><span data-stu-id="22b3f-118">JAR</span></span>
- <span data-ttu-id="22b3f-119">JPG</span><span class="sxs-lookup"><span data-stu-id="22b3f-119">JPG</span></span>
- <span data-ttu-id="22b3f-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="22b3f-120">JPEG</span></span>
- <span data-ttu-id="22b3f-121">JS</span><span class="sxs-lookup"><span data-stu-id="22b3f-121">JS</span></span>
- <span data-ttu-id="22b3f-122">MP3</span><span class="sxs-lookup"><span data-stu-id="22b3f-122">MP3</span></span>
- <span data-ttu-id="22b3f-123">MP4</span><span class="sxs-lookup"><span data-stu-id="22b3f-123">MP4</span></span>
- <span data-ttu-id="22b3f-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="22b3f-124">MPEG</span></span>
- <span data-ttu-id="22b3f-125">MPG</span><span class="sxs-lookup"><span data-stu-id="22b3f-125">MPG</span></span>
- <span data-ttu-id="22b3f-126">ODP</span><span class="sxs-lookup"><span data-stu-id="22b3f-126">ODP</span></span>
- <span data-ttu-id="22b3f-127">ODS</span><span class="sxs-lookup"><span data-stu-id="22b3f-127">ODS</span></span>
- <span data-ttu-id="22b3f-128">ODT</span><span class="sxs-lookup"><span data-stu-id="22b3f-128">ODT</span></span>
- <span data-ttu-id="22b3f-129">PDF</span><span class="sxs-lookup"><span data-stu-id="22b3f-129">PDF</span></span>
- <span data-ttu-id="22b3f-130">PNG</span><span class="sxs-lookup"><span data-stu-id="22b3f-130">PNG</span></span>
- <span data-ttu-id="22b3f-131">PPT</span><span class="sxs-lookup"><span data-stu-id="22b3f-131">PPT</span></span>
- <span data-ttu-id="22b3f-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="22b3f-132">PPTX</span></span>
- <span data-ttu-id="22b3f-133">PS</span><span class="sxs-lookup"><span data-stu-id="22b3f-133">PS</span></span>
- <span data-ttu-id="22b3f-134">QXP</span><span class="sxs-lookup"><span data-stu-id="22b3f-134">QXP</span></span>
- <span data-ttu-id="22b3f-135">RAR</span><span class="sxs-lookup"><span data-stu-id="22b3f-135">RAR</span></span>
- <span data-ttu-id="22b3f-136">RTF</span><span class="sxs-lookup"><span data-stu-id="22b3f-136">RTF</span></span>
- <span data-ttu-id="22b3f-137">SVG</span><span class="sxs-lookup"><span data-stu-id="22b3f-137">SVG</span></span>
- <span data-ttu-id="22b3f-138">TAR</span><span class="sxs-lookup"><span data-stu-id="22b3f-138">TAR</span></span>
- <span data-ttu-id="22b3f-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="22b3f-139">TGZ</span></span>
- <span data-ttu-id="22b3f-140">TXT</span><span class="sxs-lookup"><span data-stu-id="22b3f-140">TXT</span></span>
- <span data-ttu-id="22b3f-141">WMV</span><span class="sxs-lookup"><span data-stu-id="22b3f-141">WMV</span></span>
- <span data-ttu-id="22b3f-142">XLS</span><span class="sxs-lookup"><span data-stu-id="22b3f-142">XLS</span></span>
- <span data-ttu-id="22b3f-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="22b3f-143">XLSX</span></span>
- <span data-ttu-id="22b3f-144">XML</span><span class="sxs-lookup"><span data-stu-id="22b3f-144">XML</span></span>
- <span data-ttu-id="22b3f-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="22b3f-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="22b3f-146">Eine Datei hochladen</span><span class="sxs-lookup"><span data-stu-id="22b3f-146">Upload a file</span></span>

<span data-ttu-id="22b3f-147">Um eine Datei in den Commerce Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="22b3f-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="22b3f-148">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="22b3f-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="22b3f-149">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="22b3f-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="22b3f-150">Wählen Sie im Datei-Explorer eine oder mehrere Dateien aus und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="22b3f-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="22b3f-151">Geben Sie im Dialogfeld **Medienelement hochladen** Titel, Beschreibung und Schlüsselwort-Metadaten nach Bedarf ein.</span><span class="sxs-lookup"><span data-stu-id="22b3f-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="22b3f-152">Um die Datei(en) unmittelbar nach dem Hochladen zu veröffentlichen, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="22b3f-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="22b3f-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b3f-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22b3f-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="22b3f-154">Additional resources</span></span>

[<span data-ttu-id="22b3f-155">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="22b3f-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="22b3f-156">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="22b3f-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="22b3f-157">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="22b3f-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="22b3f-158">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="22b3f-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="22b3f-159">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="22b3f-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="22b3f-160">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="22b3f-160">Upload and serve static files</span></span>](upload-serve-static-files.md)

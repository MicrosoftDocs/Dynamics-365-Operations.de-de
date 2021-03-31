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
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222536"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="29ab5-103">Andere Dateien außer Bildern und Videos hochladen</span><span class="sxs-lookup"><span data-stu-id="29ab5-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="29ab5-104">In diesem Thema wird beschrieben, wie Sie andere Dateien als Bilder und Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="29ab5-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="29ab5-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="29ab5-105">Overview</span></span>

<span data-ttu-id="29ab5-106">Die Medienbibliothek des Commerce-Site-Builders unterstützt das Hochladen von anderen Binärdateien als Bildern oder Videos.</span><span class="sxs-lookup"><span data-stu-id="29ab5-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="29ab5-107">Beispielsweise können Sie Microsoft Excel, Microsoft Word, Microsoft PowerPoint oder PDF-Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="29ab5-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="29ab5-108">Die folgenden Dokumenttypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="29ab5-108">The following document types are supported:</span></span>
- <span data-ttu-id="29ab5-109">7Z</span><span class="sxs-lookup"><span data-stu-id="29ab5-109">7Z</span></span>
- <span data-ttu-id="29ab5-110">AVI</span><span class="sxs-lookup"><span data-stu-id="29ab5-110">AVI</span></span>
- <span data-ttu-id="29ab5-111">CS</span><span class="sxs-lookup"><span data-stu-id="29ab5-111">CS</span></span>
- <span data-ttu-id="29ab5-112">CSS</span><span class="sxs-lookup"><span data-stu-id="29ab5-112">CSS</span></span>
- <span data-ttu-id="29ab5-113">DOC</span><span class="sxs-lookup"><span data-stu-id="29ab5-113">DOC</span></span>
- <span data-ttu-id="29ab5-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="29ab5-114">DOCX</span></span>
- <span data-ttu-id="29ab5-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="29ab5-115">EPUB</span></span>
- <span data-ttu-id="29ab5-116">GIF</span><span class="sxs-lookup"><span data-stu-id="29ab5-116">GIF</span></span>
- <span data-ttu-id="29ab5-117">INDD</span><span class="sxs-lookup"><span data-stu-id="29ab5-117">INDD</span></span>
- <span data-ttu-id="29ab5-118">JAR</span><span class="sxs-lookup"><span data-stu-id="29ab5-118">JAR</span></span>
- <span data-ttu-id="29ab5-119">JPG</span><span class="sxs-lookup"><span data-stu-id="29ab5-119">JPG</span></span>
- <span data-ttu-id="29ab5-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="29ab5-120">JPEG</span></span>
- <span data-ttu-id="29ab5-121">JS</span><span class="sxs-lookup"><span data-stu-id="29ab5-121">JS</span></span>
- <span data-ttu-id="29ab5-122">MP3</span><span class="sxs-lookup"><span data-stu-id="29ab5-122">MP3</span></span>
- <span data-ttu-id="29ab5-123">MP4</span><span class="sxs-lookup"><span data-stu-id="29ab5-123">MP4</span></span>
- <span data-ttu-id="29ab5-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="29ab5-124">MPEG</span></span>
- <span data-ttu-id="29ab5-125">MPG</span><span class="sxs-lookup"><span data-stu-id="29ab5-125">MPG</span></span>
- <span data-ttu-id="29ab5-126">ODP</span><span class="sxs-lookup"><span data-stu-id="29ab5-126">ODP</span></span>
- <span data-ttu-id="29ab5-127">ODS</span><span class="sxs-lookup"><span data-stu-id="29ab5-127">ODS</span></span>
- <span data-ttu-id="29ab5-128">ODT</span><span class="sxs-lookup"><span data-stu-id="29ab5-128">ODT</span></span>
- <span data-ttu-id="29ab5-129">PDF</span><span class="sxs-lookup"><span data-stu-id="29ab5-129">PDF</span></span>
- <span data-ttu-id="29ab5-130">PNG</span><span class="sxs-lookup"><span data-stu-id="29ab5-130">PNG</span></span>
- <span data-ttu-id="29ab5-131">PPT</span><span class="sxs-lookup"><span data-stu-id="29ab5-131">PPT</span></span>
- <span data-ttu-id="29ab5-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="29ab5-132">PPTX</span></span>
- <span data-ttu-id="29ab5-133">PS</span><span class="sxs-lookup"><span data-stu-id="29ab5-133">PS</span></span>
- <span data-ttu-id="29ab5-134">QXP</span><span class="sxs-lookup"><span data-stu-id="29ab5-134">QXP</span></span>
- <span data-ttu-id="29ab5-135">RAR</span><span class="sxs-lookup"><span data-stu-id="29ab5-135">RAR</span></span>
- <span data-ttu-id="29ab5-136">RTF</span><span class="sxs-lookup"><span data-stu-id="29ab5-136">RTF</span></span>
- <span data-ttu-id="29ab5-137">SVG</span><span class="sxs-lookup"><span data-stu-id="29ab5-137">SVG</span></span>
- <span data-ttu-id="29ab5-138">TAR</span><span class="sxs-lookup"><span data-stu-id="29ab5-138">TAR</span></span>
- <span data-ttu-id="29ab5-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="29ab5-139">TGZ</span></span>
- <span data-ttu-id="29ab5-140">TXT</span><span class="sxs-lookup"><span data-stu-id="29ab5-140">TXT</span></span>
- <span data-ttu-id="29ab5-141">WMV</span><span class="sxs-lookup"><span data-stu-id="29ab5-141">WMV</span></span>
- <span data-ttu-id="29ab5-142">XLS</span><span class="sxs-lookup"><span data-stu-id="29ab5-142">XLS</span></span>
- <span data-ttu-id="29ab5-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="29ab5-143">XLSX</span></span>
- <span data-ttu-id="29ab5-144">XML</span><span class="sxs-lookup"><span data-stu-id="29ab5-144">XML</span></span>
- <span data-ttu-id="29ab5-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="29ab5-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="29ab5-146">Eine Datei hochladen</span><span class="sxs-lookup"><span data-stu-id="29ab5-146">Upload a file</span></span>

<span data-ttu-id="29ab5-147">Um eine Datei in den Commerce Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="29ab5-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="29ab5-148">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="29ab5-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="29ab5-149">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="29ab5-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="29ab5-150">Wählen Sie im Datei-Explorer eine oder mehrere Dateien aus und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="29ab5-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="29ab5-151">Geben Sie im Dialogfeld **Medienelement hochladen** Titel, Beschreibung und Schlüsselwort-Metadaten nach Bedarf ein.</span><span class="sxs-lookup"><span data-stu-id="29ab5-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="29ab5-152">Um die Datei(en) unmittelbar nach dem Hochladen zu veröffentlichen, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="29ab5-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="29ab5-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="29ab5-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29ab5-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="29ab5-154">Additional resources</span></span>

[<span data-ttu-id="29ab5-155">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="29ab5-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="29ab5-156">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="29ab5-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="29ab5-157">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="29ab5-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="29ab5-158">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="29ab5-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="29ab5-159">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="29ab5-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="29ab5-160">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="29ab5-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
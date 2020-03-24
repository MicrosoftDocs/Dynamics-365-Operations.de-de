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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097018"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="71686-103">Hochladen von anderen Dateien als Bildern und Videos</span><span class="sxs-lookup"><span data-stu-id="71686-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71686-104">In diesem Thema wird beschrieben, wie Sie andere Dateien als Bilder und Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="71686-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="71686-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="71686-105">Overview</span></span>

<span data-ttu-id="71686-106">Die Medienbibliothek des Commerce-Site-Builders unterstützt das Hochladen von anderen Binärdateien als Bildern oder Videos.</span><span class="sxs-lookup"><span data-stu-id="71686-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="71686-107">Beispielsweise können Sie Microsoft Excel, Microsoft Word, Microsoft PowerPoint oder PDF-Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="71686-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="71686-108">Die folgenden Dokumenttypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="71686-108">The following document types are supported:</span></span>
- <span data-ttu-id="71686-109">7Z</span><span class="sxs-lookup"><span data-stu-id="71686-109">7Z</span></span>
- <span data-ttu-id="71686-110">AVI</span><span class="sxs-lookup"><span data-stu-id="71686-110">AVI</span></span>
- <span data-ttu-id="71686-111">CS</span><span class="sxs-lookup"><span data-stu-id="71686-111">CS</span></span>
- <span data-ttu-id="71686-112">CSS</span><span class="sxs-lookup"><span data-stu-id="71686-112">CSS</span></span>
- <span data-ttu-id="71686-113">DOC</span><span class="sxs-lookup"><span data-stu-id="71686-113">DOC</span></span>
- <span data-ttu-id="71686-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="71686-114">DOCX</span></span>
- <span data-ttu-id="71686-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="71686-115">EPUB</span></span>
- <span data-ttu-id="71686-116">GIF</span><span class="sxs-lookup"><span data-stu-id="71686-116">GIF</span></span>
- <span data-ttu-id="71686-117">INDD</span><span class="sxs-lookup"><span data-stu-id="71686-117">INDD</span></span>
- <span data-ttu-id="71686-118">JAR</span><span class="sxs-lookup"><span data-stu-id="71686-118">JAR</span></span>
- <span data-ttu-id="71686-119">JPG</span><span class="sxs-lookup"><span data-stu-id="71686-119">JPG</span></span>
- <span data-ttu-id="71686-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="71686-120">JPEG</span></span>
- <span data-ttu-id="71686-121">JS</span><span class="sxs-lookup"><span data-stu-id="71686-121">JS</span></span>
- <span data-ttu-id="71686-122">MP3</span><span class="sxs-lookup"><span data-stu-id="71686-122">MP3</span></span>
- <span data-ttu-id="71686-123">MP4</span><span class="sxs-lookup"><span data-stu-id="71686-123">MP4</span></span>
- <span data-ttu-id="71686-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="71686-124">MPEG</span></span>
- <span data-ttu-id="71686-125">MPG</span><span class="sxs-lookup"><span data-stu-id="71686-125">MPG</span></span>
- <span data-ttu-id="71686-126">ODP</span><span class="sxs-lookup"><span data-stu-id="71686-126">ODP</span></span>
- <span data-ttu-id="71686-127">ODS</span><span class="sxs-lookup"><span data-stu-id="71686-127">ODS</span></span>
- <span data-ttu-id="71686-128">ODT</span><span class="sxs-lookup"><span data-stu-id="71686-128">ODT</span></span>
- <span data-ttu-id="71686-129">PDF</span><span class="sxs-lookup"><span data-stu-id="71686-129">PDF</span></span>
- <span data-ttu-id="71686-130">PNG</span><span class="sxs-lookup"><span data-stu-id="71686-130">PNG</span></span>
- <span data-ttu-id="71686-131">PPT</span><span class="sxs-lookup"><span data-stu-id="71686-131">PPT</span></span>
- <span data-ttu-id="71686-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="71686-132">PPTX</span></span>
- <span data-ttu-id="71686-133">PS</span><span class="sxs-lookup"><span data-stu-id="71686-133">PS</span></span>
- <span data-ttu-id="71686-134">QXP</span><span class="sxs-lookup"><span data-stu-id="71686-134">QXP</span></span>
- <span data-ttu-id="71686-135">RAR</span><span class="sxs-lookup"><span data-stu-id="71686-135">RAR</span></span>
- <span data-ttu-id="71686-136">RTF</span><span class="sxs-lookup"><span data-stu-id="71686-136">RTF</span></span>
- <span data-ttu-id="71686-137">SVG</span><span class="sxs-lookup"><span data-stu-id="71686-137">SVG</span></span>
- <span data-ttu-id="71686-138">TAR</span><span class="sxs-lookup"><span data-stu-id="71686-138">TAR</span></span>
- <span data-ttu-id="71686-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="71686-139">TGZ</span></span>
- <span data-ttu-id="71686-140">TXT</span><span class="sxs-lookup"><span data-stu-id="71686-140">TXT</span></span>
- <span data-ttu-id="71686-141">WMV</span><span class="sxs-lookup"><span data-stu-id="71686-141">WMV</span></span>
- <span data-ttu-id="71686-142">XLS</span><span class="sxs-lookup"><span data-stu-id="71686-142">XLS</span></span>
- <span data-ttu-id="71686-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="71686-143">XLSX</span></span>
- <span data-ttu-id="71686-144">XML</span><span class="sxs-lookup"><span data-stu-id="71686-144">XML</span></span>
- <span data-ttu-id="71686-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="71686-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="71686-146">Eine Datei hochladen</span><span class="sxs-lookup"><span data-stu-id="71686-146">Upload a file</span></span>

<span data-ttu-id="71686-147">Um eine Datei in den Commerce Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="71686-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="71686-148">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="71686-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="71686-149">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="71686-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="71686-150">Wählen Sie im Datei-Explorer eine oder mehrere Dateien aus und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="71686-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="71686-151">Geben Sie im Dialogfeld **Medienelement hochladen** Titel, Beschreibung und Schlüsselwort-Metadaten nach Bedarf ein.</span><span class="sxs-lookup"><span data-stu-id="71686-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="71686-152">Um die Datei(en) unmittelbar nach dem Hochladen zu veröffentlichen, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="71686-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="71686-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71686-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71686-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="71686-154">Additional resources</span></span>

[<span data-ttu-id="71686-155">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="71686-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="71686-156">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="71686-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="71686-157">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="71686-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="71686-158">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="71686-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="71686-159">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="71686-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

---
title: Bilder hochladen
description: In diesem Thema wird beschrieben, wie Sie Bilder in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
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
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594283"
---
# <a name="upload-images"></a><span data-ttu-id="28eb0-103">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="28eb0-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="28eb0-104">In diesem Thema wird beschrieben, wie Sie Bilder in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="28eb0-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="28eb0-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="28eb0-105">Overview</span></span>

<span data-ttu-id="28eb0-106">Die Medienbibliothek des Commerce-Site-Builders ermöglicht Ihnen das Hochladen von Bildern, entweder einzeln oder in großen Mengen mit Hilfe von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="28eb0-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="28eb0-107">Sie sollten immer die Version des Bildes mit der höchsten Auflösung und Qualität hochladen, da die Image Resizer-Komponente das Bild automatisch für verschiedene Ansichtsfenster und deren Haltepunkte optimiert.</span><span class="sxs-lookup"><span data-stu-id="28eb0-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="28eb0-108">Während des Uploads angegebene Bildinformationen</span><span class="sxs-lookup"><span data-stu-id="28eb0-108">Image information specified during upload</span></span>

<span data-ttu-id="28eb0-109">Beim Hochladen eines Bildes können die folgenden Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="28eb0-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="28eb0-110">**Titel, Alt-Text, Beschreibung, Schlüsselwörter**: Metadaten des Bildes oder der Bilder.</span><span class="sxs-lookup"><span data-stu-id="28eb0-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="28eb0-111">Titel und Alt-Text sind Pflichtwerte.</span><span class="sxs-lookup"><span data-stu-id="28eb0-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="28eb0-112">**Kategorie auswählen**:</span><span class="sxs-lookup"><span data-stu-id="28eb0-112">**Select category**:</span></span>
    - <span data-ttu-id="28eb0-113">**Keine**: Wird für ein E-Commerce-Storytelling-Bild oder -Bilder verwendet.</span><span class="sxs-lookup"><span data-stu-id="28eb0-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="28eb0-114">**Produkt, Kategorie, Kunde, Mitarbeiter, Katalog**: Wird für Dynamics 365 Commerce Omni-Channel-Bild oder -Bilder verwendet.</span><span class="sxs-lookup"><span data-stu-id="28eb0-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="28eb0-115">**Assets nach dem Hochladen veröffentlichen**: Wenn dieses Kontrollkästchen aktiviert ist, werden das Bild oder die Bilder sofort nach dem Hochladen veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="28eb0-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="28eb0-116">Bild-Assets mit einer zugewiesenen Kategorie werden auch automatisch mit der Kategorie als Schlüsselwort versehen, um die Suche nach Assets einer bestimmten Kategorie zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="28eb0-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="28eb0-117">Namenskonventionen für Omni-Channel-Bilder</span><span class="sxs-lookup"><span data-stu-id="28eb0-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="28eb0-118">Wenn Sie die Medienbibliothek als Omni-Channel-Bild-Backend konfiguriert haben, können Sie über Bildkategorien angeben, zu welcher Kategorie das hochgeladene Bild gehört.</span><span class="sxs-lookup"><span data-stu-id="28eb0-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="28eb0-119">Es gibt auch eine Namenskonvention, die befolgt werden sollte, um sicherzustellen, dass die Bilder von anderen Kanälen, wie z.B. dem Point-of-Sale (POS), korrekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="28eb0-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="28eb0-120">Die Standardnamenskonvention variiert je nach Kategorie:</span><span class="sxs-lookup"><span data-stu-id="28eb0-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="28eb0-121">Katalogbilder sollten „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“ benannt werden</span><span class="sxs-lookup"><span data-stu-id="28eb0-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="28eb0-122">Kategoriebilder sollten „**/Categories/\{CategoryName\}.png**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="28eb0-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="28eb0-123">Kundenbilder sollten „**/Customers/\{CustomerNumber\}.jpg**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="28eb0-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="28eb0-124">Bilder von Mitarbeitern sollten „**/Workers/\{WorkerNumber\}.jpg**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="28eb0-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="28eb0-125">Produktbilder sollten „**/Products/\{ProductNumber\}_000_001.png**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="28eb0-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="28eb0-126">001 ist die Bildfolge und kann 001, 002, 003, 004 oder 005 sein</span><span class="sxs-lookup"><span data-stu-id="28eb0-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="28eb0-127">Produktvariantenbilder sollten „**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="28eb0-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="28eb0-128">Ein Bild hochladen</span><span class="sxs-lookup"><span data-stu-id="28eb0-128">Upload an image</span></span>

<span data-ttu-id="28eb0-129">Um ein Bild in Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="28eb0-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="28eb0-130">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="28eb0-131">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="28eb0-132">Navigieren Sie im Fenster Datei-Explorer zu einer oder mehreren Bilddateien, die Sie hochladen möchten, und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="28eb0-133">Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.</span><span class="sxs-lookup"><span data-stu-id="28eb0-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="28eb0-134">Geben Sie eine optionale Beschreibung und Schlüsselwörter ein und wählen Sie eine Kategorie aus, falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="28eb0-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="28eb0-135">Wenn Sie das/die Bild(er) unmittelbar nach dem Upload veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Upload veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="28eb0-136">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="28eb0-137">Einen Ordner mit Bildern hochladen</span><span class="sxs-lookup"><span data-stu-id="28eb0-137">Upload a folder of images</span></span>

<span data-ttu-id="28eb0-138">Gehen Sie folgendermaßen vor, um einen Ordner mit Bildern in Site Builder hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="28eb0-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="28eb0-139">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="28eb0-140">Wählen Sie in der Befehlsleiste **Upload \> Upload-Ordner**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="28eb0-141">Navigieren Sie im Datei-Explorer-Fenster zu einem Ordner, den Sie hochladen möchten, und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="28eb0-142">Geben Sie im Dialogfenster **Medienelemente hochladen** optionale Schlüsselwörter ein und wählen Sie, falls gewünscht, eine Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="28eb0-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="28eb0-143">Wenn Sie die Bilder in dem Ordner unmittelbar nach dem Hochladen veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="28eb0-144">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28eb0-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28eb0-145">Additional resources</span></span>

[<span data-ttu-id="28eb0-146">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="28eb0-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="28eb0-147">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="28eb0-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="28eb0-148">Dateien hochladen</span><span class="sxs-lookup"><span data-stu-id="28eb0-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="28eb0-149">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="28eb0-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="28eb0-150">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="28eb0-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="28eb0-151">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="28eb0-151">Upload and serve static files</span></span>](upload-serve-static-files.md)

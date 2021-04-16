---
title: Bilder hochladen
description: In diesem Thema wird beschrieben, wie Sie Bilder in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799228"
---
# <a name="upload-images"></a><span data-ttu-id="5b43c-103">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="5b43c-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b43c-104">In diesem Thema wird beschrieben, wie Sie Bilder in Microsoft Dynamics 365 Commerce Site Builder hochladen können.</span><span class="sxs-lookup"><span data-stu-id="5b43c-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="5b43c-105">Die Medienbibliothek des Commerce-Site-Builders ermöglicht Ihnen das Hochladen von Bildern, entweder einzeln oder in großen Mengen mit Hilfe von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="5b43c-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="5b43c-106">Sie sollten immer die Version des Bildes mit der höchsten Auflösung und Qualität hochladen, da die Image Resizer-Komponente das Bild automatisch für verschiedene Ansichtsfenster und deren Haltepunkte optimiert.</span><span class="sxs-lookup"><span data-stu-id="5b43c-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="5b43c-107">Während des Uploads angegebene Bildinformationen</span><span class="sxs-lookup"><span data-stu-id="5b43c-107">Image information specified during upload</span></span>

<span data-ttu-id="5b43c-108">Beim Hochladen eines Bildes können die folgenden Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b43c-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="5b43c-109">**Titel, Alt-Text, Beschreibung, Schlüsselwörter**: Metadaten des Bildes oder der Bilder.</span><span class="sxs-lookup"><span data-stu-id="5b43c-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="5b43c-110">Titel und Alt-Text sind Pflichtwerte.</span><span class="sxs-lookup"><span data-stu-id="5b43c-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="5b43c-111">**Kategorie auswählen**:</span><span class="sxs-lookup"><span data-stu-id="5b43c-111">**Select category**:</span></span>
    - <span data-ttu-id="5b43c-112">**Keine**: Wird für ein E-Commerce-Storytelling-Bild oder -Bilder verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b43c-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="5b43c-113">**Produkt, Kategorie, Kunde, Mitarbeiter, Katalog**: Wird für Dynamics 365 Commerce Omni-Channel-Bild oder -Bilder verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b43c-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="5b43c-114">**Assets nach dem Hochladen veröffentlichen**: Wenn dieses Kontrollkästchen aktiviert ist, werden das Bild oder die Bilder sofort nach dem Hochladen veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="5b43c-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="5b43c-115">Bild-Assets mit einer zugewiesenen Kategorie werden auch automatisch mit der Kategorie als Schlüsselwort versehen, um die Suche nach Assets einer bestimmten Kategorie zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="5b43c-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="5b43c-116">Namenskonventionen für Omni-Channel-Bilder</span><span class="sxs-lookup"><span data-stu-id="5b43c-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="5b43c-117">Wenn Sie die Medienbibliothek als Omni-Channel-Bild-Backend konfiguriert haben, können Sie über Bildkategorien angeben, zu welcher Kategorie das hochgeladene Bild gehört.</span><span class="sxs-lookup"><span data-stu-id="5b43c-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="5b43c-118">Es gibt auch eine Namenskonvention, die befolgt werden sollte, um sicherzustellen, dass die Bilder von anderen Kanälen, wie z.B. dem Point-of-Sale (POS), korrekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5b43c-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="5b43c-119">Die Standardnamenskonvention variiert je nach Kategorie:</span><span class="sxs-lookup"><span data-stu-id="5b43c-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="5b43c-120">Katalogbilder sollten „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“ benannt werden</span><span class="sxs-lookup"><span data-stu-id="5b43c-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="5b43c-121">Kategoriebilder sollten „**/Categories/\{CategoryName\}.png**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="5b43c-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="5b43c-122">Kundenbilder sollten „**/Customers/\{CustomerNumber\}.jpg**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="5b43c-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="5b43c-123">Bilder von Mitarbeitern sollten „**/Workers/\{WorkerNumber\}.jpg**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="5b43c-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="5b43c-124">Produktbilder sollten „**/Products/\{ProductNumber\}_000_001.png**“ genannt werden</span><span class="sxs-lookup"><span data-stu-id="5b43c-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="5b43c-125">001 ist die Bildfolge und kann 001, 002, 003, 004 oder 005 sein</span><span class="sxs-lookup"><span data-stu-id="5b43c-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="5b43c-126">Produktvariantenbilder sollten „**/Produkte/\{Produktnummer\} \^ \{Stil\} \^ \{Größe\} \^ \{Farbe\} \^\_000_001.png**“ benannt werden.</span><span class="sxs-lookup"><span data-stu-id="5b43c-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="5b43c-127">Zum Beispiel: 93039 \^ \^ 2 \^ Schwarz \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="5b43c-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="5b43c-128">Ein Bild hochladen</span><span class="sxs-lookup"><span data-stu-id="5b43c-128">Upload an image</span></span>

<span data-ttu-id="5b43c-129">Um ein Bild in Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="5b43c-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5b43c-130">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="5b43c-131">Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="5b43c-132">Navigieren Sie im Fenster Datei-Explorer zu einer oder mehreren Bilddateien, die Sie hochladen möchten, und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="5b43c-133">Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.</span><span class="sxs-lookup"><span data-stu-id="5b43c-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="5b43c-134">Geben Sie eine optionale Beschreibung und Schlüsselwörter ein und wählen Sie eine Kategorie aus, falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="5b43c-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="5b43c-135">Wenn Sie das/die Bild(er) unmittelbar nach dem Upload veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Upload veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="5b43c-136">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="5b43c-137">Einen Ordner mit Bildern hochladen</span><span class="sxs-lookup"><span data-stu-id="5b43c-137">Upload a folder of images</span></span>

<span data-ttu-id="5b43c-138">Gehen Sie folgendermaßen vor, um einen Ordner mit Bildern in Site Builder hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="5b43c-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5b43c-139">Wählen Sie im linken Navigationsbereich **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="5b43c-140">Wählen Sie in der Befehlsleiste **Upload \> Upload-Ordner**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="5b43c-141">Navigieren Sie im Datei-Explorer-Fenster zu einem Ordner, den Sie hochladen möchten, und wählen Sie dann **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="5b43c-142">Geben Sie im Dialogfenster **Medienelemente hochladen** optionale Schlüsselwörter ein und wählen Sie, falls gewünscht, eine Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="5b43c-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="5b43c-143">Wenn Sie die Bilder in dem Ordner unmittelbar nach dem Hochladen veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="5b43c-144">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b43c-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b43c-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b43c-145">Additional resources</span></span>

[<span data-ttu-id="5b43c-146">Übersicht über die Verwaltung der digitalen Assets</span><span class="sxs-lookup"><span data-stu-id="5b43c-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="5b43c-147">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="5b43c-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="5b43c-148">Dateien hochladen</span><span class="sxs-lookup"><span data-stu-id="5b43c-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="5b43c-149">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="5b43c-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="5b43c-150">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="5b43c-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="5b43c-151">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="5b43c-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Bild-Brennpunkte anpassen
description: In diesem Thema wird beschrieben, wie die Bildfokuspunkte in Microsoft Dynamics 365 Commerce Site Builder angepasst werden können.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: b20fbc20f18243c712595795a0b16ae417e755e6
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594331"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="6a7c7-103">Bild-Brennpunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a7c7-104">In diesem Thema wird beschrieben, wie die Bildfokuspunkte in Microsoft Dynamics 365 Commerce Site Builder angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="6a7c7-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6a7c7-105">Overview</span></span>

<span data-ttu-id="6a7c7-106">Wenn ein Bild in die Medienbibliothek des Commerce-Site-Builders hochgeladen wird, versucht das System, den Brennpunkt des Bildes zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="6a7c7-107">Wenn sich beispielsweise eine Person auf dem Bild befindet, setzt das System den Fokus standardmäßig auf das Gesicht der Person.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="6a7c7-108">In den meisten Fällen funktioniert der automatisch gesetzte Fokuspunkt für alle Ansichtsfenster gut, aber manchmal möchten Sie den Fokuspunkt vielleicht anpassen, um sicherzustellen, dass ein bestimmter Teil des Bildes immer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="6a7c7-109">Definieren Sie einen benutzerdefinierten Brennpunkt für ein Bild</span><span class="sxs-lookup"><span data-stu-id="6a7c7-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="6a7c7-110">Um einen benutzerdefinierten Brennpunkt für ein Bild zu definieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="6a7c7-111">Wählen Sie im linken Navigationsbereich des Commerce Site Builders **Medienbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="6a7c7-112">Wählen Sie im Hauptfenster das Bild aus, das Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="6a7c7-113">Wählen Sie in der Befehlsleiste **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="6a7c7-114">Wählen Sie das Bild aus, um **Bearbeitungsmodus** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="6a7c7-115">Wählen Sie unter **Bearbeitungsmodus** **Fokuspunkt ändern**.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="6a7c7-116">Ein kreisförmiger Brennpunktregler erscheint über dem Bild.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="6a7c7-117">Wählen Sie das Fokussierpunkt-Steuerelement, um es über den gewünschten Fokuspunkt zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="6a7c7-118">Wenn Sie fertig sind, wählen Sie in der Befehlsleiste **Speichern** und wählen Sie dann **Bearbeitung beenden**.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a7c7-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-119">Additional resources</span></span>

[<span data-ttu-id="6a7c7-120">Überblick über die Verwaltung digitaler Anlagen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="6a7c7-121">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="6a7c7-122">Video hochladen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="6a7c7-123">Dateien hochladen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="6a7c7-124">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="6a7c7-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="6a7c7-125">Statische Dateien hochladen und bedienen</span><span class="sxs-lookup"><span data-stu-id="6a7c7-125">Upload and serve static files</span></span>](upload-serve-static-files.md)

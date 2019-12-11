---
title: Hinzufügen eines Favicons
description: In diesem Thema wird erläutert, wie ein favicon der Site hinzufügt wird.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696990"
---
# <a name="add-a-favicon"></a><span data-ttu-id="41044-103">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="41044-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="41044-104">In diesem Thema wird erläutert, wie ein favicon der Site hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="41044-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="41044-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="41044-105">Overview</span></span>

<span data-ttu-id="41044-106">Ein favicon ist eine kleine Grafikdatei, die auf einer Webbrowserregisterkarte im Browserverlauf der Adressleiste sowie in Lesezeichen oder in den Favoriten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="41044-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="41044-107">Es wird empfohlen, ein favicon dem Standort hinzufügen, da es Ihre Marke darstellt und verstärkt und hilft, den Standort von anderen Websites, die Ihre Kunden suchen, zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="41044-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="41044-108">Zwar können Sie mehrere favicons von verschiedenen Größen und Dateitypen Ihrem Standort hinzufügen, dieses Thema behandelt lediglich das Hinzufügen von einem einzelnen favicon.</span><span class="sxs-lookup"><span data-stu-id="41044-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="41044-109">Allerdings werden der gleiche Prozess und Ort verwendet, um weitere favicons hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="41044-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="41044-110">Laden Sie ein favicon in die Anlagensammlung Ihrer Site hoch</span><span class="sxs-lookup"><span data-stu-id="41044-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="41044-111">Um ein favicon aus der Anlagensammlung zu entfernen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="41044-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="41044-112">Gehen Sie zu **Anlagen \> Hochladen \> Anlagen hochladen**.</span><span class="sxs-lookup"><span data-stu-id="41044-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="41044-113">Suchen und wählen Sie das favicon auf dem lokalen Dateisystem aus.</span><span class="sxs-lookup"><span data-stu-id="41044-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="41044-114">Geben Sie einen Betreff ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="41044-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="41044-115">Im Eigenschaftenbereich auf der rechten Seite, kopieren Sie die öffentliche URL des favicon.</span><span class="sxs-lookup"><span data-stu-id="41044-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="41044-116">Wenn Sie **Anlagen nach den Hochladen veröffentlichen** auswählen, müssen Sie auf die Seite **Anlagen** zurückkehren und das favicon später manuell veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="41044-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="41044-117">Erstellen Sie das HTML für das favicon</span><span class="sxs-lookup"><span data-stu-id="41044-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="41044-118">Um das HTML für das favicon zu erstellen, verwenden Sie den folgenden HTML-Ausschnitt.</span><span class="sxs-lookup"><span data-stu-id="41044-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="41044-119">Für **href** ersetzen Sie das Attribut **„Öffentliche\_URL\_für\_Ihr\_favicon“** durch die öffentliche URL, die Sie eben kopierten.</span><span class="sxs-lookup"><span data-stu-id="41044-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="41044-120">Fügen Sie die HTML für das favicon dem \<Kopf\>-Element der Seiten hinzu</span><span class="sxs-lookup"><span data-stu-id="41044-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="41044-121">Um einen favicon dem Standort hinzuzufügen, nutzen Sie dasselbe Verfahren, das verwendet wird, um einen Typ HTML- oder Skriptelement dem **\<Kopf\>** der Standortsseiten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="41044-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41044-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41044-122">Additional resources</span></span>

[<span data-ttu-id="41044-123">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="41044-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="41044-124">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="41044-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="41044-125">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="41044-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="41044-126">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="41044-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="41044-127">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="41044-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="41044-128">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="41044-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


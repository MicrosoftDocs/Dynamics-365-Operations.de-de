---
title: Statische Dateien hochladen und bereitstellen
description: In diesem Thema wird beschrieben, wie Sie eine statische Datei im Microsoft Dynamics 365 Commerce Site Builder hochladen, und wie Sie eine benutzerdefinierte URL und Dateiname erstellen, die für die Anforderung dieser Datei verwendet werden können.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: aba9dde2ed9d5fa09e92fcdd784a53f208930eda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211018"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="6d842-103">Statische Dateien hochladen und bereitstellen</span><span class="sxs-lookup"><span data-stu-id="6d842-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6d842-104">In diesem Thema wird beschrieben, wie Sie eine statische Datei im Microsoft Dynamics 365 Commerce Site Builder hochladen, und wie Sie eine benutzerdefinierte URL und Dateiname erstellen, die für die Anforderung dieser Datei verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6d842-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="6d842-105">Bei einigen Connectors von Drittanbietern muss eine Datei von der E-Commerce-Website gehostet und von ihr aus bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d842-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="6d842-106">Diese Connectors erwarten, dass die Datei durch Anforderungen an einen bestimmten Rückruf-URL-Pfad und Dateinamen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d842-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="6d842-107">In diesem Thema wird daher erläutert, wie Sie eine statische Datei mit einer benutzerdefinierbaren URL und einem Dateinamen auf eine statische Dynamics 365 Commerce-E-Commerce-Website hochladen und auf dieser bedienen.</span><span class="sxs-lookup"><span data-stu-id="6d842-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="6d842-108">Eine Website-URL erstellen, die eine statische Datei zurückgibt</span><span class="sxs-lookup"><span data-stu-id="6d842-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="6d842-109">Führen Sie diese Schritte aus, um eine Website-URL zu erstellen, die eine statische Datei im Commerce-Website-Generator zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6d842-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6d842-110">Wechseln Sie zur Medienbibliothek Ihrer Website und laden Sie die Datei hoch, die durch Anforderungen an die URL bedient werden soll, die Sie definieren werden.</span><span class="sxs-lookup"><span data-stu-id="6d842-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="6d842-111">Wenn Sie die Datei bereits hochgeladen haben, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="6d842-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="6d842-112">Wechseln Sie zu **URLs** für Ihre Website.</span><span class="sxs-lookup"><span data-stu-id="6d842-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="6d842-113">Wählen Sie **Neu \> Neue URL** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="6d842-114">Im Dialogfeld **Neue URL** wählen Sie **Medienbibliotheksobjekt** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="6d842-115">Geben Sie im Feld **URL-Pfad** den URL-Pfad ein.</span><span class="sxs-lookup"><span data-stu-id="6d842-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="6d842-116">Fügen Sie den Dateinamen in den Pfad ein.</span><span class="sxs-lookup"><span data-stu-id="6d842-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="6d842-117">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="6d842-117">Select **Next**.</span></span> <span data-ttu-id="6d842-118">Die Medienbibliothek wird geöffnet und zeigt alle Medienobjekte des Typs **Dokument** an, die hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="6d842-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="6d842-119">Wählen Sie die Datei aus, die für Anforderungen an die von Ihnen in Schritt 5 definierte URL bedient werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d842-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="6d842-120">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-120">Select **Save**.</span></span>

<span data-ttu-id="6d842-121">An diesem Punkt ist die URL, die Sie erstellt haben, in einem Entwurfzustand.</span><span class="sxs-lookup"><span data-stu-id="6d842-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="6d842-122">Die Datei, auf die die URL verweist, wird erst zurückgegeben, wenn Sie die URL veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6d842-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="6d842-123">Bevor Sie die URL veröffentlichen, können Sie überprüfen, ob sie die richtigen Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6d842-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="6d842-124">Eine URL überprüfen und veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="6d842-124">Validate and publish a URL</span></span>

<span data-ttu-id="6d842-125">Gehen Sie folgendermaßen vor, um eine URL zu überprüfen, bevor Sie diese veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6d842-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="6d842-126">Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL für die Vorschau aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="6d842-127">Im Eigenschaftenbereich rechts unter der Schaltfläche **Bearbeiten** wählen Sie den richtigen URL-Link aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="6d842-128">Ein neues Browserfenster wird geöffnet und Sie sollten einen Fehler 404 erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d842-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="6d842-129">Fügen Sie die Abfragezeichenfolge **?preview=inprogress** an die URL an (z. B. `https://yoursite.com/callback.html?preview=inprogress`) und laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="6d842-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="6d842-130">Die Datei, die Sie in die Medienbibliothek hochgeladen haben, sollte in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6d842-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="6d842-131">Nachdem Sie die URL überprüft haben, können Sie sie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6d842-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="6d842-132">Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="6d842-133">Wählen Sie in der Befehlsleiste **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="6d842-134">Aktualisieren Sie die Datei, auf die eine URL verweist</span><span class="sxs-lookup"><span data-stu-id="6d842-134">Update the file that a URL points to</span></span>

<span data-ttu-id="6d842-135">Nachdem eine URL veröffentlicht wurde, können Sie sie aktualisieren, sodass sie auf eine andere Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="6d842-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="6d842-136">Alternativ können Sie die URL aktualisieren, damit sie auf einen anderen Ressourcentyp zeigt, wie im nächsten Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6d842-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="6d842-137">Sie können zum Beispiel mit der URL auf eine interne Seite oder eine Umleitung zeigen.</span><span class="sxs-lookup"><span data-stu-id="6d842-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="6d842-138">Führen Sie die folgenden Schritte aus, um die Datei zu aktualisieren, auf die eine URL zeigt.</span><span class="sxs-lookup"><span data-stu-id="6d842-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="6d842-139">Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL für die Aktualisierung aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="6d842-140">Wählen Sie im Eigenschaftenbereich rechts **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="6d842-141">Unter **URL-Zuweisung**, aktivieren Sie das Feld **Schritt 2** und wählen Sie dann ein neues Dokument aus der Medienbibliothek aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="6d842-142">Wählen Sie **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="6d842-143">Aktualisieren Sie den Objekttyp, auf den eine URL zeigt</span><span class="sxs-lookup"><span data-stu-id="6d842-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="6d842-144">Sie können auch eine URL aktualisieren, damit sie auf einen anderen Objekttyp (Ressource) verweist, wie z. B. eine interne Seite oder eine Umleitung.</span><span class="sxs-lookup"><span data-stu-id="6d842-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="6d842-145">Führen Sie diese Schritte aus, um den Objekttyp zu aktualisieren, auf den eine URL zeigt.</span><span class="sxs-lookup"><span data-stu-id="6d842-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="6d842-146">Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL für die Aktualisierung aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="6d842-147">Wählen Sie im Eigenschaftenbereich rechts **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="6d842-148">Unter **URL-Zuweisung** unter **Schritt 1** wählen Sie einen anderen Objekttyp aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="6d842-149">Aktivieren Sie das Feld **Schritt 2**, und wählen Sie dann das neue Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="6d842-150">Wählen Sie **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="6d842-151">Ändern Sie den URL-Pfad</span><span class="sxs-lookup"><span data-stu-id="6d842-151">Change the URL path</span></span>

<span data-ttu-id="6d842-152">Nachdem eine URL erstellt wurde, kann ihr Pfad nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6d842-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="6d842-153">Wenn Sie einen URL-Pfad ändern müssen, der eine Datei oder irgendeinen anderen Ressourcentyp bedient, müssen Sie eine neue URL erstellen, sie einer vorhandenen Datei oder anderen Ressource zuordnen und dann die Veröffentlichung aufheben und die alte URL löschen.</span><span class="sxs-lookup"><span data-stu-id="6d842-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="6d842-154">Folgen Sie diesen Schritte, um den URL-Pfad zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6d842-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="6d842-155">Um eine neue URL zu erstellen und sie zur vorhandenen Datei oder einer anderen Ressource zuzuordnen, folgen Sie den Anleitungen im Abschnitt [Eine Website-URL erstellen, die eine statische Datei zurückgibt](#create-a-site-url-that-returns-a-static-file) weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="6d842-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="6d842-156">Wählen Sie die neue URL aus und wählen Sie dann **Veröffentlichen** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="6d842-157">Die neue URL wird veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6d842-157">The new URL is published.</span></span>
1. <span data-ttu-id="6d842-158">Um die Veröffentlichung der alten URL aufzuheben, wählen Sie sie aus und wählen Sie dann **Veröffentlichung aufheben** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="6d842-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="6d842-159">Sie können jetzt die alte URL löschen, wenn Sie dies möchten.</span><span class="sxs-lookup"><span data-stu-id="6d842-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d842-160">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d842-160">Additional resources</span></span>

[<span data-ttu-id="6d842-161">Überblick über die Verwaltung digitaler Anlagen</span><span class="sxs-lookup"><span data-stu-id="6d842-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="6d842-162">Bilder hochladen</span><span class="sxs-lookup"><span data-stu-id="6d842-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="6d842-163">Videos hochladen</span><span class="sxs-lookup"><span data-stu-id="6d842-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="6d842-164">Andere Dateien außer Bildern und Videos hochladen</span><span class="sxs-lookup"><span data-stu-id="6d842-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="6d842-165">Bilder zuschneiden</span><span class="sxs-lookup"><span data-stu-id="6d842-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="6d842-166">Bildfokuspunkte anpassen</span><span class="sxs-lookup"><span data-stu-id="6d842-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]